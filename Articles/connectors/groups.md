---
title: /Groups
description: Article de référence de l’API pour interroger les données de groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399372"
---
# <a name="groups"></a><span data-ttu-id="ceff4-103">/Groups</span><span class="sxs-lookup"><span data-stu-id="ceff4-103">/groups</span></span>
<span data-ttu-id="ceff4-104">Point de terminaison API pour interagir avec les groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="ceff4-104">API end-point to interact with the conversation groups inside Kaizala.</span></span>

## <a name="post-groups"></a><span data-ttu-id="ceff4-105">/Groups POST</span><span class="sxs-lookup"><span data-stu-id="ceff4-105">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="ceff4-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ceff4-106">Request Parameters</span></span>

|  | <span data-ttu-id="ceff4-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-107">Parameter</span></span> | <span data-ttu-id="ceff4-108">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-108">Type</span></span> | <span data-ttu-id="ceff4-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="ceff4-109">Optional?</span></span> | <span data-ttu-id="ceff4-110">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ceff4-111">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ceff4-111">HTTP Header</span></span> | <span data-ttu-id="ceff4-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="ceff4-112">accessToken</span></span> | <span data-ttu-id="ceff4-113">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-113">String</span></span> | <span data-ttu-id="ceff4-114">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-114">No</span></span> | <span data-ttu-id="ceff4-115">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="ceff4-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="ceff4-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ceff4-116">HTTP Header</span></span> | <span data-ttu-id="ceff4-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-117">Content-Type</span></span> | <span data-ttu-id="ceff4-118">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-118">String</span></span> | <span data-ttu-id="ceff4-119">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-119">No</span></span> | <span data-ttu-id="ceff4-120">« application/json »</span><span class="sxs-lookup"><span data-stu-id="ceff4-120">"application/json"</span></span> |

### <a name="request-body"></a><span data-ttu-id="ceff4-121">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="ceff4-121">Request body</span></span>

| <span data-ttu-id="ceff4-122">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-122">Parameter</span></span> | <span data-ttu-id="ceff4-123">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-123">Type</span></span> | <span data-ttu-id="ceff4-124">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="ceff4-124">Optional?</span></span> | <span data-ttu-id="ceff4-125">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-125">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="ceff4-126">name</span><span class="sxs-lookup"><span data-stu-id="ceff4-126">name</span></span> | <span data-ttu-id="ceff4-127">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-127">String</span></span> | <span data-ttu-id="ceff4-128">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-128">No</span></span> | <span data-ttu-id="ceff4-129">Nom de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-129">Group name</span></span> |
| <span data-ttu-id="ceff4-130">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="ceff4-130">welcomeMessage</span></span> | <span data-ttu-id="ceff4-131">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-131">String</span></span> | <span data-ttu-id="ceff4-132">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-132">No</span></span> | <span data-ttu-id="ceff4-133">Message de bienvenue qui s’affiche à nouveau membre du groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-133">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="ceff4-134">membres</span><span class="sxs-lookup"><span data-stu-id="ceff4-134">members</span></span> | <span data-ttu-id="ceff4-135">String]</span><span class="sxs-lookup"><span data-stu-id="ceff4-135">String[]</span></span> | <span data-ttu-id="ceff4-136">Oui</span><span class="sxs-lookup"><span data-stu-id="ceff4-136">Yes</span></span> | <span data-ttu-id="ceff4-137">Numéro de Mobile (avec le code du pays) des membres à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ceff4-137">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="ceff4-138">Valeur par défaut : Utilisateur du jeton d’accès sera ajouté en tant qu’administrateur du groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-138">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="ceff4-139">groupType</span><span class="sxs-lookup"><span data-stu-id="ceff4-139">groupType</span></span> | <span data-ttu-id="ceff4-140">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-140">String</span></span> | <span data-ttu-id="ceff4-141">Oui</span><span class="sxs-lookup"><span data-stu-id="ceff4-141">Yes</span></span> | <span data-ttu-id="ceff4-142">Enum : Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="ceff4-142">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="ceff4-143">ConnectGroup créera un groupe Public gérés.</span><span class="sxs-lookup"><span data-stu-id="ceff4-143">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="ceff4-144">Par défaut : groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-144">Default: Group</span></span> |

#### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="ceff4-145">Exemple de demande JSON pour créer le groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-145">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a><span data-ttu-id="ceff4-146">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ceff4-146">Response body</span></span>

