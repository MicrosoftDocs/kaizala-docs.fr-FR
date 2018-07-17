---
title: /Subscribers
description: Référence de l’Article de l’API obtenir les abonnés données pour des groupes publics
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399364"
---
# <a name="subscribers"></a><span data-ttu-id="7f52e-103">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="7f52e-103">/subscribers</span></span>

<span data-ttu-id="7f52e-104">Point de terminaison API pour ajouter, obtenir ou supprimer les abonnés de groupe Public gérés.</span><span class="sxs-lookup"><span data-stu-id="7f52e-104">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

## <a name="add-subscribers"></a><span data-ttu-id="7f52e-105">Ajouter /subscribers</span><span class="sxs-lookup"><span data-stu-id="7f52e-105">ADD /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

### <a name="request-parameters"></a><span data-ttu-id="7f52e-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7f52e-106">Request Parameters</span></span>
|  | <span data-ttu-id="7f52e-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-107">Parameter</span></span> | <span data-ttu-id="7f52e-108">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-108">Type</span></span> | <span data-ttu-id="7f52e-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7f52e-109">Optional?</span></span> | <span data-ttu-id="7f52e-110">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7f52e-111">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="7f52e-111">URL Path Parameter</span></span> | <span data-ttu-id="7f52e-112">groupId</span><span class="sxs-lookup"><span data-stu-id="7f52e-112">groupId</span></span> | <span data-ttu-id="7f52e-113">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-113">String</span></span> | <span data-ttu-id="7f52e-114">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-114">No</span></span> | <span data-ttu-id="7f52e-115">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="7f52e-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7f52e-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7f52e-116">HTTP Header</span></span> | <span data-ttu-id="7f52e-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="7f52e-117">accessToken</span></span> | <span data-ttu-id="7f52e-118">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-118">String</span></span> | <span data-ttu-id="7f52e-119">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-119">No</span></span> | <span data-ttu-id="7f52e-120">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7f52e-120">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="7f52e-121">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="7f52e-121">Request body</span></span>
| <span data-ttu-id="7f52e-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-122">Parameter</span></span> | <span data-ttu-id="7f52e-123">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-123">Type</span></span> | <span data-ttu-id="7f52e-124">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f52e-125">abonnés</span><span class="sxs-lookup"><span data-stu-id="7f52e-125">subscribers</span></span> | <span data-ttu-id="7f52e-126">String]</span><span class="sxs-lookup"><span data-stu-id="7f52e-126">String[]</span></span> | <span data-ttu-id="7f52e-127">Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex..</span><span class="sxs-lookup"><span data-stu-id="7f52e-127">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="7f52e-128">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="7f52e-128">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="7f52e-129">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-129">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="7f52e-130">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="7f52e-130">Response body</span></span>
| <span data-ttu-id="7f52e-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-131">Parameter</span></span> | <span data-ttu-id="7f52e-132">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-132">Type</span></span> | <span data-ttu-id="7f52e-133">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f52e-134">result</span><span class="sxs-lookup"><span data-stu-id="7f52e-134">result</span></span> | <span data-ttu-id="7f52e-135">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-135">JSON object</span></span> | <span data-ttu-id="7f52e-136">chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif</span><span class="sxs-lookup"><span data-stu-id="7f52e-136">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7f52e-137">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-137">Sample JSON Response</span></span>

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

## <a name="get-subscribers"></a><span data-ttu-id="7f52e-138">OBTENIR /subscribers</span><span class="sxs-lookup"><span data-stu-id="7f52e-138">GET /subscribers</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

