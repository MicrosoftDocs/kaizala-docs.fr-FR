---
title: /Members
description: Article de référence de l’API pour interroger les données de membres de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905151"
---
# <a name="members"></a><span data-ttu-id="08771-103">/Members</span><span class="sxs-lookup"><span data-stu-id="08771-103">/members</span></span>
<span data-ttu-id="08771-104">Point de terminaison API pour ajouter ou supprimer des membres de groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="08771-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="08771-105">OBTENIR /members</span><span class="sxs-lookup"><span data-stu-id="08771-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="08771-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="08771-106">Request Parameters</span></span>

|  | <span data-ttu-id="08771-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-107">Parameter</span></span> | <span data-ttu-id="08771-108">Type</span><span class="sxs-lookup"><span data-stu-id="08771-108">Type</span></span> | <span data-ttu-id="08771-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="08771-109">Optional?</span></span> | <span data-ttu-id="08771-110">Description</span><span class="sxs-lookup"><span data-stu-id="08771-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="08771-111">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="08771-111">URL Path Parameter</span></span> | <span data-ttu-id="08771-112">groupId</span><span class="sxs-lookup"><span data-stu-id="08771-112">groupId</span></span> | <span data-ttu-id="08771-113">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-113">String</span></span> | <span data-ttu-id="08771-114">Non</span><span class="sxs-lookup"><span data-stu-id="08771-114">No</span></span> | <span data-ttu-id="08771-115">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="08771-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="08771-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="08771-116">HTTP Header</span></span> | <span data-ttu-id="08771-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="08771-117">accessToken</span></span> | <span data-ttu-id="08771-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-118">String</span></span> | <span data-ttu-id="08771-119">Non</span><span class="sxs-lookup"><span data-stu-id="08771-119">No</span></span> | <span data-ttu-id="08771-120">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="08771-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="08771-121">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="08771-121">Response body</span></span>

| <span data-ttu-id="08771-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-122">Parameter</span></span> | <span data-ttu-id="08771-123">Type</span><span class="sxs-lookup"><span data-stu-id="08771-123">Type</span></span> | <span data-ttu-id="08771-124">Description</span><span class="sxs-lookup"><span data-stu-id="08771-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="08771-125">members</span><span class="sxs-lookup"><span data-stu-id="08771-125">members</span></span> | <span data-ttu-id="08771-126">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="08771-126">JSON Array</span></span> | <span data-ttu-id="08771-127">Tableau de JSON objets chaque qui représente un membre du groupe</span><span class="sxs-lookup"><span data-stu-id="08771-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="08771-128">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="08771-128">Sample JSON Response</span></span>

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

## <a name="put-members"></a><span data-ttu-id="08771-129">Placez /members</span><span class="sxs-lookup"><span data-stu-id="08771-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="08771-130">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="08771-130">Request Parameters</span></span>

|  | <span data-ttu-id="08771-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-131">Parameter</span></span> | <span data-ttu-id="08771-132">Type</span><span class="sxs-lookup"><span data-stu-id="08771-132">Type</span></span> | <span data-ttu-id="08771-133">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="08771-133">Optional?</span></span> | <span data-ttu-id="08771-134">Description</span><span class="sxs-lookup"><span data-stu-id="08771-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="08771-135">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="08771-135">URL Path Parameter</span></span> | <span data-ttu-id="08771-136">groupId</span><span class="sxs-lookup"><span data-stu-id="08771-136">groupId</span></span> | <span data-ttu-id="08771-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-137">String</span></span> | <span data-ttu-id="08771-138">Non</span><span class="sxs-lookup"><span data-stu-id="08771-138">No</span></span> | <span data-ttu-id="08771-139">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="08771-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="08771-140">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="08771-140">HTTP Header</span></span> | <span data-ttu-id="08771-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="08771-141">accessToken</span></span> | <span data-ttu-id="08771-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-142">String</span></span> | <span data-ttu-id="08771-143">Non</span><span class="sxs-lookup"><span data-stu-id="08771-143">No</span></span> | <span data-ttu-id="08771-144">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="08771-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="08771-145">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="08771-145">HTTP Header</span></span> | <span data-ttu-id="08771-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="08771-146">Content-Type</span></span> | <span data-ttu-id="08771-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-147">String</span></span> | <span data-ttu-id="08771-148">Non</span><span class="sxs-lookup"><span data-stu-id="08771-148">No</span></span> | <span data-ttu-id="08771-149">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="08771-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="08771-150">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="08771-150">Request body</span></span>

