---
title: /Subscribers
description: Référence de l’Article de l’API obtenir les abonnés données pour des groupes publics
topic: Reference
author: nitinjms
ms.openlocfilehash: b026c8c38ce3cea600219a3e5713726013e62367
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905135"
---
# <a name="apis-to-query-subscribers-data-in-a-public-group"></a><span data-ttu-id="48849-103">API pour interroger les données d’abonnés dans un groupe public</span><span class="sxs-lookup"><span data-stu-id="48849-103">APIs to query subscribers data in a public group</span></span>
## <a name="subscribers"></a><span data-ttu-id="48849-104">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="48849-104">/subscribers</span></span>

<span data-ttu-id="48849-105">Point de terminaison API pour ajouter, obtenir ou supprimer les abonnés de groupe Public gérés.</span><span class="sxs-lookup"><span data-stu-id="48849-105">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

### <a name="add-subscribers"></a><span data-ttu-id="48849-106">Ajouter /subscribers</span><span class="sxs-lookup"><span data-stu-id="48849-106">ADD /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

##### <a name="request-parameters"></a><span data-ttu-id="48849-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="48849-107">Request Parameters</span></span>
|  | <span data-ttu-id="48849-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-108">Parameter</span></span> | <span data-ttu-id="48849-109">Type</span><span class="sxs-lookup"><span data-stu-id="48849-109">Type</span></span> | <span data-ttu-id="48849-110">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="48849-110">Optional?</span></span> | <span data-ttu-id="48849-111">Description</span><span class="sxs-lookup"><span data-stu-id="48849-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48849-112">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="48849-112">URL Path Parameter</span></span> | <span data-ttu-id="48849-113">groupId</span><span class="sxs-lookup"><span data-stu-id="48849-113">groupId</span></span> | <span data-ttu-id="48849-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-114">String</span></span> | <span data-ttu-id="48849-115">Non</span><span class="sxs-lookup"><span data-stu-id="48849-115">No</span></span> | <span data-ttu-id="48849-116">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="48849-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48849-117">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="48849-117">HTTP Header</span></span> | <span data-ttu-id="48849-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="48849-118">accessToken</span></span> | <span data-ttu-id="48849-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-119">String</span></span> | <span data-ttu-id="48849-120">Non</span><span class="sxs-lookup"><span data-stu-id="48849-120">No</span></span> | <span data-ttu-id="48849-121">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="48849-121">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="48849-122">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="48849-122">Request body</span></span>
| <span data-ttu-id="48849-123">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-123">Parameter</span></span> | <span data-ttu-id="48849-124">Type</span><span class="sxs-lookup"><span data-stu-id="48849-124">Type</span></span> | <span data-ttu-id="48849-125">Description</span><span class="sxs-lookup"><span data-stu-id="48849-125">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48849-126">abonnés</span><span class="sxs-lookup"><span data-stu-id="48849-126">subscribers</span></span> | <span data-ttu-id="48849-127">String]</span><span class="sxs-lookup"><span data-stu-id="48849-127">String[]</span></span> | <span data-ttu-id="48849-128">Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex..</span><span class="sxs-lookup"><span data-stu-id="48849-128">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="48849-129">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="48849-129">+911111111111)</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="48849-130">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="48849-130">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a><span data-ttu-id="48849-131">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="48849-131">Response body</span></span>
| <span data-ttu-id="48849-132">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-132">Parameter</span></span> | <span data-ttu-id="48849-133">Type</span><span class="sxs-lookup"><span data-stu-id="48849-133">Type</span></span> | <span data-ttu-id="48849-134">Description</span><span class="sxs-lookup"><span data-stu-id="48849-134">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48849-135">result</span><span class="sxs-lookup"><span data-stu-id="48849-135">result</span></span> | <span data-ttu-id="48849-136">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="48849-136">JSON object</span></span> | <span data-ttu-id="48849-137">chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif</span><span class="sxs-lookup"><span data-stu-id="48849-137">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="48849-138">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="48849-138">Sample JSON Response</span></span>

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

### <a name="get-subscribers"></a><span data-ttu-id="48849-139">OBTENIR /subscribers</span><span class="sxs-lookup"><span data-stu-id="48849-139">GET /subscribers</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