| <span data-ttu-id="ceff4-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-147">Parameter</span></span> | <span data-ttu-id="ceff4-148">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-148">Type</span></span> | <span data-ttu-id="ceff4-149">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ceff4-150">groupName</span><span class="sxs-lookup"><span data-stu-id="ceff4-150">groupName</span></span> | <span data-ttu-id="ceff4-151">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-151">String</span></span> | <span data-ttu-id="ceff4-152">Nom de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-152">Group name</span></span> |
| <span data-ttu-id="ceff4-153">groupId</span><span class="sxs-lookup"><span data-stu-id="ceff4-153">groupId</span></span> | <span data-ttu-id="ceff4-154">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-154">String</span></span> | <span data-ttu-id="ceff4-155">Identificateur de groupe qui peut être utilisé dans les appels d’api suivants</span><span class="sxs-lookup"><span data-stu-id="ceff4-155">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="ceff4-156">membersAdded</span><span class="sxs-lookup"><span data-stu-id="ceff4-156">membersAdded</span></span> | <span data-ttu-id="ceff4-157">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-157">bool</span></span> | <span data-ttu-id="ceff4-158">True si tous les membres sont bien ajoutés</span><span class="sxs-lookup"><span data-stu-id="ceff4-158">True if all members are successfully added</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ceff4-159">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ceff4-159">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a><span data-ttu-id="ceff4-160">OBTENIR /groups</span><span class="sxs-lookup"><span data-stu-id="ceff4-160">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="ceff4-161">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ceff4-161">Request Parameters</span></span>

|  | <span data-ttu-id="ceff4-162">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-162">Parameter</span></span> | <span data-ttu-id="ceff4-163">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-163">Type</span></span> | <span data-ttu-id="ceff4-164">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="ceff4-164">Optional?</span></span> | <span data-ttu-id="ceff4-165">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ceff4-166">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ceff4-166">HTTP Header</span></span> | <span data-ttu-id="ceff4-167">accessToken</span><span class="sxs-lookup"><span data-stu-id="ceff4-167">accessToken</span></span> | <span data-ttu-id="ceff4-168">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-168">String</span></span> | <span data-ttu-id="ceff4-169">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-169">No</span></span> | <span data-ttu-id="ceff4-170">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="ceff4-170">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="ceff4-171">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="ceff4-171">Query parameter</span></span> | <span data-ttu-id="ceff4-172">showDetail</span><span class="sxs-lookup"><span data-stu-id="ceff4-172">showDetail</span></span> | <span data-ttu-id="ceff4-173">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-173">bool</span></span> | <span data-ttu-id="ceff4-174">Oui</span><span class="sxs-lookup"><span data-stu-id="ceff4-174">Yes</span></span> | <span data-ttu-id="ceff4-175">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="ceff4-175">Default: false.</span></span> <span data-ttu-id="ceff4-176">True pour renvoyer tous les détails du groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-176">True to return all group details</span></span> |
| <span data-ttu-id="ceff4-177">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="ceff4-177">Query parameter</span></span> | <span data-ttu-id="ceff4-178">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="ceff4-178">fetchAllGroups</span></span> | <span data-ttu-id="ceff4-179">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-179">bool</span></span> | <span data-ttu-id="ceff4-180">Oui</span><span class="sxs-lookup"><span data-stu-id="ceff4-180">Yes</span></span> | <span data-ttu-id="ceff4-181">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="ceff4-181">Default: false.</span></span> <span data-ttu-id="ceff4-182">True pour renvoyer tous les parents et sub groupes</span><span class="sxs-lookup"><span data-stu-id="ceff4-182">True to return all parent and sub groups</span></span> |

### <a name="response-body"></a><span data-ttu-id="ceff4-183">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ceff4-183">Response body</span></span>

