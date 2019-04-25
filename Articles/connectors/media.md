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
# <a name="media"></a><span data-ttu-id="d0d04-103">/Media</span><span class="sxs-lookup"><span data-stu-id="d0d04-103">/media</span></span>
<span data-ttu-id="d0d04-104">Point de terminaison d'API pour envoyer des pièces jointes aux groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="d0d04-104">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="d0d04-105">Les formats de fichier pris en charge sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="d0d04-105">Supported file formats are:</span></span>

| <span data-ttu-id="d0d04-106">Type de média</span><span class="sxs-lookup"><span data-stu-id="d0d04-106">Media Type</span></span> | <span data-ttu-id="d0d04-107">ActionType</span><span class="sxs-lookup"><span data-stu-id="d0d04-107">ActionType</span></span> | <span data-ttu-id="d0d04-108">Extension</span><span class="sxs-lookup"><span data-stu-id="d0d04-108">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="d0d04-109">Des images</span><span class="sxs-lookup"><span data-stu-id="d0d04-109">Images</span></span> | <span data-ttu-id="d0d04-110">Image</span><span class="sxs-lookup"><span data-stu-id="d0d04-110">Image</span></span> | <span data-ttu-id="d0d04-111">. jpg,. jpeg,. png</span><span class="sxs-lookup"><span data-stu-id="d0d04-111">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="d0d04-112">Album</span><span class="sxs-lookup"><span data-stu-id="d0d04-112">Album</span></span> | <span data-ttu-id="d0d04-113">Album</span><span class="sxs-lookup"><span data-stu-id="d0d04-113">Album</span></span> | <span data-ttu-id="d0d04-114">. jpg,. jpeg,. png</span><span class="sxs-lookup"><span data-stu-id="d0d04-114">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="d0d04-115">Fichiers audio</span><span class="sxs-lookup"><span data-stu-id="d0d04-115">Audio Files</span></span> | <span data-ttu-id="d0d04-116">Audio</span><span class="sxs-lookup"><span data-stu-id="d0d04-116">Audio</span></span> |<span data-ttu-id="d0d04-117">. mp3,. wav</span><span class="sxs-lookup"><span data-stu-id="d0d04-117">.mp3, .wav</span></span> |
| <span data-ttu-id="d0d04-118">Documents</span><span class="sxs-lookup"><span data-stu-id="d0d04-118">Documents</span></span> | <span data-ttu-id="d0d04-119">Document</span><span class="sxs-lookup"><span data-stu-id="d0d04-119">Document</span></span> | <span data-ttu-id="d0d04-120">. doc,. docx,. xls,. xlsx,. ppt,. pptx,. pdf</span><span class="sxs-lookup"><span data-stu-id="d0d04-120">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="d0d04-121">Vidéos</span><span class="sxs-lookup"><span data-stu-id="d0d04-121">Videos</span></span> | <span data-ttu-id="d0d04-122">Vidéo</span><span class="sxs-lookup"><span data-stu-id="d0d04-122">Video</span></span> | <span data-ttu-id="d0d04-123">. MP4,. 3GPP</span><span class="sxs-lookup"><span data-stu-id="d0d04-123">.mp4, .3gpp</span></span> |

<span data-ttu-id="d0d04-124">La publication de pièces jointes de média dans Kaizala est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="d0d04-124">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="d0d04-125">Tout d'abord, vous devez télécharger le fichier multimédia dans un référentiel à l'aide du point de terminaison/Media, puis utiliser l'URL de la ressource plus tard pour publier en tant qu'action dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="d0d04-125">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="d0d04-126">Le type de contenu correspondant (type MIME) doit être défini dans l'en-tête de contenu du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="d0d04-126">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="d0d04-127">Sans cette API générera une erreur de support non pris en charge (415).</span><span class="sxs-lookup"><span data-stu-id="d0d04-127">Without this api will throw unsupported Media(415) error.</span></span> 

## <a name="post-media"></a><span data-ttu-id="d0d04-128">POST/Media</span><span class="sxs-lookup"><span data-stu-id="d0d04-128">POST /media</span></span>

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a><span data-ttu-id="d0d04-129">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="d0d04-129">Request Parameters</span></span>

