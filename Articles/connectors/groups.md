---
title: /Groups
description: Article de référence pour l'API permettant de rechercher des données de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190715"
---
# <a name="groups"></a><span data-ttu-id="1933f-103">/Groups</span><span class="sxs-lookup"><span data-stu-id="1933f-103">/groups</span></span>
<span data-ttu-id="1933f-104">Point de terminaison d'API pour interagir avec les groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="1933f-104">API end-point to interact with the conversation groups inside Kaizala.</span></span>

## <a name="post-groups"></a><span data-ttu-id="1933f-105">POST/Groups</span><span class="sxs-lookup"><span data-stu-id="1933f-105">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="1933f-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="1933f-106">Request Parameters</span></span>

|  | <span data-ttu-id="1933f-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-107">Parameter</span></span> | <span data-ttu-id="1933f-108">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-108">Type</span></span> | <span data-ttu-id="1933f-109">Module?</span><span class="sxs-lookup"><span data-stu-id="1933f-109">Optional?</span></span> | <span data-ttu-id="1933f-110">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="1933f-111">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1933f-111">HTTP Header</span></span> | <span data-ttu-id="1933f-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="1933f-112">accessToken</span></span> | <span data-ttu-id="1933f-113">String</span><span class="sxs-lookup"><span data-stu-id="1933f-113">String</span></span> | <span data-ttu-id="1933f-114">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-114">No</span></span> | <span data-ttu-id="1933f-115">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="1933f-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="1933f-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1933f-116">HTTP Header</span></span> | <span data-ttu-id="1933f-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1933f-117">Content-Type</span></span> | <span data-ttu-id="1933f-118">String</span><span class="sxs-lookup"><span data-stu-id="1933f-118">String</span></span> | <span data-ttu-id="1933f-119">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-119">No</span></span> | <span data-ttu-id="1933f-120">«application/JSON»</span><span class="sxs-lookup"><span data-stu-id="1933f-120">"application/json"</span></span> |

### <a name="request-body"></a><span data-ttu-id="1933f-121">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1933f-121">Request body</span></span>

| <span data-ttu-id="1933f-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-122">Parameter</span></span> | <span data-ttu-id="1933f-123">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-123">Type</span></span> | <span data-ttu-id="1933f-124">Module?</span><span class="sxs-lookup"><span data-stu-id="1933f-124">Optional?</span></span> | <span data-ttu-id="1933f-125">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-125">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="1933f-126">name</span><span class="sxs-lookup"><span data-stu-id="1933f-126">name</span></span> | <span data-ttu-id="1933f-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-127">String</span></span> | <span data-ttu-id="1933f-128">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-128">No</span></span> | <span data-ttu-id="1933f-129">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-129">Group name</span></span> |
| <span data-ttu-id="1933f-130">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="1933f-130">welcomeMessage</span></span> | <span data-ttu-id="1933f-131">String</span><span class="sxs-lookup"><span data-stu-id="1933f-131">String</span></span> | <span data-ttu-id="1933f-132">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-132">No</span></span> | <span data-ttu-id="1933f-133">Message d'accueil qui sera affiché dans le nouveau membre de groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-133">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="1933f-134">membres</span><span class="sxs-lookup"><span data-stu-id="1933f-134">members</span></span> | <span data-ttu-id="1933f-135">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="1933f-135">String[]</span></span> | <span data-ttu-id="1933f-136">Oui</span><span class="sxs-lookup"><span data-stu-id="1933f-136">Yes</span></span> | <span data-ttu-id="1933f-137">Numéro de téléphone mobile (avec code de pays) des membres à ajouter.</span><span class="sxs-lookup"><span data-stu-id="1933f-137">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="1933f-138">Valeur par défaut: l'utilisateur du jeton d'accès est ajouté en tant qu'administrateur du groupe.</span><span class="sxs-lookup"><span data-stu-id="1933f-138">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="1933f-139">groupType</span><span class="sxs-lookup"><span data-stu-id="1933f-139">groupType</span></span> | <span data-ttu-id="1933f-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-140">String</span></span> | <span data-ttu-id="1933f-141">Oui</span><span class="sxs-lookup"><span data-stu-id="1933f-141">Yes</span></span> | <span data-ttu-id="1933f-142">Énumération: Group/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="1933f-142">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="1933f-143">ConnectGroup crée un groupe public géré.</span><span class="sxs-lookup"><span data-stu-id="1933f-143">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="1933f-144">Valeur par défaut: groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-144">Default: Group</span></span> |

#### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="1933f-145">Exemple de requête JSON pour Create Group</span><span class="sxs-lookup"><span data-stu-id="1933f-145">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a><span data-ttu-id="1933f-146">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="1933f-146">Response body</span></span>

