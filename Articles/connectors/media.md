---
title: / Media
description: Article de référence de l’API envoyer des pièces jointes multimédias à des groupes
topic: Reference
author: nitinjms
ms.openlocfilehash: 0b74ce931344407b6e2962f447a0b2c8e721275e
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905148"
---
# <a name="apis-to-query-media-resources"></a><span data-ttu-id="175c6-103">API de ressources de support de requête</span><span class="sxs-lookup"><span data-stu-id="175c6-103">APIs to query media resources</span></span>
## <a name="media"></a><span data-ttu-id="175c6-104">/ Media</span><span class="sxs-lookup"><span data-stu-id="175c6-104">/media</span></span>
<span data-ttu-id="175c6-105">Point de terminaison API envoyer des pièces jointes multimédias à des groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="175c6-105">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="175c6-106">Formats de fichiers pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="175c6-106">Supported file formats are:</span></span>

| <span data-ttu-id="175c6-107">Type de média</span><span class="sxs-lookup"><span data-stu-id="175c6-107">Media Type</span></span> | <span data-ttu-id="175c6-108">ActionType</span><span class="sxs-lookup"><span data-stu-id="175c6-108">ActionType</span></span> | <span data-ttu-id="175c6-109">Extension</span><span class="sxs-lookup"><span data-stu-id="175c6-109">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="175c6-110">Des images</span><span class="sxs-lookup"><span data-stu-id="175c6-110">Images</span></span> | <span data-ttu-id="175c6-111">Image</span><span class="sxs-lookup"><span data-stu-id="175c6-111">Image</span></span> | <span data-ttu-id="175c6-112">.jpg, .jpeg, .png</span><span class="sxs-lookup"><span data-stu-id="175c6-112">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="175c6-113">Album</span><span class="sxs-lookup"><span data-stu-id="175c6-113">Album</span></span> | <span data-ttu-id="175c6-114">Album</span><span class="sxs-lookup"><span data-stu-id="175c6-114">Album</span></span> | <span data-ttu-id="175c6-115">.jpg, .jpeg, .png</span><span class="sxs-lookup"><span data-stu-id="175c6-115">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="175c6-116">Fichiers audio</span><span class="sxs-lookup"><span data-stu-id="175c6-116">Audio Files</span></span> | <span data-ttu-id="175c6-117">Audio</span><span class="sxs-lookup"><span data-stu-id="175c6-117">Audio</span></span> |<span data-ttu-id="175c6-118">.mp3, .wav</span><span class="sxs-lookup"><span data-stu-id="175c6-118">.mp3, .wav</span></span> |
| <span data-ttu-id="175c6-119">Documents</span><span class="sxs-lookup"><span data-stu-id="175c6-119">Documents</span></span> | <span data-ttu-id="175c6-120">Document</span><span class="sxs-lookup"><span data-stu-id="175c6-120">Document</span></span> | <span data-ttu-id="175c6-121">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span><span class="sxs-lookup"><span data-stu-id="175c6-121">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="175c6-122">Vidéos</span><span class="sxs-lookup"><span data-stu-id="175c6-122">Videos</span></span> | <span data-ttu-id="175c6-123">Vidéo</span><span class="sxs-lookup"><span data-stu-id="175c6-123">Video</span></span> | <span data-ttu-id="175c6-124">.mp4, .3gpp</span><span class="sxs-lookup"><span data-stu-id="175c6-124">.mp4, .3gpp</span></span> |

<span data-ttu-id="175c6-125">Validation des médias joints à Kaizala est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="175c6-125">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="175c6-126">Tout d’abord, vous devez télécharger le fichier multimédia dans un référentiel en utilisant le point de terminaison/Media et utiliser l’URL de ressource ultérieurement à publier en tant qu’Action à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="175c6-126">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="175c6-127">Le contenu correspondant-type(mime type) doit être définie dans l’en-tête de contenu du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="175c6-127">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="175c6-128">Sans cette api génère des erreur Media(415) non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="175c6-128">Without this api will throw unsupported Media(415) error.</span></span> 

### <a name="post-media"></a><span data-ttu-id="175c6-129">/ Media POST</span><span class="sxs-lookup"><span data-stu-id="175c6-129">POST /media</span></span>

    POST {endpoint-url}/v1/media