|  | <span data-ttu-id="d0d04-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-130">Parameter</span></span> | <span data-ttu-id="d0d04-131">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-131">Type</span></span> | <span data-ttu-id="d0d04-132">Module?</span><span class="sxs-lookup"><span data-stu-id="d0d04-132">Optional?</span></span> | <span data-ttu-id="d0d04-133">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-133">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d0d04-134">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d0d04-134">HTTP Header</span></span> | <span data-ttu-id="d0d04-135">accessToken</span><span class="sxs-lookup"><span data-stu-id="d0d04-135">accessToken</span></span> | <span data-ttu-id="d0d04-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-136">String</span></span> | <span data-ttu-id="d0d04-137">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-137">No</span></span> | <span data-ttu-id="d0d04-138">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="d0d04-138">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="d0d04-139">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d0d04-139">HTTP Header</span></span> | <span data-ttu-id="d0d04-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-140">Content-Type</span></span> | <span data-ttu-id="d0d04-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-141">String</span></span> | <span data-ttu-id="d0d04-142">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-142">No</span></span> | <span data-ttu-id="d0d04-143">Pour indiquer qu'un fichier est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d0d04-143">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="d0d04-144">valeur: multipart/form-data</span><span class="sxs-lookup"><span data-stu-id="d0d04-144">value: multipart/form-data</span></span> |

### <a name="request-body"></a><span data-ttu-id="d0d04-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d0d04-145">Request body</span></span>

| <span data-ttu-id="d0d04-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-146">Parameter</span></span> | <span data-ttu-id="d0d04-147">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-147">Type</span></span> | <span data-ttu-id="d0d04-148">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d0d04-149">Corps de la publication</span><span class="sxs-lookup"><span data-stu-id="d0d04-149">POST Body</span></span> | <span data-ttu-id="d0d04-150">fichiers</span><span class="sxs-lookup"><span data-stu-id="d0d04-150">files</span></span> | <span data-ttu-id="d0d04-151">Fichier multimédia à charger dans un format multipart/form-data</span><span class="sxs-lookup"><span data-stu-id="d0d04-151">Media file to be uploaded in a multipart/form-data format</span></span> |

### <a name="response-body"></a><span data-ttu-id="d0d04-152">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="d0d04-152">Response body</span></span>

| <span data-ttu-id="d0d04-153">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-153">Parameter</span></span> | <span data-ttu-id="d0d04-154">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-154">Type</span></span> | <span data-ttu-id="d0d04-155">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-155">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d0d04-156">mediaResource</span><span class="sxs-lookup"><span data-stu-id="d0d04-156">mediaResource</span></span> | <span data-ttu-id="d0d04-157">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-157">String</span></span> | <span data-ttu-id="d0d04-158">Données multimédias codées à utiliser dans les appels d'action d'envoi suivants</span><span class="sxs-lookup"><span data-stu-id="d0d04-158">Encoded media data to be used in subsequent send action calls</span></span> |

## <a name="post-groupsgroupidactions"></a><span data-ttu-id="d0d04-159">POST/groups/{groupId}/actions</span><span class="sxs-lookup"><span data-stu-id="d0d04-159">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="d0d04-160">Une fois que vous avez téléchargé le fichier multimédia, vous pouvez publier un fichier multimédia dans un groupe à l'aide de l'API ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d0d04-160">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="d0d04-161">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="d0d04-161">Request Parameters</span></span>

|  | <span data-ttu-id="d0d04-162">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-162">Parameter</span></span> | <span data-ttu-id="d0d04-163">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-163">Type</span></span> | <span data-ttu-id="d0d04-164">Module?</span><span class="sxs-lookup"><span data-stu-id="d0d04-164">Optional?</span></span> | <span data-ttu-id="d0d04-165">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d0d04-166">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="d0d04-166">URL Path Parameter</span></span> | <span data-ttu-id="d0d04-167">groupId</span><span class="sxs-lookup"><span data-stu-id="d0d04-167">groupId</span></span> | <span data-ttu-id="d0d04-168">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-168">String</span></span> | <span data-ttu-id="d0d04-169">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-169">No</span></span> | <span data-ttu-id="d0d04-170">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="d0d04-170">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="d0d04-171">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d0d04-171">HTTP Header</span></span> | <span data-ttu-id="d0d04-172">accessToken</span><span class="sxs-lookup"><span data-stu-id="d0d04-172">accessToken</span></span> | <span data-ttu-id="d0d04-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-173">String</span></span> | <span data-ttu-id="d0d04-174">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-174">No</span></span> | <span data-ttu-id="d0d04-175">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="d0d04-175">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="d0d04-176">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d0d04-176">HTTP Header</span></span> | <span data-ttu-id="d0d04-177">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-177">Content-Type</span></span> | <span data-ttu-id="d0d04-178">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-178">String</span></span> | <span data-ttu-id="d0d04-179">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-179">No</span></span> | <span data-ttu-id="d0d04-180">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="d0d04-180">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="d0d04-181">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d0d04-181">Request body</span></span>

