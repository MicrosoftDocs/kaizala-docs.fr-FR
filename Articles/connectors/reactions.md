---
title: /REACTION
description: Article de référence de l’API réactions de requête sur n’importe quelle Action envoyé dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 4f2da7302133371dba5edd6035a57068e16aae63
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20425631"
---
# <a name="reaction"></a><span data-ttu-id="264a9-103">/REACTION</span><span class="sxs-lookup"><span data-stu-id="264a9-103">/reaction</span></span>
<span data-ttu-id="264a9-104">Point de terminaison API pour interroger les données réactions sur n’importe quelle Action envoyée dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="264a9-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="264a9-105">/Reaction POST</span><span class="sxs-lookup"><span data-stu-id="264a9-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="264a9-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="264a9-106">Request Parameters</span></span>

| | <span data-ttu-id="264a9-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-107">Parameter</span></span> | <span data-ttu-id="264a9-108">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-108">Type</span></span> | <span data-ttu-id="264a9-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="264a9-109">Optional?</span></span> | <span data-ttu-id="264a9-110">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="264a9-111">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-111">URL Path Parameter</span></span> | <span data-ttu-id="264a9-112">groupId</span><span class="sxs-lookup"><span data-stu-id="264a9-112">groupId</span></span> | <span data-ttu-id="264a9-113">String</span><span class="sxs-lookup"><span data-stu-id="264a9-113">String</span></span> | <span data-ttu-id="264a9-114">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-114">No</span></span> | <span data-ttu-id="264a9-115">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="264a9-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="264a9-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="264a9-116">HTTP Header</span></span> | <span data-ttu-id="264a9-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="264a9-117">accessToken</span></span> | <span data-ttu-id="264a9-118">String</span><span class="sxs-lookup"><span data-stu-id="264a9-118">String</span></span> | <span data-ttu-id="264a9-119">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-119">No</span></span> | <span data-ttu-id="264a9-120">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="264a9-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="264a9-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="264a9-121">HTTP Header</span></span> | <span data-ttu-id="264a9-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="264a9-122">Content-Type</span></span> | <span data-ttu-id="264a9-123">String</span><span class="sxs-lookup"><span data-stu-id="264a9-123">String</span></span> | <span data-ttu-id="264a9-124">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-124">No</span></span> | <span data-ttu-id="264a9-125">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="264a9-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="264a9-126">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="264a9-126">Request body</span></span>

| <span data-ttu-id="264a9-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-127">Parameter</span></span> | <span data-ttu-id="264a9-128">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-128">Type</span></span> | <span data-ttu-id="264a9-129">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="264a9-129">Optional?</span></span> | <span data-ttu-id="264a9-130">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="264a9-131">referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-131">referenceId</span></span> | <span data-ttu-id="264a9-132">String</span><span class="sxs-lookup"><span data-stu-id="264a9-132">String</span></span> | <span data-ttu-id="264a9-133">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-133">No</span></span> | <span data-ttu-id="264a9-134">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="264a9-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="264a9-135">sourceGroupId</span></span> | <span data-ttu-id="264a9-136">String</span><span class="sxs-lookup"><span data-stu-id="264a9-136">String</span></span> | <span data-ttu-id="264a9-137">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-137">No</span></span> | <span data-ttu-id="264a9-138">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="264a9-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="264a9-139">En cas de groupes est d’un autre groupe de celle-ci peut différer de 'groupId' fourni dans l’url de paramètre de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="264a9-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="264a9-140">reactionType</span><span class="sxs-lookup"><span data-stu-id="264a9-140">reactionType</span></span> | <span data-ttu-id="264a9-141">String</span><span class="sxs-lookup"><span data-stu-id="264a9-141">String</span></span> | <span data-ttu-id="264a9-142">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-142">No</span></span> | <span data-ttu-id="264a9-143">Valeur enum : « Like'/ ' commentaire »</span><span class="sxs-lookup"><span data-stu-id="264a9-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="264a9-144">comment</span><span class="sxs-lookup"><span data-stu-id="264a9-144">comment</span></span> | <span data-ttu-id="264a9-145">String</span><span class="sxs-lookup"><span data-stu-id="264a9-145">String</span></span> | <span data-ttu-id="264a9-146">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-146">No</span></span> | <span data-ttu-id="264a9-147">Texte de commentaire est obligatoire uniquement pour reactionType « Comment ».</span><span class="sxs-lookup"><span data-stu-id="264a9-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="264a9-148">Pour « Like », il doit être ignoré</span><span class="sxs-lookup"><span data-stu-id="264a9-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="264a9-149">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="264a9-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-150">Response body</span></span>

