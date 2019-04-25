---
title: /subscribers
description: Article de référence pour les API permettant d'obtenir les données des abonnés pour les groupes publics
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190697"
---
# <a name="subscribers"></a><span data-ttu-id="ff158-103">/subscribers</span><span class="sxs-lookup"><span data-stu-id="ff158-103">/subscribers</span></span>

<span data-ttu-id="ff158-104">Point de terminaison d'API pour ajouter, obtenir ou supprimer des abonnés à partir d'un groupe public géré.</span><span class="sxs-lookup"><span data-stu-id="ff158-104">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

## <a name="add-subscribers"></a><span data-ttu-id="ff158-105">Ajouter/subscribers</span><span class="sxs-lookup"><span data-stu-id="ff158-105">ADD /subscribers</span></span>

    <span data-ttu-id="ff158-106">PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/add</span><span class="sxs-lookup"><span data-stu-id="ff158-106">PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add</span></span>

### <a name="request-parameters"></a><span data-ttu-id="ff158-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-107">Request Parameters</span></span>
|  | <span data-ttu-id="ff158-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-108">Parameter</span></span> | <span data-ttu-id="ff158-109">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-109">Type</span></span> | <span data-ttu-id="ff158-110">Module?</span><span class="sxs-lookup"><span data-stu-id="ff158-110">Optional?</span></span> | <span data-ttu-id="ff158-111">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ff158-112">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ff158-112">URL Path Parameter</span></span> | <span data-ttu-id="ff158-113">groupId</span><span class="sxs-lookup"><span data-stu-id="ff158-113">groupId</span></span> | <span data-ttu-id="ff158-114">String</span><span class="sxs-lookup"><span data-stu-id="ff158-114">String</span></span> | <span data-ttu-id="ff158-115">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-115">No</span></span> | <span data-ttu-id="ff158-116">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ff158-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ff158-117">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ff158-117">HTTP Header</span></span> | <span data-ttu-id="ff158-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="ff158-118">accessToken</span></span> | <span data-ttu-id="ff158-119">String</span><span class="sxs-lookup"><span data-stu-id="ff158-119">String</span></span> | <span data-ttu-id="ff158-120">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-120">No</span></span> | <span data-ttu-id="ff158-121">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ff158-121">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="ff158-122">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-122">Request body</span></span>
| <span data-ttu-id="ff158-123">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-123">Parameter</span></span> | <span data-ttu-id="ff158-124">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-124">Type</span></span> | <span data-ttu-id="ff158-125">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-125">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ff158-126">leurs</span><span class="sxs-lookup"><span data-stu-id="ff158-126">subscribers</span></span> | <span data-ttu-id="ff158-127">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="ff158-127">String[]</span></span> | <span data-ttu-id="ff158-128">Chaque chaîne représente le numéro de téléphone mobile avec le code pays (par exemple,</span><span class="sxs-lookup"><span data-stu-id="ff158-128">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="ff158-129">+ 911111111111)</span><span class="sxs-lookup"><span data-stu-id="ff158-129">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="ff158-130">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-130">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="ff158-131">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ff158-131">Response body</span></span>
| <span data-ttu-id="ff158-132">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-132">Parameter</span></span> | <span data-ttu-id="ff158-133">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-133">Type</span></span> | <span data-ttu-id="ff158-134">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-134">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ff158-135">result</span><span class="sxs-lookup"><span data-stu-id="ff158-135">result</span></span> | <span data-ttu-id="ff158-136">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-136">JSON object</span></span> | <span data-ttu-id="ff158-137">chaque clé de cet objet JSON représente le numéro de téléphone mobile et la valeur représente l'objet JSON contenant la réussite ou l'échec avec la raison</span><span class="sxs-lookup"><span data-stu-id="ff158-137">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ff158-138">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-138">Sample JSON Response</span></span>

```javascript
{
    "result": {
        "+911111111111": {
            "isAdded": true
        },
        "+911111111112": {
            "isAdded": true
        }
    }
}
```

## <a name="get-subscribers"></a><span data-ttu-id="ff158-139">OBTENIR/subscribers</span><span class="sxs-lookup"><span data-stu-id="ff158-139">GET /subscribers</span></span>

    <span data-ttu-id="ff158-140">POST {Endpoint-URL}/v1/groups/{groupId}/subscribers</span><span class="sxs-lookup"><span data-stu-id="ff158-140">POST {endpoint-url}/v1/groups/{groupId}/subscribers</span></span>

