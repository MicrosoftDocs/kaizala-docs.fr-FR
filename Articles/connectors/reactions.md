---
title: /Reaction
description: Article de référence pour l'API permettant d'interroger les réactions sur n'importe quelle action envoyée dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33191301"
---
# <a name="reaction"></a><span data-ttu-id="ab7a7-103">/Reaction</span><span class="sxs-lookup"><span data-stu-id="ab7a7-103">/reaction</span></span>
<span data-ttu-id="ab7a7-104">Point de terminaison d'API pour les données de réactions de requête sur n'importe quelle action envoyée dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="ab7a7-105">POST/reaction</span><span class="sxs-lookup"><span data-stu-id="ab7a7-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="ab7a7-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-106">Request Parameters</span></span>

| | <span data-ttu-id="ab7a7-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-107">Parameter</span></span> | <span data-ttu-id="ab7a7-108">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-108">Type</span></span> | <span data-ttu-id="ab7a7-109">Module?</span><span class="sxs-lookup"><span data-stu-id="ab7a7-109">Optional?</span></span> | <span data-ttu-id="ab7a7-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="ab7a7-111">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-111">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-112">groupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-112">groupId</span></span> | <span data-ttu-id="ab7a7-113">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-113">String</span></span> | <span data-ttu-id="ab7a7-114">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-114">No</span></span> | <span data-ttu-id="ab7a7-115">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ab7a7-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ab7a7-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ab7a7-116">HTTP Header</span></span> | <span data-ttu-id="ab7a7-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="ab7a7-117">accessToken</span></span> | <span data-ttu-id="ab7a7-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-118">String</span></span> | <span data-ttu-id="ab7a7-119">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-119">No</span></span> | <span data-ttu-id="ab7a7-120">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ab7a7-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="ab7a7-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ab7a7-121">HTTP Header</span></span> | <span data-ttu-id="ab7a7-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-122">Content-Type</span></span> | <span data-ttu-id="ab7a7-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-123">String</span></span> | <span data-ttu-id="ab7a7-124">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-124">No</span></span> | <span data-ttu-id="ab7a7-125">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="ab7a7-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-126">Request body</span></span>

| <span data-ttu-id="ab7a7-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-127">Parameter</span></span> | <span data-ttu-id="ab7a7-128">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-128">Type</span></span> | <span data-ttu-id="ab7a7-129">Module?</span><span class="sxs-lookup"><span data-stu-id="ab7a7-129">Optional?</span></span> | <span data-ttu-id="ab7a7-130">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="ab7a7-131">ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-131">referenceId</span></span> | <span data-ttu-id="ab7a7-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-132">String</span></span> | <span data-ttu-id="ab7a7-133">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-133">No</span></span> | <span data-ttu-id="ab7a7-134">GUID représentant l'ID de la référence d'entité représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="ab7a7-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-135">sourceGroupId</span></span> | <span data-ttu-id="ab7a7-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-136">String</span></span> | <span data-ttu-id="ab7a7-137">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-137">No</span></span> | <span data-ttu-id="ab7a7-138">GUID du groupe dans lequel l'action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="ab7a7-139">Dans le cas de groupes qui sont un sous-groupe d'un autre groupe, cela peut être différent de «groupId» fourni dans le paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="ab7a7-140">reactionType</span><span class="sxs-lookup"><span data-stu-id="ab7a7-140">reactionType</span></span> | <span data-ttu-id="ab7a7-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-141">String</span></span> | <span data-ttu-id="ab7a7-142">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-142">No</span></span> | <span data-ttu-id="ab7a7-143">Valeur enum: 'like'/'commentaire'</span><span class="sxs-lookup"><span data-stu-id="ab7a7-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="ab7a7-144">comment</span><span class="sxs-lookup"><span data-stu-id="ab7a7-144">comment</span></span> | <span data-ttu-id="ab7a7-145">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-145">String</span></span> | <span data-ttu-id="ab7a7-146">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-146">No</span></span> | <span data-ttu-id="ab7a7-147">Le texte du commentaire est obligatoire uniquement pour reactionType'commentaire'.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="ab7a7-148">Pour'like', ceci doit être ignoré</span><span class="sxs-lookup"><span data-stu-id="ab7a7-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="ab7a7-149">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="ab7a7-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-150">Response body</span></span>

