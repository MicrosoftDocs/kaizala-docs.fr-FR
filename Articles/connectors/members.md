---
title: /Members
description: Article de référence pour l'API permettant d'interroger les données des membres du groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190791"
---
# <a name="members"></a><span data-ttu-id="89670-103">/Members</span><span class="sxs-lookup"><span data-stu-id="89670-103">/members</span></span>
<span data-ttu-id="89670-104">Point de terminaison d'API pour ajouter ou supprimer des membres de groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="89670-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="89670-105">OBTENIR/members</span><span class="sxs-lookup"><span data-stu-id="89670-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="89670-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="89670-106">Request Parameters</span></span>

|  | <span data-ttu-id="89670-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-107">Parameter</span></span> | <span data-ttu-id="89670-108">Type</span><span class="sxs-lookup"><span data-stu-id="89670-108">Type</span></span> | <span data-ttu-id="89670-109">Module?</span><span class="sxs-lookup"><span data-stu-id="89670-109">Optional?</span></span> | <span data-ttu-id="89670-110">Description</span><span class="sxs-lookup"><span data-stu-id="89670-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="89670-111">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="89670-111">URL Path Parameter</span></span> | <span data-ttu-id="89670-112">groupId</span><span class="sxs-lookup"><span data-stu-id="89670-112">groupId</span></span> | <span data-ttu-id="89670-113">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-113">String</span></span> | <span data-ttu-id="89670-114">Non</span><span class="sxs-lookup"><span data-stu-id="89670-114">No</span></span> | <span data-ttu-id="89670-115">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="89670-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="89670-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="89670-116">HTTP Header</span></span> | <span data-ttu-id="89670-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="89670-117">accessToken</span></span> | <span data-ttu-id="89670-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-118">String</span></span> | <span data-ttu-id="89670-119">Non</span><span class="sxs-lookup"><span data-stu-id="89670-119">No</span></span> | <span data-ttu-id="89670-120">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="89670-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="89670-121">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="89670-121">Response body</span></span>

| <span data-ttu-id="89670-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-122">Parameter</span></span> | <span data-ttu-id="89670-123">Type</span><span class="sxs-lookup"><span data-stu-id="89670-123">Type</span></span> | <span data-ttu-id="89670-124">Description</span><span class="sxs-lookup"><span data-stu-id="89670-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="89670-125">members</span><span class="sxs-lookup"><span data-stu-id="89670-125">members</span></span> | <span data-ttu-id="89670-126">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="89670-126">JSON Array</span></span> | <span data-ttu-id="89670-127">Tableau d'objets JSON chacun représentant un membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="89670-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="89670-128">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="89670-128">Sample JSON Response</span></span>

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

## <a name="put-members"></a><span data-ttu-id="89670-129">PUT/members</span><span class="sxs-lookup"><span data-stu-id="89670-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="89670-130">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="89670-130">Request Parameters</span></span>

|  | <span data-ttu-id="89670-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-131">Parameter</span></span> | <span data-ttu-id="89670-132">Type</span><span class="sxs-lookup"><span data-stu-id="89670-132">Type</span></span> | <span data-ttu-id="89670-133">Module?</span><span class="sxs-lookup"><span data-stu-id="89670-133">Optional?</span></span> | <span data-ttu-id="89670-134">Description</span><span class="sxs-lookup"><span data-stu-id="89670-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="89670-135">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="89670-135">URL Path Parameter</span></span> | <span data-ttu-id="89670-136">groupId</span><span class="sxs-lookup"><span data-stu-id="89670-136">groupId</span></span> | <span data-ttu-id="89670-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-137">String</span></span> | <span data-ttu-id="89670-138">Non</span><span class="sxs-lookup"><span data-stu-id="89670-138">No</span></span> | <span data-ttu-id="89670-139">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="89670-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="89670-140">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="89670-140">HTTP Header</span></span> | <span data-ttu-id="89670-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="89670-141">accessToken</span></span> | <span data-ttu-id="89670-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-142">String</span></span> | <span data-ttu-id="89670-143">Non</span><span class="sxs-lookup"><span data-stu-id="89670-143">No</span></span> | <span data-ttu-id="89670-144">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="89670-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="89670-145">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="89670-145">HTTP Header</span></span> | <span data-ttu-id="89670-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="89670-146">Content-Type</span></span> | <span data-ttu-id="89670-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-147">String</span></span> | <span data-ttu-id="89670-148">Non</span><span class="sxs-lookup"><span data-stu-id="89670-148">No</span></span> | <span data-ttu-id="89670-149">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="89670-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="89670-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="89670-150">Request body</span></span>

