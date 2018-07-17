---
title: / Media
description: Article de référence de l’API envoyer des pièces jointes multimédias à des groupes
topic: Reference
author: nitinjms
ms.openlocfilehash: 3cf1e6b235d6bf324011f0b054408eb418eb0871
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399376"
---
# <a name="media"></a>/ Media
Point de terminaison API envoyer des pièces jointes multimédias à des groupes de conversation à l’intérieur de Kaizala.

Formats de fichiers pris en charge sont les suivants :

| Type de média | ActionType | Extension |
|---|---|---|
| Des images | Image | .jpg, .jpeg, .png |
| Album | Album | .jpg, .jpeg, .png |
| Fichiers audio | Audio |.mp3, .wav |
| Documents | Document | .doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf |
| Vidéos | Vidéo | .mp4, .3gpp |

Validation des médias joints à Kaizala est un processus en deux étapes. Tout d’abord, vous devez télécharger le fichier multimédia dans un référentiel en utilisant le point de terminaison/Media et utiliser l’URL de ressource ultérieurement à publier en tant qu’Action à l’intérieur de Kaizala.

Le contenu correspondant-type(mime type) doit être définie dans l’en-tête de contenu du fichier multimédia. Sans cette api génère des erreur Media(415) non pris en charge. 

## <a name="post-media"></a>/ Media POST

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | String | Non | Pour indiquer qu’un fichier est en cours d’envoi. valeur : multipart/form data |

### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| Corps de publication | fichiers | Fichier à télécharger dans un format de données multipart/form |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| mediaResource | String | Données multimédias à être utilisé dans les appels d’action suivants envoi codées |

## <a name="post-groupsgroupidactions"></a>POST /groups/ {groupId} / actions

Une fois que vous avez téléchargé le fichier multimédia, vous pouvez publier un fichier multimédia à un groupe à l’aide de ci-dessous API

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | String | Non | valeur : application/json |

### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionType | String | ID de l’Action Kaizala à envoyer. Reportez-vous au tableau ci-dessus pour les formats de fichiers pris en charge et leur ActionType respectif. |
| actionBody | Objet JSON | Objet représentant les données nécessaires pour l’Action respectif. Paramètres définis ci-dessous pour chacun du MediaType pris en charge. |

#### <a name="actionbody-for-media-files"></a>actionBody des fichiers multimédias

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| mediaResource | String | Non | Chaîne MediaResource à partir d’un appel précédent à/Media où vous devez télécharger la pièce jointe |
| légende | String | Oui | Texte chaîne qui est illustré alongwith le fichier multimédia dans le cadre du message |


#### <a name="sample-json-request-for-a-media-action"></a>Exemple de demande JSON pour une Action de média

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


