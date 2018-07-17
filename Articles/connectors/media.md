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
# <a name="media"></a><span data-ttu-id="af04c-103">/ Media</span><span class="sxs-lookup"><span data-stu-id="af04c-103">/media</span></span>
<span data-ttu-id="af04c-104">Point de terminaison API envoyer des pièces jointes multimédias à des groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="af04c-104">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="af04c-105">Formats de fichiers pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="af04c-105">Supported file formats are:</span></span>

| <span data-ttu-id="af04c-106">Type de média</span><span class="sxs-lookup"><span data-stu-id="af04c-106">Media Type</span></span> | <span data-ttu-id="af04c-107">ActionType</span><span class="sxs-lookup"><span data-stu-id="af04c-107">ActionType</span></span> | <span data-ttu-id="af04c-108">Extension</span><span class="sxs-lookup"><span data-stu-id="af04c-108">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="af04c-109">Des images</span><span class="sxs-lookup"><span data-stu-id="af04c-109">Images</span></span> | <span data-ttu-id="af04c-110">Image</span><span class="sxs-lookup"><span data-stu-id="af04c-110">Image</span></span> | <span data-ttu-id="af04c-111">.jpg, .jpeg, .png</span><span class="sxs-lookup"><span data-stu-id="af04c-111">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="af04c-112">Album</span><span class="sxs-lookup"><span data-stu-id="af04c-112">Album</span></span> | <span data-ttu-id="af04c-113">Album</span><span class="sxs-lookup"><span data-stu-id="af04c-113">Album</span></span> | <span data-ttu-id="af04c-114">.jpg, .jpeg, .png</span><span class="sxs-lookup"><span data-stu-id="af04c-114">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="af04c-115">Fichiers audio</span><span class="sxs-lookup"><span data-stu-id="af04c-115">Audio Files</span></span> | <span data-ttu-id="af04c-116">Audio</span><span class="sxs-lookup"><span data-stu-id="af04c-116">Audio</span></span> |<span data-ttu-id="af04c-117">.mp3, .wav</span><span class="sxs-lookup"><span data-stu-id="af04c-117">.mp3, .wav</span></span> |
| <span data-ttu-id="af04c-118">Documents</span><span class="sxs-lookup"><span data-stu-id="af04c-118">Documents</span></span> | <span data-ttu-id="af04c-119">Document</span><span class="sxs-lookup"><span data-stu-id="af04c-119">Document</span></span> | <span data-ttu-id="af04c-120">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span><span class="sxs-lookup"><span data-stu-id="af04c-120">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="af04c-121">Vidéos</span><span class="sxs-lookup"><span data-stu-id="af04c-121">Videos</span></span> | <span data-ttu-id="af04c-122">Vidéo</span><span class="sxs-lookup"><span data-stu-id="af04c-122">Video</span></span> | <span data-ttu-id="af04c-123">.mp4, .3gpp</span><span class="sxs-lookup"><span data-stu-id="af04c-123">.mp4, .3gpp</span></span> |

<span data-ttu-id="af04c-124">Validation des médias joints à Kaizala est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="af04c-124">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="af04c-125">Tout d’abord, vous devez télécharger le fichier multimédia dans un référentiel en utilisant le point de terminaison/Media et utiliser l’URL de ressource ultérieurement à publier en tant qu’Action à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="af04c-125">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="af04c-126">Le contenu correspondant-type(mime type) doit être définie dans l’en-tête de contenu du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="af04c-126">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="af04c-127">Sans cette api génère des erreur Media(415) non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="af04c-127">Without this api will throw unsupported Media(415) error.</span></span> 

## <a name="post-media"></a><span data-ttu-id="af04c-128">/ Media POST</span><span class="sxs-lookup"><span data-stu-id="af04c-128">POST /media</span></span>

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a><span data-ttu-id="af04c-129">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="af04c-129">Request Parameters</span></span>