##### <a name="request-parameters"></a><span data-ttu-id="48849-140">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="48849-140">Request Parameters</span></span>
|  | <span data-ttu-id="48849-141">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-141">Parameter</span></span> | <span data-ttu-id="48849-142">Type</span><span class="sxs-lookup"><span data-stu-id="48849-142">Type</span></span> | <span data-ttu-id="48849-143">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="48849-143">Optional?</span></span> | <span data-ttu-id="48849-144">Description</span><span class="sxs-lookup"><span data-stu-id="48849-144">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48849-145">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="48849-145">URL Path Parameter</span></span> | <span data-ttu-id="48849-146">groupId</span><span class="sxs-lookup"><span data-stu-id="48849-146">groupId</span></span> | <span data-ttu-id="48849-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-147">String</span></span> | <span data-ttu-id="48849-148">Non</span><span class="sxs-lookup"><span data-stu-id="48849-148">No</span></span> | <span data-ttu-id="48849-149">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="48849-149">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48849-150">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="48849-150">HTTP Header</span></span> | <span data-ttu-id="48849-151">accessToken</span><span class="sxs-lookup"><span data-stu-id="48849-151">accessToken</span></span> | <span data-ttu-id="48849-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-152">String</span></span> | <span data-ttu-id="48849-153">Non</span><span class="sxs-lookup"><span data-stu-id="48849-153">No</span></span> | <span data-ttu-id="48849-154">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="48849-154">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="48849-155">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="48849-155">Request body</span></span>

| <span data-ttu-id="48849-156">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-156">Parameter</span></span> | <span data-ttu-id="48849-157">Type</span><span class="sxs-lookup"><span data-stu-id="48849-157">Type</span></span> | <span data-ttu-id="48849-158">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="48849-158">Optional?</span></span> | <span data-ttu-id="48849-159">Description</span><span class="sxs-lookup"><span data-stu-id="48849-159">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="48849-160">curseur</span><span class="sxs-lookup"><span data-stu-id="48849-160">cursor</span></span> | <span data-ttu-id="48849-161">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-161">String</span></span> | <span data-ttu-id="48849-162">Oui</span><span class="sxs-lookup"><span data-stu-id="48849-162">Yes</span></span> | <span data-ttu-id="48849-163">Début du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="48849-163">Start of resultset.</span></span> <span data-ttu-id="48849-164">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="48849-164">For pagination.</span></span> <span data-ttu-id="48849-165">Renvoyée dans le corps de réponse</span><span class="sxs-lookup"><span data-stu-id="48849-165">Returned in Response Body</span></span> |
| <span data-ttu-id="48849-166">count</span><span class="sxs-lookup"><span data-stu-id="48849-166">count</span></span> | <span data-ttu-id="48849-167">entier</span><span class="sxs-lookup"><span data-stu-id="48849-167">int</span></span> | <span data-ttu-id="48849-168">Oui</span><span class="sxs-lookup"><span data-stu-id="48849-168">Yes</span></span> | <span data-ttu-id="48849-169">Par défaut : 50.</span><span class="sxs-lookup"><span data-stu-id="48849-169">Default: 50.</span></span> <span data-ttu-id="48849-170">Max : 50.</span><span class="sxs-lookup"><span data-stu-id="48849-170">Max: 50.</span></span> <span data-ttu-id="48849-171">Nombre d’abonnés à renvoyer dans un jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="48849-171">Number of subscribers to be returned in a resultset</span></span>|

##### <a name="response-body"></a><span data-ttu-id="48849-172">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="48849-172">Response body</span></span>

