---
title: /messages
description: Article de référence de l’API pour les messages de requête envoyée groupe carte réseau interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 58839035fca768f92eda40974029208eb31dda7f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/31/2018
ms.locfileid: "27465700"
---
# <a name="messages"></a>/messages

Point de terminaison API pour envoyer des messages à des groupes de conversation à l’intérieur de Kaizala.

## <a name="post-messages"></a>/Messages POST

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | String | Non | valeur : application/json |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :--- | :--- |
| message | String | Non | Message texte envoyé (limite maximale de 1 000 caractères) |
| sendToAllSubscribers | Bool | Oui | Par défaut : false. Valide uniquement dans les cas groupId appartient à un groupe Public. True pour envoyer le message à tous les abonnés qui requiert l’utilisateur du jeton admin du groupe Public |
| abonnés | String] | Oui | Chaque élément correspond à un numéro de téléphone mobile (avec le code du pays. Par exemple. +911999999999). Message texte sera envoyé uniquement pour les abonnés sélectionnés. À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe Public |

#### <a name="sample-json-request"></a>Exemple de demande JSON

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| referenceId | String | GUID représentant l’exécution réussie de la demande |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