|  | <span data-ttu-id="af04c-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-130">Parameter</span></span> | <span data-ttu-id="af04c-131">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-131">Type</span></span> | <span data-ttu-id="af04c-132">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="af04c-132">Optional?</span></span> | <span data-ttu-id="af04c-133">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-133">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="af04c-134">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="af04c-134">HTTP Header</span></span> | <span data-ttu-id="af04c-135">accessToken</span><span class="sxs-lookup"><span data-stu-id="af04c-135">accessToken</span></span> | <span data-ttu-id="af04c-136">String</span><span class="sxs-lookup"><span data-stu-id="af04c-136">String</span></span> | <span data-ttu-id="af04c-137">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-137">No</span></span> | <span data-ttu-id="af04c-138">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="af04c-138">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="af04c-139">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="af04c-139">HTTP Header</span></span> | <span data-ttu-id="af04c-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="af04c-140">Content-Type</span></span> | <span data-ttu-id="af04c-141">String</span><span class="sxs-lookup"><span data-stu-id="af04c-141">String</span></span> | <span data-ttu-id="af04c-142">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-142">No</span></span> | <span data-ttu-id="af04c-143">Pour indiquer qu’un fichier est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="af04c-143">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="af04c-144">valeur : multipart/form data</span><span class="sxs-lookup"><span data-stu-id="af04c-144">value: multipart/form-data</span></span> |

### <a name="request-body"></a><span data-ttu-id="af04c-145">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="af04c-145">Request body</span></span>

| <span data-ttu-id="af04c-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-146">Parameter</span></span> | <span data-ttu-id="af04c-147">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-147">Type</span></span> | <span data-ttu-id="af04c-148">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="af04c-149">Corps de publication</span><span class="sxs-lookup"><span data-stu-id="af04c-149">POST Body</span></span> | <span data-ttu-id="af04c-150">fichiers</span><span class="sxs-lookup"><span data-stu-id="af04c-150">files</span></span> | <span data-ttu-id="af04c-151">Fichier à télécharger dans un format de données multipart/form</span><span class="sxs-lookup"><span data-stu-id="af04c-151">Media file to be uploaded in a multipart/form-data format</span></span> |

### <a name="response-body"></a><span data-ttu-id="af04c-152">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="af04c-152">Response body</span></span>

| <span data-ttu-id="af04c-153">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-153">Parameter</span></span> | <span data-ttu-id="af04c-154">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-154">Type</span></span> | <span data-ttu-id="af04c-155">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-155">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="af04c-156">mediaResource</span><span class="sxs-lookup"><span data-stu-id="af04c-156">mediaResource</span></span> | <span data-ttu-id="af04c-157">String</span><span class="sxs-lookup"><span data-stu-id="af04c-157">String</span></span> | <span data-ttu-id="af04c-158">Données multimédias à être utilisé dans les appels d’action suivants envoi codées</span><span class="sxs-lookup"><span data-stu-id="af04c-158">Encoded media data to be used in subsequent send action calls</span></span> |

## <a name="post-groupsgroupidactions"></a><span data-ttu-id="af04c-159">POST /groups/ {groupId} / actions</span><span class="sxs-lookup"><span data-stu-id="af04c-159">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="af04c-160">Une fois que vous avez téléchargé le fichier multimédia, vous pouvez publier un fichier multimédia à un groupe à l’aide de ci-dessous API</span><span class="sxs-lookup"><span data-stu-id="af04c-160">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="af04c-161">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="af04c-161">Request Parameters</span></span>

|  | <span data-ttu-id="af04c-162">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-162">Parameter</span></span> | <span data-ttu-id="af04c-163">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-163">Type</span></span> | <span data-ttu-id="af04c-164">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="af04c-164">Optional?</span></span> | <span data-ttu-id="af04c-165">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="af04c-166">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="af04c-166">URL Path Parameter</span></span> | <span data-ttu-id="af04c-167">groupId</span><span class="sxs-lookup"><span data-stu-id="af04c-167">groupId</span></span> | <span data-ttu-id="af04c-168">String</span><span class="sxs-lookup"><span data-stu-id="af04c-168">String</span></span> | <span data-ttu-id="af04c-169">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-169">No</span></span> | <span data-ttu-id="af04c-170">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="af04c-170">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="af04c-171">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="af04c-171">HTTP Header</span></span> | <span data-ttu-id="af04c-172">accessToken</span><span class="sxs-lookup"><span data-stu-id="af04c-172">accessToken</span></span> | <span data-ttu-id="af04c-173">String</span><span class="sxs-lookup"><span data-stu-id="af04c-173">String</span></span> | <span data-ttu-id="af04c-174">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-174">No</span></span> | <span data-ttu-id="af04c-175">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="af04c-175">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="af04c-176">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="af04c-176">HTTP Header</span></span> | <span data-ttu-id="af04c-177">Content-Type</span><span class="sxs-lookup"><span data-stu-id="af04c-177">Content-Type</span></span> | <span data-ttu-id="af04c-178">String</span><span class="sxs-lookup"><span data-stu-id="af04c-178">String</span></span> | <span data-ttu-id="af04c-179">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-179">No</span></span> | <span data-ttu-id="af04c-180">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="af04c-180">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="af04c-181">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="af04c-181">Request body</span></span>

