---
title: /REACTION
description: Article de référence de l’API réactions de requête sur n’importe quelle Action envoyé dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 9ac64dcb3ef72a84589483e45ae8e528aaa5aa4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2018
ms.locfileid: "20457303"
---
# <a name="reaction"></a><span data-ttu-id="39d55-103">/REACTION</span><span class="sxs-lookup"><span data-stu-id="39d55-103">/reaction</span></span>
<span data-ttu-id="39d55-104">Point de terminaison API pour interroger les données réactions sur n’importe quelle Action envoyée dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="39d55-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="39d55-105">/Reaction POST</span><span class="sxs-lookup"><span data-stu-id="39d55-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="39d55-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="39d55-106">Request Parameters</span></span>

| | <span data-ttu-id="39d55-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-107">Parameter</span></span> | <span data-ttu-id="39d55-108">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-108">Type</span></span> | <span data-ttu-id="39d55-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="39d55-109">Optional?</span></span> | <span data-ttu-id="39d55-110">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="39d55-111">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-111">URL Path Parameter</span></span> | <span data-ttu-id="39d55-112">groupId</span><span class="sxs-lookup"><span data-stu-id="39d55-112">groupId</span></span> | <span data-ttu-id="39d55-113">String</span><span class="sxs-lookup"><span data-stu-id="39d55-113">String</span></span> | <span data-ttu-id="39d55-114">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-114">No</span></span> | <span data-ttu-id="39d55-115">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="39d55-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="39d55-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="39d55-116">HTTP Header</span></span> | <span data-ttu-id="39d55-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="39d55-117">accessToken</span></span> | <span data-ttu-id="39d55-118">String</span><span class="sxs-lookup"><span data-stu-id="39d55-118">String</span></span> | <span data-ttu-id="39d55-119">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-119">No</span></span> | <span data-ttu-id="39d55-120">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="39d55-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="39d55-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="39d55-121">HTTP Header</span></span> | <span data-ttu-id="39d55-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="39d55-122">Content-Type</span></span> | <span data-ttu-id="39d55-123">String</span><span class="sxs-lookup"><span data-stu-id="39d55-123">String</span></span> | <span data-ttu-id="39d55-124">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-124">No</span></span> | <span data-ttu-id="39d55-125">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="39d55-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="39d55-126">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="39d55-126">Request body</span></span>

| <span data-ttu-id="39d55-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-127">Parameter</span></span> | <span data-ttu-id="39d55-128">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-128">Type</span></span> | <span data-ttu-id="39d55-129">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="39d55-129">Optional?</span></span> | <span data-ttu-id="39d55-130">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="39d55-131">referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-131">referenceId</span></span> | <span data-ttu-id="39d55-132">String</span><span class="sxs-lookup"><span data-stu-id="39d55-132">String</span></span> | <span data-ttu-id="39d55-133">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-133">No</span></span> | <span data-ttu-id="39d55-134">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="39d55-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="39d55-135">sourceGroupId</span></span> | <span data-ttu-id="39d55-136">String</span><span class="sxs-lookup"><span data-stu-id="39d55-136">String</span></span> | <span data-ttu-id="39d55-137">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-137">No</span></span> | <span data-ttu-id="39d55-138">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="39d55-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="39d55-139">En cas de groupes est d’un autre groupe de celle-ci peut différer de 'groupId' fourni dans l’url de paramètre de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="39d55-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="39d55-140">reactionType</span><span class="sxs-lookup"><span data-stu-id="39d55-140">reactionType</span></span> | <span data-ttu-id="39d55-141">String</span><span class="sxs-lookup"><span data-stu-id="39d55-141">String</span></span> | <span data-ttu-id="39d55-142">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-142">No</span></span> | <span data-ttu-id="39d55-143">Valeur enum : « Like'/ ' commentaire »</span><span class="sxs-lookup"><span data-stu-id="39d55-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="39d55-144">comment</span><span class="sxs-lookup"><span data-stu-id="39d55-144">comment</span></span> | <span data-ttu-id="39d55-145">String</span><span class="sxs-lookup"><span data-stu-id="39d55-145">String</span></span> | <span data-ttu-id="39d55-146">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-146">No</span></span> | <span data-ttu-id="39d55-147">Texte de commentaire est obligatoire uniquement pour reactionType « Comment ».</span><span class="sxs-lookup"><span data-stu-id="39d55-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="39d55-148">Pour « Like », il doit être ignoré</span><span class="sxs-lookup"><span data-stu-id="39d55-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="39d55-149">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="39d55-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-150">Response body</span></span>