| <span data-ttu-id="1933f-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-147">Parameter</span></span> | <span data-ttu-id="1933f-148">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-148">Type</span></span> | <span data-ttu-id="1933f-149">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1933f-150">groupName</span><span class="sxs-lookup"><span data-stu-id="1933f-150">groupName</span></span> | <span data-ttu-id="1933f-151">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-151">String</span></span> | <span data-ttu-id="1933f-152">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-152">Group name</span></span> |
| <span data-ttu-id="1933f-153">groupId</span><span class="sxs-lookup"><span data-stu-id="1933f-153">groupId</span></span> | <span data-ttu-id="1933f-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-154">String</span></span> | <span data-ttu-id="1933f-155">Identificateur de groupe qui peut être utilisé dans les appels d'API suivants</span><span class="sxs-lookup"><span data-stu-id="1933f-155">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="1933f-156">membersAdded</span><span class="sxs-lookup"><span data-stu-id="1933f-156">membersAdded</span></span> | <span data-ttu-id="1933f-157">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-157">bool</span></span> | <span data-ttu-id="1933f-158">True si tous les membres sont ajoutés avec succès</span><span class="sxs-lookup"><span data-stu-id="1933f-158">True if all members are successfully added</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="1933f-159">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="1933f-159">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a><span data-ttu-id="1933f-160">OBTENIR/Groups</span><span class="sxs-lookup"><span data-stu-id="1933f-160">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="1933f-161">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="1933f-161">Request Parameters</span></span>

|  | <span data-ttu-id="1933f-162">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-162">Parameter</span></span> | <span data-ttu-id="1933f-163">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-163">Type</span></span> | <span data-ttu-id="1933f-164">Module?</span><span class="sxs-lookup"><span data-stu-id="1933f-164">Optional?</span></span> | <span data-ttu-id="1933f-165">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="1933f-166">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1933f-166">HTTP Header</span></span> | <span data-ttu-id="1933f-167">accessToken</span><span class="sxs-lookup"><span data-stu-id="1933f-167">accessToken</span></span> | <span data-ttu-id="1933f-168">String</span><span class="sxs-lookup"><span data-stu-id="1933f-168">String</span></span> | <span data-ttu-id="1933f-169">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-169">No</span></span> | <span data-ttu-id="1933f-170">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="1933f-170">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="1933f-171">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="1933f-171">Query parameter</span></span> | <span data-ttu-id="1933f-172">showDetail</span><span class="sxs-lookup"><span data-stu-id="1933f-172">showDetail</span></span> | <span data-ttu-id="1933f-173">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-173">bool</span></span> | <span data-ttu-id="1933f-174">Oui</span><span class="sxs-lookup"><span data-stu-id="1933f-174">Yes</span></span> | <span data-ttu-id="1933f-175">Valeur par défaut: false.</span><span class="sxs-lookup"><span data-stu-id="1933f-175">Default: false.</span></span> <span data-ttu-id="1933f-176">True pour renvoyer tous les détails du groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-176">True to return all group details</span></span> |
| <span data-ttu-id="1933f-177">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="1933f-177">Query parameter</span></span> | <span data-ttu-id="1933f-178">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="1933f-178">fetchAllGroups</span></span> | <span data-ttu-id="1933f-179">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-179">bool</span></span> | <span data-ttu-id="1933f-180">Oui</span><span class="sxs-lookup"><span data-stu-id="1933f-180">Yes</span></span> | <span data-ttu-id="1933f-181">Valeur par défaut: false.</span><span class="sxs-lookup"><span data-stu-id="1933f-181">Default: false.</span></span> <span data-ttu-id="1933f-182">True pour renvoyer tous les parents et sous-groupes</span><span class="sxs-lookup"><span data-stu-id="1933f-182">True to return all parent and sub groups</span></span> |

### <a name="response-body"></a><span data-ttu-id="1933f-183">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="1933f-183">Response body</span></span>