| <span data-ttu-id="af04c-182">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-182">Parameter</span></span> | <span data-ttu-id="af04c-183">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-183">Type</span></span> | <span data-ttu-id="af04c-184">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-184">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="af04c-185">actionType</span><span class="sxs-lookup"><span data-stu-id="af04c-185">actionType</span></span> | <span data-ttu-id="af04c-186">String</span><span class="sxs-lookup"><span data-stu-id="af04c-186">String</span></span> | <span data-ttu-id="af04c-187">ID de l’Action Kaizala à envoyer.</span><span class="sxs-lookup"><span data-stu-id="af04c-187">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="af04c-188">Reportez-vous au tableau ci-dessus pour les formats de fichiers pris en charge et leur ActionType respectif.</span><span class="sxs-lookup"><span data-stu-id="af04c-188">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="af04c-189">actionBody</span><span class="sxs-lookup"><span data-stu-id="af04c-189">actionBody</span></span> | <span data-ttu-id="af04c-190">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="af04c-190">JSON Object</span></span> | <span data-ttu-id="af04c-191">Objet représentant les données nécessaires pour l’Action respectif.</span><span class="sxs-lookup"><span data-stu-id="af04c-191">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="af04c-192">Paramètres définis ci-dessous pour chacun du MediaType pris en charge.</span><span class="sxs-lookup"><span data-stu-id="af04c-192">Parameters defined below for each of the supported MediaType.</span></span> |

#### <a name="actionbody-for-media-files"></a><span data-ttu-id="af04c-193">actionBody des fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="af04c-193">actionBody for media files</span></span>

| <span data-ttu-id="af04c-194">Paramètre</span><span class="sxs-lookup"><span data-stu-id="af04c-194">Parameter</span></span> | <span data-ttu-id="af04c-195">Type</span><span class="sxs-lookup"><span data-stu-id="af04c-195">Type</span></span> | <span data-ttu-id="af04c-196">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="af04c-196">Optional?</span></span> | <span data-ttu-id="af04c-197">Description</span><span class="sxs-lookup"><span data-stu-id="af04c-197">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="af04c-198">mediaResource</span><span class="sxs-lookup"><span data-stu-id="af04c-198">mediaResource</span></span> | <span data-ttu-id="af04c-199">String</span><span class="sxs-lookup"><span data-stu-id="af04c-199">String</span></span> | <span data-ttu-id="af04c-200">Non</span><span class="sxs-lookup"><span data-stu-id="af04c-200">No</span></span> | <span data-ttu-id="af04c-201">Chaîne MediaResource à partir d’un appel précédent à/Media où vous devez télécharger la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="af04c-201">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="af04c-202">légende</span><span class="sxs-lookup"><span data-stu-id="af04c-202">caption</span></span> | <span data-ttu-id="af04c-203">String</span><span class="sxs-lookup"><span data-stu-id="af04c-203">String</span></span> | <span data-ttu-id="af04c-204">Oui</span><span class="sxs-lookup"><span data-stu-id="af04c-204">Yes</span></span> | <span data-ttu-id="af04c-205">Texte chaîne qui est illustré alongwith le fichier multimédia dans le cadre du message</span><span class="sxs-lookup"><span data-stu-id="af04c-205">Text String that is shown alongwith the media file as a part of the message</span></span> |


#### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="af04c-206">Exemple de demande JSON pour une Action de média</span><span class="sxs-lookup"><span data-stu-id="af04c-206">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a><span data-ttu-id="af04c-207">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="af04c-207">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


