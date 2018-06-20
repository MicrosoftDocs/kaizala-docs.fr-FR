---
title: /subGroups
description: Article de référence de l’API pour interroger les données sous-groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6d013b4d6657eaaaadb9fe3244c2d9383e56f6
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905128"
---
# <a name="apis-to-query-subgroups-within-a-group"></a>API de sous-groupes de requête au sein d’un groupe
## <a name="subgroups"></a>/subGroups
Prévoit d’API pour interagir avec la conversation sous-groupes à l’intérieur de Kaizala.

### <a name="get-subgroups"></a>OBTENIR /subGroups

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de requête URL | fetchAllGroups | Booléen | Oui | Paramètre pour spécifier si vous souhaitez extraire tous les sous-groupes dans la hiérarchie |

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d’objets JSON | Tableau des groupes à la liste des sous-groupes, le cas échéant |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | GUID associé au groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l’URL de l’image de profil de groupe |

###### <a name="sample-json-response"></a>Exemple de réponse JSON

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

### <a name="post-subgroups"></a>/SubGroups POST

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |

##### <a name="request-body"></a>Corps de la requête

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| groupName | Chaîne | Non | Nom du groupe sub |
| groupImageURL | Chaîne | Oui | URL de support de l’image de groupe ; Image doit être téléchargé via le chemin d’accès/Media |
| membres | Tableau | Oui | Tableau de chaînes de numéros de téléphone au format correct |
| welcomeMessage | Tableau | Non | Tableau de chaînes de numéros de téléphone au format correct  |
| addUserToGroup | Booléen | Oui | La valeur False si l’utilisateur appelant ne doit pas être ajouté au groupe par défaut  |


###### <a name="sample-json-request"></a>Exemple de demande JSON

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe créé |


###### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
