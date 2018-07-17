---
title: /subGroups
description: Article de référence de l’API pour interroger les données sous-groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399366"
---
# <a name="subgroups"></a><span data-ttu-id="3f4cb-103">/subGroups</span><span class="sxs-lookup"><span data-stu-id="3f4cb-103">/subGroups</span></span>
<span data-ttu-id="3f4cb-104">Prévoit d’API pour interagir avec la conversation sous-groupes à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="3f4cb-104">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

## <a name="get-subgroups"></a><span data-ttu-id="3f4cb-105">OBTENIR /subGroups</span><span class="sxs-lookup"><span data-stu-id="3f4cb-105">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="3f4cb-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="3f4cb-106">Request Parameters</span></span>

|  | <span data-ttu-id="3f4cb-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-107">Parameter</span></span> | <span data-ttu-id="3f4cb-108">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-108">Type</span></span> | <span data-ttu-id="3f4cb-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3f4cb-109">Optional?</span></span> | <span data-ttu-id="3f4cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-111">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3f4cb-111">HTTP Header</span></span> | <span data-ttu-id="3f4cb-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="3f4cb-112">accessToken</span></span> | <span data-ttu-id="3f4cb-113">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-113">String</span></span> | <span data-ttu-id="3f4cb-114">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-114">No</span></span> | <span data-ttu-id="3f4cb-115">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4cb-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="3f4cb-116">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="3f4cb-116">URL Path Parameter</span></span> | <span data-ttu-id="3f4cb-117">groupId</span><span class="sxs-lookup"><span data-stu-id="3f4cb-117">groupId</span></span> | <span data-ttu-id="3f4cb-118">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-118">String</span></span> | <span data-ttu-id="3f4cb-119">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-119">No</span></span> | <span data-ttu-id="3f4cb-120">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="3f4cb-120">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="3f4cb-121">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="3f4cb-121">URL Query Parameter</span></span> | <span data-ttu-id="3f4cb-122">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="3f4cb-122">fetchAllGroups</span></span> | <span data-ttu-id="3f4cb-123">Booléen</span><span class="sxs-lookup"><span data-stu-id="3f4cb-123">Boolean</span></span> | <span data-ttu-id="3f4cb-124">Oui</span><span class="sxs-lookup"><span data-stu-id="3f4cb-124">Yes</span></span> | <span data-ttu-id="3f4cb-125">Paramètre pour spécifier si vous souhaitez extraire tous les sous-groupes dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="3f4cb-125">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

### <a name="response-body"></a><span data-ttu-id="3f4cb-126">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3f4cb-126">Response body</span></span>

