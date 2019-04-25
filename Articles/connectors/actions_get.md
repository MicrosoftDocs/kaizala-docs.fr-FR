---
title: /actions
description: Article de référence pour l'API permettant d'obtenir la liste des actions dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190719"
---
# <a name="get-list-of-actions-in-a-group"></a><span data-ttu-id="1e10e-103">Obtenir la liste des actions dans un groupe</span><span class="sxs-lookup"><span data-stu-id="1e10e-103">Get list of Actions in a group</span></span>
## <a name="get-actions"></a><span data-ttu-id="1e10e-104">OBTENIR/actions</span><span class="sxs-lookup"><span data-stu-id="1e10e-104">GET /actions</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a><span data-ttu-id="1e10e-105">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="1e10e-105">Request Parameters</span></span>

|  | <span data-ttu-id="1e10e-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-106">Parameter</span></span> | <span data-ttu-id="1e10e-107">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-107">Type</span></span> | <span data-ttu-id="1e10e-108">Module?</span><span class="sxs-lookup"><span data-stu-id="1e10e-108">Optional?</span></span> | <span data-ttu-id="1e10e-109">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="1e10e-110">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="1e10e-110">URL Path Parameter</span></span> | <span data-ttu-id="1e10e-111">groupId</span><span class="sxs-lookup"><span data-stu-id="1e10e-111">groupId</span></span> | <span data-ttu-id="1e10e-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-112">String</span></span> | <span data-ttu-id="1e10e-113">Non</span><span class="sxs-lookup"><span data-stu-id="1e10e-113">No</span></span> | <span data-ttu-id="1e10e-114">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="1e10e-114">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="1e10e-115">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1e10e-115">HTTP Header</span></span> | <span data-ttu-id="1e10e-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="1e10e-116">accessToken</span></span> | <span data-ttu-id="1e10e-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-117">String</span></span> | <span data-ttu-id="1e10e-118">Non</span><span class="sxs-lookup"><span data-stu-id="1e10e-118">No</span></span> | <span data-ttu-id="1e10e-119">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="1e10e-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="1e10e-120">Paramètre de requête d'URL</span><span class="sxs-lookup"><span data-stu-id="1e10e-120">URL Query Parameter</span></span> | <span data-ttu-id="1e10e-121">actionType</span><span class="sxs-lookup"><span data-stu-id="1e10e-121">actionType</span></span> | <span data-ttu-id="1e10e-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-122">String</span></span> | <span data-ttu-id="1e10e-123">Non</span><span class="sxs-lookup"><span data-stu-id="1e10e-123">No</span></span> | <span data-ttu-id="1e10e-124">Type d'action à récupérer</span><span class="sxs-lookup"><span data-stu-id="1e10e-124">Type of action to retrieve</span></span> |
| <span data-ttu-id="1e10e-125">Paramètre de requête d'URL</span><span class="sxs-lookup"><span data-stu-id="1e10e-125">URL Query Parameter</span></span> | <span data-ttu-id="1e10e-126">fromDate</span><span class="sxs-lookup"><span data-stu-id="1e10e-126">fromDate</span></span> | <span data-ttu-id="1e10e-127">Date/heure (époque)</span><span class="sxs-lookup"><span data-stu-id="1e10e-127">DateTime (epoch time)</span></span> | <span data-ttu-id="1e10e-128">Oui</span><span class="sxs-lookup"><span data-stu-id="1e10e-128">Yes</span></span> | <span data-ttu-id="1e10e-129">Heure à partir de laquelle les actions doivent être récupérées</span><span class="sxs-lookup"><span data-stu-id="1e10e-129">Time from which the actions need to be retrieved</span></span> |
| <span data-ttu-id="1e10e-130">Paramètre de requête d'URL</span><span class="sxs-lookup"><span data-stu-id="1e10e-130">URL Query Parameter</span></span> | <span data-ttu-id="1e10e-131">count</span><span class="sxs-lookup"><span data-stu-id="1e10e-131">count</span></span> | <span data-ttu-id="1e10e-132">number</span><span class="sxs-lookup"><span data-stu-id="1e10e-132">number</span></span> | <span data-ttu-id="1e10e-133">Oui</span><span class="sxs-lookup"><span data-stu-id="1e10e-133">Yes</span></span> | <span data-ttu-id="1e10e-134">Nombre d'actions individuelles à renvoyer; Valeur par défaut = 30</span><span class="sxs-lookup"><span data-stu-id="1e10e-134">Count of individual actions to be returned; Default = 30</span></span> |