##### <a name="request-parameters"></a><span data-ttu-id="175c6-130">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="175c6-130">Request Parameters</span></span>

|  | <span data-ttu-id="175c6-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-131">Parameter</span></span> | <span data-ttu-id="175c6-132">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-132">Type</span></span> | <span data-ttu-id="175c6-133">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="175c6-133">Optional?</span></span> | <span data-ttu-id="175c6-134">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="175c6-135">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="175c6-135">HTTP Header</span></span> | <span data-ttu-id="175c6-136">accessToken</span><span class="sxs-lookup"><span data-stu-id="175c6-136">accessToken</span></span> | <span data-ttu-id="175c6-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-137">String</span></span> | <span data-ttu-id="175c6-138">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-138">No</span></span> | <span data-ttu-id="175c6-139">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="175c6-139">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="175c6-140">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="175c6-140">HTTP Header</span></span> | <span data-ttu-id="175c6-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="175c6-141">Content-Type</span></span> | <span data-ttu-id="175c6-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-142">String</span></span> | <span data-ttu-id="175c6-143">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-143">No</span></span> | <span data-ttu-id="175c6-144">Pour indiquer qu’un fichier est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="175c6-144">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="175c6-145">valeur : multipart/form data</span><span class="sxs-lookup"><span data-stu-id="175c6-145">value: multipart/form-data</span></span> |

##### <a name="request-body"></a><span data-ttu-id="175c6-146">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="175c6-146">Request body</span></span>

| <span data-ttu-id="175c6-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-147">Parameter</span></span> | <span data-ttu-id="175c6-148">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-148">Type</span></span> | <span data-ttu-id="175c6-149">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="175c6-150">Corps de publication</span><span class="sxs-lookup"><span data-stu-id="175c6-150">POST Body</span></span> | <span data-ttu-id="175c6-151">fichiers</span><span class="sxs-lookup"><span data-stu-id="175c6-151">files</span></span> | <span data-ttu-id="175c6-152">Fichier à télécharger dans un format de données multipart/form</span><span class="sxs-lookup"><span data-stu-id="175c6-152">Media file to be uploaded in a multipart/form-data format</span></span> |

##### <a name="response-body"></a><span data-ttu-id="175c6-153">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="175c6-153">Response body</span></span>

| <span data-ttu-id="175c6-154">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-154">Parameter</span></span> | <span data-ttu-id="175c6-155">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-155">Type</span></span> | <span data-ttu-id="175c6-156">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-156">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="175c6-157">mediaResource</span><span class="sxs-lookup"><span data-stu-id="175c6-157">mediaResource</span></span> | <span data-ttu-id="175c6-158">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-158">String</span></span> | <span data-ttu-id="175c6-159">Données multimédias à être utilisé dans les appels d’action suivants envoi codées</span><span class="sxs-lookup"><span data-stu-id="175c6-159">Encoded media data to be used in subsequent send action calls</span></span> |

### <a name="post-groupsgroupidactions"></a><span data-ttu-id="175c6-160">POST /groups/ {groupId} / actions</span><span class="sxs-lookup"><span data-stu-id="175c6-160">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="175c6-161">Une fois que vous avez téléchargé le fichier multimédia, vous pouvez publier un fichier multimédia à un groupe à l’aide de ci-dessous API</span><span class="sxs-lookup"><span data-stu-id="175c6-161">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

##### <a name="request-parameters"></a><span data-ttu-id="175c6-162">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="175c6-162">Request Parameters</span></span>

|  | <span data-ttu-id="175c6-163">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-163">Parameter</span></span> | <span data-ttu-id="175c6-164">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-164">Type</span></span> | <span data-ttu-id="175c6-165">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="175c6-165">Optional?</span></span> | <span data-ttu-id="175c6-166">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-166">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="175c6-167">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="175c6-167">URL Path Parameter</span></span> | <span data-ttu-id="175c6-168">groupId</span><span class="sxs-lookup"><span data-stu-id="175c6-168">groupId</span></span> | <span data-ttu-id="175c6-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-169">String</span></span> | <span data-ttu-id="175c6-170">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-170">No</span></span> | <span data-ttu-id="175c6-171">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="175c6-171">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="175c6-172">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="175c6-172">HTTP Header</span></span> | <span data-ttu-id="175c6-173">accessToken</span><span class="sxs-lookup"><span data-stu-id="175c6-173">accessToken</span></span> | <span data-ttu-id="175c6-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-174">String</span></span> | <span data-ttu-id="175c6-175">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-175">No</span></span> | <span data-ttu-id="175c6-176">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="175c6-176">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="175c6-177">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="175c6-177">HTTP Header</span></span> | <span data-ttu-id="175c6-178">Content-Type</span><span class="sxs-lookup"><span data-stu-id="175c6-178">Content-Type</span></span> | <span data-ttu-id="175c6-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-179">String</span></span> | <span data-ttu-id="175c6-180">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-180">No</span></span> | <span data-ttu-id="175c6-181">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="175c6-181">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="175c6-182">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="175c6-182">Request body</span></span>