| <span data-ttu-id="39d55-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-151">Parameter</span></span> | <span data-ttu-id="39d55-152">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-152">Type</span></span> | <span data-ttu-id="39d55-153">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-154">reactionId</span><span class="sxs-lookup"><span data-stu-id="39d55-154">reactionId</span></span> | <span data-ttu-id="39d55-155">String</span><span class="sxs-lookup"><span data-stu-id="39d55-155">String</span></span> | <span data-ttu-id="39d55-156">GUID représentant l’id de l’entité réaction après l’exécution réussie de la demande</span><span class="sxs-lookup"><span data-stu-id="39d55-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="39d55-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="39d55-158">OBTENIR /reaction résumé au niveau de l’Action</span><span class="sxs-lookup"><span data-stu-id="39d55-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="39d55-159">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="39d55-159">Request Parameters</span></span>

|  | <span data-ttu-id="39d55-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-160">Parameter</span></span> | <span data-ttu-id="39d55-161">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-161">Type</span></span> | <span data-ttu-id="39d55-162">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="39d55-162">Optional?</span></span> | <span data-ttu-id="39d55-163">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="39d55-164">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-164">URL Path Parameter</span></span> | <span data-ttu-id="39d55-165">groupId</span><span class="sxs-lookup"><span data-stu-id="39d55-165">groupId</span></span> | <span data-ttu-id="39d55-166">String</span><span class="sxs-lookup"><span data-stu-id="39d55-166">String</span></span> | <span data-ttu-id="39d55-167">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-167">No</span></span> | <span data-ttu-id="39d55-168">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="39d55-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="39d55-169">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-169">URL Path Parameter</span></span> | <span data-ttu-id="39d55-170">referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-170">referenceId</span></span> | <span data-ttu-id="39d55-171">String</span><span class="sxs-lookup"><span data-stu-id="39d55-171">String</span></span> | <span data-ttu-id="39d55-172">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-172">No</span></span> | <span data-ttu-id="39d55-173">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="39d55-174">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-174">URL Path Parameter</span></span> | <span data-ttu-id="39d55-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="39d55-175">sourceGroupId</span></span> | <span data-ttu-id="39d55-176">String</span><span class="sxs-lookup"><span data-stu-id="39d55-176">String</span></span> | <span data-ttu-id="39d55-177">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-177">No</span></span> | <span data-ttu-id="39d55-178">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="39d55-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="39d55-179">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="39d55-179">HTTP Header</span></span> | <span data-ttu-id="39d55-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="39d55-180">accessToken</span></span> | <span data-ttu-id="39d55-181">String</span><span class="sxs-lookup"><span data-stu-id="39d55-181">String</span></span> | <span data-ttu-id="39d55-182">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-182">No</span></span> | <span data-ttu-id="39d55-183">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="39d55-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="39d55-184">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-184">Response body</span></span>

| <span data-ttu-id="39d55-185">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-185">Parameter</span></span> | <span data-ttu-id="39d55-186">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-186">Type</span></span> | <span data-ttu-id="39d55-187">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-188">Résumé</span><span class="sxs-lookup"><span data-stu-id="39d55-188">summary</span></span> | <span data-ttu-id="39d55-189">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-189">JSON Array</span></span> | <span data-ttu-id="39d55-190">Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="39d55-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="39d55-191">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-191">Response body summary object</span></span>