| <span data-ttu-id="1933f-184">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-184">Parameter</span></span> | <span data-ttu-id="1933f-185">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-185">Type</span></span> | <span data-ttu-id="1933f-186">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1933f-187">groupes</span><span class="sxs-lookup"><span data-stu-id="1933f-187">groups</span></span> | <span data-ttu-id="1933f-188">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="1933f-188">JSON Object Array</span></span> | <span data-ttu-id="1933f-189">Tableau de groupes auxquels l'utilisateur a accès à l'aide du accessToken</span><span class="sxs-lookup"><span data-stu-id="1933f-189">Array of groups that the user has access to with the accessToken</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="1933f-190">Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:</span><span class="sxs-lookup"><span data-stu-id="1933f-190">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="1933f-191">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-191">Parameter</span></span> | <span data-ttu-id="1933f-192">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-192">Type</span></span> | <span data-ttu-id="1933f-193">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1933f-194">groupId</span><span class="sxs-lookup"><span data-stu-id="1933f-194">groupId</span></span> | <span data-ttu-id="1933f-195">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-195">String</span></span> | <span data-ttu-id="1933f-196">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-196">Group Identifier</span></span> |
| <span data-ttu-id="1933f-197">groupName</span><span class="sxs-lookup"><span data-stu-id="1933f-197">groupName</span></span> | <span data-ttu-id="1933f-198">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-198">String</span></span> | <span data-ttu-id="1933f-199">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-199">Name of the group</span></span> |
| <span data-ttu-id="1933f-200">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="1933f-200">groupImageURL</span></span> | <span data-ttu-id="1933f-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-201">String</span></span> | <span data-ttu-id="1933f-202">Chaîne spécifiant l'URL de l'image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-202">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="1933f-203">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="1933f-203">hasSubGroups</span></span> | <span data-ttu-id="1933f-204">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-204">bool</span></span> | <span data-ttu-id="1933f-205">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="1933f-205">True if the group has subgroups</span></span> |
| <span data-ttu-id="1933f-206">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="1933f-206">hasParentGroups</span></span> | <span data-ttu-id="1933f-207">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-207">bool</span></span> | <span data-ttu-id="1933f-208">True si le groupe a des groupes parents</span><span class="sxs-lookup"><span data-stu-id="1933f-208">True if the group has parent groups</span></span> |
| <span data-ttu-id="1933f-209">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="1933f-209">isMappedToTenant</span></span> | <span data-ttu-id="1933f-210">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-210">bool</span></span> | <span data-ttu-id="1933f-211">True si le groupe est un groupe d'organisation</span><span class="sxs-lookup"><span data-stu-id="1933f-211">True if the group is Organisation group</span></span> |
| <span data-ttu-id="1933f-212">groupType</span><span class="sxs-lookup"><span data-stu-id="1933f-212">groupType</span></span> | <span data-ttu-id="1933f-213">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-213">String</span></span> | <span data-ttu-id="1933f-214">Group/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="1933f-214">Group/ConnectGroup.</span></span> <span data-ttu-id="1933f-215">ConnectGroup si le groupe dans le groupe public géré</span><span class="sxs-lookup"><span data-stu-id="1933f-215">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="1933f-216">Nombre</span><span class="sxs-lookup"><span data-stu-id="1933f-216">userCount</span></span> | <span data-ttu-id="1933f-217">Numérique</span><span class="sxs-lookup"><span data-stu-id="1933f-217">Numeric</span></span> | <span data-ttu-id="1933f-218">Nombre total d'utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="1933f-218">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="1933f-219">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="1933f-219">currentLevelUserCount</span></span> | <span data-ttu-id="1933f-220">Numérique</span><span class="sxs-lookup"><span data-stu-id="1933f-220">Numeric</span></span> | <span data-ttu-id="1933f-221">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="1933f-221">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="1933f-222">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="1933f-222">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": false,
      "hasParentGroups": false,
      "callerRole": "Admin",
      "currentLevelSubGroupCount": 0,
      "currentLevelParentGroupCount": 0,
      "userCount": 2,
      "uniqueUserCount": 0,
      "currentLevelUserCount": 2,
      "currentLevelUnProvisionedUserCount": 0,
      "unProvisionedUserCount": 0,
      "isMappedToTenant": false,
      "groupType": "Group",
      "isDuplicate": false,
      "isEditable": true,
      "isDetailsReadable": true
    }
  ]
}
```

## <a name="get-groupsgroupid"></a><span data-ttu-id="1933f-223">OBTENIR/groups/{groupId}</span><span class="sxs-lookup"><span data-stu-id="1933f-223">GET /groups/{groupId}</span></span>

<span data-ttu-id="1933f-224">Vous pouvez obtenir des détails sur un membre de ressource spécifique (un groupe ici) en spécifiant l'identificateur sous la forme d'un paramètre de chemin d'URL.</span><span class="sxs-lookup"><span data-stu-id="1933f-224">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a><span data-ttu-id="1933f-225">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="1933f-225">Request Parameters</span></span>

|  | <span data-ttu-id="1933f-226">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-226">Parameter</span></span> | <span data-ttu-id="1933f-227">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-227">Type</span></span> | <span data-ttu-id="1933f-228">Module?</span><span class="sxs-lookup"><span data-stu-id="1933f-228">Optional?</span></span> | <span data-ttu-id="1933f-229">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-229">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="1933f-230">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="1933f-230">URL Path Parameter</span></span> | <span data-ttu-id="1933f-231">groupId</span><span class="sxs-lookup"><span data-stu-id="1933f-231">groupId</span></span> | <span data-ttu-id="1933f-232">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-232">String</span></span> | <span data-ttu-id="1933f-233">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-233">No</span></span> | <span data-ttu-id="1933f-234">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="1933f-234">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="1933f-235">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1933f-235">HTTP Header</span></span> | <span data-ttu-id="1933f-236">accessToken</span><span class="sxs-lookup"><span data-stu-id="1933f-236">accessToken</span></span> | <span data-ttu-id="1933f-237">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-237">String</span></span> | <span data-ttu-id="1933f-238">Non</span><span class="sxs-lookup"><span data-stu-id="1933f-238">No</span></span> | <span data-ttu-id="1933f-239">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="1933f-239">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="1933f-240">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="1933f-240">Response body</span></span>

| <span data-ttu-id="1933f-241">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-241">Parameter</span></span> | <span data-ttu-id="1933f-242">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-242">Type</span></span> | <span data-ttu-id="1933f-243">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1933f-244">groupes</span><span class="sxs-lookup"><span data-stu-id="1933f-244">groups</span></span> | <span data-ttu-id="1933f-245">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="1933f-245">JSON Object Array</span></span> | <span data-ttu-id="1933f-246">Tableau de groupes auxquels l'utilisateur a accès à l'aide du accessToken</span><span class="sxs-lookup"><span data-stu-id="1933f-246">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="1933f-247">Structure JSON pour chaque groupe individuel dans les groupes de tableaux []:</span><span class="sxs-lookup"><span data-stu-id="1933f-247">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="1933f-248">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1933f-248">Parameter</span></span> | <span data-ttu-id="1933f-249">Type</span><span class="sxs-lookup"><span data-stu-id="1933f-249">Type</span></span> | <span data-ttu-id="1933f-250">Description</span><span class="sxs-lookup"><span data-stu-id="1933f-250">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1933f-251">groupId</span><span class="sxs-lookup"><span data-stu-id="1933f-251">groupId</span></span> | <span data-ttu-id="1933f-252">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-252">String</span></span> | <span data-ttu-id="1933f-253">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-253">Group Identifier</span></span> |
| <span data-ttu-id="1933f-254">groupName</span><span class="sxs-lookup"><span data-stu-id="1933f-254">groupName</span></span> | <span data-ttu-id="1933f-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-255">String</span></span> | <span data-ttu-id="1933f-256">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-256">Name of the group</span></span> |
| <span data-ttu-id="1933f-257">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="1933f-257">groupImageURL</span></span> | <span data-ttu-id="1933f-258">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-258">String</span></span> | <span data-ttu-id="1933f-259">Chaîne spécifiant l'URL de l'image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="1933f-259">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="1933f-260">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="1933f-260">hasSubGroups</span></span> | <span data-ttu-id="1933f-261">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-261">bool</span></span> | <span data-ttu-id="1933f-262">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="1933f-262">True if the group has subgroups</span></span> |
| <span data-ttu-id="1933f-263">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="1933f-263">hasParentGroups</span></span> | <span data-ttu-id="1933f-264">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-264">bool</span></span> | <span data-ttu-id="1933f-265">True si le groupe a des groupes parents</span><span class="sxs-lookup"><span data-stu-id="1933f-265">True if the group has parent groups</span></span> |
| <span data-ttu-id="1933f-266">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="1933f-266">isMappedToTenant</span></span> | <span data-ttu-id="1933f-267">bool</span><span class="sxs-lookup"><span data-stu-id="1933f-267">bool</span></span> | <span data-ttu-id="1933f-268">True si le groupe est un groupe d'organisation</span><span class="sxs-lookup"><span data-stu-id="1933f-268">True if the group is Organisation group</span></span> |
| <span data-ttu-id="1933f-269">groupType</span><span class="sxs-lookup"><span data-stu-id="1933f-269">groupType</span></span> | <span data-ttu-id="1933f-270">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1933f-270">String</span></span> | <span data-ttu-id="1933f-271">Group/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="1933f-271">Group/ConnectGroup.</span></span> <span data-ttu-id="1933f-272">ConnectGroup si le groupe dans le groupe public géré</span><span class="sxs-lookup"><span data-stu-id="1933f-272">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="1933f-273">Nombre</span><span class="sxs-lookup"><span data-stu-id="1933f-273">userCount</span></span> | <span data-ttu-id="1933f-274">Numérique</span><span class="sxs-lookup"><span data-stu-id="1933f-274">Numeric</span></span> | <span data-ttu-id="1933f-275">Nombre total d'utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="1933f-275">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="1933f-276">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="1933f-276">currentLevelUserCount</span></span> | <span data-ttu-id="1933f-277">Numérique</span><span class="sxs-lookup"><span data-stu-id="1933f-277">Numeric</span></span> | <span data-ttu-id="1933f-278">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="1933f-278">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="1933f-279">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="1933f-279">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": true,
      "userCount": 200,
      "currentLevelUserCount": 10
    }
  ]
}
```

