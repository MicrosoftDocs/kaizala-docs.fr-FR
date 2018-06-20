---
title: /messages
description: Article de référence de l’API pour les messages de requête envoyée groupe carte réseau interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 25e3a918c95bd045a374de0420eda6324d46046a
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905168"
---
# <a name="apis-to-query-messages-sent-in-a-group"></a>API de requête les messages envoyés dans un groupe
## <a name="messages"></a>/messages
Point de terminaison API pour envoyer des messages à des groupes de conversation à l’intérieur de Kaizala.

### <a name="post-messages"></a>/Messages POST

    POST {endpoint-url}/v1/groups/{groupId}/messages

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur : application/json |

##### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :--- | :--- |
| message | Chaîne | Non | Message texte envoyé (limite maximale de 1 000 caractères) |
| sendToAllSubscribers | Bool | Oui | Par défaut : false. Valide uniquement dans les cas groupId appartient à un groupe Public. True pour envoyer le message à tous les abonnés qui requiert l’utilisateur du jeton admin du groupe Public |
| abonnés | String] | Oui | Chaque élément correspond à un numéro de téléphone mobile (avec le code du pays. Par exemple. +911999999999). Message texte sera envoyé uniquement pour les abonnés sélectionnés. À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe Public |

###### <a name="sample-json-request"></a>Exemple de demande JSON

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| referenceId | Chaîne | GUID représentant l’achèvement succesful de la demande |

###### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
