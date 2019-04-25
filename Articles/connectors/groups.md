---
title: /Groups
description: Article de référence pour l'API permettant de rechercher des données de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190715"
---
# <a name="groups"></a>/Groups
Point de terminaison d'API pour interagir avec les groupes de conversation dans Kaizala.

## <a name="post-groups"></a>POST/Groups

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | String | Non | «application/JSON» |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Module? | Description |
| :---: | :---: | :--- | :--- |
| name | Chaîne | Non | Nom du groupe |
| welcomeMessage | String | Non | Message d'accueil qui sera affiché dans le nouveau membre de groupe |
| membres | Chaîne [] | Oui | Numéro de téléphone mobile (avec code de pays) des membres à ajouter. Valeur par défaut: l'utilisateur du jeton d'accès est ajouté en tant qu'administrateur du groupe. |
| groupType | Chaîne | Oui | Énumération: Group/ConnectGroup. ConnectGroup crée un groupe public géré. Valeur par défaut: groupe |

#### <a name="sample-json-request-for-create-group"></a>Exemple de requête JSON pour Create Group

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupName | Chaîne | Nom du groupe |
| groupId | Chaîne | Identificateur de groupe qui peut être utilisé dans les appels d'API suivants |
| membersAdded | bool | True si tous les membres sont ajoutés avec succès |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a>OBTENIR/Groups

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre de requête | showDetail | bool | Oui | Valeur par défaut: false. True pour renvoyer tous les détails du groupe |
| Paramètre de requête | fetchAllGroups | bool | Oui | Valeur par défaut: false. True pour renvoyer tous les parents et sous-groupes |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d'objets JSON | Tableau de groupes auxquels l'utilisateur a accès à l'aide du accessToken |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l'URL de l'image de profil de groupe |
| hasSubGroups | bool | True si le groupe a des sous-groupes |
| hasParentGroups | bool | True si le groupe a des groupes parents |
| isMappedToTenant | bool | True si le groupe est un groupe d'organisation |
| groupType | Chaîne | Group/ConnectGroup. ConnectGroup si le groupe dans le groupe public géré |
| Nombre | Numérique | Nombre total d'utilisateurs sous ce groupe dans la hiérarchie |
| currentLevelUserCount | Numérique | Nombre total de membres individuels du groupe au niveau actuel |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

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

## <a name="get-groupsgroupid"></a>OBTENIR/groups/{groupId}

Vous pouvez obtenir des détails sur un membre de ressource spécifique (un groupe ici) en spécifiant l'identificateur sous la forme d'un paramètre de chemin d'URL.

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupes | Tableau d'objets JSON | Tableau de groupes auxquels l'utilisateur a accès à l'aide du accessToken |

Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| groupId | Chaîne | Identificateur de groupe |
| groupName | Chaîne | Nom du groupe |
| groupImageURL | Chaîne | Chaîne spécifiant l'URL de l'image de profil de groupe |
| hasSubGroups | bool | True si le groupe a des sous-groupes |
| hasParentGroups | bool | True si le groupe a des groupes parents |
| isMappedToTenant | bool | True si le groupe est un groupe d'organisation |
| groupType | Chaîne | Group/ConnectGroup. ConnectGroup si le groupe dans le groupe public géré |
| Nombre | Numérique | Nombre total d'utilisateurs sous ce groupe dans la hiérarchie |
| currentLevelUserCount | Numérique | Nombre total de membres individuels du groupe au niveau actuel |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

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

