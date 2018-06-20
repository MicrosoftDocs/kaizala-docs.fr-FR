---
title: /Groups
description: Article de référence de l’API pour interroger les données de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 010d6d30c72355e2575cda2f8104316a5a770ac4
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905141"
---
# <a name="apis-to-query-kaizala-groups"></a>API de groupes Kaizala de requêtes
## <a name="groups"></a>/Groups
Point de terminaison API pour interagir avec les groupes de conversation à l’intérieur de Kaizala.

### <a name="post-groups"></a>/Groups POST

    Post {endpoint-url}/v1/groups

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | Chaîne | Non | « application/json » |

##### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :--- | :--- |
| name | Chaîne | Non | Nom de groupe |
| welcomeMessage | Chaîne | Non | Message de bienvenue qui s’affiche à nouveau membre du groupe |
| membres | String] | Oui | Numéro de Mobile (avec le code du pays) des membres à ajouter. Valeur par défaut : Utilisateur du jeton d’accès sera ajouté en tant qu’administrateur du groupe |
| groupType | Chaîne | Oui | Enum : Groupe/ConnectGroup. ConnectGroup créera un groupe Public gérés. Par défaut : groupe |

###### <a name="sample-json-request-for-create-group"></a>Exemple de demande JSON pour créer le groupe

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupName | Chaîne | Nom de groupe |
| groupId | Chaîne | Identificateur de groupe qui peut être utilisé dans les appels d’api suivants |
| membersAdded | bool | True si tous les membres sont bien ajoutés |

###### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


### <a name="get-groups"></a>OBTENIR /groups

    GET {endpoint-url}/v1/groups

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de requête | showDetail | bool | Oui | Par défaut : false. True pour renvoyer tous les détails du groupe |
| Paramètre de requête | fetchAllGroups | bool | Oui | Par défaut : false. True pour renvoyer tous les parents et sub groupes |

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d’objets JSON | Tableau de groupes que l’utilisateur a accès à avec l’accessToken |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l’URL de l’image de profil de groupe |
| hasSubGroups | bool | True si le groupe a des sous-groupes |
| hasParentGroups | bool | True si le groupe a groupes parents |
| isMappedToTenant | bool | True si le groupe est le groupe d’Organisation |
| groupType | Chaîne | Groupe/ConnectGroup. ConnectGroup si le groupe dans le groupe Public gérés |
| userCount | Numérique | Nombre total d’utilisateurs sous ce groupe dans la hiérarchie |
| currentLevelUserCount | Numérique | Nombre total de membres individuels du groupe au niveau actuel |

###### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": false,
      "hasParentGroups": false,
      "callerRole": "Admin",
      "currentLevelSubGroupCount": 0,
      "currentLevelParentGroupCount": 0,
      "userCount": 2,
      "uniqueUserCount": 0,
      "currentLevelUserCount": 2,
      "currentLevelUnProvisionedUserCount": 0,
      "unProvisionedUserCount": 0,
      "isMappedToTenant": false,
      "groupType": "Group",
      "isDuplicate": false,
      "isEditable": true,
      "isDetailsReadable": true
    }
  ]
}
```

### <a name="get-groupsgroupid"></a>OBTENIR /groups/ {groupId}

Vous pouvez obtenir plus d’informations sur un membre de ressources spécifiques (groupe ici) en spécifiant l’identificateur comme un paramètre de chemin d’accès d’URL

    GET {endpoint-url}/groups/{groupId}

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d’objets JSON | Tableau de groupes que l’utilisateur a accès à avec l’accessToken |

Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l’URL de l’image de profil de groupe |
| hasSubGroups | bool | True si le groupe a des sous-groupes |
| hasParentGroups | bool | True si le groupe a groupes parents |
| isMappedToTenant | bool | True si le groupe est le groupe d’Organisation |
| groupType | Chaîne | Groupe/ConnectGroup. ConnectGroup si le groupe dans le groupe Public gérés |
| userCount | Numérique | Nombre total d’utilisateurs sous ce groupe dans la hiérarchie |
| currentLevelUserCount | Numérique | Nombre total de membres individuels du groupe au niveau actuel |

###### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": true,
      "userCount": 200,
      "currentLevelUserCount": 10
    }
  ]
}
```