| <span data-ttu-id="264a9-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-151">Parameter</span></span> | <span data-ttu-id="264a9-152">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-152">Type</span></span> | <span data-ttu-id="264a9-153">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-154">reactionId</span><span class="sxs-lookup"><span data-stu-id="264a9-154">reactionId</span></span> | <span data-ttu-id="264a9-155">String</span><span class="sxs-lookup"><span data-stu-id="264a9-155">String</span></span> | <span data-ttu-id="264a9-156">GUID représentant l’id de l’entité réaction après l’exécution réussie de la demande</span><span class="sxs-lookup"><span data-stu-id="264a9-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="264a9-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="264a9-158">OBTENIR /reaction résumé au niveau de l’Action</span><span class="sxs-lookup"><span data-stu-id="264a9-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="264a9-159">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="264a9-159">Request Parameters</span></span>

|  | <span data-ttu-id="264a9-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-160">Parameter</span></span> | <span data-ttu-id="264a9-161">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-161">Type</span></span> | <span data-ttu-id="264a9-162">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="264a9-162">Optional?</span></span> | <span data-ttu-id="264a9-163">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="264a9-164">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-164">URL Path Parameter</span></span> | <span data-ttu-id="264a9-165">groupId</span><span class="sxs-lookup"><span data-stu-id="264a9-165">groupId</span></span> | <span data-ttu-id="264a9-166">String</span><span class="sxs-lookup"><span data-stu-id="264a9-166">String</span></span> | <span data-ttu-id="264a9-167">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-167">No</span></span> | <span data-ttu-id="264a9-168">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="264a9-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="264a9-169">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-169">URL Path Parameter</span></span> | <span data-ttu-id="264a9-170">referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-170">referenceId</span></span> | <span data-ttu-id="264a9-171">String</span><span class="sxs-lookup"><span data-stu-id="264a9-171">String</span></span> | <span data-ttu-id="264a9-172">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-172">No</span></span> | <span data-ttu-id="264a9-173">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="264a9-174">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-174">URL Path Parameter</span></span> | <span data-ttu-id="264a9-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="264a9-175">sourceGroupId</span></span> | <span data-ttu-id="264a9-176">String</span><span class="sxs-lookup"><span data-stu-id="264a9-176">String</span></span> | <span data-ttu-id="264a9-177">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-177">No</span></span> | <span data-ttu-id="264a9-178">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="264a9-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="264a9-179">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="264a9-179">HTTP Header</span></span> | <span data-ttu-id="264a9-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="264a9-180">accessToken</span></span> | <span data-ttu-id="264a9-181">String</span><span class="sxs-lookup"><span data-stu-id="264a9-181">String</span></span> | <span data-ttu-id="264a9-182">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-182">No</span></span> | <span data-ttu-id="264a9-183">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="264a9-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="264a9-184">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-184">Response body</span></span>

| <span data-ttu-id="264a9-185">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-185">Parameter</span></span> | <span data-ttu-id="264a9-186">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-186">Type</span></span> | <span data-ttu-id="264a9-187">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-188">Résumé</span><span class="sxs-lookup"><span data-stu-id="264a9-188">summary</span></span> | <span data-ttu-id="264a9-189">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-189">JSON Array</span></span> | <span data-ttu-id="264a9-190">Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="264a9-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="264a9-191">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-191">Response body summary object</span></span>

| <span data-ttu-id="264a9-192">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-192">Parameter</span></span> | <span data-ttu-id="264a9-193">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-193">Type</span></span> | <span data-ttu-id="264a9-194">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-195">referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-195">referenceId</span></span> | <span data-ttu-id="264a9-196">String</span><span class="sxs-lookup"><span data-stu-id="264a9-196">String</span></span> | <span data-ttu-id="264a9-197">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="264a9-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="264a9-198">reactionsCountMap</span></span> | <span data-ttu-id="264a9-199">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-199">Json object</span></span> | <span data-ttu-id="264a9-200">Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="264a9-201">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-201">Sample JSON Response</span></span>

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

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="264a9-202">OBTENIR /reaction résumé au niveau de groupe</span><span class="sxs-lookup"><span data-stu-id="264a9-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="264a9-203">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="264a9-203">Request Parameters</span></span>

