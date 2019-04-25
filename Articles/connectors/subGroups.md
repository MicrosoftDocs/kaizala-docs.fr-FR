---
title: /subGroups
description: Article de référence pour l'API permettant d'interroger les données de sous-groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190687"
---
# <a name="subgroups"></a><span data-ttu-id="5ec99-103">/subGroups</span><span class="sxs-lookup"><span data-stu-id="5ec99-103">/subGroups</span></span>
<span data-ttu-id="5ec99-104">Point de terminaison d'API pour interagir avec les sous-groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="5ec99-104">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

## <a name="get-subgroups"></a><span data-ttu-id="5ec99-105">OBTENIR/subGroups</span><span class="sxs-lookup"><span data-stu-id="5ec99-105">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="5ec99-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="5ec99-106">Request Parameters</span></span>

|  | <span data-ttu-id="5ec99-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-107">Parameter</span></span> | <span data-ttu-id="5ec99-108">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-108">Type</span></span> | <span data-ttu-id="5ec99-109">Module?</span><span class="sxs-lookup"><span data-stu-id="5ec99-109">Optional?</span></span> | <span data-ttu-id="5ec99-110">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5ec99-111">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="5ec99-111">HTTP Header</span></span> | <span data-ttu-id="5ec99-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="5ec99-112">accessToken</span></span> | <span data-ttu-id="5ec99-113">String</span><span class="sxs-lookup"><span data-stu-id="5ec99-113">String</span></span> | <span data-ttu-id="5ec99-114">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-114">No</span></span> | <span data-ttu-id="5ec99-115">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="5ec99-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="5ec99-116">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="5ec99-116">URL Path Parameter</span></span> | <span data-ttu-id="5ec99-117">groupId</span><span class="sxs-lookup"><span data-stu-id="5ec99-117">groupId</span></span> | <span data-ttu-id="5ec99-118">String</span><span class="sxs-lookup"><span data-stu-id="5ec99-118">String</span></span> | <span data-ttu-id="5ec99-119">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-119">No</span></span> | <span data-ttu-id="5ec99-120">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="5ec99-120">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="5ec99-121">Paramètre de requête d'URL</span><span class="sxs-lookup"><span data-stu-id="5ec99-121">URL Query Parameter</span></span> | <span data-ttu-id="5ec99-122">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="5ec99-122">fetchAllGroups</span></span> | <span data-ttu-id="5ec99-123">Booléen</span><span class="sxs-lookup"><span data-stu-id="5ec99-123">Boolean</span></span> | <span data-ttu-id="5ec99-124">Oui</span><span class="sxs-lookup"><span data-stu-id="5ec99-124">Yes</span></span> | <span data-ttu-id="5ec99-125">Paramètre pour spécifier si vous souhaitez extraire tous les sous-groupes de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="5ec99-125">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

### <a name="response-body"></a><span data-ttu-id="5ec99-126">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="5ec99-126">Response body</span></span>

| <span data-ttu-id="5ec99-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-127">Parameter</span></span> | <span data-ttu-id="5ec99-128">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-128">Type</span></span> | <span data-ttu-id="5ec99-129">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-129">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5ec99-130">groupes</span><span class="sxs-lookup"><span data-stu-id="5ec99-130">groups</span></span> | <span data-ttu-id="5ec99-131">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="5ec99-131">JSON Object Array</span></span> | <span data-ttu-id="5ec99-132">Tableau de groupes avec la liste des sous-groupes, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="5ec99-132">Array of groups with the list of subGroups if any</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="5ec99-133">Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:</span><span class="sxs-lookup"><span data-stu-id="5ec99-133">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="5ec99-134">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-134">Parameter</span></span> | <span data-ttu-id="5ec99-135">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-135">Type</span></span> | <span data-ttu-id="5ec99-136">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-136">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5ec99-137">groupId</span><span class="sxs-lookup"><span data-stu-id="5ec99-137">groupId</span></span> | <span data-ttu-id="5ec99-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-138">String</span></span> | <span data-ttu-id="5ec99-139">GUID associé au groupe</span><span class="sxs-lookup"><span data-stu-id="5ec99-139">GUID associated with the group</span></span> |
| <span data-ttu-id="5ec99-140">groupName</span><span class="sxs-lookup"><span data-stu-id="5ec99-140">groupName</span></span> | <span data-ttu-id="5ec99-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-141">String</span></span> | <span data-ttu-id="5ec99-142">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="5ec99-142">Name of the group</span></span> |
| <span data-ttu-id="5ec99-143">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="5ec99-143">groupImageURL</span></span> | <span data-ttu-id="5ec99-144">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-144">String</span></span> | <span data-ttu-id="5ec99-145">Chaîne spécifiant l'URL de l'image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="5ec99-145">String specifying the URL of the group profile picture</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="5ec99-146">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="5ec99-146">Sample JSON Response</span></span>

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

## <a name="post-subgroups"></a><span data-ttu-id="5ec99-147">POST/subGroups</span><span class="sxs-lookup"><span data-stu-id="5ec99-147">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="5ec99-148">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="5ec99-148">Request Parameters</span></span>

