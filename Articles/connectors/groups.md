---
title: /Groups
description: Article de référence de l’API pour interroger les données de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 010d6d30c72355e2575cda2f8104316a5a770ac4
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905141"
---
# <a name="apis-to-query-kaizala-groups"></a><span data-ttu-id="3cac0-103">API de groupes Kaizala de requêtes</span><span class="sxs-lookup"><span data-stu-id="3cac0-103">APIs to query Kaizala groups</span></span>
## <a name="groups"></a><span data-ttu-id="3cac0-104">/Groups</span><span class="sxs-lookup"><span data-stu-id="3cac0-104">/groups</span></span>
<span data-ttu-id="3cac0-105">Point de terminaison API pour interagir avec les groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="3cac0-105">API end-point to interact with the conversation groups inside Kaizala.</span></span>

### <a name="post-groups"></a><span data-ttu-id="3cac0-106">/Groups POST</span><span class="sxs-lookup"><span data-stu-id="3cac0-106">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

##### <a name="request-parameters"></a><span data-ttu-id="3cac0-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="3cac0-107">Request Parameters</span></span>

|  | <span data-ttu-id="3cac0-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-108">Parameter</span></span> | <span data-ttu-id="3cac0-109">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-109">Type</span></span> | <span data-ttu-id="3cac0-110">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3cac0-110">Optional?</span></span> | <span data-ttu-id="3cac0-111">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3cac0-112">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3cac0-112">HTTP Header</span></span> | <span data-ttu-id="3cac0-113">accessToken</span><span class="sxs-lookup"><span data-stu-id="3cac0-113">accessToken</span></span> | <span data-ttu-id="3cac0-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-114">String</span></span> | <span data-ttu-id="3cac0-115">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-115">No</span></span> | <span data-ttu-id="3cac0-116">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="3cac0-116">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="3cac0-117">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3cac0-117">HTTP Header</span></span> | <span data-ttu-id="3cac0-118">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-118">Content-Type</span></span> | <span data-ttu-id="3cac0-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-119">String</span></span> | <span data-ttu-id="3cac0-120">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-120">No</span></span> | <span data-ttu-id="3cac0-121">« application/json »</span><span class="sxs-lookup"><span data-stu-id="3cac0-121">"application/json"</span></span> |

##### <a name="request-body"></a><span data-ttu-id="3cac0-122">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="3cac0-122">Request body</span></span>

| <span data-ttu-id="3cac0-123">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-123">Parameter</span></span> | <span data-ttu-id="3cac0-124">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-124">Type</span></span> | <span data-ttu-id="3cac0-125">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3cac0-125">Optional?</span></span> | <span data-ttu-id="3cac0-126">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-126">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="3cac0-127">name</span><span class="sxs-lookup"><span data-stu-id="3cac0-127">name</span></span> | <span data-ttu-id="3cac0-128">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-128">String</span></span> | <span data-ttu-id="3cac0-129">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-129">No</span></span> | <span data-ttu-id="3cac0-130">Nom de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-130">Group name</span></span> |
| <span data-ttu-id="3cac0-131">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="3cac0-131">welcomeMessage</span></span> | <span data-ttu-id="3cac0-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-132">String</span></span> | <span data-ttu-id="3cac0-133">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-133">No</span></span> | <span data-ttu-id="3cac0-134">Message de bienvenue qui s’affiche à nouveau membre du groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-134">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="3cac0-135">membres</span><span class="sxs-lookup"><span data-stu-id="3cac0-135">members</span></span> | <span data-ttu-id="3cac0-136">String]</span><span class="sxs-lookup"><span data-stu-id="3cac0-136">String[]</span></span> | <span data-ttu-id="3cac0-137">Oui</span><span class="sxs-lookup"><span data-stu-id="3cac0-137">Yes</span></span> | <span data-ttu-id="3cac0-138">Numéro de Mobile (avec le code du pays) des membres à ajouter.</span><span class="sxs-lookup"><span data-stu-id="3cac0-138">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="3cac0-139">Valeur par défaut : Utilisateur du jeton d’accès sera ajouté en tant qu’administrateur du groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-139">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="3cac0-140">groupType</span><span class="sxs-lookup"><span data-stu-id="3cac0-140">groupType</span></span> | <span data-ttu-id="3cac0-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-141">String</span></span> | <span data-ttu-id="3cac0-142">Oui</span><span class="sxs-lookup"><span data-stu-id="3cac0-142">Yes</span></span> | <span data-ttu-id="3cac0-143">Enum : Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="3cac0-143">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="3cac0-144">ConnectGroup créera un groupe Public gérés.</span><span class="sxs-lookup"><span data-stu-id="3cac0-144">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="3cac0-145">Par défaut : groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-145">Default: Group</span></span> |

###### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="3cac0-146">Exemple de demande JSON pour créer le groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-146">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

##### <a name="response-body"></a><span data-ttu-id="3cac0-147">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3cac0-147">Response body</span></span>

| <span data-ttu-id="3cac0-148">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-148">Parameter</span></span> | <span data-ttu-id="3cac0-149">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-149">Type</span></span> | <span data-ttu-id="3cac0-150">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-150">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3cac0-151">groupName</span><span class="sxs-lookup"><span data-stu-id="3cac0-151">groupName</span></span> | <span data-ttu-id="3cac0-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-152">String</span></span> | <span data-ttu-id="3cac0-153">Nom de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-153">Group name</span></span> |
| <span data-ttu-id="3cac0-154">groupId</span><span class="sxs-lookup"><span data-stu-id="3cac0-154">groupId</span></span> | <span data-ttu-id="3cac0-155">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-155">String</span></span> | <span data-ttu-id="3cac0-156">Identificateur de groupe qui peut être utilisé dans les appels d’api suivants</span><span class="sxs-lookup"><span data-stu-id="3cac0-156">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="3cac0-157">membersAdded</span><span class="sxs-lookup"><span data-stu-id="3cac0-157">membersAdded</span></span> | <span data-ttu-id="3cac0-158">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-158">bool</span></span> | <span data-ttu-id="3cac0-159">True si tous les membres sont bien ajoutés</span><span class="sxs-lookup"><span data-stu-id="3cac0-159">True if all members are successfully added</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="3cac0-160">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="3cac0-160">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


### <a name="get-groups"></a><span data-ttu-id="3cac0-161">OBTENIR /groups</span><span class="sxs-lookup"><span data-stu-id="3cac0-161">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

##### <a name="request-parameters"></a><span data-ttu-id="3cac0-162">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="3cac0-162">Request Parameters</span></span>

|  | <span data-ttu-id="3cac0-163">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-163">Parameter</span></span> | <span data-ttu-id="3cac0-164">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-164">Type</span></span> | <span data-ttu-id="3cac0-165">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3cac0-165">Optional?</span></span> | <span data-ttu-id="3cac0-166">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-166">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3cac0-167">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3cac0-167">HTTP Header</span></span> | <span data-ttu-id="3cac0-168">accessToken</span><span class="sxs-lookup"><span data-stu-id="3cac0-168">accessToken</span></span> | <span data-ttu-id="3cac0-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-169">String</span></span> | <span data-ttu-id="3cac0-170">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-170">No</span></span> | <span data-ttu-id="3cac0-171">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="3cac0-171">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="3cac0-172">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="3cac0-172">Query parameter</span></span> | <span data-ttu-id="3cac0-173">showDetail</span><span class="sxs-lookup"><span data-stu-id="3cac0-173">showDetail</span></span> | <span data-ttu-id="3cac0-174">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-174">bool</span></span> | <span data-ttu-id="3cac0-175">Oui</span><span class="sxs-lookup"><span data-stu-id="3cac0-175">Yes</span></span> | <span data-ttu-id="3cac0-176">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="3cac0-176">Default: false.</span></span> <span data-ttu-id="3cac0-177">True pour renvoyer tous les détails du groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-177">True to return all group details</span></span> |
| <span data-ttu-id="3cac0-178">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="3cac0-178">Query parameter</span></span> | <span data-ttu-id="3cac0-179">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="3cac0-179">fetchAllGroups</span></span> | <span data-ttu-id="3cac0-180">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-180">bool</span></span> | <span data-ttu-id="3cac0-181">Oui</span><span class="sxs-lookup"><span data-stu-id="3cac0-181">Yes</span></span> | <span data-ttu-id="3cac0-182">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="3cac0-182">Default: false.</span></span> <span data-ttu-id="3cac0-183">True pour renvoyer tous les parents et sub groupes</span><span class="sxs-lookup"><span data-stu-id="3cac0-183">True to return all parent and sub groups</span></span> |

##### <a name="response-body"></a><span data-ttu-id="3cac0-184">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3cac0-184">Response body</span></span>