| <span data-ttu-id="39d55-192">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-192">Parameter</span></span> | <span data-ttu-id="39d55-193">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-193">Type</span></span> | <span data-ttu-id="39d55-194">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-195">referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-195">referenceId</span></span> | <span data-ttu-id="39d55-196">String</span><span class="sxs-lookup"><span data-stu-id="39d55-196">String</span></span> | <span data-ttu-id="39d55-197">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="39d55-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="39d55-198">reactionsCountMap</span></span> | <span data-ttu-id="39d55-199">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-199">Json object</span></span> | <span data-ttu-id="39d55-200">Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="39d55-201">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-201">Sample JSON Response</span></span>

```javascript
{
    "summary": [
        {
            "referenceId": "4a44e62e-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        }
    ]
}
```

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="39d55-202">OBTENIR /reaction résumé au niveau de groupe</span><span class="sxs-lookup"><span data-stu-id="39d55-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="39d55-203">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="39d55-203">Request Parameters</span></span>

|  | <span data-ttu-id="39d55-204">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-204">Parameter</span></span> | <span data-ttu-id="39d55-205">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-205">Type</span></span> | <span data-ttu-id="39d55-206">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="39d55-206">Optional?</span></span> | <span data-ttu-id="39d55-207">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="39d55-208">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-208">URL Path Parameter</span></span> | <span data-ttu-id="39d55-209">groupId</span><span class="sxs-lookup"><span data-stu-id="39d55-209">groupId</span></span> | <span data-ttu-id="39d55-210">String</span><span class="sxs-lookup"><span data-stu-id="39d55-210">String</span></span> | <span data-ttu-id="39d55-211">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-211">No</span></span> | <span data-ttu-id="39d55-212">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="39d55-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="39d55-213">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-213">URL Path Parameter</span></span> | <span data-ttu-id="39d55-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="39d55-214">sourceGroupId</span></span> | <span data-ttu-id="39d55-215">String</span><span class="sxs-lookup"><span data-stu-id="39d55-215">String</span></span> | <span data-ttu-id="39d55-216">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-216">No</span></span> | <span data-ttu-id="39d55-217">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="39d55-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="39d55-218">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-218">URL Path Parameter</span></span> | <span data-ttu-id="39d55-219">curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-219">cursor</span></span> | <span data-ttu-id="39d55-220">Horodatage</span><span class="sxs-lookup"><span data-stu-id="39d55-220">timeStamp</span></span> | <span data-ttu-id="39d55-221">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-221">No</span></span> | <span data-ttu-id="39d55-222">Horodatage à partir de laquelle le résumé doit être calculée.</span><span class="sxs-lookup"><span data-stu-id="39d55-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="39d55-223">La valeur 0 par défaut</span><span class="sxs-lookup"><span data-stu-id="39d55-223">Default value 0</span></span> |
| <span data-ttu-id="39d55-224">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="39d55-224">HTTP Header</span></span> | <span data-ttu-id="39d55-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="39d55-225">accessToken</span></span> | <span data-ttu-id="39d55-226">String</span><span class="sxs-lookup"><span data-stu-id="39d55-226">String</span></span> | <span data-ttu-id="39d55-227">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-227">No</span></span> | <span data-ttu-id="39d55-228">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="39d55-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="39d55-229">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-229">Response body</span></span>

| <span data-ttu-id="39d55-230">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-230">Parameter</span></span> | <span data-ttu-id="39d55-231">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-231">Type</span></span> | <span data-ttu-id="39d55-232">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-233">curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-233">cursor</span></span> | <span data-ttu-id="39d55-234">Horodatage</span><span class="sxs-lookup"><span data-stu-id="39d55-234">timeStamp</span></span> | <span data-ttu-id="39d55-235">Horodatage jusqu'à laquelle résumé a été calculé.</span><span class="sxs-lookup"><span data-stu-id="39d55-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="39d55-236">L’ensemble suivant de reactionSummary peut être générée à l’aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="39d55-237">Résumé</span><span class="sxs-lookup"><span data-stu-id="39d55-237">summary</span></span> | <span data-ttu-id="39d55-238">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-238">JSON Array</span></span> | <span data-ttu-id="39d55-239">Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="39d55-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="39d55-240">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-240">Response body summary object</span></span>

