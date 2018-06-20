---
title: /subGroups
description: Article de référence de l’API pour interroger les données sous-groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6d013b4d6657eaaaadb9fe3244c2d9383e56f6
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905128"
---
# <a name="apis-to-query-subgroups-within-a-group"></a><span data-ttu-id="64a63-103">API de sous-groupes de requête au sein d’un groupe</span><span class="sxs-lookup"><span data-stu-id="64a63-103">APIs to query subgroups within a group</span></span>
## <a name="subgroups"></a><span data-ttu-id="64a63-104">/subGroups</span><span class="sxs-lookup"><span data-stu-id="64a63-104">/subGroups</span></span>
<span data-ttu-id="64a63-105">Prévoit d’API pour interagir avec la conversation sous-groupes à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="64a63-105">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

### <a name="get-subgroups"></a><span data-ttu-id="64a63-106">OBTENIR /subGroups</span><span class="sxs-lookup"><span data-stu-id="64a63-106">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a><span data-ttu-id="64a63-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="64a63-107">Request Parameters</span></span>

|  | <span data-ttu-id="64a63-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-108">Parameter</span></span> | <span data-ttu-id="64a63-109">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-109">Type</span></span> | <span data-ttu-id="64a63-110">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="64a63-110">Optional?</span></span> | <span data-ttu-id="64a63-111">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="64a63-112">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="64a63-112">HTTP Header</span></span> | <span data-ttu-id="64a63-113">accessToken</span><span class="sxs-lookup"><span data-stu-id="64a63-113">accessToken</span></span> | <span data-ttu-id="64a63-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-114">String</span></span> | <span data-ttu-id="64a63-115">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-115">No</span></span> | <span data-ttu-id="64a63-116">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="64a63-116">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="64a63-117">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="64a63-117">URL Path Parameter</span></span> | <span data-ttu-id="64a63-118">groupId</span><span class="sxs-lookup"><span data-stu-id="64a63-118">groupId</span></span> | <span data-ttu-id="64a63-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-119">String</span></span> | <span data-ttu-id="64a63-120">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-120">No</span></span> | <span data-ttu-id="64a63-121">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="64a63-121">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="64a63-122">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="64a63-122">URL Query Parameter</span></span> | <span data-ttu-id="64a63-123">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="64a63-123">fetchAllGroups</span></span> | <span data-ttu-id="64a63-124">Booléen</span><span class="sxs-lookup"><span data-stu-id="64a63-124">Boolean</span></span> | <span data-ttu-id="64a63-125">Oui</span><span class="sxs-lookup"><span data-stu-id="64a63-125">Yes</span></span> | <span data-ttu-id="64a63-126">Paramètre pour spécifier si vous souhaitez extraire tous les sous-groupes dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="64a63-126">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

##### <a name="response-body"></a><span data-ttu-id="64a63-127">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="64a63-127">Response body</span></span>

| <span data-ttu-id="64a63-128">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-128">Parameter</span></span> | <span data-ttu-id="64a63-129">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-129">Type</span></span> | <span data-ttu-id="64a63-130">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-130">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="64a63-131">groupes</span><span class="sxs-lookup"><span data-stu-id="64a63-131">groups</span></span> | <span data-ttu-id="64a63-132">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="64a63-132">JSON Object Array</span></span> | <span data-ttu-id="64a63-133">Tableau des groupes à la liste des sous-groupes, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="64a63-133">Array of groups with the list of subGroups if any</span></span> |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="64a63-134">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="64a63-134">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="64a63-135">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-135">Parameter</span></span> | <span data-ttu-id="64a63-136">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-136">Type</span></span> | <span data-ttu-id="64a63-137">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-137">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="64a63-138">groupId</span><span class="sxs-lookup"><span data-stu-id="64a63-138">groupId</span></span> | <span data-ttu-id="64a63-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-139">String</span></span> | <span data-ttu-id="64a63-140">GUID associé au groupe</span><span class="sxs-lookup"><span data-stu-id="64a63-140">GUID associated with the group</span></span> |
| <span data-ttu-id="64a63-141">groupName</span><span class="sxs-lookup"><span data-stu-id="64a63-141">groupName</span></span> | <span data-ttu-id="64a63-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-142">String</span></span> | <span data-ttu-id="64a63-143">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="64a63-143">Name of the group</span></span> |
| <span data-ttu-id="64a63-144">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="64a63-144">groupImageURL</span></span> | <span data-ttu-id="64a63-145">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-145">String</span></span> | <span data-ttu-id="64a63-146">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="64a63-146">String specifying the URL of the group profile picture</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="64a63-147">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="64a63-147">Sample JSON Response</span></span>

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

### <a name="post-subgroups"></a><span data-ttu-id="64a63-148">/SubGroups POST</span><span class="sxs-lookup"><span data-stu-id="64a63-148">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a><span data-ttu-id="64a63-149">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="64a63-149">Request Parameters</span></span>