### <a name="request-parameters"></a><span data-ttu-id="ff158-141">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-141">Request Parameters</span></span>
|  | <span data-ttu-id="ff158-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-142">Parameter</span></span> | <span data-ttu-id="ff158-143">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-143">Type</span></span> | <span data-ttu-id="ff158-144">Module?</span><span class="sxs-lookup"><span data-stu-id="ff158-144">Optional?</span></span> | <span data-ttu-id="ff158-145">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-145">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ff158-146">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ff158-146">URL Path Parameter</span></span> | <span data-ttu-id="ff158-147">groupId</span><span class="sxs-lookup"><span data-stu-id="ff158-147">groupId</span></span> | <span data-ttu-id="ff158-148">String</span><span class="sxs-lookup"><span data-stu-id="ff158-148">String</span></span> | <span data-ttu-id="ff158-149">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-149">No</span></span> | <span data-ttu-id="ff158-150">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ff158-150">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ff158-151">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ff158-151">HTTP Header</span></span> | <span data-ttu-id="ff158-152">accessToken</span><span class="sxs-lookup"><span data-stu-id="ff158-152">accessToken</span></span> | <span data-ttu-id="ff158-153">String</span><span class="sxs-lookup"><span data-stu-id="ff158-153">String</span></span> | <span data-ttu-id="ff158-154">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-154">No</span></span> | <span data-ttu-id="ff158-155">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ff158-155">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="ff158-156">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-156">Request body</span></span>

| <span data-ttu-id="ff158-157">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-157">Parameter</span></span> | <span data-ttu-id="ff158-158">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-158">Type</span></span> | <span data-ttu-id="ff158-159">Module?</span><span class="sxs-lookup"><span data-stu-id="ff158-159">Optional?</span></span> | <span data-ttu-id="ff158-160">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-160">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="ff158-161">curseur</span><span class="sxs-lookup"><span data-stu-id="ff158-161">cursor</span></span> | <span data-ttu-id="ff158-162">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ff158-162">String</span></span> | <span data-ttu-id="ff158-163">Oui</span><span class="sxs-lookup"><span data-stu-id="ff158-163">Yes</span></span> | <span data-ttu-id="ff158-164">Début de l'ResultSet.</span><span class="sxs-lookup"><span data-stu-id="ff158-164">Start of resultset.</span></span> <span data-ttu-id="ff158-165">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="ff158-165">For pagination.</span></span> <span data-ttu-id="ff158-166">Renvoyé dans le corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ff158-166">Returned in Response Body</span></span> |
| <span data-ttu-id="ff158-167">count</span><span class="sxs-lookup"><span data-stu-id="ff158-167">count</span></span> | <span data-ttu-id="ff158-168">int</span><span class="sxs-lookup"><span data-stu-id="ff158-168">int</span></span> | <span data-ttu-id="ff158-169">Oui</span><span class="sxs-lookup"><span data-stu-id="ff158-169">Yes</span></span> | <span data-ttu-id="ff158-170">Valeur par défaut: 50.</span><span class="sxs-lookup"><span data-stu-id="ff158-170">Default: 50.</span></span> <span data-ttu-id="ff158-171">Max: 50.</span><span class="sxs-lookup"><span data-stu-id="ff158-171">Max: 50.</span></span> <span data-ttu-id="ff158-172">Nombre d'abonnés à renvoyer dans un jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="ff158-172">Number of subscribers to be returned in a resultset</span></span>|

### <a name="response-body"></a><span data-ttu-id="ff158-173">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ff158-173">Response body</span></span>

| <span data-ttu-id="ff158-174">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-174">Parameter</span></span> | <span data-ttu-id="ff158-175">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-175">Type</span></span> | <span data-ttu-id="ff158-176">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-176">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ff158-177">leurs</span><span class="sxs-lookup"><span data-stu-id="ff158-177">subscribers</span></span> | <span data-ttu-id="ff158-178">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-178">JSON Array</span></span> | <span data-ttu-id="ff158-179">Tableau d'objets JSON représentant chacun un abonné du groupe</span><span class="sxs-lookup"><span data-stu-id="ff158-179">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="ff158-180">curseur</span><span class="sxs-lookup"><span data-stu-id="ff158-180">cursor</span></span> | <span data-ttu-id="ff158-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ff158-181">String</span></span> | <span data-ttu-id="ff158-182">Début de l'ResultSet.</span><span class="sxs-lookup"><span data-stu-id="ff158-182">Start of resultset.</span></span> <span data-ttu-id="ff158-183">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="ff158-183">For pagination.</span></span> <span data-ttu-id="ff158-184">À utiliser dans le corps de la demande pour récupérer le jeu de résultats suivant.</span><span class="sxs-lookup"><span data-stu-id="ff158-184">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="ff158-185">Présent en réponse uniquement s'il existe un jeu de résultats suivant valide.</span><span class="sxs-lookup"><span data-stu-id="ff158-185">Present in response only if there is a valid next result set.</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ff158-186">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-186">Sample JSON Response</span></span>

