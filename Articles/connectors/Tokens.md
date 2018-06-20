---
title: Mécanisme d’authentification
description: Article pour obtenir les jetons d’accès aux ressources Kaizala de requête
topic: Article
author: nitinjms
ms.openlocfilehash: e46d5ec6e6af4d125c9aef3dead5bc7a8e7e257c
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905113"
---
# <a name="authentication-mechanism"></a>Mécanisme d’authentification

Avant de commencer, reportez-vous au [programme d’installation pour l’utilisation de connecteurs Kaizala](setup.md)

## <a name="authentication-for-kaizala-connectors"></a>Authentification pour les connecteurs Kaizala
 
Nous avons mis en place un mécanisme d’autorisation en fonction de jeton personnalisé. Ce mécanisme utilise le concept d’actualisation et les jetons d’accès pour gérer les autorisations d’accès pour les API de plateforme Kaizala.
*   Actualiser les jetons effectués pendant les informations nécessaires pour obtenir un jeton d’accès. Ils doivent être transmis au Service d’émission de jeton lorsqu’un jeton d’accès arrive à expiration ou lorsqu’un jeton d’accès doit être généré pour la première fois. Jetons d’actualisation pour les connecteurs Kaizala ont un délai d’expiration de 365 jours. 

*   Jetons d’accès comportent les informations nécessaires pour accéder à une ressource Kaizala. Un 3ème partie client doit transmettre un jeton d’accès à la plateforme Kaizala avec chaque demande de l’API. Jetons d’accès pour les connecteurs Kaizala ont un délai d’expiration de 24 heures.


|              | Détails           | Comment générer   | Délai d’expiration    |
| :---: | :---: | :---: | :---: |
| Actualisation de jeton  | Les informations nécessaires pour obtenir un jeton d’accès     | Différentes manières pour générer un jeton d’actualisation sont documentées dans la section suivante | 365 jours           |
| Jeton d’accès   | Les informations nécessaires pour accéder à une ressource Kaizala  | Actualiser les détails de connecteur d’émission de jeton et autres pour interroger le point de terminaison Kaizala API pour générer un jeton d’accès utilise pour les développeurs    | 24 heures            |

*   Jetons d’actualisation peuvent être invalidés par le serveur de deux manières : en génération de nouveaux jetons d’actualisation pour le connecteur Kaizala même ou en supprimant le connecteur Kaizala correspondant entièrement.
## <a name="different-types-of-refresh-tokens"></a>Différents types de jetons d’actualisation

Connecteurs Kaizala autoriser les options permettant de générer deux types d’actualiser le jeton. Jeton des utilisateurs peut être généré via le portail de gestion Kaizala ou oAuth.

|              |   Outils permettant de générer  | Portée de l’accès   | Qui peut générer | Détails |
| :---: | :---: | :---: | :---: | :---: |
| Émission de jeton de groupe  | Portail de gestion Kaizala     | Groupe sélectionné   | Groupe/client d’administration |À l’aide de ce jeton, pour les développeurs peuvent effectuer des opérations qu’un administrateur de groupe dispose des autorisations pour dans ce groupe |
| Jeton de l’utilisateur   | Portail de gestion Kaizala  | Tous les groupes dont un utilisateur est membre | N’importe quel utilisateur | Si l’utilisateur est administrateur du client, ce jeton exécute l’accès au niveau du client. Pour d’autres, le jeton peut être utilisé pour accéder aux groupes en fonction de son accès |
| Jeton de l’utilisateur   | Utilisation d’OAuth 2.0, à l’aide des API | Tous les groupes dont un utilisateur est membre | N’importe quel utilisateur |À l’aide de ce jeton, pour les développeurs peuvent effectuer des opérations dans tous les groupes.|

*   En cas de jetons utilisateur, jeton unique fournit l’accès à tous les groupes de de qu'un utilisateur fait partie
*   Pour un connecteur unique, les développeurs peuvent générer des jetons de plusieurs groupes

Kaizala fournit deux autres méthodes pour générer des jetons d’actualisation par programmation
* À l’aide des API (ajouter bientôt)
* Utilisation d’OAuth (ajouter bientôt)

Une fois actualiser le jeton est fourni par l’administrateur du groupe ou utilisateur pour le développeur, il doit être utilisé pour générer un jeton d’accès.
## <a name="methods-to-generate-access-token"></a>Méthodes pour générer un jeton d’accès

En tant que développeur, vous pouvez maintenant choisir un ID de connecteur, clé secrète et un jeton actualiser qui doivent être passés vous. Utilisez cette, vous pouvez générer un jeton d’accès.

Kaizala fournit deux méthode pour générer des jetons d’accès
* À l’aide des API
* Utilisation d’OAuth

### <a name="generate-access-token-using-api"></a>Générer un jeton d’accès à l’aide des API

Le domaine racine pour appeler les APIs Kazaila est la suivante :

    https://api.kaiza.la/v1/

Vous devez utiliser le point de terminaison suivant pour obtenir un jeton d’accès (le premier temps et ultérieur lorsque le jeton d’accès arrive à expiration) :

    GET https://{api_root}/accessToken

##### <a name="request-parameters"></a>Paramètres de la demande