| <span data-ttu-id="d0d04-182">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-182">Parameter</span></span> | <span data-ttu-id="d0d04-183">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-183">Type</span></span> | <span data-ttu-id="d0d04-184">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-184">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d0d04-185">actionType</span><span class="sxs-lookup"><span data-stu-id="d0d04-185">actionType</span></span> | <span data-ttu-id="d0d04-186">String</span><span class="sxs-lookup"><span data-stu-id="d0d04-186">String</span></span> | <span data-ttu-id="d0d04-187">ID de l'action Kaizala à envoyer.</span><span class="sxs-lookup"><span data-stu-id="d0d04-187">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="d0d04-188">Consultez le tableau ci-dessus pour les formats de fichier pris en charge et leurs ActionType respectifs.</span><span class="sxs-lookup"><span data-stu-id="d0d04-188">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="d0d04-189">actionBody</span><span class="sxs-lookup"><span data-stu-id="d0d04-189">actionBody</span></span> | <span data-ttu-id="d0d04-190">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="d0d04-190">JSON Object</span></span> | <span data-ttu-id="d0d04-191">Objet représentant les données nécessaires pour l'action correspondante.</span><span class="sxs-lookup"><span data-stu-id="d0d04-191">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="d0d04-192">Paramètres définis ci-dessous pour chacun des MediaType pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d0d04-192">Parameters defined below for each of the supported MediaType.</span></span> |

#### <a name="actionbody-for-media-files"></a><span data-ttu-id="d0d04-193">actionBody pour les fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="d0d04-193">actionBody for media files</span></span>

| <span data-ttu-id="d0d04-194">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0d04-194">Parameter</span></span> | <span data-ttu-id="d0d04-195">Type</span><span class="sxs-lookup"><span data-stu-id="d0d04-195">Type</span></span> | <span data-ttu-id="d0d04-196">Module?</span><span class="sxs-lookup"><span data-stu-id="d0d04-196">Optional?</span></span> | <span data-ttu-id="d0d04-197">Description</span><span class="sxs-lookup"><span data-stu-id="d0d04-197">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d0d04-198">mediaResource</span><span class="sxs-lookup"><span data-stu-id="d0d04-198">mediaResource</span></span> | <span data-ttu-id="d0d04-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-199">String</span></span> | <span data-ttu-id="d0d04-200">Non</span><span class="sxs-lookup"><span data-stu-id="d0d04-200">No</span></span> | <span data-ttu-id="d0d04-201">MediaResource chaîne d'un appel précédent à/Media où vous devez télécharger la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="d0d04-201">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="d0d04-202">caption</span><span class="sxs-lookup"><span data-stu-id="d0d04-202">caption</span></span> | <span data-ttu-id="d0d04-203">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d0d04-203">String</span></span> | <span data-ttu-id="d0d04-204">Oui</span><span class="sxs-lookup"><span data-stu-id="d0d04-204">Yes</span></span> | <span data-ttu-id="d0d04-205">Chaîne de texte affichée alongwith le fichier multimédia dans le cadre du message</span><span class="sxs-lookup"><span data-stu-id="d0d04-205">Text String that is shown alongwith the media file as a part of the message</span></span> |


#### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="d0d04-206">Exemple de demande JSON pour une action multimédia</span><span class="sxs-lookup"><span data-stu-id="d0d04-206">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a><span data-ttu-id="d0d04-207">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="d0d04-207">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