### <a name="request-parameters"></a><span data-ttu-id="7f52e-139">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7f52e-139">Request Parameters</span></span>
|  | <span data-ttu-id="7f52e-140">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-140">Parameter</span></span> | <span data-ttu-id="7f52e-141">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-141">Type</span></span> | <span data-ttu-id="7f52e-142">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7f52e-142">Optional?</span></span> | <span data-ttu-id="7f52e-143">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-143">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7f52e-144">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="7f52e-144">URL Path Parameter</span></span> | <span data-ttu-id="7f52e-145">groupId</span><span class="sxs-lookup"><span data-stu-id="7f52e-145">groupId</span></span> | <span data-ttu-id="7f52e-146">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-146">String</span></span> | <span data-ttu-id="7f52e-147">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-147">No</span></span> | <span data-ttu-id="7f52e-148">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="7f52e-148">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7f52e-149">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7f52e-149">HTTP Header</span></span> | <span data-ttu-id="7f52e-150">accessToken</span><span class="sxs-lookup"><span data-stu-id="7f52e-150">accessToken</span></span> | <span data-ttu-id="7f52e-151">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-151">String</span></span> | <span data-ttu-id="7f52e-152">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-152">No</span></span> | <span data-ttu-id="7f52e-153">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7f52e-153">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="7f52e-154">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="7f52e-154">Request body</span></span>

| <span data-ttu-id="7f52e-155">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-155">Parameter</span></span> | <span data-ttu-id="7f52e-156">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-156">Type</span></span> | <span data-ttu-id="7f52e-157">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7f52e-157">Optional?</span></span> | <span data-ttu-id="7f52e-158">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-158">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="7f52e-159">curseur</span><span class="sxs-lookup"><span data-stu-id="7f52e-159">cursor</span></span> | <span data-ttu-id="7f52e-160">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-160">String</span></span> | <span data-ttu-id="7f52e-161">Oui</span><span class="sxs-lookup"><span data-stu-id="7f52e-161">Yes</span></span> | <span data-ttu-id="7f52e-162">Début du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="7f52e-162">Start of resultset.</span></span> <span data-ttu-id="7f52e-163">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="7f52e-163">For pagination.</span></span> <span data-ttu-id="7f52e-164">Renvoyée dans le corps de réponse</span><span class="sxs-lookup"><span data-stu-id="7f52e-164">Returned in Response Body</span></span> |
| <span data-ttu-id="7f52e-165">count</span><span class="sxs-lookup"><span data-stu-id="7f52e-165">count</span></span> | <span data-ttu-id="7f52e-166">entier</span><span class="sxs-lookup"><span data-stu-id="7f52e-166">int</span></span> | <span data-ttu-id="7f52e-167">Oui</span><span class="sxs-lookup"><span data-stu-id="7f52e-167">Yes</span></span> | <span data-ttu-id="7f52e-168">Par défaut : 50.</span><span class="sxs-lookup"><span data-stu-id="7f52e-168">Default: 50.</span></span> <span data-ttu-id="7f52e-169">Max : 50.</span><span class="sxs-lookup"><span data-stu-id="7f52e-169">Max: 50.</span></span> <span data-ttu-id="7f52e-170">Nombre d’abonnés à renvoyer dans un jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="7f52e-170">Number of subscribers to be returned in a resultset</span></span>|

### <a name="response-body"></a><span data-ttu-id="7f52e-171">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="7f52e-171">Response body</span></span>

| <span data-ttu-id="7f52e-172">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-172">Parameter</span></span> | <span data-ttu-id="7f52e-173">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-173">Type</span></span> | <span data-ttu-id="7f52e-174">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-174">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f52e-175">abonnés</span><span class="sxs-lookup"><span data-stu-id="7f52e-175">subscribers</span></span> | <span data-ttu-id="7f52e-176">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-176">JSON Array</span></span> | <span data-ttu-id="7f52e-177">Tableau de JSON objets représentant chacun un abonné du groupe</span><span class="sxs-lookup"><span data-stu-id="7f52e-177">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="7f52e-178">curseur</span><span class="sxs-lookup"><span data-stu-id="7f52e-178">cursor</span></span> | <span data-ttu-id="7f52e-179">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-179">String</span></span> | <span data-ttu-id="7f52e-180">Début du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="7f52e-180">Start of resultset.</span></span> <span data-ttu-id="7f52e-181">Pour la pagination.</span><span class="sxs-lookup"><span data-stu-id="7f52e-181">For pagination.</span></span> <span data-ttu-id="7f52e-182">Pour être utilisé dans le corps de la requête pour extraire le résultat suivant défini.</span><span class="sxs-lookup"><span data-stu-id="7f52e-182">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="7f52e-183">Présenter en réponse uniquement s’il existe un jeu de résultats valide suivant.</span><span class="sxs-lookup"><span data-stu-id="7f52e-183">Present in response only if there is a valid next result set.</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7f52e-184">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-184">Sample JSON Response</span></span>

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