### <a name="response-body"></a><span data-ttu-id="1e10e-135">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="1e10e-135">Response body</span></span>

| <span data-ttu-id="1e10e-136">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-136">Parameter</span></span> | <span data-ttu-id="1e10e-137">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-137">Type</span></span> | <span data-ttu-id="1e10e-138">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-138">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-139">actions</span><span class="sxs-lookup"><span data-stu-id="1e10e-139">actions</span></span> | <span data-ttu-id="1e10e-140">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="1e10e-140">JSON Object Array</span></span> | <span data-ttu-id="1e10e-141">Tableau d'objets action</span><span class="sxs-lookup"><span data-stu-id="1e10e-141">Array of action objects</span></span> |
| <span data-ttu-id="1e10e-142">hasMore</span><span class="sxs-lookup"><span data-stu-id="1e10e-142">hasMore</span></span> | <span data-ttu-id="1e10e-143">booléen</span><span class="sxs-lookup"><span data-stu-id="1e10e-143">boolean</span></span> | <span data-ttu-id="1e10e-144">Si le nombre maximal d'actions par réponse est atteint, cette variable sera définie sur true.</span><span class="sxs-lookup"><span data-stu-id="1e10e-144">If the max count of actions per response has reached, this variable will be set to true</span></span> |

<span data-ttu-id="1e10e-145">Structure JSON pour chaque action individuelle dans les actions de tableau []:</span><span class="sxs-lookup"><span data-stu-id="1e10e-145">JSON structure for each individual action in the array actions[]:</span></span>

| <span data-ttu-id="1e10e-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-146">Parameter</span></span> | <span data-ttu-id="1e10e-147">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-147">Type</span></span> | <span data-ttu-id="1e10e-148">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-149">ID</span><span class="sxs-lookup"><span data-stu-id="1e10e-149">referenceId</span></span> | <span data-ttu-id="1e10e-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-150">String</span></span> | <span data-ttu-id="1e10e-151">ID pour le message</span><span class="sxs-lookup"><span data-stu-id="1e10e-151">referenceID for the message</span></span> |
| <span data-ttu-id="1e10e-152">actionType</span><span class="sxs-lookup"><span data-stu-id="1e10e-152">actionType</span></span> | <span data-ttu-id="1e10e-153">String</span><span class="sxs-lookup"><span data-stu-id="1e10e-153">String</span></span> | <span data-ttu-id="1e10e-154">Type d'action retourné</span><span class="sxs-lookup"><span data-stu-id="1e10e-154">Type of action being returned</span></span> |
| <span data-ttu-id="1e10e-155">actionBody</span><span class="sxs-lookup"><span data-stu-id="1e10e-155">actionBody</span></span> | <span data-ttu-id="1e10e-156">Tableau d'objets JSON propre au ActionType</span><span class="sxs-lookup"><span data-stu-id="1e10e-156">JSON object array specific to the actiontype</span></span> | <span data-ttu-id="1e10e-157">Tableau avec des objets spécifiques au ActionType</span><span class="sxs-lookup"><span data-stu-id="1e10e-157">Array with objects specific to the actiontype</span></span> |
| <span data-ttu-id="1e10e-158">expéditeur</span><span class="sxs-lookup"><span data-stu-id="1e10e-158">sender</span></span> | <span data-ttu-id="1e10e-159">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-159">String</span></span> | <span data-ttu-id="1e10e-160">Numéro de téléphone de l'utilisateur qui a envoyé l'action au groupe</span><span class="sxs-lookup"><span data-stu-id="1e10e-160">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="1e10e-161">sentAt</span><span class="sxs-lookup"><span data-stu-id="1e10e-161">sentAt</span></span> | <span data-ttu-id="1e10e-162">DateTime
</span><span class="sxs-lookup"><span data-stu-id="1e10e-162">DateTime</span></span> | <span data-ttu-id="1e10e-163">Heure à laquelle l'action a été publiée dans le groupe</span><span class="sxs-lookup"><span data-stu-id="1e10e-163">Time when the action was posted to the group</span></span> |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a><span data-ttu-id="1e10e-164">structure d'objet actionBody pour la pièce jointe image/image:</span><span class="sxs-lookup"><span data-stu-id="1e10e-164">actionBody object structure for image/picture attachment:</span></span>

