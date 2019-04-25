---
title: /Members
description: Article de référence pour l'API permettant d'interroger les données des membres du groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190791"
---
# <a name="members"></a>/Members
Point de terminaison d'API pour ajouter ou supprimer des membres de groupes de conversation dans Kaizala.

## <a name="get-members"></a>OBTENIR/members

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| members | Tableau JSON | Tableau d'objets JSON chacun représentant un membre du groupe. |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
  "members": [
    {
      "id": "4deffa08-guid-4b87-8c2f-d944565f5f31",
      "role": "Admin",
      "mobileNumber": "+919652000000",
      "isProvisioned": true
    },
    {
      "id": "2e20e9ac-guid-47bd-abac-1f5236004684",
      "role": "Member",
      "mobileNumber": "+919652000001",
      "isProvisioned": false
    }
  ]
}
```

## <a name="put-members"></a>PUT/members

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur: application/JSON |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| members | Tableau de chaînes | Tableau de numéros de téléphone bien mis en forme des nouveaux membres à ajouter |

#### <a name="sample-json-request"></a>Exemple de requête JSON

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Booléen | True lorsque tous les numéros de téléphone ont été ajoutés au groupe avec succès |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a>SUPPRIMER/members

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| Paramètre de chemin d'URL | ID | Chaîne | Non | GUID représentant l'ID de membre du membre spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Booléen | True lorsque le membre spécifié a été supprimé du groupe avec succès. |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": "true"
}
```
