---
title: /members
description: Article de référence pour l’API permettant d’interroger les données des membres du groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: d4f71858cfd58a4d6dd33f3d3d14b5ac855a757a
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535773"
---
# <a name="members"></a><span data-ttu-id="45b01-103">/members</span><span class="sxs-lookup"><span data-stu-id="45b01-103">/members</span></span>
<span data-ttu-id="45b01-104">Point de terminaison d’API pour ajouter ou supprimer des membres de groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="45b01-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="45b01-105">OBTENIR/members</span><span class="sxs-lookup"><span data-stu-id="45b01-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="45b01-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="45b01-106">Request Parameters</span></span>

|  | <span data-ttu-id="45b01-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-107">Parameter</span></span> | <span data-ttu-id="45b01-108">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-108">Type</span></span> | <span data-ttu-id="45b01-109">Module?</span><span class="sxs-lookup"><span data-stu-id="45b01-109">Optional?</span></span> | <span data-ttu-id="45b01-110">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b01-111">Paramètre de chemin d’URL</span><span class="sxs-lookup"><span data-stu-id="45b01-111">URL Path Parameter</span></span> | <span data-ttu-id="45b01-112">groupId</span><span class="sxs-lookup"><span data-stu-id="45b01-112">groupId</span></span> | <span data-ttu-id="45b01-113">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-113">String</span></span> | <span data-ttu-id="45b01-114">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-114">No</span></span> | <span data-ttu-id="45b01-115">GUID représentant l’ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="45b01-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b01-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="45b01-116">HTTP Header</span></span> | <span data-ttu-id="45b01-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b01-117">accessToken</span></span> | <span data-ttu-id="45b01-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-118">String</span></span> | <span data-ttu-id="45b01-119">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-119">No</span></span> | <span data-ttu-id="45b01-120">Jeton d’accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="45b01-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="45b01-121">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="45b01-121">Response body</span></span>

| <span data-ttu-id="45b01-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-122">Parameter</span></span> | <span data-ttu-id="45b01-123">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-123">Type</span></span> | <span data-ttu-id="45b01-124">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b01-125">members</span><span class="sxs-lookup"><span data-stu-id="45b01-125">members</span></span> | <span data-ttu-id="45b01-126">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-126">JSON Array</span></span> | <span data-ttu-id="45b01-127">Tableau d’objets JSON chacun représentant un membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="45b01-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="45b01-128">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-128">Sample JSON Response</span></span>

```javascript
{
  "members": [
    {
      "id": "4deffa08-guid-4b87-8c2f-d944565f5f31",
      "role": "Admin",
      "mobileNumber": "+919652000000",
      "isProvisioned": true
    },
    {
      "id": "2e20e9ac-guid-47bd-abac-1f5236004684",
      "role": "Member",
      "mobileNumber": "+919652000001",
      "isProvisioned": false
    }
  ]
}
```

## <a name="put-members"></a><span data-ttu-id="45b01-129">PUT/members</span><span class="sxs-lookup"><span data-stu-id="45b01-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="45b01-130">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="45b01-130">Request Parameters</span></span>

|  | <span data-ttu-id="45b01-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-131">Parameter</span></span> | <span data-ttu-id="45b01-132">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-132">Type</span></span> | <span data-ttu-id="45b01-133">Module?</span><span class="sxs-lookup"><span data-stu-id="45b01-133">Optional?</span></span> | <span data-ttu-id="45b01-134">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b01-135">Paramètre de chemin d’URL</span><span class="sxs-lookup"><span data-stu-id="45b01-135">URL Path Parameter</span></span> | <span data-ttu-id="45b01-136">groupId</span><span class="sxs-lookup"><span data-stu-id="45b01-136">groupId</span></span> | <span data-ttu-id="45b01-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-137">String</span></span> | <span data-ttu-id="45b01-138">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-138">No</span></span> | <span data-ttu-id="45b01-139">GUID représentant l’ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="45b01-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b01-140">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="45b01-140">HTTP Header</span></span> | <span data-ttu-id="45b01-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b01-141">accessToken</span></span> | <span data-ttu-id="45b01-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-142">String</span></span> | <span data-ttu-id="45b01-143">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-143">No</span></span> | <span data-ttu-id="45b01-144">Jeton d’accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="45b01-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="45b01-145">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="45b01-145">HTTP Header</span></span> | <span data-ttu-id="45b01-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="45b01-146">Content-Type</span></span> | <span data-ttu-id="45b01-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-147">String</span></span> | <span data-ttu-id="45b01-148">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-148">No</span></span> | <span data-ttu-id="45b01-149">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="45b01-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="45b01-150">Request body</span></span>

