---
title: /subscribers
description: Article de référence pour les API permettant d'obtenir les données des abonnés pour les groupes publics
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190697"
---
# <a name="subscribers"></a>/subscribers

Point de terminaison d'API pour ajouter, obtenir ou supprimer des abonnés à partir d'un groupe public géré.

## <a name="add-subscribers"></a>Ajouter/subscribers

    PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/add

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | String | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="request-body"></a>Corps de la demande
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| leurs | Chaîne [] | Chaque chaîne représente le numéro de téléphone mobile avec le code pays (par exemple, + 911111111111) |

#### <a name="sample-json-request"></a>Exemple de requête JSON
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Objet JSON | chaque clé de cet objet JSON représente le numéro de téléphone mobile et la valeur représente l'objet JSON contenant la réussite ou l'échec avec la raison |

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

## <a name="get-subscribers"></a>OBTENIR/subscribers

    POST {Endpoint-URL}/v1/groups/{groupId}/subscribers

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | String | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Module? | Description |
| :---: | :---: | :--- | :--- |
| curseur | Chaîne | Oui | Début de l'ResultSet. Pour la pagination. Renvoyé dans le corps de la réponse |
| count | int | Oui | Valeur par défaut: 50. Max: 50. Nombre d'abonnés à renvoyer dans un jeu de résultats|

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| leurs | Tableau JSON | Tableau d'objets JSON représentant chacun un abonné du groupe |
| curseur | Chaîne | Début de l'ResultSet. Pour la pagination. À utiliser dans le corps de la demande pour récupérer le jeu de résultats suivant. Présent en réponse uniquement s'il existe un jeu de résultats suivant valide. |

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

## <a name="remove-subscribers"></a>SUPPRIMER/subscribers

    PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/remove

### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | String | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="request-body"></a>Corps de la demande
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| leurs | Chaîne [] | Chaque chaîne représente le numéro de téléphone mobile avec le code pays (par exemple, + 911111111111) |

#### <a name="sample-json-request"></a>Exemple de requête JSON
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Objet JSON | chaque clé de cet objet JSON représente le numéro de téléphone mobile et la valeur représente l'objet JSON contenant la réussite ou l'échec avec la raison |

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