| <span data-ttu-id="39d55-241">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-241">Parameter</span></span> | <span data-ttu-id="39d55-242">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-242">Type</span></span> | <span data-ttu-id="39d55-243">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-244">referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-244">referenceId</span></span> | <span data-ttu-id="39d55-245">String</span><span class="sxs-lookup"><span data-stu-id="39d55-245">String</span></span> | <span data-ttu-id="39d55-246">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="39d55-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="39d55-247">reactionsCountMap</span></span> | <span data-ttu-id="39d55-248">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-248">Json object</span></span> | <span data-ttu-id="39d55-249">Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="39d55-250">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-250">Sample JSON Response</span></span>

```javascript
{
    "cursor": 636674054802000000,
    "summary": [
        {
            "referenceId": "4a44-51be-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        },
        {
            "referenceId": "4a44-51be-4b420-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 10,
                "comment": 14
            }
        }
    ]
}
```

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="39d55-251">OBTENIR plus d’informations /reaction pour une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="39d55-252">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="39d55-252">Request Parameters</span></span>

|  | <span data-ttu-id="39d55-253">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-253">Parameter</span></span> | <span data-ttu-id="39d55-254">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-254">Type</span></span> | <span data-ttu-id="39d55-255">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="39d55-255">Optional?</span></span> | <span data-ttu-id="39d55-256">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="39d55-257">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-257">URL Path Parameter</span></span> | <span data-ttu-id="39d55-258">groupId</span><span class="sxs-lookup"><span data-stu-id="39d55-258">groupId</span></span> | <span data-ttu-id="39d55-259">String</span><span class="sxs-lookup"><span data-stu-id="39d55-259">String</span></span> | <span data-ttu-id="39d55-260">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-260">No</span></span> | <span data-ttu-id="39d55-261">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="39d55-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="39d55-262">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-262">URL Path Parameter</span></span> | <span data-ttu-id="39d55-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="39d55-263">sourceGroupId</span></span> | <span data-ttu-id="39d55-264">String</span><span class="sxs-lookup"><span data-stu-id="39d55-264">String</span></span> | <span data-ttu-id="39d55-265">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-265">No</span></span> | <span data-ttu-id="39d55-266">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="39d55-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="39d55-267">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-267">URL Path Parameter</span></span> | <span data-ttu-id="39d55-268">referenceId</span><span class="sxs-lookup"><span data-stu-id="39d55-268">referenceId</span></span> | <span data-ttu-id="39d55-269">String</span><span class="sxs-lookup"><span data-stu-id="39d55-269">String</span></span> | <span data-ttu-id="39d55-270">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-270">No</span></span> | <span data-ttu-id="39d55-271">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="39d55-272">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-272">URL Path Parameter</span></span> | <span data-ttu-id="39d55-273">reactionType</span><span class="sxs-lookup"><span data-stu-id="39d55-273">reactionType</span></span> | <span data-ttu-id="39d55-274">String</span><span class="sxs-lookup"><span data-stu-id="39d55-274">String</span></span> | <span data-ttu-id="39d55-275">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-275">No</span></span> | <span data-ttu-id="39d55-276">Valeur enum : « Like'/ ' commentaire »</span><span class="sxs-lookup"><span data-stu-id="39d55-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="39d55-277">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="39d55-277">URL Path Parameter</span></span> | <span data-ttu-id="39d55-278">curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-278">cursor</span></span> | <span data-ttu-id="39d55-279">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="39d55-279">TimeStamp</span></span> | <span data-ttu-id="39d55-280">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-280">No</span></span> | <span data-ttu-id="39d55-281">Horodatage à partir de laquelle le résumé doit être calculée.</span><span class="sxs-lookup"><span data-stu-id="39d55-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="39d55-282">La valeur 0 par défaut</span><span class="sxs-lookup"><span data-stu-id="39d55-282">Default value 0</span></span> |
| <span data-ttu-id="39d55-283">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="39d55-283">HTTP Header</span></span> | <span data-ttu-id="39d55-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="39d55-284">accessToken</span></span> | <span data-ttu-id="39d55-285">String</span><span class="sxs-lookup"><span data-stu-id="39d55-285">String</span></span> | <span data-ttu-id="39d55-286">Non</span><span class="sxs-lookup"><span data-stu-id="39d55-286">No</span></span> | <span data-ttu-id="39d55-287">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="39d55-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="39d55-288">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-288">Response body</span></span>