| <span data-ttu-id="89670-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-151">Parameter</span></span> | <span data-ttu-id="89670-152">Type</span><span class="sxs-lookup"><span data-stu-id="89670-152">Type</span></span> | <span data-ttu-id="89670-153">Description</span><span class="sxs-lookup"><span data-stu-id="89670-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="89670-154">members</span><span class="sxs-lookup"><span data-stu-id="89670-154">members</span></span> | <span data-ttu-id="89670-155">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="89670-155">String Array</span></span> | <span data-ttu-id="89670-156">Tableau de numéros de téléphone bien mis en forme des nouveaux membres à ajouter</span><span class="sxs-lookup"><span data-stu-id="89670-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="89670-157">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="89670-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="89670-158">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="89670-158">Response body</span></span>

| <span data-ttu-id="89670-159">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-159">Parameter</span></span> | <span data-ttu-id="89670-160">Type</span><span class="sxs-lookup"><span data-stu-id="89670-160">Type</span></span> | <span data-ttu-id="89670-161">Description</span><span class="sxs-lookup"><span data-stu-id="89670-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="89670-162">result</span><span class="sxs-lookup"><span data-stu-id="89670-162">result</span></span> | <span data-ttu-id="89670-163">Booléen</span><span class="sxs-lookup"><span data-stu-id="89670-163">Boolean</span></span> | <span data-ttu-id="89670-164">True lorsque tous les numéros de téléphone ont été ajoutés au groupe avec succès</span><span class="sxs-lookup"><span data-stu-id="89670-164">True when all phone numbers have succesfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="89670-165">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="89670-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="89670-166">SUPPRIMER/members</span><span class="sxs-lookup"><span data-stu-id="89670-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="89670-167">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="89670-167">Request Parameters</span></span>

|  | <span data-ttu-id="89670-168">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-168">Parameter</span></span> | <span data-ttu-id="89670-169">Type</span><span class="sxs-lookup"><span data-stu-id="89670-169">Type</span></span> | <span data-ttu-id="89670-170">Module?</span><span class="sxs-lookup"><span data-stu-id="89670-170">Optional?</span></span> | <span data-ttu-id="89670-171">Description</span><span class="sxs-lookup"><span data-stu-id="89670-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="89670-172">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="89670-172">URL Path Parameter</span></span> | <span data-ttu-id="89670-173">groupId</span><span class="sxs-lookup"><span data-stu-id="89670-173">groupId</span></span> | <span data-ttu-id="89670-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-174">String</span></span> | <span data-ttu-id="89670-175">Non</span><span class="sxs-lookup"><span data-stu-id="89670-175">No</span></span> | <span data-ttu-id="89670-176">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="89670-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="89670-177">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="89670-177">URL Path Parameter</span></span> | <span data-ttu-id="89670-178">ID</span><span class="sxs-lookup"><span data-stu-id="89670-178">memberId</span></span> | <span data-ttu-id="89670-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-179">String</span></span> | <span data-ttu-id="89670-180">Non</span><span class="sxs-lookup"><span data-stu-id="89670-180">No</span></span> | <span data-ttu-id="89670-181">GUID représentant l'ID de membre du membre spécifique</span><span class="sxs-lookup"><span data-stu-id="89670-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="89670-182">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="89670-182">HTTP Header</span></span> | <span data-ttu-id="89670-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="89670-183">accessToken</span></span> | <span data-ttu-id="89670-184">Chaîne</span><span class="sxs-lookup"><span data-stu-id="89670-184">String</span></span> | <span data-ttu-id="89670-185">Non</span><span class="sxs-lookup"><span data-stu-id="89670-185">No</span></span> | <span data-ttu-id="89670-186">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="89670-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="89670-187">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="89670-187">Response body</span></span>

| <span data-ttu-id="89670-188">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89670-188">Parameter</span></span> | <span data-ttu-id="89670-189">Type</span><span class="sxs-lookup"><span data-stu-id="89670-189">Type</span></span> | <span data-ttu-id="89670-190">Description</span><span class="sxs-lookup"><span data-stu-id="89670-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="89670-191">result</span><span class="sxs-lookup"><span data-stu-id="89670-191">result</span></span> | <span data-ttu-id="89670-192">Booléen</span><span class="sxs-lookup"><span data-stu-id="89670-192">Boolean</span></span> | <span data-ttu-id="89670-193">True lorsque le membre spécifié a été supprimé du groupe avec succès.</span><span class="sxs-lookup"><span data-stu-id="89670-193">True when the specified member has succesfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="89670-194">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="89670-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
