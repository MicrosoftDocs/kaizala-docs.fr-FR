---
title: Mécanisme d'authentification
description: Article permettant d'obtenir des jetons d'accès pour interroger les ressources Kaizala
topic: Article
author: nitinjms
ms.openlocfilehash: e46d5ec6e6af4d125c9aef3dead5bc7a8e7e257c
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190807"
---
# <a name="authentication-mechanism"></a>Mécanisme d'authentification

Avant de commencer, reportez-vous à [la rubrique Configuration de l'utilisation des connecteurs Kaizala](setup.md)

## <a name="authentication-for-kaizala-connectors"></a>Authentification pour les connecteurs Kaizala
 
Nous avons implémenté un mécanisme d'autorisation basé sur un jeton personnalisé. Ce mécanisme utilise le concept de jeton d'actualisation et d'accès pour gérer l'autorisation d'accès pour les API de plateforme Kaizala.
*   Les jetons d'actualisation contiennent les informations nécessaires pour obtenir un nouveau jeton d'accès. Elles doivent être transmises au service de jetons lorsqu'un jeton d'accès expire ou lorsqu'un jeton d'accès doit être généré pour la première fois. Les jetons d'actualisation pour les connecteurs Kaizala ont une heure d'expiration de 365 jours. 

*   Les jetons d'accès contiennent les informations nécessaires pour accéder à une ressource Kaizala. Un client tiers doit transmettre un jeton d'accès à la plateforme Kaizala à chaque demande d'API. Les jetons d'accès pour les connecteurs Kaizala ont une heure d'expiration de 24 heures.


|              | Détails           | Comment générer   | Heure d'expiration    |
| :---: | :---: | :---: | :---: |
| Jeton d'actualisation  | Transporter les informations nécessaires pour obtenir un nouveau jeton d'accès     | Les différentes façons de générer un jeton d'actualisation sont décrites dans la section suivante ci-dessous. | 365 jours           |
| Jeton d'accès   | Contenir les informations nécessaires pour accéder à une ressource Kaizala  | Le développeur utilise le jeton d'actualisation & autres détails du connecteur pour interroger le point de terminaison de l'API Kaizala afin de générer un jeton d'accès    | 24 heures            |

*   Les jetons d'actualisation peuvent être invalidés par le serveur de deux manières: en générant de nouveaux jetons d'actualisation pour le même connecteur Kaizala ou en supprimant le connecteur Kaizala correspondant.
## <a name="different-types-of-refresh-tokens"></a>Différents types de jetons d'actualisation

Les connecteurs Kaizala permettent aux options de générer deux types différents de jeton d'actualisation. Les jetons utilisateur peuvent être générés via le portail de gestion Kaizala ou oAuth.

|              |   Outils à générer  | Portée de l'accès   | Qui peut générer | Détails |
| :---: | :---: | :---: | :---: | :---: |
| Jeton de groupe  | Portail de gestion Kaizala     | Groupe sélectionné   | Administrateur de groupe/client |À l'aide de ce jeton, le développeur peut effectuer des opérations pour lesquelles un administrateur de groupe dispose d'autorisations pour ce groupe. |
| Jeton de l'utilisateur   | Portail de gestion Kaizala  | Tous les groupes dont un utilisateur est membre | Tout utilisateur | Si User est administrateur client, ce jeton transmet l'accès au niveau du client. Pour d'autres, le jeton peut être utilisé pour accéder aux groupes en fonction de son accès. |
| Jeton de l'utilisateur   | Utilisation de OAuth 2,0, à l'aide des API | Tous les groupes dont un utilisateur est membre | Tout utilisateur |À l'aide de ce jeton, le développeur peut effectuer des opérations au sein de tous les groupes.|

*   En cas de jetons utilisateur, un jeton unique fournit l'accès à tous les groupes dont un utilisateur fait partie
*   Pour un connecteur unique, les développeurs peuvent générer des jetons pour plusieurs groupes

Kaizala fournit deux autres méthodes pour générer des jetons d'actualisation par programmation.
* Utilisation de l'API (va bientôt s'ajouter)
* Utilisation de OAuth (va bientôt s'ajouter)

Une fois que le jeton d'actualisation est fourni par un administrateur de groupe ou un utilisateur au développeur, il doit être utilisé pour générer un jeton d'accès.
## <a name="methods-to-generate-access-token"></a>Méthodes pour générer un jeton d'accès

En tant que développeur, vous devez disposer d'un ID de connecteur, d'un jeton secret et d'un jeton d'actualisation qui doit être transmis à vous. À l'aide de cela, vous pouvez générer un jeton d'accès.

Kaizala fournit deux méthodes pour générer des jetons d'accès
* Utilisation de l'API
* Utilisation d’OAuth

### <a name="generate-access-token-using-api"></a>Générer un jeton d'accès à l'aide de l'API

Le domaine racine pour l'appel des API Kazaila est le suivant:

    https://api.kaiza.la/v1/

Vous devrez utiliser le point de terminaison suivant pour obtenir un jeton d'accès (la première fois & plus tard lorsque le jeton d'accès expire):

    GET https://{api_root}/accessToken

##### <a name="request-parameters"></a>Paramètres de la demande