| <span data-ttu-id="3cac0-185">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-185">Parameter</span></span> | <span data-ttu-id="3cac0-186">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-186">Type</span></span> | <span data-ttu-id="3cac0-187">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3cac0-188">groupes</span><span class="sxs-lookup"><span data-stu-id="3cac0-188">groups</span></span> | <span data-ttu-id="3cac0-189">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="3cac0-189">JSON Object Array</span></span> | <span data-ttu-id="3cac0-190">Tableau de groupes que l’utilisateur a accès à avec l’accessToken</span><span class="sxs-lookup"><span data-stu-id="3cac0-190">Array of groups that the user has access to with the accessToken</span></span> |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="3cac0-191">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="3cac0-191">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="3cac0-192">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-192">Parameter</span></span> | <span data-ttu-id="3cac0-193">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-193">Type</span></span> | <span data-ttu-id="3cac0-194">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3cac0-195">groupId</span><span class="sxs-lookup"><span data-stu-id="3cac0-195">groupId</span></span> | <span data-ttu-id="3cac0-196">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-196">String</span></span> | <span data-ttu-id="3cac0-197">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-197">Group Identifier</span></span> |
| <span data-ttu-id="3cac0-198">groupName</span><span class="sxs-lookup"><span data-stu-id="3cac0-198">groupName</span></span> | <span data-ttu-id="3cac0-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-199">String</span></span> | <span data-ttu-id="3cac0-200">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-200">Name of the group</span></span> |
| <span data-ttu-id="3cac0-201">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="3cac0-201">groupImageURL</span></span> | <span data-ttu-id="3cac0-202">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-202">String</span></span> | <span data-ttu-id="3cac0-203">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-203">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="3cac0-204">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="3cac0-204">hasSubGroups</span></span> | <span data-ttu-id="3cac0-205">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-205">bool</span></span> | <span data-ttu-id="3cac0-206">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="3cac0-206">True if the group has subgroups</span></span> |
| <span data-ttu-id="3cac0-207">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="3cac0-207">hasParentGroups</span></span> | <span data-ttu-id="3cac0-208">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-208">bool</span></span> | <span data-ttu-id="3cac0-209">True si le groupe a groupes parents</span><span class="sxs-lookup"><span data-stu-id="3cac0-209">True if the group has parent groups</span></span> |
| <span data-ttu-id="3cac0-210">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="3cac0-210">isMappedToTenant</span></span> | <span data-ttu-id="3cac0-211">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-211">bool</span></span> | <span data-ttu-id="3cac0-212">True si le groupe est le groupe d’Organisation</span><span class="sxs-lookup"><span data-stu-id="3cac0-212">True if the group is Organisation group</span></span> |
| <span data-ttu-id="3cac0-213">groupType</span><span class="sxs-lookup"><span data-stu-id="3cac0-213">groupType</span></span> | <span data-ttu-id="3cac0-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-214">String</span></span> | <span data-ttu-id="3cac0-215">Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="3cac0-215">Group/ConnectGroup.</span></span> <span data-ttu-id="3cac0-216">ConnectGroup si le groupe dans le groupe Public gérés</span><span class="sxs-lookup"><span data-stu-id="3cac0-216">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="3cac0-217">userCount</span><span class="sxs-lookup"><span data-stu-id="3cac0-217">userCount</span></span> | <span data-ttu-id="3cac0-218">Numérique</span><span class="sxs-lookup"><span data-stu-id="3cac0-218">Numeric</span></span> | <span data-ttu-id="3cac0-219">Nombre total d’utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="3cac0-219">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="3cac0-220">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="3cac0-220">currentLevelUserCount</span></span> | <span data-ttu-id="3cac0-221">Numérique</span><span class="sxs-lookup"><span data-stu-id="3cac0-221">Numeric</span></span> | <span data-ttu-id="3cac0-222">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="3cac0-222">Total number of individual members of the group at the current level</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="3cac0-223">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="3cac0-223">Sample JSON Response</span></span>

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

### <a name="get-groupsgroupid"></a><span data-ttu-id="3cac0-224">OBTENIR /groups/ {groupId}</span><span class="sxs-lookup"><span data-stu-id="3cac0-224">GET /groups/{groupId}</span></span>

<span data-ttu-id="3cac0-225">Vous pouvez obtenir plus d’informations sur un membre de ressources spécifiques (groupe ici) en spécifiant l’identificateur comme un paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="3cac0-225">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

##### <a name="request-parameters"></a><span data-ttu-id="3cac0-226">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="3cac0-226">Request Parameters</span></span>

|  | <span data-ttu-id="3cac0-227">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-227">Parameter</span></span> | <span data-ttu-id="3cac0-228">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-228">Type</span></span> | <span data-ttu-id="3cac0-229">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="3cac0-229">Optional?</span></span> | <span data-ttu-id="3cac0-230">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-230">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="3cac0-231">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="3cac0-231">URL Path Parameter</span></span> | <span data-ttu-id="3cac0-232">groupId</span><span class="sxs-lookup"><span data-stu-id="3cac0-232">groupId</span></span> | <span data-ttu-id="3cac0-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-233">String</span></span> | <span data-ttu-id="3cac0-234">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-234">No</span></span> | <span data-ttu-id="3cac0-235">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="3cac0-235">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="3cac0-236">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="3cac0-236">HTTP Header</span></span> | <span data-ttu-id="3cac0-237">accessToken</span><span class="sxs-lookup"><span data-stu-id="3cac0-237">accessToken</span></span> | <span data-ttu-id="3cac0-238">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-238">String</span></span> | <span data-ttu-id="3cac0-239">Non</span><span class="sxs-lookup"><span data-stu-id="3cac0-239">No</span></span> | <span data-ttu-id="3cac0-240">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="3cac0-240">Access Token received from the auth end-point</span></span> |

