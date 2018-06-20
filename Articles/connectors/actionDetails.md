---
title: / Détails de l’action
description: Article de référence de l’API à la requête concernant les détails des Actions Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: a0871eec8a0247cea122bd14f968dd1e16936101
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905123"
---
# <a name="get-details-for-an-action-in-a-group"></a>Obtenir plus d’informations pour une Action dans un groupe
## <a name="get-actionsactionid"></a>GET /actions/ {actionId} /

Extraction l’API pour extraire la liste des instances de l’action envoyé à un groupe à l’aide de l' [API pour obtenir /actions ici](actions_get.md). Vous pouvez récupérer plus de détails sur une instance d’action spécifique référencé par un actionId.

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de chemin d’accès d’URL | actionId | Chaîne | Non | GUID représentant l’instance de l’action spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de requête URL | getDetails | Booléen | Oui | Permet d’obtenir l’affichage des détails de l’action spécifique ; Valeur par défaut est False |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionType | String | Type d’action renvoyée |
| actionDetails | Objet JSON | JSON onbject spécifique à l’actiontype |
| sender | Chaîne | Numéro de téléphone de l’utilisateur qui a envoyé l’action pour le groupe |
| sentAt | Date/heure | Publication de l’action pour le groupe |

####  <a name="actiondetails-object-structure-for-the-action-job"></a>structure d’objet actionDetails pour l’action 'Job' :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| dueDate | Date/heure | Date d’échéance de la tâche |
| title | Chaîne | Titre de la tâche |
| status | Bool�en | True si tous les intervenants ont effectué le travail |
| responseCount | Numérique | Nombre d’intervenants a marqué le travail terminée |
| assigneeCount | Numérique | Nombre de destinataires |
| réponses | Tableau JSON | Tableau JSON de réponses individuelles de travail |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a>structure d’objet actionDetails pour l’action « Enquête » :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l’instance de l’action spécifique |
| title | Chaîne | Titre de l’enquête |
| responseCount | Numérique | Nombre de personnes qui a répondu à l’enquête |
| affichait | Date/heure | DateTime de délai d’expiration de l’enquête |

##### <a name="sample-json-response"></a>Exemple de réponse JSON :

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