## <a name="remove-subscribers"></a><span data-ttu-id="7f52e-185">SUPPRIMER /subscribers</span><span class="sxs-lookup"><span data-stu-id="7f52e-185">REMOVE /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

### <a name="request-parameters"></a><span data-ttu-id="7f52e-186">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7f52e-186">Request Parameters</span></span>
|  | <span data-ttu-id="7f52e-187">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-187">Parameter</span></span> | <span data-ttu-id="7f52e-188">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-188">Type</span></span> | <span data-ttu-id="7f52e-189">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7f52e-189">Optional?</span></span> | <span data-ttu-id="7f52e-190">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-190">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7f52e-191">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="7f52e-191">URL Path Parameter</span></span> | <span data-ttu-id="7f52e-192">groupId</span><span class="sxs-lookup"><span data-stu-id="7f52e-192">groupId</span></span> | <span data-ttu-id="7f52e-193">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-193">String</span></span> | <span data-ttu-id="7f52e-194">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-194">No</span></span> | <span data-ttu-id="7f52e-195">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="7f52e-195">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7f52e-196">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7f52e-196">HTTP Header</span></span> | <span data-ttu-id="7f52e-197">accessToken</span><span class="sxs-lookup"><span data-stu-id="7f52e-197">accessToken</span></span> | <span data-ttu-id="7f52e-198">String</span><span class="sxs-lookup"><span data-stu-id="7f52e-198">String</span></span> | <span data-ttu-id="7f52e-199">Non</span><span class="sxs-lookup"><span data-stu-id="7f52e-199">No</span></span> | <span data-ttu-id="7f52e-200">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7f52e-200">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="7f52e-201">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="7f52e-201">Request body</span></span>
| <span data-ttu-id="7f52e-202">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-202">Parameter</span></span> | <span data-ttu-id="7f52e-203">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-203">Type</span></span> | <span data-ttu-id="7f52e-204">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f52e-205">abonnés</span><span class="sxs-lookup"><span data-stu-id="7f52e-205">subscribers</span></span> | <span data-ttu-id="7f52e-206">String]</span><span class="sxs-lookup"><span data-stu-id="7f52e-206">String[]</span></span> | <span data-ttu-id="7f52e-207">Chaque chaîne représente le numéro de téléphone mobile avec le code du pays (par ex..</span><span class="sxs-lookup"><span data-stu-id="7f52e-207">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="7f52e-208">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="7f52e-208">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="7f52e-209">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-209">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="7f52e-210">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="7f52e-210">Response body</span></span>
| <span data-ttu-id="7f52e-211">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7f52e-211">Parameter</span></span> | <span data-ttu-id="7f52e-212">Type</span><span class="sxs-lookup"><span data-stu-id="7f52e-212">Type</span></span> | <span data-ttu-id="7f52e-213">Description</span><span class="sxs-lookup"><span data-stu-id="7f52e-213">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f52e-214">result</span><span class="sxs-lookup"><span data-stu-id="7f52e-214">result</span></span> | <span data-ttu-id="7f52e-215">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-215">JSON object</span></span> | <span data-ttu-id="7f52e-216">chaque clé de cet objet Json représente le numéro de téléphone mobile et valeur l’objet Json contenant a réussi ou échoué avec motif</span><span class="sxs-lookup"><span data-stu-id="7f52e-216">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7f52e-217">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="7f52e-217">Sample JSON Response</span></span>

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