```javascript
{
    "subscribers": [
        {
            "id": "e2238eb5-2f45-4783-8f4b-571549db86c0",
            "mobileNumber": "+91109999999",
            "name": "",
            "profilePic": "",
            "isProvisioned": false
        }
    ]
}
```

## <a name="remove-subscribers"></a><span data-ttu-id="ff158-187">SUPPRIMER/subscribers</span><span class="sxs-lookup"><span data-stu-id="ff158-187">REMOVE /subscribers</span></span>

    <span data-ttu-id="ff158-188">PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/remove</span><span class="sxs-lookup"><span data-stu-id="ff158-188">PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove</span></span>

### <a name="request-parameters"></a><span data-ttu-id="ff158-189">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-189">Request Parameters</span></span>
|  | <span data-ttu-id="ff158-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-190">Parameter</span></span> | <span data-ttu-id="ff158-191">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-191">Type</span></span> | <span data-ttu-id="ff158-192">Module?</span><span class="sxs-lookup"><span data-stu-id="ff158-192">Optional?</span></span> | <span data-ttu-id="ff158-193">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-193">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ff158-194">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="ff158-194">URL Path Parameter</span></span> | <span data-ttu-id="ff158-195">groupId</span><span class="sxs-lookup"><span data-stu-id="ff158-195">groupId</span></span> | <span data-ttu-id="ff158-196">String</span><span class="sxs-lookup"><span data-stu-id="ff158-196">String</span></span> | <span data-ttu-id="ff158-197">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-197">No</span></span> | <span data-ttu-id="ff158-198">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ff158-198">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ff158-199">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ff158-199">HTTP Header</span></span> | <span data-ttu-id="ff158-200">accessToken</span><span class="sxs-lookup"><span data-stu-id="ff158-200">accessToken</span></span> | <span data-ttu-id="ff158-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ff158-201">String</span></span> | <span data-ttu-id="ff158-202">Non</span><span class="sxs-lookup"><span data-stu-id="ff158-202">No</span></span> | <span data-ttu-id="ff158-203">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="ff158-203">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="ff158-204">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ff158-204">Request body</span></span>
| <span data-ttu-id="ff158-205">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-205">Parameter</span></span> | <span data-ttu-id="ff158-206">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-206">Type</span></span> | <span data-ttu-id="ff158-207">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-207">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ff158-208">leurs</span><span class="sxs-lookup"><span data-stu-id="ff158-208">subscribers</span></span> | <span data-ttu-id="ff158-209">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="ff158-209">String[]</span></span> | <span data-ttu-id="ff158-210">Chaque chaîne représente le numéro de téléphone mobile avec le code pays (par exemple,</span><span class="sxs-lookup"><span data-stu-id="ff158-210">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="ff158-211">+ 911111111111)</span><span class="sxs-lookup"><span data-stu-id="ff158-211">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="ff158-212">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-212">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="ff158-213">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ff158-213">Response body</span></span>
| <span data-ttu-id="ff158-214">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff158-214">Parameter</span></span> | <span data-ttu-id="ff158-215">Type</span><span class="sxs-lookup"><span data-stu-id="ff158-215">Type</span></span> | <span data-ttu-id="ff158-216">Description</span><span class="sxs-lookup"><span data-stu-id="ff158-216">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ff158-217">result</span><span class="sxs-lookup"><span data-stu-id="ff158-217">result</span></span> | <span data-ttu-id="ff158-218">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-218">JSON object</span></span> | <span data-ttu-id="ff158-219">chaque clé de cet objet JSON représente le numéro de téléphone mobile et la valeur représente l'objet JSON contenant la réussite ou l'échec avec la raison</span><span class="sxs-lookup"><span data-stu-id="ff158-219">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ff158-220">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ff158-220">Sample JSON Response</span></span>

```javascript
{
    "result": {
        "+911111111111": {
            "isRemoved": true
        },
        "+911111111112": {
            "isRemoved": true
        }
    }
}
```