|  | <span data-ttu-id="264a9-204">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-204">Parameter</span></span> | <span data-ttu-id="264a9-205">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-205">Type</span></span> | <span data-ttu-id="264a9-206">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="264a9-206">Optional?</span></span> | <span data-ttu-id="264a9-207">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="264a9-208">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-208">URL Path Parameter</span></span> | <span data-ttu-id="264a9-209">groupId</span><span class="sxs-lookup"><span data-stu-id="264a9-209">groupId</span></span> | <span data-ttu-id="264a9-210">String</span><span class="sxs-lookup"><span data-stu-id="264a9-210">String</span></span> | <span data-ttu-id="264a9-211">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-211">No</span></span> | <span data-ttu-id="264a9-212">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="264a9-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="264a9-213">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-213">URL Path Parameter</span></span> | <span data-ttu-id="264a9-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="264a9-214">sourceGroupId</span></span> | <span data-ttu-id="264a9-215">String</span><span class="sxs-lookup"><span data-stu-id="264a9-215">String</span></span> | <span data-ttu-id="264a9-216">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-216">No</span></span> | <span data-ttu-id="264a9-217">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="264a9-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="264a9-218">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-218">URL Path Parameter</span></span> | <span data-ttu-id="264a9-219">curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-219">cursor</span></span> | <span data-ttu-id="264a9-220">Horodatage</span><span class="sxs-lookup"><span data-stu-id="264a9-220">timeStamp</span></span> | <span data-ttu-id="264a9-221">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-221">No</span></span> | <span data-ttu-id="264a9-222">Horodatage à partir de laquelle le résumé doit être calculée.</span><span class="sxs-lookup"><span data-stu-id="264a9-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="264a9-223">La valeur 0 par défaut</span><span class="sxs-lookup"><span data-stu-id="264a9-223">Default value 0</span></span> |
| <span data-ttu-id="264a9-224">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="264a9-224">HTTP Header</span></span> | <span data-ttu-id="264a9-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="264a9-225">accessToken</span></span> | <span data-ttu-id="264a9-226">String</span><span class="sxs-lookup"><span data-stu-id="264a9-226">String</span></span> | <span data-ttu-id="264a9-227">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-227">No</span></span> | <span data-ttu-id="264a9-228">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="264a9-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="264a9-229">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-229">Response body</span></span>

| <span data-ttu-id="264a9-230">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-230">Parameter</span></span> | <span data-ttu-id="264a9-231">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-231">Type</span></span> | <span data-ttu-id="264a9-232">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-233">curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-233">cursor</span></span> | <span data-ttu-id="264a9-234">Horodatage</span><span class="sxs-lookup"><span data-stu-id="264a9-234">timeStamp</span></span> | <span data-ttu-id="264a9-235">Horodatage jusqu'à laquelle résumé a été calculé.</span><span class="sxs-lookup"><span data-stu-id="264a9-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="264a9-236">L’ensemble suivant de reactionSummary peut être générée à l’aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="264a9-237">Résumé</span><span class="sxs-lookup"><span data-stu-id="264a9-237">summary</span></span> | <span data-ttu-id="264a9-238">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-238">JSON Array</span></span> | <span data-ttu-id="264a9-239">Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="264a9-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="264a9-240">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-240">Response body summary object</span></span>

| <span data-ttu-id="264a9-241">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-241">Parameter</span></span> | <span data-ttu-id="264a9-242">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-242">Type</span></span> | <span data-ttu-id="264a9-243">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-244">referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-244">referenceId</span></span> | <span data-ttu-id="264a9-245">String</span><span class="sxs-lookup"><span data-stu-id="264a9-245">String</span></span> | <span data-ttu-id="264a9-246">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="264a9-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="264a9-247">reactionsCountMap</span></span> | <span data-ttu-id="264a9-248">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-248">Json object</span></span> | <span data-ttu-id="264a9-249">Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="264a9-250">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-250">Sample JSON Response</span></span>

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

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="264a9-251">OBTENIR plus d’informations /reaction pour une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="264a9-252">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="264a9-252">Request Parameters</span></span>