|               | Paramètre             | Type      | Facultatif ?     | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP   | `applicationId`       | Chaîne    | Non            | ID associé au connecteur  |
| En-tête HTTP   | `applicationSecret`   | Chaîne    | Non            | Secret associé au connecteur |
| En-tête HTTP   | `refreshToken`        | Chaîne    | Non            | refreshToken partagée par l’administrateur de groupe Kaizala lorsque le connecteur respectif a été accordé l’accès au groupe 

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| `accessToken` | Chaîne | Authentification réussie, un jeton d’application est renvoyé qui peut être utilisé pour effectuer des appels d’API suivants |
| `endpointUrl` | Chaîne | Authentification réussie, une url de point de terminaison est renvoyée qui doivent être utilisées comme url de base d’api pour effectuer des appels d’API suivants |
| `accessTokenExpiry` | Long | Il indique le délai d’expiration pour accessToken dans time(milliseconds) époque |
| `refreshToken` | Chaîne | À la fin de 328 jours (90 % de validité du jeton Actualiser), elle renvoie le nouveau refreshToken qui doit être utilisé pour la génération accessToken. Sinon, l’expiration de la validité d’un jeton d’actualisation en cours, connecteur serait cesser de fonctionner. La valeur est Null jusqu'à ce que l’expiration de 90 % de validité de refreshToken en cours |
| `scope` | Chaîne | Ensemble d’autorisations fournie avec le connecteur |

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
### <a name="generate-access-token-using-oauth-20"></a>Générer un jeton d’accès à l’aide d’oAuth 2.0

#### <a name="steps-to-generate-access-token-using-oauth-20"></a>Étapes pour générer un jeton d’accès à l’aide d’oAuth 2.0
*    **Étape 1 :** Créer/mettre à jour un connecteur sur le portail de gestion Kaizala pour inclure des url de redirection
     *    Dans le connecteur que vous utilisez, assurez-vous que vous avez entré une redirection url lors de la création du connecteur. Si ce n’est pas le cas, veuillez mettre à jour les url de redirection
     *    À des fins de test, vous pouvez utiliser la sous URL de rappel postman, qui vous permet simplement d’une page par le code. 
        
          `https://www.getpostman.com/oauth2/callback`
 
*    **Étape 2 :** Sous l’url dans le navigateur et appuyez sur entrée

          `https://ds.kaiza.la/api/Oauth/Authorize?client_id={{ConnectorID}}&redirect_uri={{re-directURL}}`
      
      *   Vérifiez que vous avez correctement entré 'identifiant_client' et 'redirect_uri'
       ##### <a name="request-parameters"></a>Paramètres de la demande

       |                | Paramètre             | Type      | Facultatif ?     | Description |
       | :---: | :---: | :---: | :---:  | :--- |
       | Paramètre d’URL  | `client_id`       | Chaîne    | Non            | ID associé au connecteur  |
       | Paramètre d’URL  | `redirect_uri`    | Chaîne    | Non            | Secret associé au connecteur |

     *    Par exemple, serait d’url
     
            `https://ds.kaiza.la/api/Oauth/Authorize?client_id=2AB9B82044683484EE9D958E7&redirect_uri=https://www.getpostman.com/oauth2/callback`


*    **Étape 3 :** Ouvrez une session dans Kaizala et générer « code »
     *   Dès que vous appuyez sur entrer à l’étape 2, vous être tenu à la page de connexion Kaizala
     *   Authentifier à l’aide de votre numéro d’enregistrement Kaizala
     *   Après avoir correctement sign-in, vous va être redirigée vers l’url de redirection avec « code » en tant que paramètre de requête dans l’url de rappel
     *   Notez le code renvoyé 
     
*    **Étape 4 :** Utiliser le code pour générer un jeton d’accès
     *   Vérifiez sous l’appel d’API pour générer un jeton d’accès
     
         `POST https://ds.kaiza.la/api/oauth/token `
     
     ##### <a name="request-parameters"></a>Paramètres de la demande

       |                | Paramètre             | Type      | Facultatif ?     | Description |
       | :---: | :---: | :---: | :---:  | :--- |
       | En-tête HTTP    | `Content-Type`        | Chaîne    | Non            | Valeur autorisée : application/x-www-form-urlencoded  |
       | Paramètre BODY     | `client_id`       | Chaîne    | Non            | ID associé au connecteur  |
       | Paramètre BODY     | `client_secret`   | Chaîne    | Non            | Secret associé au connecteur |
       | Paramètre BODY     | `code`    | Chaîne    | Non            | Code qui a été renvoyé dans le paramètre de requête de l’url redirection |
     
Vous recevrez accessToken, endpointUrl, accessToken expiration dans le cadre de la réponse.

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| `accessToken` | Chaîne | Authentification réussie, un jeton d’application est renvoyé qui peut être utilisé pour effectuer des appels d’API suivants |
| `endpointUrl` | Chaîne | Authentification réussie, une url de point de terminaison est renvoyée qui doivent être utilisées comme url de base d’api pour effectuer des appels d’API suivants |
| `accessTokenExpiry` | Long | Il indique le délai d’expiration pour accessToken dans time(milliseconds) époque |
| `refreshToken` | Chaîne | À la fin de 328 jours (90 % de validité du jeton Actualiser), elle renvoie le nouveau refreshToken qui doit être utilisé pour la génération accessToken. Sinon, l’expiration de la validité d’un jeton d’actualisation en cours, connecteur serait cesser de fonctionner. La valeur est Null jusqu'à ce que l’expiration de 90 % de validité de refreshToken en cours |
| `scope` | Chaîne | Ensemble d’autorisations fournie avec le connecteur |

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

[Documentation de l’API](API.md) de la suivante :
