---
title: /messages
description: Article de référence pour l’API permettant de demander des messages envoyés à l’adresse interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 64d694e067336a7da0c08ea116498086ee5650ce
ms.sourcegitcommit: 9e57984827280ed977019d33dd78b1ce5e3097fc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809430"
---
# <a name="messages"></a>/messages

Point de terminaison de l’API pour envoyer des messages à des groupes de conversation dans Kaizala.

## <a name="post-messages"></a>POST/messages

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’URL | groupId | String | Non | GUID représentant l’ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Jeton d’accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | String | Non | valeur : application/JSON |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Module? | Description |
| :---: | :---: | :--- | :--- |
| message | String | Non | Message texte à envoyer (limite maximale de 4000 caractères) |
| sendToAllSubscribers | Bool | Oui | Valeur par défaut : false. Valide uniquement si le groupId appartient à un groupe public. True pour envoyer le message texte à tous les abonnés qui nécessitent l’administrateur du jeton pour être administrateur du groupe public |
| leurs | Chaîne [] | Oui | Chaque élément correspond à un numéro de téléphone mobile (avec le code pays. Nnn. + 911999999999). Le message texte n’est envoyé qu’aux abonnés sélectionnés. À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe public |

#### <a name="sample-json-request"></a>Exemple de requête JSON

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| ID | String | GUID représentant la fin de la demande |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