|  | <span data-ttu-id="64a63-150">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-150">Parameter</span></span> | <span data-ttu-id="64a63-151">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-151">Type</span></span> | <span data-ttu-id="64a63-152">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="64a63-152">Optional?</span></span> | <span data-ttu-id="64a63-153">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-153">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="64a63-154">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="64a63-154">HTTP Header</span></span> | <span data-ttu-id="64a63-155">accessToken</span><span class="sxs-lookup"><span data-stu-id="64a63-155">accessToken</span></span> | <span data-ttu-id="64a63-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-156">String</span></span> | <span data-ttu-id="64a63-157">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-157">No</span></span> | <span data-ttu-id="64a63-158">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="64a63-158">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="64a63-159">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="64a63-159">URL Path Parameter</span></span> | <span data-ttu-id="64a63-160">groupId</span><span class="sxs-lookup"><span data-stu-id="64a63-160">groupId</span></span> | <span data-ttu-id="64a63-161">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-161">String</span></span> | <span data-ttu-id="64a63-162">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-162">No</span></span> | <span data-ttu-id="64a63-163">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="64a63-163">GUID representing the groupId of the specific group resource</span></span> |

##### <a name="request-body"></a><span data-ttu-id="64a63-164">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="64a63-164">Request body</span></span>

|  | <span data-ttu-id="64a63-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-165">Parameter</span></span> | <span data-ttu-id="64a63-166">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-166">Type</span></span> | <span data-ttu-id="64a63-167">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="64a63-167">Optional?</span></span> | <span data-ttu-id="64a63-168">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-168">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="64a63-169">groupName</span><span class="sxs-lookup"><span data-stu-id="64a63-169">groupName</span></span> | <span data-ttu-id="64a63-170">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-170">String</span></span> | <span data-ttu-id="64a63-171">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-171">No</span></span> | <span data-ttu-id="64a63-172">Nom du groupe sub</span><span class="sxs-lookup"><span data-stu-id="64a63-172">Name of the sub group</span></span> |
| <span data-ttu-id="64a63-173">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="64a63-173">groupImageURL</span></span> | <span data-ttu-id="64a63-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-174">String</span></span> | <span data-ttu-id="64a63-175">Oui</span><span class="sxs-lookup"><span data-stu-id="64a63-175">Yes</span></span> | <span data-ttu-id="64a63-176">URL de support de l’image de groupe ; Image doit être téléchargé via le chemin d’accès/Media</span><span class="sxs-lookup"><span data-stu-id="64a63-176">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="64a63-177">membres</span><span class="sxs-lookup"><span data-stu-id="64a63-177">members</span></span> | <span data-ttu-id="64a63-178">Tableau</span><span class="sxs-lookup"><span data-stu-id="64a63-178">Array</span></span> | <span data-ttu-id="64a63-179">Oui</span><span class="sxs-lookup"><span data-stu-id="64a63-179">Yes</span></span> | <span data-ttu-id="64a63-180">Tableau de chaînes de numéros de téléphone au format correct</span><span class="sxs-lookup"><span data-stu-id="64a63-180">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="64a63-181">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="64a63-181">welcomeMessage</span></span> | <span data-ttu-id="64a63-182">Tableau</span><span class="sxs-lookup"><span data-stu-id="64a63-182">Array</span></span> | <span data-ttu-id="64a63-183">Non</span><span class="sxs-lookup"><span data-stu-id="64a63-183">No</span></span> | <span data-ttu-id="64a63-184">Tableau de chaînes de numéros de téléphone au format correct</span><span class="sxs-lookup"><span data-stu-id="64a63-184">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="64a63-185">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="64a63-185">addUserToGroup</span></span> | <span data-ttu-id="64a63-186">Booléen</span><span class="sxs-lookup"><span data-stu-id="64a63-186">Boolean</span></span> | <span data-ttu-id="64a63-187">Oui</span><span class="sxs-lookup"><span data-stu-id="64a63-187">Yes</span></span> | <span data-ttu-id="64a63-188">La valeur False si l’utilisateur appelant ne doit pas être ajouté au groupe par défaut</span><span class="sxs-lookup"><span data-stu-id="64a63-188">Set to False if the calling user should not be added to the group by default</span></span>  |


###### <a name="sample-json-request"></a><span data-ttu-id="64a63-189">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="64a63-189">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

##### <a name="response-body"></a><span data-ttu-id="64a63-190">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="64a63-190">Response body</span></span>

| <span data-ttu-id="64a63-191">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64a63-191">Parameter</span></span> | <span data-ttu-id="64a63-192">Type</span><span class="sxs-lookup"><span data-stu-id="64a63-192">Type</span></span> | <span data-ttu-id="64a63-193">Description</span><span class="sxs-lookup"><span data-stu-id="64a63-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="64a63-194">groupId</span><span class="sxs-lookup"><span data-stu-id="64a63-194">groupId</span></span> | <span data-ttu-id="64a63-195">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-195">String</span></span> | <span data-ttu-id="64a63-196">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="64a63-196">Group Identifier</span></span> |
| <span data-ttu-id="64a63-197">groupName</span><span class="sxs-lookup"><span data-stu-id="64a63-197">groupName</span></span> | <span data-ttu-id="64a63-198">Chaîne</span><span class="sxs-lookup"><span data-stu-id="64a63-198">String</span></span> | <span data-ttu-id="64a63-199">Nom du groupe créé</span><span class="sxs-lookup"><span data-stu-id="64a63-199">Name of the group created</span></span> |


###### <a name="sample-json-response"></a><span data-ttu-id="64a63-200">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="64a63-200">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