| <span data-ttu-id="ceff4-184">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-184">Parameter</span></span> | <span data-ttu-id="ceff4-185">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-185">Type</span></span> | <span data-ttu-id="ceff4-186">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ceff4-187">groupes</span><span class="sxs-lookup"><span data-stu-id="ceff4-187">groups</span></span> | <span data-ttu-id="ceff4-188">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="ceff4-188">JSON Object Array</span></span> | <span data-ttu-id="ceff4-189">Tableau de groupes que l’utilisateur a accès à avec l’accessToken</span><span class="sxs-lookup"><span data-stu-id="ceff4-189">Array of groups that the user has access to with the accessToken</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="ceff4-190">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="ceff4-190">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="ceff4-191">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-191">Parameter</span></span> | <span data-ttu-id="ceff4-192">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-192">Type</span></span> | <span data-ttu-id="ceff4-193">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ceff4-194">groupId</span><span class="sxs-lookup"><span data-stu-id="ceff4-194">groupId</span></span> | <span data-ttu-id="ceff4-195">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-195">String</span></span> | <span data-ttu-id="ceff4-196">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-196">Group Identifier</span></span> |
| <span data-ttu-id="ceff4-197">groupName</span><span class="sxs-lookup"><span data-stu-id="ceff4-197">groupName</span></span> | <span data-ttu-id="ceff4-198">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-198">String</span></span> | <span data-ttu-id="ceff4-199">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-199">Name of the group</span></span> |
| <span data-ttu-id="ceff4-200">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="ceff4-200">groupImageURL</span></span> | <span data-ttu-id="ceff4-201">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-201">String</span></span> | <span data-ttu-id="ceff4-202">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-202">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="ceff4-203">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="ceff4-203">hasSubGroups</span></span> | <span data-ttu-id="ceff4-204">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-204">bool</span></span> | <span data-ttu-id="ceff4-205">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="ceff4-205">True if the group has subgroups</span></span> |
| <span data-ttu-id="ceff4-206">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="ceff4-206">hasParentGroups</span></span> | <span data-ttu-id="ceff4-207">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-207">bool</span></span> | <span data-ttu-id="ceff4-208">True si le groupe a groupes parents</span><span class="sxs-lookup"><span data-stu-id="ceff4-208">True if the group has parent groups</span></span> |
| <span data-ttu-id="ceff4-209">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="ceff4-209">isMappedToTenant</span></span> | <span data-ttu-id="ceff4-210">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-210">bool</span></span> | <span data-ttu-id="ceff4-211">True si le groupe est le groupe d’Organisation</span><span class="sxs-lookup"><span data-stu-id="ceff4-211">True if the group is Organisation group</span></span> |
| <span data-ttu-id="ceff4-212">groupType</span><span class="sxs-lookup"><span data-stu-id="ceff4-212">groupType</span></span> | <span data-ttu-id="ceff4-213">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-213">String</span></span> | <span data-ttu-id="ceff4-214">Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="ceff4-214">Group/ConnectGroup.</span></span> <span data-ttu-id="ceff4-215">ConnectGroup si le groupe dans le groupe Public gérés</span><span class="sxs-lookup"><span data-stu-id="ceff4-215">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="ceff4-216">userCount</span><span class="sxs-lookup"><span data-stu-id="ceff4-216">userCount</span></span> | <span data-ttu-id="ceff4-217">Numérique</span><span class="sxs-lookup"><span data-stu-id="ceff4-217">Numeric</span></span> | <span data-ttu-id="ceff4-218">Nombre total d’utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="ceff4-218">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="ceff4-219">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="ceff4-219">currentLevelUserCount</span></span> | <span data-ttu-id="ceff4-220">Numérique</span><span class="sxs-lookup"><span data-stu-id="ceff4-220">Numeric</span></span> | <span data-ttu-id="ceff4-221">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="ceff4-221">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ceff4-222">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ceff4-222">Sample JSON Response</span></span>

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

## <a name="get-groupsgroupid"></a><span data-ttu-id="ceff4-223">OBTENIR /groups/ {groupId}</span><span class="sxs-lookup"><span data-stu-id="ceff4-223">GET /groups/{groupId}</span></span>

<span data-ttu-id="ceff4-224">Vous pouvez obtenir plus d’informations sur un membre de ressources spécifiques (groupe ici) en spécifiant l’identificateur comme un paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="ceff4-224">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a><span data-ttu-id="ceff4-225">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="ceff4-225">Request Parameters</span></span>

|  | <span data-ttu-id="ceff4-226">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-226">Parameter</span></span> | <span data-ttu-id="ceff4-227">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-227">Type</span></span> | <span data-ttu-id="ceff4-228">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="ceff4-228">Optional?</span></span> | <span data-ttu-id="ceff4-229">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-229">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="ceff4-230">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="ceff4-230">URL Path Parameter</span></span> | <span data-ttu-id="ceff4-231">groupId</span><span class="sxs-lookup"><span data-stu-id="ceff4-231">groupId</span></span> | <span data-ttu-id="ceff4-232">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-232">String</span></span> | <span data-ttu-id="ceff4-233">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-233">No</span></span> | <span data-ttu-id="ceff4-234">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="ceff4-234">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="ceff4-235">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="ceff4-235">HTTP Header</span></span> | <span data-ttu-id="ceff4-236">accessToken</span><span class="sxs-lookup"><span data-stu-id="ceff4-236">accessToken</span></span> | <span data-ttu-id="ceff4-237">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-237">String</span></span> | <span data-ttu-id="ceff4-238">Non</span><span class="sxs-lookup"><span data-stu-id="ceff4-238">No</span></span> | <span data-ttu-id="ceff4-239">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="ceff4-239">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="ceff4-240">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="ceff4-240">Response body</span></span>