| <span data-ttu-id="45b01-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-151">Parameter</span></span> | <span data-ttu-id="45b01-152">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-152">Type</span></span> | <span data-ttu-id="45b01-153">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b01-154">members</span><span class="sxs-lookup"><span data-stu-id="45b01-154">members</span></span> | <span data-ttu-id="45b01-155">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="45b01-155">String Array</span></span> | <span data-ttu-id="45b01-156">Tableau de numéros de téléphone bien mis en forme des nouveaux membres à ajouter</span><span class="sxs-lookup"><span data-stu-id="45b01-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="45b01-157">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="45b01-158">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="45b01-158">Response body</span></span>

| <span data-ttu-id="45b01-159">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-159">Parameter</span></span> | <span data-ttu-id="45b01-160">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-160">Type</span></span> | <span data-ttu-id="45b01-161">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b01-162">result</span><span class="sxs-lookup"><span data-stu-id="45b01-162">result</span></span> | <span data-ttu-id="45b01-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="45b01-163">Boolean</span></span> | <span data-ttu-id="45b01-164">True lorsque tous les numéros de téléphone ont été ajoutés au groupe avec succès</span><span class="sxs-lookup"><span data-stu-id="45b01-164">True when all phone numbers have successfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="45b01-165">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="45b01-166">SUPPRIMER/members</span><span class="sxs-lookup"><span data-stu-id="45b01-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="45b01-167">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="45b01-167">Request Parameters</span></span>

|  | <span data-ttu-id="45b01-168">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-168">Parameter</span></span> | <span data-ttu-id="45b01-169">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-169">Type</span></span> | <span data-ttu-id="45b01-170">Module?</span><span class="sxs-lookup"><span data-stu-id="45b01-170">Optional?</span></span> | <span data-ttu-id="45b01-171">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b01-172">Paramètre de chemin d’URL</span><span class="sxs-lookup"><span data-stu-id="45b01-172">URL Path Parameter</span></span> | <span data-ttu-id="45b01-173">groupId</span><span class="sxs-lookup"><span data-stu-id="45b01-173">groupId</span></span> | <span data-ttu-id="45b01-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-174">String</span></span> | <span data-ttu-id="45b01-175">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-175">No</span></span> | <span data-ttu-id="45b01-176">GUID représentant l’ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="45b01-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b01-177">Paramètre de chemin d’URL</span><span class="sxs-lookup"><span data-stu-id="45b01-177">URL Path Parameter</span></span> | <span data-ttu-id="45b01-178">ID</span><span class="sxs-lookup"><span data-stu-id="45b01-178">memberId</span></span> | <span data-ttu-id="45b01-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-179">String</span></span> | <span data-ttu-id="45b01-180">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-180">No</span></span> | <span data-ttu-id="45b01-181">GUID représentant l’ID de membre du membre spécifique</span><span class="sxs-lookup"><span data-stu-id="45b01-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="45b01-182">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="45b01-182">HTTP Header</span></span> | <span data-ttu-id="45b01-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b01-183">accessToken</span></span> | <span data-ttu-id="45b01-184">Chaîne</span><span class="sxs-lookup"><span data-stu-id="45b01-184">String</span></span> | <span data-ttu-id="45b01-185">Non</span><span class="sxs-lookup"><span data-stu-id="45b01-185">No</span></span> | <span data-ttu-id="45b01-186">Jeton d’accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="45b01-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="45b01-187">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="45b01-187">Response body</span></span>

| <span data-ttu-id="45b01-188">Paramètre</span><span class="sxs-lookup"><span data-stu-id="45b01-188">Parameter</span></span> | <span data-ttu-id="45b01-189">Type</span><span class="sxs-lookup"><span data-stu-id="45b01-189">Type</span></span> | <span data-ttu-id="45b01-190">Description</span><span class="sxs-lookup"><span data-stu-id="45b01-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b01-191">result</span><span class="sxs-lookup"><span data-stu-id="45b01-191">result</span></span> | <span data-ttu-id="45b01-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="45b01-192">Boolean</span></span> | <span data-ttu-id="45b01-193">True lorsque le membre spécifié a été supprimé du groupe.</span><span class="sxs-lookup"><span data-stu-id="45b01-193">True when the specified member has successfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="45b01-194">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="45b01-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