|  | <span data-ttu-id="5ec99-149">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-149">Parameter</span></span> | <span data-ttu-id="5ec99-150">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-150">Type</span></span> | <span data-ttu-id="5ec99-151">Module?</span><span class="sxs-lookup"><span data-stu-id="5ec99-151">Optional?</span></span> | <span data-ttu-id="5ec99-152">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-152">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5ec99-153">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="5ec99-153">HTTP Header</span></span> | <span data-ttu-id="5ec99-154">accessToken</span><span class="sxs-lookup"><span data-stu-id="5ec99-154">accessToken</span></span> | <span data-ttu-id="5ec99-155">String</span><span class="sxs-lookup"><span data-stu-id="5ec99-155">String</span></span> | <span data-ttu-id="5ec99-156">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-156">No</span></span> | <span data-ttu-id="5ec99-157">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="5ec99-157">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="5ec99-158">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="5ec99-158">URL Path Parameter</span></span> | <span data-ttu-id="5ec99-159">groupId</span><span class="sxs-lookup"><span data-stu-id="5ec99-159">groupId</span></span> | <span data-ttu-id="5ec99-160">String</span><span class="sxs-lookup"><span data-stu-id="5ec99-160">String</span></span> | <span data-ttu-id="5ec99-161">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-161">No</span></span> | <span data-ttu-id="5ec99-162">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="5ec99-162">GUID representing the groupId of the specific group resource</span></span> |

### <a name="request-body"></a><span data-ttu-id="5ec99-163">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="5ec99-163">Request body</span></span>

|  | <span data-ttu-id="5ec99-164">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-164">Parameter</span></span> | <span data-ttu-id="5ec99-165">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-165">Type</span></span> | <span data-ttu-id="5ec99-166">Module?</span><span class="sxs-lookup"><span data-stu-id="5ec99-166">Optional?</span></span> | <span data-ttu-id="5ec99-167">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-167">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5ec99-168">groupName</span><span class="sxs-lookup"><span data-stu-id="5ec99-168">groupName</span></span> | <span data-ttu-id="5ec99-169">String</span><span class="sxs-lookup"><span data-stu-id="5ec99-169">String</span></span> | <span data-ttu-id="5ec99-170">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-170">No</span></span> | <span data-ttu-id="5ec99-171">Nom du sous-groupe</span><span class="sxs-lookup"><span data-stu-id="5ec99-171">Name of the sub group</span></span> |
| <span data-ttu-id="5ec99-172">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="5ec99-172">groupImageURL</span></span> | <span data-ttu-id="5ec99-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-173">String</span></span> | <span data-ttu-id="5ec99-174">Oui</span><span class="sxs-lookup"><span data-stu-id="5ec99-174">Yes</span></span> | <span data-ttu-id="5ec99-175">URL de média de l'image de groupe; L'image doit être téléchargée via le chemin d'accès/Media</span><span class="sxs-lookup"><span data-stu-id="5ec99-175">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="5ec99-176">membres</span><span class="sxs-lookup"><span data-stu-id="5ec99-176">members</span></span> | <span data-ttu-id="5ec99-177">Tableau</span><span class="sxs-lookup"><span data-stu-id="5ec99-177">Array</span></span> | <span data-ttu-id="5ec99-178">Oui</span><span class="sxs-lookup"><span data-stu-id="5ec99-178">Yes</span></span> | <span data-ttu-id="5ec99-179">Tableau de chaînes de numéros de téléphone bien mis en forme</span><span class="sxs-lookup"><span data-stu-id="5ec99-179">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="5ec99-180">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="5ec99-180">welcomeMessage</span></span> | <span data-ttu-id="5ec99-181">Tableau</span><span class="sxs-lookup"><span data-stu-id="5ec99-181">Array</span></span> | <span data-ttu-id="5ec99-182">Non</span><span class="sxs-lookup"><span data-stu-id="5ec99-182">No</span></span> | <span data-ttu-id="5ec99-183">Tableau de chaînes de numéros de téléphone bien mis en forme</span><span class="sxs-lookup"><span data-stu-id="5ec99-183">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="5ec99-184">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="5ec99-184">addUserToGroup</span></span> | <span data-ttu-id="5ec99-185">Booléen</span><span class="sxs-lookup"><span data-stu-id="5ec99-185">Boolean</span></span> | <span data-ttu-id="5ec99-186">Oui</span><span class="sxs-lookup"><span data-stu-id="5ec99-186">Yes</span></span> | <span data-ttu-id="5ec99-187">Valeur false si l'utilisateur appelant ne doit pas être ajouté au groupe par défaut</span><span class="sxs-lookup"><span data-stu-id="5ec99-187">Set to False if the calling user should not be added to the group by default</span></span>  |


#### <a name="sample-json-request"></a><span data-ttu-id="5ec99-188">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="5ec99-188">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a><span data-ttu-id="5ec99-189">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="5ec99-189">Response body</span></span>

| <span data-ttu-id="5ec99-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5ec99-190">Parameter</span></span> | <span data-ttu-id="5ec99-191">Type</span><span class="sxs-lookup"><span data-stu-id="5ec99-191">Type</span></span> | <span data-ttu-id="5ec99-192">Description</span><span class="sxs-lookup"><span data-stu-id="5ec99-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5ec99-193">groupId</span><span class="sxs-lookup"><span data-stu-id="5ec99-193">groupId</span></span> | <span data-ttu-id="5ec99-194">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-194">String</span></span> | <span data-ttu-id="5ec99-195">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="5ec99-195">Group Identifier</span></span> |
| <span data-ttu-id="5ec99-196">groupName</span><span class="sxs-lookup"><span data-stu-id="5ec99-196">groupName</span></span> | <span data-ttu-id="5ec99-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5ec99-197">String</span></span> | <span data-ttu-id="5ec99-198">Nom du groupe créé</span><span class="sxs-lookup"><span data-stu-id="5ec99-198">Name of the group created</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="5ec99-199">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="5ec99-199">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