| <span data-ttu-id="ab7a7-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-151">Parameter</span></span> | <span data-ttu-id="ab7a7-152">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-152">Type</span></span> | <span data-ttu-id="ab7a7-153">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-154">reactionId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-154">reactionId</span></span> | <span data-ttu-id="ab7a7-155">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-155">String</span></span> | <span data-ttu-id="ab7a7-156">GUID représentant l'ID de l'entité de réaction après exécution réussie de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ab7a7-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="ab7a7-158">OBTENIR un résumé/reaction au niveau de l'action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="ab7a7-159">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-159">Request Parameters</span></span>

|  | <span data-ttu-id="ab7a7-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-160">Parameter</span></span> | <span data-ttu-id="ab7a7-161">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-161">Type</span></span> | <span data-ttu-id="ab7a7-162">Module?</span><span class="sxs-lookup"><span data-stu-id="ab7a7-162">Optional?</span></span> | <span data-ttu-id="ab7a7-163">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-164">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-164">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-165">groupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-165">groupId</span></span> | <span data-ttu-id="ab7a7-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-166">String</span></span> | <span data-ttu-id="ab7a7-167">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-167">No</span></span> | <span data-ttu-id="ab7a7-168">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ab7a7-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ab7a7-169">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-169">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-170">ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-170">referenceId</span></span> | <span data-ttu-id="ab7a7-171">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-171">String</span></span> | <span data-ttu-id="ab7a7-172">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-172">No</span></span> | <span data-ttu-id="ab7a7-173">GUID représentant l'ID de la référence d'entité représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="ab7a7-174">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-174">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-175">sourceGroupId</span></span> | <span data-ttu-id="ab7a7-176">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-176">String</span></span> | <span data-ttu-id="ab7a7-177">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-177">No</span></span> | <span data-ttu-id="ab7a7-178">GUID du groupe dans lequel l'action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="ab7a7-179">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ab7a7-179">HTTP Header</span></span> | <span data-ttu-id="ab7a7-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="ab7a7-180">accessToken</span></span> | <span data-ttu-id="ab7a7-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-181">String</span></span> | <span data-ttu-id="ab7a7-182">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-182">No</span></span> | <span data-ttu-id="ab7a7-183">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ab7a7-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="ab7a7-184">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-184">Response body</span></span>

| <span data-ttu-id="ab7a7-185">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-185">Parameter</span></span> | <span data-ttu-id="ab7a7-186">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-186">Type</span></span> | <span data-ttu-id="ab7a7-187">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-188">résumé</span><span class="sxs-lookup"><span data-stu-id="ab7a7-188">summary</span></span> | <span data-ttu-id="ab7a7-189">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-189">JSON Array</span></span> | <span data-ttu-id="ab7a7-190">Tableau d'objets JSON représentant chacun une synthèse des réactions sur une action envoyée dans un groupe</span><span class="sxs-lookup"><span data-stu-id="ab7a7-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="ab7a7-191">Objet de synthèse du corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-191">Response body summary object</span></span>

| <span data-ttu-id="ab7a7-192">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-192">Parameter</span></span> | <span data-ttu-id="ab7a7-193">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-193">Type</span></span> | <span data-ttu-id="ab7a7-194">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-195">ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-195">referenceId</span></span> | <span data-ttu-id="ab7a7-196">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-196">String</span></span> | <span data-ttu-id="ab7a7-197">GUID représentant l'ID de la référence d'entité représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="ab7a7-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="ab7a7-198">reactionsCountMap</span></span> | <span data-ttu-id="ab7a7-199">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-199">Json object</span></span> | <span data-ttu-id="ab7a7-200">Objet JSON contenant le nombre d'objets et de commentaires pour ce ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="ab7a7-201">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-201">Sample JSON Response</span></span>

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

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="ab7a7-202">OBTENIR un résumé/reaction au niveau du groupe</span><span class="sxs-lookup"><span data-stu-id="ab7a7-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="ab7a7-203">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-203">Request Parameters</span></span>