| <span data-ttu-id="08771-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-151">Parameter</span></span> | <span data-ttu-id="08771-152">Type</span><span class="sxs-lookup"><span data-stu-id="08771-152">Type</span></span> | <span data-ttu-id="08771-153">Description</span><span class="sxs-lookup"><span data-stu-id="08771-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="08771-154">members</span><span class="sxs-lookup"><span data-stu-id="08771-154">members</span></span> | <span data-ttu-id="08771-155">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="08771-155">String Array</span></span> | <span data-ttu-id="08771-156">Tableau des numéros de téléphone au format correct de nouveaux membres à ajouter</span><span class="sxs-lookup"><span data-stu-id="08771-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="08771-157">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="08771-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="08771-158">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="08771-158">Response body</span></span>

| <span data-ttu-id="08771-159">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-159">Parameter</span></span> | <span data-ttu-id="08771-160">Type</span><span class="sxs-lookup"><span data-stu-id="08771-160">Type</span></span> | <span data-ttu-id="08771-161">Description</span><span class="sxs-lookup"><span data-stu-id="08771-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="08771-162">result</span><span class="sxs-lookup"><span data-stu-id="08771-162">result</span></span> | <span data-ttu-id="08771-163">Bool�en</span><span class="sxs-lookup"><span data-stu-id="08771-163">Boolean</span></span> | <span data-ttu-id="08771-164">True si tous les numéros de téléphone ont correctement été ajouté au groupe</span><span class="sxs-lookup"><span data-stu-id="08771-164">True when all phone numbers have succesfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="08771-165">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="08771-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="08771-166">SUPPRIMER /members</span><span class="sxs-lookup"><span data-stu-id="08771-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="08771-167">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="08771-167">Request Parameters</span></span>

|  | <span data-ttu-id="08771-168">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-168">Parameter</span></span> | <span data-ttu-id="08771-169">Type</span><span class="sxs-lookup"><span data-stu-id="08771-169">Type</span></span> | <span data-ttu-id="08771-170">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="08771-170">Optional?</span></span> | <span data-ttu-id="08771-171">Description</span><span class="sxs-lookup"><span data-stu-id="08771-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="08771-172">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="08771-172">URL Path Parameter</span></span> | <span data-ttu-id="08771-173">groupId</span><span class="sxs-lookup"><span data-stu-id="08771-173">groupId</span></span> | <span data-ttu-id="08771-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-174">String</span></span> | <span data-ttu-id="08771-175">Non</span><span class="sxs-lookup"><span data-stu-id="08771-175">No</span></span> | <span data-ttu-id="08771-176">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="08771-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="08771-177">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="08771-177">URL Path Parameter</span></span> | <span data-ttu-id="08771-178">ID de membre</span><span class="sxs-lookup"><span data-stu-id="08771-178">memberId</span></span> | <span data-ttu-id="08771-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-179">String</span></span> | <span data-ttu-id="08771-180">Non</span><span class="sxs-lookup"><span data-stu-id="08771-180">No</span></span> | <span data-ttu-id="08771-181">GUID représentant l’ID de membre spécifique</span><span class="sxs-lookup"><span data-stu-id="08771-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="08771-182">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="08771-182">HTTP Header</span></span> | <span data-ttu-id="08771-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="08771-183">accessToken</span></span> | <span data-ttu-id="08771-184">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08771-184">String</span></span> | <span data-ttu-id="08771-185">Non</span><span class="sxs-lookup"><span data-stu-id="08771-185">No</span></span> | <span data-ttu-id="08771-186">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="08771-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="08771-187">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="08771-187">Response body</span></span>

| <span data-ttu-id="08771-188">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08771-188">Parameter</span></span> | <span data-ttu-id="08771-189">Type</span><span class="sxs-lookup"><span data-stu-id="08771-189">Type</span></span> | <span data-ttu-id="08771-190">Description</span><span class="sxs-lookup"><span data-stu-id="08771-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="08771-191">result</span><span class="sxs-lookup"><span data-stu-id="08771-191">result</span></span> | <span data-ttu-id="08771-192">Bool�en</span><span class="sxs-lookup"><span data-stu-id="08771-192">Boolean</span></span> | <span data-ttu-id="08771-193">La valeur True après le membre spécifié a correctement été supprimé du groupe</span><span class="sxs-lookup"><span data-stu-id="08771-193">True when the specified member has succesfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="08771-194">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="08771-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