| <span data-ttu-id="3f4cb-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-127">Parameter</span></span> | <span data-ttu-id="3f4cb-128">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-128">Type</span></span> | <span data-ttu-id="3f4cb-129">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-129">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-130">groupes</span><span class="sxs-lookup"><span data-stu-id="3f4cb-130">groups</span></span> | <span data-ttu-id="3f4cb-131">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="3f4cb-131">JSON Object Array</span></span> | <span data-ttu-id="3f4cb-132">Tableau des groupes à la liste des sous-groupes, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="3f4cb-132">Array of groups with the list of subGroups if any</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="3f4cb-133">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="3f4cb-133">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="3f4cb-134">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-134">Parameter</span></span> | <span data-ttu-id="3f4cb-135">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-135">Type</span></span> | <span data-ttu-id="3f4cb-136">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-136">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-137">groupId</span><span class="sxs-lookup"><span data-stu-id="3f4cb-137">groupId</span></span> | <span data-ttu-id="3f4cb-138">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-138">String</span></span> | <span data-ttu-id="3f4cb-139">GUID associé au groupe</span><span class="sxs-lookup"><span data-stu-id="3f4cb-139">GUID associated with the group</span></span> |
| <span data-ttu-id="3f4cb-140">groupName</span><span class="sxs-lookup"><span data-stu-id="3f4cb-140">groupName</span></span> | <span data-ttu-id="3f4cb-141">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-141">String</span></span> | <span data-ttu-id="3f4cb-142">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="3f4cb-142">Name of the group</span></span> |
| <span data-ttu-id="3f4cb-143">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="3f4cb-143">groupImageURL</span></span> | <span data-ttu-id="3f4cb-144">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-144">String</span></span> | <span data-ttu-id="3f4cb-145">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="3f4cb-145">String specifying the URL of the group profile picture</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="3f4cb-146">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="3f4cb-146">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "subGroups": [
          {
            "groupName": "Sample sub group name",
            "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
            "groupImageUrl": "{sample sub group image URL here}",
          }
      ]
    }
  ]
}
```

## <a name="post-subgroups"></a><span data-ttu-id="3f4cb-147">/SubGroups POST</span><span class="sxs-lookup"><span data-stu-id="3f4cb-147">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="3f4cb-148">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="3f4cb-148">Request Parameters</span></span>

|  | <span data-ttu-id="3f4cb-149">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-149">Parameter</span></span> | <span data-ttu-id="3f4cb-150">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-150">Type</span></span> | <span data-ttu-id="3f4cb-151">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3f4cb-151">Optional?</span></span> | <span data-ttu-id="3f4cb-152">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-152">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-153">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3f4cb-153">HTTP Header</span></span> | <span data-ttu-id="3f4cb-154">accessToken</span><span class="sxs-lookup"><span data-stu-id="3f4cb-154">accessToken</span></span> | <span data-ttu-id="3f4cb-155">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-155">String</span></span> | <span data-ttu-id="3f4cb-156">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-156">No</span></span> | <span data-ttu-id="3f4cb-157">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4cb-157">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="3f4cb-158">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="3f4cb-158">URL Path Parameter</span></span> | <span data-ttu-id="3f4cb-159">groupId</span><span class="sxs-lookup"><span data-stu-id="3f4cb-159">groupId</span></span> | <span data-ttu-id="3f4cb-160">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-160">String</span></span> | <span data-ttu-id="3f4cb-161">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-161">No</span></span> | <span data-ttu-id="3f4cb-162">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="3f4cb-162">GUID representing the groupId of the specific group resource</span></span> |

### <a name="request-body"></a><span data-ttu-id="3f4cb-163">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="3f4cb-163">Request body</span></span>

|  | <span data-ttu-id="3f4cb-164">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-164">Parameter</span></span> | <span data-ttu-id="3f4cb-165">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-165">Type</span></span> | <span data-ttu-id="3f4cb-166">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3f4cb-166">Optional?</span></span> | <span data-ttu-id="3f4cb-167">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-167">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-168">groupName</span><span class="sxs-lookup"><span data-stu-id="3f4cb-168">groupName</span></span> | <span data-ttu-id="3f4cb-169">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-169">String</span></span> | <span data-ttu-id="3f4cb-170">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-170">No</span></span> | <span data-ttu-id="3f4cb-171">Nom du groupe sub</span><span class="sxs-lookup"><span data-stu-id="3f4cb-171">Name of the sub group</span></span> |
| <span data-ttu-id="3f4cb-172">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="3f4cb-172">groupImageURL</span></span> | <span data-ttu-id="3f4cb-173">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-173">String</span></span> | <span data-ttu-id="3f4cb-174">Oui</span><span class="sxs-lookup"><span data-stu-id="3f4cb-174">Yes</span></span> | <span data-ttu-id="3f4cb-175">URL de support de l’image de groupe ; Image doit être téléchargé via le chemin d’accès/Media</span><span class="sxs-lookup"><span data-stu-id="3f4cb-175">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="3f4cb-176">membres</span><span class="sxs-lookup"><span data-stu-id="3f4cb-176">members</span></span> | <span data-ttu-id="3f4cb-177">Tableau</span><span class="sxs-lookup"><span data-stu-id="3f4cb-177">Array</span></span> | <span data-ttu-id="3f4cb-178">Oui</span><span class="sxs-lookup"><span data-stu-id="3f4cb-178">Yes</span></span> | <span data-ttu-id="3f4cb-179">Tableau de chaînes de numéros de téléphone au format correct</span><span class="sxs-lookup"><span data-stu-id="3f4cb-179">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="3f4cb-180">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="3f4cb-180">welcomeMessage</span></span> | <span data-ttu-id="3f4cb-181">Tableau</span><span class="sxs-lookup"><span data-stu-id="3f4cb-181">Array</span></span> | <span data-ttu-id="3f4cb-182">Non</span><span class="sxs-lookup"><span data-stu-id="3f4cb-182">No</span></span> | <span data-ttu-id="3f4cb-183">Tableau de chaînes de numéros de téléphone au format correct</span><span class="sxs-lookup"><span data-stu-id="3f4cb-183">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="3f4cb-184">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="3f4cb-184">addUserToGroup</span></span> | <span data-ttu-id="3f4cb-185">Booléen</span><span class="sxs-lookup"><span data-stu-id="3f4cb-185">Boolean</span></span> | <span data-ttu-id="3f4cb-186">Oui</span><span class="sxs-lookup"><span data-stu-id="3f4cb-186">Yes</span></span> | <span data-ttu-id="3f4cb-187">La valeur False si l’utilisateur appelant ne doit pas être ajouté au groupe par défaut</span><span class="sxs-lookup"><span data-stu-id="3f4cb-187">Set to False if the calling user should not be added to the group by default</span></span>  |


#### <a name="sample-json-request"></a><span data-ttu-id="3f4cb-188">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="3f4cb-188">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a><span data-ttu-id="3f4cb-189">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3f4cb-189">Response body</span></span>

| <span data-ttu-id="3f4cb-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3f4cb-190">Parameter</span></span> | <span data-ttu-id="3f4cb-191">Type</span><span class="sxs-lookup"><span data-stu-id="3f4cb-191">Type</span></span> | <span data-ttu-id="3f4cb-192">Description</span><span class="sxs-lookup"><span data-stu-id="3f4cb-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3f4cb-193">groupId</span><span class="sxs-lookup"><span data-stu-id="3f4cb-193">groupId</span></span> | <span data-ttu-id="3f4cb-194">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-194">String</span></span> | <span data-ttu-id="3f4cb-195">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="3f4cb-195">Group Identifier</span></span> |
| <span data-ttu-id="3f4cb-196">groupName</span><span class="sxs-lookup"><span data-stu-id="3f4cb-196">groupName</span></span> | <span data-ttu-id="3f4cb-197">String</span><span class="sxs-lookup"><span data-stu-id="3f4cb-197">String</span></span> | <span data-ttu-id="3f4cb-198">Nom du groupe créé</span><span class="sxs-lookup"><span data-stu-id="3f4cb-198">Name of the group created</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="3f4cb-199">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="3f4cb-199">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