| <span data-ttu-id="ceff4-241">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-241">Parameter</span></span> | <span data-ttu-id="ceff4-242">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-242">Type</span></span> | <span data-ttu-id="ceff4-243">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ceff4-244">groupes</span><span class="sxs-lookup"><span data-stu-id="ceff4-244">groups</span></span> | <span data-ttu-id="ceff4-245">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="ceff4-245">JSON Object Array</span></span> | <span data-ttu-id="ceff4-246">Tableau de groupes que l’utilisateur a accès à avec l’accessToken</span><span class="sxs-lookup"><span data-stu-id="ceff4-246">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="ceff4-247">Structure de JSON pour chaque groupe individuel dans le tableau groupes [] :</span><span class="sxs-lookup"><span data-stu-id="ceff4-247">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="ceff4-248">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ceff4-248">Parameter</span></span> | <span data-ttu-id="ceff4-249">Type</span><span class="sxs-lookup"><span data-stu-id="ceff4-249">Type</span></span> | <span data-ttu-id="ceff4-250">Description</span><span class="sxs-lookup"><span data-stu-id="ceff4-250">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="ceff4-251">groupId</span><span class="sxs-lookup"><span data-stu-id="ceff4-251">groupId</span></span> | <span data-ttu-id="ceff4-252">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-252">String</span></span> | <span data-ttu-id="ceff4-253">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-253">Group Identifier</span></span> |
| <span data-ttu-id="ceff4-254">groupName</span><span class="sxs-lookup"><span data-stu-id="ceff4-254">groupName</span></span> | <span data-ttu-id="ceff4-255">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-255">String</span></span> | <span data-ttu-id="ceff4-256">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-256">Name of the group</span></span> |
| <span data-ttu-id="ceff4-257">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="ceff4-257">groupImageURL</span></span> | <span data-ttu-id="ceff4-258">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-258">String</span></span> | <span data-ttu-id="ceff4-259">Chaîne spécifiant l’URL de l’image de profil de groupe</span><span class="sxs-lookup"><span data-stu-id="ceff4-259">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="ceff4-260">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="ceff4-260">hasSubGroups</span></span> | <span data-ttu-id="ceff4-261">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-261">bool</span></span> | <span data-ttu-id="ceff4-262">True si le groupe a des sous-groupes</span><span class="sxs-lookup"><span data-stu-id="ceff4-262">True if the group has subgroups</span></span> |
| <span data-ttu-id="ceff4-263">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="ceff4-263">hasParentGroups</span></span> | <span data-ttu-id="ceff4-264">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-264">bool</span></span> | <span data-ttu-id="ceff4-265">True si le groupe a groupes parents</span><span class="sxs-lookup"><span data-stu-id="ceff4-265">True if the group has parent groups</span></span> |
| <span data-ttu-id="ceff4-266">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="ceff4-266">isMappedToTenant</span></span> | <span data-ttu-id="ceff4-267">bool</span><span class="sxs-lookup"><span data-stu-id="ceff4-267">bool</span></span> | <span data-ttu-id="ceff4-268">True si le groupe est le groupe d’Organisation</span><span class="sxs-lookup"><span data-stu-id="ceff4-268">True if the group is Organisation group</span></span> |
| <span data-ttu-id="ceff4-269">groupType</span><span class="sxs-lookup"><span data-stu-id="ceff4-269">groupType</span></span> | <span data-ttu-id="ceff4-270">String</span><span class="sxs-lookup"><span data-stu-id="ceff4-270">String</span></span> | <span data-ttu-id="ceff4-271">Groupe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="ceff4-271">Group/ConnectGroup.</span></span> <span data-ttu-id="ceff4-272">ConnectGroup si le groupe dans le groupe Public gérés</span><span class="sxs-lookup"><span data-stu-id="ceff4-272">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="ceff4-273">userCount</span><span class="sxs-lookup"><span data-stu-id="ceff4-273">userCount</span></span> | <span data-ttu-id="ceff4-274">Numérique</span><span class="sxs-lookup"><span data-stu-id="ceff4-274">Numeric</span></span> | <span data-ttu-id="ceff4-275">Nombre total d’utilisateurs sous ce groupe dans la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="ceff4-275">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="ceff4-276">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="ceff4-276">currentLevelUserCount</span></span> | <span data-ttu-id="ceff4-277">Numérique</span><span class="sxs-lookup"><span data-stu-id="ceff4-277">Numeric</span></span> | <span data-ttu-id="ceff4-278">Nombre total de membres individuels du groupe au niveau actuel</span><span class="sxs-lookup"><span data-stu-id="ceff4-278">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="ceff4-279">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="ceff4-279">Sample JSON Response</span></span>

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