|  | <span data-ttu-id="ab7a7-204">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-204">Parameter</span></span> | <span data-ttu-id="ab7a7-205">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-205">Type</span></span> | <span data-ttu-id="ab7a7-206">Module?</span><span class="sxs-lookup"><span data-stu-id="ab7a7-206">Optional?</span></span> | <span data-ttu-id="ab7a7-207">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-208">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-208">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-209">groupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-209">groupId</span></span> | <span data-ttu-id="ab7a7-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-210">String</span></span> | <span data-ttu-id="ab7a7-211">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-211">No</span></span> | <span data-ttu-id="ab7a7-212">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ab7a7-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ab7a7-213">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-213">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-214">sourceGroupId</span></span> | <span data-ttu-id="ab7a7-215">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-215">String</span></span> | <span data-ttu-id="ab7a7-216">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-216">No</span></span> | <span data-ttu-id="ab7a7-217">GUID du groupe dans lequel l'action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="ab7a7-218">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-218">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-219">curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-219">cursor</span></span> | <span data-ttu-id="ab7a7-220">Dates</span><span class="sxs-lookup"><span data-stu-id="ab7a7-220">timeStamp</span></span> | <span data-ttu-id="ab7a7-221">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-221">No</span></span> | <span data-ttu-id="ab7a7-222">Horodatage à partir duquel le résumé doit être calculé.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="ab7a7-223">Valeur par défaut 0</span><span class="sxs-lookup"><span data-stu-id="ab7a7-223">Default value 0</span></span> |
| <span data-ttu-id="ab7a7-224">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ab7a7-224">HTTP Header</span></span> | <span data-ttu-id="ab7a7-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="ab7a7-225">accessToken</span></span> | <span data-ttu-id="ab7a7-226">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-226">String</span></span> | <span data-ttu-id="ab7a7-227">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-227">No</span></span> | <span data-ttu-id="ab7a7-228">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ab7a7-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="ab7a7-229">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-229">Response body</span></span>

| <span data-ttu-id="ab7a7-230">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-230">Parameter</span></span> | <span data-ttu-id="ab7a7-231">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-231">Type</span></span> | <span data-ttu-id="ab7a7-232">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-233">curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-233">cursor</span></span> | <span data-ttu-id="ab7a7-234">Dates</span><span class="sxs-lookup"><span data-stu-id="ab7a7-234">timeStamp</span></span> | <span data-ttu-id="ab7a7-235">timeStamp: le résumé qui a été calculé.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="ab7a7-236">Le prochain jeu de reactionSummary peut être généré à l'aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="ab7a7-237">résumé</span><span class="sxs-lookup"><span data-stu-id="ab7a7-237">summary</span></span> | <span data-ttu-id="ab7a7-238">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-238">JSON Array</span></span> | <span data-ttu-id="ab7a7-239">Tableau d'objets JSON représentant chacun une synthèse des réactions sur une action envoyée dans un groupe</span><span class="sxs-lookup"><span data-stu-id="ab7a7-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="ab7a7-240">Objet de synthèse du corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-240">Response body summary object</span></span>

| <span data-ttu-id="ab7a7-241">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-241">Parameter</span></span> | <span data-ttu-id="ab7a7-242">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-242">Type</span></span> | <span data-ttu-id="ab7a7-243">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-244">ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-244">referenceId</span></span> | <span data-ttu-id="ab7a7-245">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-245">String</span></span> | <span data-ttu-id="ab7a7-246">GUID représentant l'ID de la référence d'entité représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="ab7a7-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="ab7a7-247">reactionsCountMap</span></span> | <span data-ttu-id="ab7a7-248">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-248">Json object</span></span> | <span data-ttu-id="ab7a7-249">Objet JSON contenant le nombre d'objets et de commentaires pour ce ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="ab7a7-250">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-250">Sample JSON Response</span></span>

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

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="ab7a7-251">OBTENIR les détails de/reaction pour une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="ab7a7-252">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ab7a7-252">Request Parameters</span></span>

