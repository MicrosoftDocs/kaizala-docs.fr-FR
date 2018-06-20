---
title: /Members
description: Article de référence de l’API pour interroger les données de membres de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905151"
---
# <a name="members"></a>/Members
Point de terminaison API pour ajouter ou supprimer des membres de groupes de conversation à l’intérieur de Kaizala.

## <a name="get-members"></a>OBTENIR /members

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| members | Tableau JSON | Tableau de JSON objets chaque qui représente un membre du groupe |

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

## <a name="put-members"></a>Placez /members

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur : application/json |

### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| members | Tableau de chaînes | Tableau des numéros de téléphone au format correct de nouveaux membres à ajouter |

#### <a name="sample-json-request"></a>Exemple de demande JSON

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
| result | Bool�en | True si tous les numéros de téléphone ont correctement été ajouté au groupe |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a>SUPPRIMER /members

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de chemin d’accès d’URL | ID de membre | Chaîne | Non | GUID représentant l’ID de membre spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| result | Bool�en | La valeur True après le membre spécifié a correctement été supprimé du groupe |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "result": "true"
}
```