|               | Paramètre             | Type      | Module?     | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP   | `applicationId`       | Chaîne    | Non            | ID associé au connecteur  |
| En-tête HTTP   | `applicationSecret`   | Chaîne    | Non            | Clé secrète associée au connecteur |
| En-tête HTTP   | `refreshToken`        | Chaîne    | Non            | refreshToken partagé par l'administrateur de groupe Kaizala lorsque le connecteur respectif a été autorisé à accéder au groupe 

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| `accessToken` | Chaîne | En cas de réussite de l'authentification, un jeton d'application est renvoyé qui peut être utilisé pour effectuer des appels d'API ultérieurs. |
| `endpointUrl` | Chaîne | Lors de l'authentification réussie, une URL de point de terminaison renvoyée doit être utilisée comme URL de base de l'API pour effectuer les appels d'API suivants. |
| `accessTokenExpiry` | Entier long | Il indique le temps d'expiration pour accessToken pendant la durée de validité (millisecondes). |
| `refreshToken` | Chaîne | À l'issue de 328 jours (90% de la validité du jeton d'actualisation), il renverra le nouveau refreshToken à utiliser pour générer accessToken. Dans le cas contraire, une fois que la validité du jeton d'actualisation actuel arrive à expiration, le connecteur ne fonctionne plus. La valeur est null jusqu'à 90% de la validité de la refreshToken actuelle. |
| `scope` | Chaîne | Jeu d'autorisations avec lequel le connecteur est fourni |

##### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```
### <a name="generate-access-token-using-oauth-20"></a>Générer un jeton d'accès à l'aide de oAuth 2,0

#### <a name="steps-to-generate-access-token-using-oauth-20"></a>Étapes à suivre pour générer un jeton d'accès à l'aide de oAuth 2,0
*    **Étape 1:** Créer/mettre à jour un connecteur sur le portail de gestion Kaizala afin d'inclure l'URL de redirection
     *    Dans le connecteur que vous utilisez, vérifiez que vous avez entré une URL de redirection lors de la création du connecteur. Si ce n'est pas le cas, veuillez mettre à jour l'URL de redirection
     *    À des fins de test, vous pouvez utiliser l'URL de rappel du billet, qui fournit uniquement une page avec le code. 
        
          `https://www.getpostman.com/oauth2/callback`
 
*    **Étape 2:** Tapez ci-dessous URL dans le navigateur, puis appuyez sur entrée.

          `https://ds.kaiza.la/api/Oauth/Authorize?client_id={{ConnectorID}}&redirect_uri={{re-directURL}}`
      
      *   Vérifiez que vous avez entré «client_id» & «redirect_uri» correctement
       ##### <a name="request-parameters"></a>Paramètres de la demande

       |                | Paramètre             | Type      | Module?     | Description |
       | :---: | :---: | :---: | :---:  | :--- |
       | Paramètre URL  | `client_id`       | Chaîne    | Non            | ID associé au connecteur  |
       | Paramètre URL  | `redirect_uri`    | Chaîne    | Non            | Clé secrète associée au connecteur |

     *    Par exemple, l'exemple d'URL pourrait être
     
            `https://ds.kaiza.la/api/Oauth/Authorize?client_id=2AB9B82044683484EE9D958E7&redirect_uri=https://www.getpostman.com/oauth2/callback`


*    **Étape 3:** Se connecter à Kaizala et générer «code»
     *   Dès que vous appuyez sur entrée à l'étape 2, vous serez redirigé vers la page de connexion Kaizala
     *   S'authentifier à l'aide de votre numéro Kaizala enregistré
     *   Une fois que vous vous êtes connecté, vous serez redirigé vers l'URL de redirection avec «code» en tant que paramètre de requête dans l'URL de rappel
     *   Notez le «code» renvoyé 
     
*    **Étape 4:** Utiliser du code pour générer un jeton d'accès
     *   Faire en dessous de l'appel de l'API pour générer un jeton d'accès
     
         `POST https://ds.kaiza.la/api/oauth/token `
     
     ##### <a name="request-parameters"></a>Paramètres de la demande

       |                | Paramètre             | Type      | Module?     | Description |
       | :---: | :---: | :---: | :---:  | :--- |
       | En-tête HTTP    | `Content-Type`        | Chaîne    | Non            | Valeur autorisée: application/x-www-form-urlencoded  |
       | Paramètre Body     | `client_id`       | Chaîne    | Non            | ID associé au connecteur  |
       | Paramètre Body     | `client_secret`   | Chaîne    | Non            | Clé secrète associée au connecteur |
       | Paramètre Body     | `code`    | Chaîne    | Non            | Code renvoyé dans le paramètre de requête de l'URL de redirection |
     
Vous recevrez accessToken, endpointUrl, accessToken expiration dans le cadre de la réponse.

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| `accessToken` | Chaîne | En cas de réussite de l'authentification, un jeton d'application est renvoyé qui peut être utilisé pour effectuer des appels d'API ultérieurs. |
| `endpointUrl` | Chaîne | Lors de l'authentification réussie, une URL de point de terminaison renvoyée doit être utilisée comme URL de base de l'API pour effectuer les appels d'API suivants. |
| `accessTokenExpiry` | Entier long | Il indique le temps d'expiration pour accessToken pendant la durée de validité (millisecondes). |
| `refreshToken` | Chaîne | À l'issue de 328 jours (90% de la validité du jeton d'actualisation), il renverra le nouveau refreshToken à utiliser pour générer accessToken. Dans le cas contraire, une fois que la validité du jeton d'actualisation actuel arrive à expiration, le connecteur ne fonctionne plus. La valeur est null jusqu'à 90% de la validité de la refreshToken actuelle. |
| `scope` | Chaîne | Jeu d'autorisations avec lequel le connecteur est fourni |

##### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```

Next: [documentation](API.md) de l'API