| <span data-ttu-id="175c6-183">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-183">Parameter</span></span> | <span data-ttu-id="175c6-184">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-184">Type</span></span> | <span data-ttu-id="175c6-185">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-185">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="175c6-186">actionType</span><span class="sxs-lookup"><span data-stu-id="175c6-186">actionType</span></span> | <span data-ttu-id="175c6-187">String</span><span class="sxs-lookup"><span data-stu-id="175c6-187">String</span></span> | <span data-ttu-id="175c6-188">ID de l’Action Kaizala à envoyer.</span><span class="sxs-lookup"><span data-stu-id="175c6-188">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="175c6-189">Reportez-vous au tableau ci-dessus pour les formats de fichiers pris en charge et leur ActionType respectif.</span><span class="sxs-lookup"><span data-stu-id="175c6-189">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="175c6-190">actionBody</span><span class="sxs-lookup"><span data-stu-id="175c6-190">actionBody</span></span> | <span data-ttu-id="175c6-191">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="175c6-191">JSON Object</span></span> | <span data-ttu-id="175c6-192">Objet représentant les données nécessaires pour l’Action respectif.</span><span class="sxs-lookup"><span data-stu-id="175c6-192">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="175c6-193">Paramètres définis ci-dessous pour chacun du MediaType pris en charge.</span><span class="sxs-lookup"><span data-stu-id="175c6-193">Parameters defined below for each of the supported MediaType.</span></span> |

###### <a name="actionbody-for-media-files"></a><span data-ttu-id="175c6-194">actionBody des fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="175c6-194">actionBody for media files</span></span>

| <span data-ttu-id="175c6-195">Paramètre</span><span class="sxs-lookup"><span data-stu-id="175c6-195">Parameter</span></span> | <span data-ttu-id="175c6-196">Type</span><span class="sxs-lookup"><span data-stu-id="175c6-196">Type</span></span> | <span data-ttu-id="175c6-197">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="175c6-197">Optional?</span></span> | <span data-ttu-id="175c6-198">Description</span><span class="sxs-lookup"><span data-stu-id="175c6-198">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="175c6-199">mediaResource</span><span class="sxs-lookup"><span data-stu-id="175c6-199">mediaResource</span></span> | <span data-ttu-id="175c6-200">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-200">String</span></span> | <span data-ttu-id="175c6-201">Non</span><span class="sxs-lookup"><span data-stu-id="175c6-201">No</span></span> | <span data-ttu-id="175c6-202">Chaîne MediaResource à partir d’un appel précédent à/Media où vous devez télécharger la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="175c6-202">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="175c6-203">légende</span><span class="sxs-lookup"><span data-stu-id="175c6-203">caption</span></span> | <span data-ttu-id="175c6-204">Chaîne</span><span class="sxs-lookup"><span data-stu-id="175c6-204">String</span></span> | <span data-ttu-id="175c6-205">Oui</span><span class="sxs-lookup"><span data-stu-id="175c6-205">Yes</span></span> | <span data-ttu-id="175c6-206">Texte chaîne qui est illustré alongwith le fichier multimédia dans le cadre du message</span><span class="sxs-lookup"><span data-stu-id="175c6-206">Text String that is shown alongwith the media file as a part of the message</span></span> |


###### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="175c6-207">Exemple de demande JSON pour une Action de média</span><span class="sxs-lookup"><span data-stu-id="175c6-207">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

###### <a name="sample-json-response"></a><span data-ttu-id="175c6-208">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="175c6-208">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