| <span data-ttu-id="1e10e-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-165">Parameter</span></span> | <span data-ttu-id="1e10e-166">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-166">Type</span></span> | <span data-ttu-id="1e10e-167">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-168">imageURL</span><span class="sxs-lookup"><span data-stu-id="1e10e-168">imageURL</span></span> | <span data-ttu-id="1e10e-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-169">String</span></span> | <span data-ttu-id="1e10e-170">Chaîne de l'URL de l'image</span><span class="sxs-lookup"><span data-stu-id="1e10e-170">URL string for the picture</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-171">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-171">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "8a93c6cc-8499-44b0-aa54-016648100080",
      "actionType": "Image",
      "sender": "+9196500000",
      "creationTime": 1481180806,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg"
      }
    }
]
}
```

####  <a name="actionbody-object-structure-for-the-action-share-location"></a><span data-ttu-id="1e10e-172">structure d'objet actionBody pour l'action «emplacement de partage»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-172">actionBody object structure for the action 'Share Location':</span></span>

| <span data-ttu-id="1e10e-173">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-173">Parameter</span></span> | <span data-ttu-id="1e10e-174">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-174">Type</span></span> | <span data-ttu-id="1e10e-175">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-176">latitude</span><span class="sxs-lookup"><span data-stu-id="1e10e-176">latitude</span></span> | <span data-ttu-id="1e10e-177">Double</span><span class="sxs-lookup"><span data-stu-id="1e10e-177">Double</span></span> | <span data-ttu-id="1e10e-178">Coordonnées latitude de l'emplacement</span><span class="sxs-lookup"><span data-stu-id="1e10e-178">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="1e10e-179">longitude</span><span class="sxs-lookup"><span data-stu-id="1e10e-179">longitude</span></span> | <span data-ttu-id="1e10e-180">Double</span><span class="sxs-lookup"><span data-stu-id="1e10e-180">Double</span></span> | <span data-ttu-id="1e10e-181">Coordonnées de longitude de l'emplacement</span><span class="sxs-lookup"><span data-stu-id="1e10e-181">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-182">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-182">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a><span data-ttu-id="1e10e-183">structure d'objet actionBody pour l'action «photo avec emplacement»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-183">actionBody object structure for the action 'Photo with Location':</span></span>

| <span data-ttu-id="1e10e-184">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-184">Parameter</span></span> | <span data-ttu-id="1e10e-185">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-185">Type</span></span> | <span data-ttu-id="1e10e-186">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-187">imageURL</span><span class="sxs-lookup"><span data-stu-id="1e10e-187">imageURL</span></span> | <span data-ttu-id="1e10e-188">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-188">String</span></span> | <span data-ttu-id="1e10e-189">Chaîne de l'URL de l'image</span><span class="sxs-lookup"><span data-stu-id="1e10e-189">URL string for the picture</span></span> |
| <span data-ttu-id="1e10e-190">latitude</span><span class="sxs-lookup"><span data-stu-id="1e10e-190">latitude</span></span> | <span data-ttu-id="1e10e-191">Double</span><span class="sxs-lookup"><span data-stu-id="1e10e-191">Double</span></span> | <span data-ttu-id="1e10e-192">Coordonnées latitude de l'emplacement</span><span class="sxs-lookup"><span data-stu-id="1e10e-192">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="1e10e-193">longitude</span><span class="sxs-lookup"><span data-stu-id="1e10e-193">longitude</span></span> | <span data-ttu-id="1e10e-194">Double</span><span class="sxs-lookup"><span data-stu-id="1e10e-194">Double</span></span> | <span data-ttu-id="1e10e-195">Coordonnées de longitude de l'emplacement</span><span class="sxs-lookup"><span data-stu-id="1e10e-195">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-196">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-196">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg",
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

####  <a name="actionbody-object-structure-for-the-action-job"></a><span data-ttu-id="1e10e-197">structure d'objet actionBody pour l'action «Job»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-197">actionBody object structure for the action 'Job':</span></span>

| <span data-ttu-id="1e10e-198">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-198">Parameter</span></span> | <span data-ttu-id="1e10e-199">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-199">Type</span></span> | <span data-ttu-id="1e10e-200">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-201">actionId</span><span class="sxs-lookup"><span data-stu-id="1e10e-201">actionId</span></span> | <span data-ttu-id="1e10e-202">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-202">String</span></span> | <span data-ttu-id="1e10e-203">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="1e10e-203">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="1e10e-204">title</span><span class="sxs-lookup"><span data-stu-id="1e10e-204">title</span></span> | <span data-ttu-id="1e10e-205">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-205">String</span></span> | <span data-ttu-id="1e10e-206">Titre du travail</span><span class="sxs-lookup"><span data-stu-id="1e10e-206">Title of the Job</span></span> |
| <span data-ttu-id="1e10e-207">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="1e10e-207">assigneeCount</span></span> | <span data-ttu-id="1e10e-208">Numérique</span><span class="sxs-lookup"><span data-stu-id="1e10e-208">Numeric</span></span> | <span data-ttu-id="1e10e-209">Nombre de personnes affectées</span><span class="sxs-lookup"><span data-stu-id="1e10e-209">Number of assignees</span></span> |
| <span data-ttu-id="1e10e-210">responseCount</span><span class="sxs-lookup"><span data-stu-id="1e10e-210">responseCount</span></span> | <span data-ttu-id="1e10e-211">Numérique</span><span class="sxs-lookup"><span data-stu-id="1e10e-211">Numeric</span></span> | <span data-ttu-id="1e10e-212">Nombre d'utilisateurs ayant marqué le travail comme terminé</span><span class="sxs-lookup"><span data-stu-id="1e10e-212">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="1e10e-213">isCompleted</span><span class="sxs-lookup"><span data-stu-id="1e10e-213">isCompleted</span></span> | <span data-ttu-id="1e10e-214">Booléen</span><span class="sxs-lookup"><span data-stu-id="1e10e-214">Boolean</span></span> | <span data-ttu-id="1e10e-215">True lorsque tous les utilisateurs ont effectué le travail</span><span class="sxs-lookup"><span data-stu-id="1e10e-215">True when all assignees have completed the job</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-216">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-216">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3214841c-eaa2-4bf3-a583-acc69d9279c4",
      "actionType": "Job",
      "sender": "+919910005",
      "creationTime": 1481179788,
      "actionBody": {
        "actionId": "f260dc09-f1f3-4305-84f6-6edbedb82fb7",
        "title": "Test",
        "assigneeCount": 1,
        "responseCount": 0,
        "isCompleted": false
      }
    }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-poll"></a><span data-ttu-id="1e10e-217">structure d'objet actionBody pour l'action «Poll»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-217">actionBody object structure for the action 'Poll':</span></span>

| <span data-ttu-id="1e10e-218">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-218">Parameter</span></span> | <span data-ttu-id="1e10e-219">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-219">Type</span></span> | <span data-ttu-id="1e10e-220">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-220">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-221">actionId</span><span class="sxs-lookup"><span data-stu-id="1e10e-221">actionId</span></span> | <span data-ttu-id="1e10e-222">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-222">String</span></span> | <span data-ttu-id="1e10e-223">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="1e10e-223">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="1e10e-224">relative</span><span class="sxs-lookup"><span data-stu-id="1e10e-224">question</span></span> | <span data-ttu-id="1e10e-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-225">String</span></span> | <span data-ttu-id="1e10e-226">Question de sondage</span><span class="sxs-lookup"><span data-stu-id="1e10e-226">Poll Question</span></span> |
| <span data-ttu-id="1e10e-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="1e10e-227">isSenderOnly</span></span> | <span data-ttu-id="1e10e-228">Booléen</span><span class="sxs-lookup"><span data-stu-id="1e10e-228">Boolean</span></span> | <span data-ttu-id="1e10e-229">True lorsque le résumé de l'interRogation est visible uniquement par l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="1e10e-229">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="1e10e-230">expiryDate</span><span class="sxs-lookup"><span data-stu-id="1e10e-230">expiryDate</span></span> | <span data-ttu-id="1e10e-231">DateTime
</span><span class="sxs-lookup"><span data-stu-id="1e10e-231">DateTime</span></span> | <span data-ttu-id="1e10e-232">Date et heure de l'expiration du sondage</span><span class="sxs-lookup"><span data-stu-id="1e10e-232">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="1e10e-233">Choix</span><span class="sxs-lookup"><span data-stu-id="1e10e-233">Choices</span></span> | <span data-ttu-id="1e10e-234">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="1e10e-234">Json Array</span></span> | <span data-ttu-id="1e10e-235">Liste d'objets JSON avec le composant suivant</span><span class="sxs-lookup"><span data-stu-id="1e10e-235">List of Json objects with following component</span></span> <ol><li><span data-ttu-id="1e10e-236">titre-texte d'option</span><span class="sxs-lookup"><span data-stu-id="1e10e-236">title - Option Text</span></span></li><li><span data-ttu-id="1e10e-237">image de l'option image</span><span class="sxs-lookup"><span data-stu-id="1e10e-237">image - Option Image</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-238">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-238">Sample JSON Response:</span></span>

```javascript
{
    "actions": [
        {
            "referenceId": "d4753fdc-13fe-4162-a48f-5bf071bfd380",
            "actionType": "Poll",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:33:51Z",
            "actionBody": {
                "actionId": "27c7dbcf-48bb-4523-8273-d53a3da2343b",
                "question": "Do you find Kaizala extensibility easy to use?",
                "isSenderOnly": false,
                "expiryDate": "2017-12-20T18:33:51Z",
                "choices": [
                    {
                        "title": "Yes",
                        "image": "https://cdn.kascore.osi.office.net/75e8e7b63d2a4c10cdc30208aa27f1c2987d868a0e764fc742a94f6549d8bdb2.png?sv=2015-12-11&sr=b&sig=4iqswjFVYyqGqyKg6cdMdUQmiAez8sV951UScUmLzLk%3D&st=2017-05-17T07%3A04%3A41Z&se=2291-03-02T08%3A04%3A41Z&sp=r"
                    },
                    {
                        "title": "No"
                    },
                    {
                        "title": "Not at all"
                    }
                ]
            }
        }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a><span data-ttu-id="1e10e-239">structure d'objet actionBody pour l'action «je suis en réunion»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-239">actionBody object structure for the action 'Let's Meet':</span></span>

| <span data-ttu-id="1e10e-240">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-240">Parameter</span></span> | <span data-ttu-id="1e10e-241">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-241">Type</span></span> | <span data-ttu-id="1e10e-242">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-242">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-243">actionId</span><span class="sxs-lookup"><span data-stu-id="1e10e-243">actionId</span></span> | <span data-ttu-id="1e10e-244">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-244">String</span></span> | <span data-ttu-id="1e10e-245">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="1e10e-245">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="1e10e-246">title</span><span class="sxs-lookup"><span data-stu-id="1e10e-246">title</span></span> | <span data-ttu-id="1e10e-247">String</span><span class="sxs-lookup"><span data-stu-id="1e10e-247">String</span></span> | <span data-ttu-id="1e10e-248">Titre de la demande de réunion</span><span class="sxs-lookup"><span data-stu-id="1e10e-248">Title of the Meeting request</span></span> |
| <span data-ttu-id="1e10e-249">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="1e10e-249">isSenderOnly</span></span> | <span data-ttu-id="1e10e-250">Booléen</span><span class="sxs-lookup"><span data-stu-id="1e10e-250">Boolean</span></span> | <span data-ttu-id="1e10e-251">True lorsque le résumé de l'interRogation est visible uniquement par l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="1e10e-251">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="1e10e-252">duration</span><span class="sxs-lookup"><span data-stu-id="1e10e-252">duration</span></span> | <span data-ttu-id="1e10e-253">Entier</span><span class="sxs-lookup"><span data-stu-id="1e10e-253">Integer</span></span> | <span data-ttu-id="1e10e-254">Durée de la réunion (en minutes)</span><span class="sxs-lookup"><span data-stu-id="1e10e-254">Duration of the meeting (in mins)</span></span> |
| <span data-ttu-id="1e10e-255">réunion</span><span class="sxs-lookup"><span data-stu-id="1e10e-255">agenda</span></span> | <span data-ttu-id="1e10e-256">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-256">String</span></span> | <span data-ttu-id="1e10e-257">Calendrier défini pour la réunion</span><span class="sxs-lookup"><span data-stu-id="1e10e-257">Agenda set for the meeting</span></span> |
| <span data-ttu-id="1e10e-258">startingTime</span><span class="sxs-lookup"><span data-stu-id="1e10e-258">startingTime</span></span> | <span data-ttu-id="1e10e-259">DateTime
</span><span class="sxs-lookup"><span data-stu-id="1e10e-259">DateTime</span></span> | <span data-ttu-id="1e10e-260">Date et heure de l'expiration du sondage</span><span class="sxs-lookup"><span data-stu-id="1e10e-260">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="1e10e-261">Positionnement</span><span class="sxs-lookup"><span data-stu-id="1e10e-261">Place</span></span> | <span data-ttu-id="1e10e-262">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="1e10e-262">Json Object</span></span> | <span data-ttu-id="1e10e-263">Données de localisation avec le composant suivant</span><span class="sxs-lookup"><span data-stu-id="1e10e-263">Location Data with following component</span></span> <ol><li><span data-ttu-id="1e10e-264">Système</span><span class="sxs-lookup"><span data-stu-id="1e10e-264">Latitude</span></span></li><li><span data-ttu-id="1e10e-265">Ouest</span><span class="sxs-lookup"><span data-stu-id="1e10e-265">Longitude</span></span></li><li><span data-ttu-id="1e10e-266">name</span><span class="sxs-lookup"><span data-stu-id="1e10e-266">name</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-267">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-267">Sample JSON Response:</span></span>

```javascript
{
    "actions": [
        {
            "referenceId": "32d1e5ad-36ff-4237-a49c-4be95a10cd12",
            "actionType": "LetsMeet",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:55:04Z",
            "actionBody": {
                "actionId": "3c80f0f1-2b2f-460a-b760-ec10adb7dbb1",
                "title": "lets catch up?",
                "startingTime": "2018-01-01T00:00:00Z",
                "agenda": "no agenda",
                "duration": 30,
                "isSenderOnly": false,
                "place": {
                    "latitude": 15,
                    "longitude": 96,
                    "name": "MS Building 3"
                }
            }
        }
  ]
}
```


####  <a name="actionbody-object-structure-for-the-action-survey"></a><span data-ttu-id="1e10e-268">structure d'objet actionBody pour l'action «Survey»:</span><span class="sxs-lookup"><span data-stu-id="1e10e-268">actionBody object structure for the action 'Survey':</span></span>

| <span data-ttu-id="1e10e-269">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e10e-269">Parameter</span></span> | <span data-ttu-id="1e10e-270">Type</span><span class="sxs-lookup"><span data-stu-id="1e10e-270">Type</span></span> | <span data-ttu-id="1e10e-271">Description</span><span class="sxs-lookup"><span data-stu-id="1e10e-271">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1e10e-272">actionId</span><span class="sxs-lookup"><span data-stu-id="1e10e-272">actionId</span></span> | <span data-ttu-id="1e10e-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e10e-273">String</span></span> | <span data-ttu-id="1e10e-274">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="1e10e-274">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="1e10e-275">title</span><span class="sxs-lookup"><span data-stu-id="1e10e-275">title</span></span> | <span data-ttu-id="1e10e-276">String</span><span class="sxs-lookup"><span data-stu-id="1e10e-276">String</span></span> | <span data-ttu-id="1e10e-277">Titre de l'enquête</span><span class="sxs-lookup"><span data-stu-id="1e10e-277">Title of the Survey</span></span> |
| <span data-ttu-id="1e10e-278">responseCount</span><span class="sxs-lookup"><span data-stu-id="1e10e-278">responseCount</span></span> | <span data-ttu-id="1e10e-279">Numérique</span><span class="sxs-lookup"><span data-stu-id="1e10e-279">Numeric</span></span> | <span data-ttu-id="1e10e-280">Nombre de personnes ayant répondu à l'enquête</span><span class="sxs-lookup"><span data-stu-id="1e10e-280">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="1e10e-281">expiryDate</span><span class="sxs-lookup"><span data-stu-id="1e10e-281">expiryDate</span></span> | <span data-ttu-id="1e10e-282">DateTime
</span><span class="sxs-lookup"><span data-stu-id="1e10e-282">DateTime</span></span> | <span data-ttu-id="1e10e-283">Date et heure de l'expiration de l'enquête</span><span class="sxs-lookup"><span data-stu-id="1e10e-283">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="1e10e-284">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="1e10e-284">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "88a93ddd-0349d-4d18-86ee-c0f8484728db",
      "actionType": "Survey",
      "sender": "+91960000",
      "creationTime": 1480931759,
      "actionBody": {
        "actionId": "8106b2bb-236c-4952-a554-2baadcbd49a0",
        "title": "Sample Survey",
        "responseCount": 1
      }
    }
]
}
```

<span data-ttu-id="1e10e-285">Ensuite: vous pouvez récupérer des informations supplémentaires sur chaque instance d'action avec l'actionId correspondant.</span><span class="sxs-lookup"><span data-stu-id="1e10e-285">Next: You can retrieve further details of each action instance with the corresponding actionId.</span></span> [<span data-ttu-id="1e10e-286">API pour la récupération des détails d'instance d'action</span><span class="sxs-lookup"><span data-stu-id="1e10e-286">API for retrieving Action instance Details</span></span>](actionDetails.md)