##### <a name="response-body"></a><span data-ttu-id="3cac0-241">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3cac0-241">Response body</span></span>

| <span data-ttu-id="3cac0-242">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-242">Parameter</span></span> | <span data-ttu-id="3cac0-243">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-243">Type</span></span> | <span data-ttu-id="3cac0-244">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-244">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3cac0-245">groupes</span><span class="sxs-lookup"><span data-stu-id="3cac0-245">groups</span></span> | <span data-ttu-id="3cac0-246">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="3cac0-246">JSON Object Array</span></span> | <span data-ttu-id="3cac0-247">Tableau de groupes que l’utilisateur a accès à avec l’accessToken</span><span class="sxs-lookup"><span data-stu-id="3cac0-247">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="3cac0-248">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="3cac0-248">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="3cac0-249">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3cac0-249">Parameter</span></span> | <span data-ttu-id="3cac0-250">Type</span><span class="sxs-lookup"><span data-stu-id="3cac0-250">Type</span></span> | <span data-ttu-id="3cac0-251">Description</span><span class="sxs-lookup"><span data-stu-id="3cac0-251">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="3cac0-252">groupId</span><span class="sxs-lookup"><span data-stu-id="3cac0-252">groupId</span></span> | <span data-ttu-id="3cac0-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-253">String</span></span> | <span data-ttu-id="3cac0-254">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-254">Group Identifier</span></span> |
| <span data-ttu-id="3cac0-255">groupName</span><span class="sxs-lookup"><span data-stu-id="3cac0-255">groupName</span></span> | <span data-ttu-id="3cac0-256">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-256">String</span></span> | <span data-ttu-id="3cac0-257">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-257">Name of the group</span></span> |
| <span data-ttu-id="3cac0-258">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="3cac0-258">groupImageURL</span></span> | <span data-ttu-id="3cac0-259">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-259">String</span></span> | <span data-ttu-id="3cac0-260">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="3cac0-260">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="3cac0-261">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="3cac0-261">hasSubGroups</span></span> | <span data-ttu-id="3cac0-262">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-262">bool</span></span> | <span data-ttu-id="3cac0-263">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="3cac0-263">True if the group has subgroups</span></span> |
| <span data-ttu-id="3cac0-264">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="3cac0-264">hasParentGroups</span></span> | <span data-ttu-id="3cac0-265">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-265">bool</span></span> | <span data-ttu-id="3cac0-266">True si le groupe a groupes parents</span><span class="sxs-lookup"><span data-stu-id="3cac0-266">True if the group has parent groups</span></span> |
| <span data-ttu-id="3cac0-267">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="3cac0-267">isMappedToTenant</span></span> | <span data-ttu-id="3cac0-268">bool</span><span class="sxs-lookup"><span data-stu-id="3cac0-268">bool</span></span> | <span data-ttu-id="3cac0-269">True si le groupe est le groupe d’Organisation</span><span class="sxs-lookup"><span data-stu-id="3cac0-269">True if the group is Organisation group</span></span> |
| <span data-ttu-id="3cac0-270">groupType</span><span class="sxs-lookup"><span data-stu-id="3cac0-270">groupType</span></span> | <span data-ttu-id="3cac0-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3cac0-271">String</span></span> | <span data-ttu-id="3cac0-272">Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="3cac0-272">Group/ConnectGroup.</span></span> <span data-ttu-id="3cac0-273">ConnectGroup si le groupe dans le groupe Public gérés</span><span class="sxs-lookup"><span data-stu-id="3cac0-273">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="3cac0-274">userCount</span><span class="sxs-lookup"><span data-stu-id="3cac0-274">userCount</span></span> | <span data-ttu-id="3cac0-275">Numérique</span><span class="sxs-lookup"><span data-stu-id="3cac0-275">Numeric</span></span> | <span data-ttu-id="3cac0-276">Nombre total d’utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="3cac0-276">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="3cac0-277">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="3cac0-277">currentLevelUserCount</span></span> | <span data-ttu-id="3cac0-278">Numérique</span><span class="sxs-lookup"><span data-stu-id="3cac0-278">Numeric</span></span> | <span data-ttu-id="3cac0-279">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="3cac0-279">Total number of individual members of the group at the current level</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="3cac0-280">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="3cac0-280">Sample JSON Response</span></span>

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

