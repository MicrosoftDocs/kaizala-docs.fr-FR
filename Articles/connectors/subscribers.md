---
title: /Subscribers
description: Référence de l’Article de l’API obtenir les abonnés données pour des groupes publics
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399364"
---
# <a name="subscribers"></a>/Subscribers

Point de terminaison API pour ajouter, obtenir ou supprimer les abonnés de groupe Public gérés.

## <a name="add-subscribers"></a>Ajouter /subscribers

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="request-body"></a>Corps de la requête
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| abonnés | String] | Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex.. +911111111111) |

#### <a name="sample-json-request"></a>Exemple de demande JSON
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Objet JSON | chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": {
        "+911111111111": {
            "isAdded": true
        },
        "+911111111112": {
            "isAdded": true
        }
    }
}
```

## <a name="get-subscribers"></a>OBTENIR /subscribers

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :--- | :--- |
| curseur | String | Oui | Début du jeu de résultats. Pour la pagination. Renvoyée dans le corps de réponse |
| count | entier | Oui | Par défaut : 50. Max : 50. Nombre d’abonnés à renvoyer dans un jeu de résultats|

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| abonnés | Tableau JSON | Tableau de JSON objets représentant chacun un abonné du groupe |
| curseur | String | Début du jeu de résultats. Pour la pagination. Pour être utilisé dans le corps de la requête pour extraire le résultat suivant défini. Présenter en réponse uniquement s’il existe un jeu de résultats valide suivant. |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "subscribers": [
        {
            "id": "e2238eb5-2f45-4783-8f4b-571549db86c0",
            "mobileNumber": "+91109999999",
            "name": "",
            "profilePic": "",
            "isProvisioned": false
        }
    ]
}
```

## <a name="remove-subscribers"></a>SUPPRIMER /subscribers

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="request-body"></a>Corps de la requête
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| abonnés | String] | Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex.. +911111111111) |

#### <a name="sample-json-request"></a>Exemple de demande JSON
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Objet JSON | chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": {
        "+911111111111": {
            "isRemoved": true
        },
        "+911111111112": {
            "isRemoved": true
        }
    }
}
```