|  | <span data-ttu-id="ab7a7-253">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-253">Parameter</span></span> | <span data-ttu-id="ab7a7-254">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-254">Type</span></span> | <span data-ttu-id="ab7a7-255">Module?</span><span class="sxs-lookup"><span data-stu-id="ab7a7-255">Optional?</span></span> | <span data-ttu-id="ab7a7-256">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-257">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-257">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-258">groupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-258">groupId</span></span> | <span data-ttu-id="ab7a7-259">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-259">String</span></span> | <span data-ttu-id="ab7a7-260">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-260">No</span></span> | <span data-ttu-id="ab7a7-261">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ab7a7-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ab7a7-262">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-262">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-263">sourceGroupId</span></span> | <span data-ttu-id="ab7a7-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-264">String</span></span> | <span data-ttu-id="ab7a7-265">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-265">No</span></span> | <span data-ttu-id="ab7a7-266">GUID du groupe dans lequel l'action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="ab7a7-267">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-267">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-268">ID</span><span class="sxs-lookup"><span data-stu-id="ab7a7-268">referenceId</span></span> | <span data-ttu-id="ab7a7-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-269">String</span></span> | <span data-ttu-id="ab7a7-270">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-270">No</span></span> | <span data-ttu-id="ab7a7-271">GUID représentant l'ID de la référence d'entité représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="ab7a7-272">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-272">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-273">reactionType</span><span class="sxs-lookup"><span data-stu-id="ab7a7-273">reactionType</span></span> | <span data-ttu-id="ab7a7-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-274">String</span></span> | <span data-ttu-id="ab7a7-275">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-275">No</span></span> | <span data-ttu-id="ab7a7-276">Valeur enum: 'like'/'commentaire'</span><span class="sxs-lookup"><span data-stu-id="ab7a7-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="ab7a7-277">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ab7a7-277">URL Path Parameter</span></span> | <span data-ttu-id="ab7a7-278">curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-278">cursor</span></span> | <span data-ttu-id="ab7a7-279">Dates</span><span class="sxs-lookup"><span data-stu-id="ab7a7-279">TimeStamp</span></span> | <span data-ttu-id="ab7a7-280">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-280">No</span></span> | <span data-ttu-id="ab7a7-281">Horodatage à partir duquel le résumé doit être calculé.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="ab7a7-282">Valeur par défaut 0</span><span class="sxs-lookup"><span data-stu-id="ab7a7-282">Default value 0</span></span> |
| <span data-ttu-id="ab7a7-283">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ab7a7-283">HTTP Header</span></span> | <span data-ttu-id="ab7a7-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="ab7a7-284">accessToken</span></span> | <span data-ttu-id="ab7a7-285">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-285">String</span></span> | <span data-ttu-id="ab7a7-286">Non</span><span class="sxs-lookup"><span data-stu-id="ab7a7-286">No</span></span> | <span data-ttu-id="ab7a7-287">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ab7a7-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="ab7a7-288">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-288">Response body</span></span>

| <span data-ttu-id="ab7a7-289">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-289">Parameter</span></span> | <span data-ttu-id="ab7a7-290">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-290">Type</span></span> | <span data-ttu-id="ab7a7-291">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-292">curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-292">cursor</span></span> | <span data-ttu-id="ab7a7-293">Dates</span><span class="sxs-lookup"><span data-stu-id="ab7a7-293">TimeStamp</span></span> | <span data-ttu-id="ab7a7-294">TimeStamp pour laquelle reactionDetail a été fourni.</span><span class="sxs-lookup"><span data-stu-id="ab7a7-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="ab7a7-295">Le prochain jeu de reactionDetails peut être généré à l'aide de cette valeur de curseur</span><span class="sxs-lookup"><span data-stu-id="ab7a7-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="ab7a7-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="ab7a7-296">reactionDetails</span></span> | <span data-ttu-id="ab7a7-297">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-297">JSON Array</span></span> | <span data-ttu-id="ab7a7-298">Tableau d'objets JSON chacun représentant les réactions détaillées sur une action envoyée dans un groupe</span><span class="sxs-lookup"><span data-stu-id="ab7a7-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="ab7a7-299">Objet de synthèse du corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ab7a7-299">Response body summary object</span></span>

| <span data-ttu-id="ab7a7-300">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ab7a7-300">Parameter</span></span> | <span data-ttu-id="ab7a7-301">Type</span><span class="sxs-lookup"><span data-stu-id="ab7a7-301">Type</span></span> | <span data-ttu-id="ab7a7-302">Description</span><span class="sxs-lookup"><span data-stu-id="ab7a7-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ab7a7-303">reactionId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-303">reactionId</span></span> | <span data-ttu-id="ab7a7-304">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ab7a7-304">String</span></span> | <span data-ttu-id="ab7a7-305">GUID représentant l'ID de la réaction créée sur ID représentant une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="ab7a7-306">userId</span><span class="sxs-lookup"><span data-stu-id="ab7a7-306">userId</span></span> | <span data-ttu-id="ab7a7-307">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-307">Json object</span></span> | <span data-ttu-id="ab7a7-308">UserId de l'utilisateur qui a créé la réaction sur une action</span><span class="sxs-lookup"><span data-stu-id="ab7a7-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="ab7a7-309">lastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="ab7a7-309">lastModifiedTime</span></span> | <span data-ttu-id="ab7a7-310">Timestamp</span><span class="sxs-lookup"><span data-stu-id="ab7a7-310">Timestamp</span></span> | <span data-ttu-id="ab7a7-311">Horodateur à partir duquel la réaction a été créée/mise à jour</span><span class="sxs-lookup"><span data-stu-id="ab7a7-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="ab7a7-312">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ab7a7-312">Sample JSON Response</span></span>

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