| <span data-ttu-id="48849-173">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-173">Parameter</span></span> | <span data-ttu-id="48849-174">Type</span><span class="sxs-lookup"><span data-stu-id="48849-174">Type</span></span> | <span data-ttu-id="48849-175">Description</span><span class="sxs-lookup"><span data-stu-id="48849-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48849-176">abonnés</span><span class="sxs-lookup"><span data-stu-id="48849-176">subscribers</span></span> | <span data-ttu-id="48849-177">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="48849-177">JSON Array</span></span> | <span data-ttu-id="48849-178">Tableau de JSON objets représentant chacun un abonné du groupe</span><span class="sxs-lookup"><span data-stu-id="48849-178">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="48849-179">curseur</span><span class="sxs-lookup"><span data-stu-id="48849-179">cursor</span></span> | <span data-ttu-id="48849-180">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-180">String</span></span> | <span data-ttu-id="48849-181">Début du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="48849-181">Start of resultset.</span></span> <span data-ttu-id="48849-182">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="48849-182">For pagination.</span></span> <span data-ttu-id="48849-183">Pour être utilisé dans le corps de la requête pour extraire le résultat suivant défini.</span><span class="sxs-lookup"><span data-stu-id="48849-183">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="48849-184">Présenter en réponse uniquement s’il existe un jeu de résultats valide suivant.</span><span class="sxs-lookup"><span data-stu-id="48849-184">Present in response only if there is a valid next result set.</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="48849-185">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="48849-185">Sample JSON Response</span></span>

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

### <a name="remove-subscribers"></a><span data-ttu-id="48849-186">SUPPRIMER /subscribers</span><span class="sxs-lookup"><span data-stu-id="48849-186">REMOVE /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

##### <a name="request-parameters"></a><span data-ttu-id="48849-187">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="48849-187">Request Parameters</span></span>
|  | <span data-ttu-id="48849-188">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-188">Parameter</span></span> | <span data-ttu-id="48849-189">Type</span><span class="sxs-lookup"><span data-stu-id="48849-189">Type</span></span> | <span data-ttu-id="48849-190">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="48849-190">Optional?</span></span> | <span data-ttu-id="48849-191">Description</span><span class="sxs-lookup"><span data-stu-id="48849-191">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48849-192">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="48849-192">URL Path Parameter</span></span> | <span data-ttu-id="48849-193">groupId</span><span class="sxs-lookup"><span data-stu-id="48849-193">groupId</span></span> | <span data-ttu-id="48849-194">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-194">String</span></span> | <span data-ttu-id="48849-195">Non</span><span class="sxs-lookup"><span data-stu-id="48849-195">No</span></span> | <span data-ttu-id="48849-196">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="48849-196">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48849-197">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="48849-197">HTTP Header</span></span> | <span data-ttu-id="48849-198">accessToken</span><span class="sxs-lookup"><span data-stu-id="48849-198">accessToken</span></span> | <span data-ttu-id="48849-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="48849-199">String</span></span> | <span data-ttu-id="48849-200">Non</span><span class="sxs-lookup"><span data-stu-id="48849-200">No</span></span> | <span data-ttu-id="48849-201">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="48849-201">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="48849-202">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="48849-202">Request body</span></span>
| <span data-ttu-id="48849-203">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-203">Parameter</span></span> | <span data-ttu-id="48849-204">Type</span><span class="sxs-lookup"><span data-stu-id="48849-204">Type</span></span> | <span data-ttu-id="48849-205">Description</span><span class="sxs-lookup"><span data-stu-id="48849-205">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48849-206">abonnés</span><span class="sxs-lookup"><span data-stu-id="48849-206">subscribers</span></span> | <span data-ttu-id="48849-207">String]</span><span class="sxs-lookup"><span data-stu-id="48849-207">String[]</span></span> | <span data-ttu-id="48849-208">Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex..</span><span class="sxs-lookup"><span data-stu-id="48849-208">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="48849-209">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="48849-209">+911111111111)</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="48849-210">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="48849-210">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a><span data-ttu-id="48849-211">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="48849-211">Response body</span></span>
| <span data-ttu-id="48849-212">Paramètre</span><span class="sxs-lookup"><span data-stu-id="48849-212">Parameter</span></span> | <span data-ttu-id="48849-213">Type</span><span class="sxs-lookup"><span data-stu-id="48849-213">Type</span></span> | <span data-ttu-id="48849-214">Description</span><span class="sxs-lookup"><span data-stu-id="48849-214">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48849-215">result</span><span class="sxs-lookup"><span data-stu-id="48849-215">result</span></span> | <span data-ttu-id="48849-216">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="48849-216">JSON object</span></span> | <span data-ttu-id="48849-217">chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif</span><span class="sxs-lookup"><span data-stu-id="48849-217">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="48849-218">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="48849-218">Sample JSON Response</span></span>

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

