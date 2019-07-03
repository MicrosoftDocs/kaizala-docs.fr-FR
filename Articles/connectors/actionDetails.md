---
title: Détails de l'/action
description: Article de référence pour l’API permettant de rechercher des détails sur les actions Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: edb02de0ab8d88e058dc2ad20be236986984226f
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535673"
---
# <a name="get-details-for-an-action-in-a-group"></a>Obtenir les détails d’une action dans un groupe
## <a name="get-actionsactionid"></a>OBTENIR/actions/{actionId}/

Extrayez l’API pour récupérer la liste des instances d’action envoyées à un groupe à l’aide [de l’API pour Get/actions ici](actions_get.md). Vous pouvez récupérer des informations supplémentaires sur une instance d’action spécifique référencée par un actionId.

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’URL | groupId | Chaîne | Non | GUID représentant l’ID de ressource de la ressource de groupe spécifique |
| Paramètre de chemin d’URL | actionId | Chaîne | Non | GUID représentant l’instance d’action spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d’accès reçu depuis le point de terminaison auth |
| Paramètre de requête d’URL | getDetails | Boolean | Oui | Utilisez pour obtenir des informations détaillées sur l’action spécifique; La valeur par défaut est false |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionType | String | Type d’action retourné |
| actionDetails | Objet JSON | Objet JSON propre au ActionType |
| expéditeur | Chaîne | Numéro de téléphone de l’utilisateur qui a envoyé l’action au groupe |
| sentAt | Date/heure | Heure à laquelle l’action a été publiée dans le groupe |

####  <a name="actiondetails-object-structure-for-the-action-job"></a>structure d’objet actionDetails pour l’action «Job»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| dueDate | Date/heure | Date d’échéance de la tâche |
| title | Chaîne | Titre du travail |
| statut | Boolean | True lorsque tous les utilisateurs ont effectué le travail |
| responseCount | Numérique | Nombre d’utilisateurs ayant marqué le travail comme terminé |
| assigneeCount | Numérique | Nombre de personnes affectées |
| renvoyé | Tableau JSON | Tableau JSON de réponses aux travaux individuels |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a>structure d’objet actionDetails pour l’action «Survey»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l’instance d’action spécifique |
| title | Chaîne | Titre de l’enquête |
| responseCount | Numérique | Nombre de personnes ayant répondu à l’enquête |
| expiryDate | Date/heure | Date et heure de l’expiration de l’enquête |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "88a93ddd-0349d-4d18-86ee-c0f8484728db",
      "actionType": "Survey",
      "sender": "+91960000",
      "creationTime": 1480931759,
      "actionBody": {
        "actionId": "8106b2bb-236c-4952-a554-2baadcbd49a0",
        "title": "Sample Survey",
        "responseCount": 1
      }
    }
]
}
```
