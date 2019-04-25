---
title: /subGroups
description: Article de référence pour l'API permettant d'interroger les données de sous-groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190687"
---
# <a name="subgroups"></a>/subGroups
Point de terminaison d'API pour interagir avec les sous-groupes de conversation dans Kaizala.

## <a name="get-subgroups"></a>OBTENIR/subGroups

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre de chemin d'URL | groupId | String | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| Paramètre de requête d'URL | fetchAllGroups | Booléen | Oui | Paramètre pour spécifier si vous souhaitez extraire tous les sous-groupes de la hiérarchie |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d'objets JSON | Tableau de groupes avec la liste des sous-groupes, le cas échéant |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | GUID associé au groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l'URL de l'image de profil de groupe |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "subGroups": [
          {
            "groupName": "Sample sub group name",
            "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
            "groupImageUrl": "{sample sub group image URL here}",
          }
      ]
    }
  ]
}
```

## <a name="post-subgroups"></a>POST/subGroups

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre de chemin d'URL | groupId | String | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |

### <a name="request-body"></a>Corps de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| groupName | String | Non | Nom du sous-groupe |
| groupImageURL | Chaîne | Oui | URL de média de l'image de groupe; L'image doit être téléchargée via le chemin d'accès/Media |
| membres | Tableau | Oui | Tableau de chaînes de numéros de téléphone bien mis en forme |
| welcomeMessage | Tableau | Non | Tableau de chaînes de numéros de téléphone bien mis en forme  |
| addUserToGroup | Booléen | Oui | Valeur false si l'utilisateur appelant ne doit pas être ajouté au groupe par défaut  |


#### <a name="sample-json-request"></a>Exemple de requête JSON

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe créé |


#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
