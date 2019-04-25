---
title: /Media
description: Article de référence pour l'API permettant d'envoyer des pièces jointes à des groupes
topic: Reference
author: nitinjms
ms.openlocfilehash: 3cf1e6b235d6bf324011f0b054408eb418eb0871
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190693"
---
# <a name="media"></a>/Media
Point de terminaison d'API pour envoyer des pièces jointes aux groupes de conversation dans Kaizala.

Les formats de fichier pris en charge sont les suivants:

| Type de média | ActionType | Extension |
|---|---|---|
| Des images | Image | . jpg,. jpeg,. png |
| Album | Album | . jpg,. jpeg,. png |
| Fichiers audio | Audio |. mp3,. wav |
| Documents | Document | . doc,. docx,. xls,. xlsx,. ppt,. pptx,. pdf |
| Vidéos | Vidéo | . MP4,. 3GPP |

La publication de pièces jointes de média dans Kaizala est un processus en deux étapes. Tout d'abord, vous devez télécharger le fichier multimédia dans un référentiel à l'aide du point de terminaison/Media, puis utiliser l'URL de la ressource plus tard pour publier en tant qu'action dans Kaizala.

Le type de contenu correspondant (type MIME) doit être défini dans l'en-tête de contenu du fichier multimédia. Sans cette API générera une erreur de support non pris en charge (415). 

## <a name="post-media"></a>POST/Media

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | Chaîne | Non | Pour indiquer qu'un fichier est en cours de téléchargement. valeur: multipart/form-data |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| Corps de la publication | fichiers | Fichier multimédia à charger dans un format multipart/form-data |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| mediaResource | Chaîne | Données multimédias codées à utiliser dans les appels d'action d'envoi suivants |

## <a name="post-groupsgroupidactions"></a>POST/groups/{groupId}/actions

Une fois que vous avez téléchargé le fichier multimédia, vous pouvez publier un fichier multimédia dans un groupe à l'aide de l'API ci-dessous.

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur: application/JSON |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionType | String | ID de l'action Kaizala à envoyer. Consultez le tableau ci-dessus pour les formats de fichier pris en charge et leurs ActionType respectifs. |
| actionBody | Objet JSON | Objet représentant les données nécessaires pour l'action correspondante. Paramètres définis ci-dessous pour chacun des MediaType pris en charge. |

#### <a name="actionbody-for-media-files"></a>actionBody pour les fichiers multimédias

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| mediaResource | Chaîne | Non | MediaResource chaîne d'un appel précédent à/Media où vous devez télécharger la pièce jointe |
| caption | Chaîne | Oui | Chaîne de texte affichée alongwith le fichier multimédia dans le cadre du message |


#### <a name="sample-json-request-for-a-media-action"></a>Exemple de demande JSON pour une action multimédia

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