| <span data-ttu-id="39d55-289">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-289">Parameter</span></span> | <span data-ttu-id="39d55-290">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-290">Type</span></span> | <span data-ttu-id="39d55-291">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-292">curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-292">cursor</span></span> | <span data-ttu-id="39d55-293">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="39d55-293">TimeStamp</span></span> | <span data-ttu-id="39d55-294">Horodatage jusqu'à laquelle reactionDetail a été fournie.</span><span class="sxs-lookup"><span data-stu-id="39d55-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="39d55-295">L’ensemble suivant de reactionDetails peut être générée à l’aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="39d55-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="39d55-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="39d55-296">reactionDetails</span></span> | <span data-ttu-id="39d55-297">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-297">JSON Array</span></span> | <span data-ttu-id="39d55-298">Tableau de JSON objets chaque détail réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="39d55-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="39d55-299">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="39d55-299">Response body summary object</span></span>

| <span data-ttu-id="39d55-300">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39d55-300">Parameter</span></span> | <span data-ttu-id="39d55-301">Type</span><span class="sxs-lookup"><span data-stu-id="39d55-301">Type</span></span> | <span data-ttu-id="39d55-302">Description</span><span class="sxs-lookup"><span data-stu-id="39d55-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="39d55-303">reactionId</span><span class="sxs-lookup"><span data-stu-id="39d55-303">reactionId</span></span> | <span data-ttu-id="39d55-304">String</span><span class="sxs-lookup"><span data-stu-id="39d55-304">String</span></span> | <span data-ttu-id="39d55-305">GUID représentant l’id de la réaction créée sur referenceId représentant une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="39d55-306">userId</span><span class="sxs-lookup"><span data-stu-id="39d55-306">userId</span></span> | <span data-ttu-id="39d55-307">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-307">Json object</span></span> | <span data-ttu-id="39d55-308">Nom d’utilisateur de l’utilisateur qui a créé la réaction d’une Action</span><span class="sxs-lookup"><span data-stu-id="39d55-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="39d55-309">heure de dernière modification</span><span class="sxs-lookup"><span data-stu-id="39d55-309">lastModifiedTime</span></span> | <span data-ttu-id="39d55-310">Timestamp</span><span class="sxs-lookup"><span data-stu-id="39d55-310">Timestamp</span></span> | <span data-ttu-id="39d55-311">Horodatage auquel réaction a été créé ou mis à jour</span><span class="sxs-lookup"><span data-stu-id="39d55-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="39d55-312">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="39d55-312">Sample JSON Response</span></span>

```javascript
{
    "cursor": 636674054802000000,
    "reactionDetails": [
        {
            "lastModifiedTime": 1529573303063,
            "reactionId": "4b2fb78b-b529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4e7b-84eb-4e228406fb9b"
        },
        {
            "lastModifiedTime": 1529573313063,
            "reactionId": "4b2fb7529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4eb-4e228406fb9b"
        }
    ]
}
```