|  | <span data-ttu-id="264a9-253">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-253">Parameter</span></span> | <span data-ttu-id="264a9-254">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-254">Type</span></span> | <span data-ttu-id="264a9-255">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="264a9-255">Optional?</span></span> | <span data-ttu-id="264a9-256">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="264a9-257">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-257">URL Path Parameter</span></span> | <span data-ttu-id="264a9-258">groupId</span><span class="sxs-lookup"><span data-stu-id="264a9-258">groupId</span></span> | <span data-ttu-id="264a9-259">String</span><span class="sxs-lookup"><span data-stu-id="264a9-259">String</span></span> | <span data-ttu-id="264a9-260">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-260">No</span></span> | <span data-ttu-id="264a9-261">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="264a9-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="264a9-262">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-262">URL Path Parameter</span></span> | <span data-ttu-id="264a9-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="264a9-263">sourceGroupId</span></span> | <span data-ttu-id="264a9-264">String</span><span class="sxs-lookup"><span data-stu-id="264a9-264">String</span></span> | <span data-ttu-id="264a9-265">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-265">No</span></span> | <span data-ttu-id="264a9-266">GUID du groupe dans lequel l’Action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="264a9-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="264a9-267">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-267">URL Path Parameter</span></span> | <span data-ttu-id="264a9-268">referenceId</span><span class="sxs-lookup"><span data-stu-id="264a9-268">referenceId</span></span> | <span data-ttu-id="264a9-269">String</span><span class="sxs-lookup"><span data-stu-id="264a9-269">String</span></span> | <span data-ttu-id="264a9-270">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-270">No</span></span> | <span data-ttu-id="264a9-271">GUID représentant l’id de référence d’entité qui représente une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="264a9-272">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-272">URL Path Parameter</span></span> | <span data-ttu-id="264a9-273">reactionType</span><span class="sxs-lookup"><span data-stu-id="264a9-273">reactionType</span></span> | <span data-ttu-id="264a9-274">String</span><span class="sxs-lookup"><span data-stu-id="264a9-274">String</span></span> | <span data-ttu-id="264a9-275">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-275">No</span></span> | <span data-ttu-id="264a9-276">Valeur enum : « Like'/ ' commentaire »</span><span class="sxs-lookup"><span data-stu-id="264a9-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="264a9-277">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="264a9-277">URL Path Parameter</span></span> | <span data-ttu-id="264a9-278">curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-278">cursor</span></span> | <span data-ttu-id="264a9-279">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="264a9-279">TimeStamp</span></span> | <span data-ttu-id="264a9-280">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-280">No</span></span> | <span data-ttu-id="264a9-281">Horodatage à partir de laquelle le résumé doit être calculée.</span><span class="sxs-lookup"><span data-stu-id="264a9-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="264a9-282">La valeur 0 par défaut</span><span class="sxs-lookup"><span data-stu-id="264a9-282">Default value 0</span></span> |
| <span data-ttu-id="264a9-283">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="264a9-283">HTTP Header</span></span> | <span data-ttu-id="264a9-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="264a9-284">accessToken</span></span> | <span data-ttu-id="264a9-285">String</span><span class="sxs-lookup"><span data-stu-id="264a9-285">String</span></span> | <span data-ttu-id="264a9-286">Non</span><span class="sxs-lookup"><span data-stu-id="264a9-286">No</span></span> | <span data-ttu-id="264a9-287">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="264a9-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="264a9-288">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-288">Response body</span></span>

| <span data-ttu-id="264a9-289">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-289">Parameter</span></span> | <span data-ttu-id="264a9-290">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-290">Type</span></span> | <span data-ttu-id="264a9-291">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-292">curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-292">cursor</span></span> | <span data-ttu-id="264a9-293">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="264a9-293">TimeStamp</span></span> | <span data-ttu-id="264a9-294">Horodatage jusqu'à laquelle reactionDetail a été fournie.</span><span class="sxs-lookup"><span data-stu-id="264a9-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="264a9-295">L’ensemble suivant de reactionDetails peut être générée à l’aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="264a9-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="264a9-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="264a9-296">reactionDetails</span></span> | <span data-ttu-id="264a9-297">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-297">JSON Array</span></span> | <span data-ttu-id="264a9-298">Tableau de JSON objets chaque détail réactions représentant une action envoyé dans un groupe</span><span class="sxs-lookup"><span data-stu-id="264a9-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="264a9-299">Objet synthèse de corps de réponse</span><span class="sxs-lookup"><span data-stu-id="264a9-299">Response body summary object</span></span>

| <span data-ttu-id="264a9-300">Paramètre</span><span class="sxs-lookup"><span data-stu-id="264a9-300">Parameter</span></span> | <span data-ttu-id="264a9-301">Type</span><span class="sxs-lookup"><span data-stu-id="264a9-301">Type</span></span> | <span data-ttu-id="264a9-302">Description</span><span class="sxs-lookup"><span data-stu-id="264a9-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="264a9-303">reactionId</span><span class="sxs-lookup"><span data-stu-id="264a9-303">reactionId</span></span> | <span data-ttu-id="264a9-304">String</span><span class="sxs-lookup"><span data-stu-id="264a9-304">String</span></span> | <span data-ttu-id="264a9-305">GUID représentant l’id de la réaction créée sur referenceId représentant une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="264a9-306">userId</span><span class="sxs-lookup"><span data-stu-id="264a9-306">userId</span></span> | <span data-ttu-id="264a9-307">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-307">Json object</span></span> | <span data-ttu-id="264a9-308">Nom d’utilisateur de l’utilisateur qui a créé la réaction d’une Action</span><span class="sxs-lookup"><span data-stu-id="264a9-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="264a9-309">heure de dernière modification</span><span class="sxs-lookup"><span data-stu-id="264a9-309">lastModifiedTime</span></span> | <span data-ttu-id="264a9-310">Timestamp</span><span class="sxs-lookup"><span data-stu-id="264a9-310">Timestamp</span></span> | <span data-ttu-id="264a9-311">Horodatage auquel réaction a été créé ou mis à jour</span><span class="sxs-lookup"><span data-stu-id="264a9-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="264a9-312">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="264a9-312">Sample JSON Response</span></span>

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