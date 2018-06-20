---
title: /actions
description: Article de référence de l’API obtenir la liste des actions d’un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905131"
---
# <a name="get-list-of-actions-in-a-group"></a><span data-ttu-id="52277-103">Obtenir la liste des Actions d’un groupe</span><span class="sxs-lookup"><span data-stu-id="52277-103">Get list of Actions in a group</span></span>
## <a name="get-actions"></a><span data-ttu-id="52277-104">OBTENIR /actions</span><span class="sxs-lookup"><span data-stu-id="52277-104">GET /actions</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a><span data-ttu-id="52277-105">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="52277-105">Request Parameters</span></span>

|  | <span data-ttu-id="52277-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-106">Parameter</span></span> | <span data-ttu-id="52277-107">Type</span><span class="sxs-lookup"><span data-stu-id="52277-107">Type</span></span> | <span data-ttu-id="52277-108">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="52277-108">Optional?</span></span> | <span data-ttu-id="52277-109">Description</span><span class="sxs-lookup"><span data-stu-id="52277-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="52277-110">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="52277-110">URL Path Parameter</span></span> | <span data-ttu-id="52277-111">groupId</span><span class="sxs-lookup"><span data-stu-id="52277-111">groupId</span></span> | <span data-ttu-id="52277-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-112">String</span></span> | <span data-ttu-id="52277-113">Non</span><span class="sxs-lookup"><span data-stu-id="52277-113">No</span></span> | <span data-ttu-id="52277-114">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="52277-114">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="52277-115">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="52277-115">HTTP Header</span></span> | <span data-ttu-id="52277-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="52277-116">accessToken</span></span> | <span data-ttu-id="52277-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-117">String</span></span> | <span data-ttu-id="52277-118">Non</span><span class="sxs-lookup"><span data-stu-id="52277-118">No</span></span> | <span data-ttu-id="52277-119">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="52277-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="52277-120">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="52277-120">URL Query Parameter</span></span> | <span data-ttu-id="52277-121">actionType</span><span class="sxs-lookup"><span data-stu-id="52277-121">actionType</span></span> | <span data-ttu-id="52277-122">String</span><span class="sxs-lookup"><span data-stu-id="52277-122">String</span></span> | <span data-ttu-id="52277-123">Non</span><span class="sxs-lookup"><span data-stu-id="52277-123">No</span></span> | <span data-ttu-id="52277-124">Type d’action à récupérer</span><span class="sxs-lookup"><span data-stu-id="52277-124">Type of action to retrieve</span></span> |
| <span data-ttu-id="52277-125">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="52277-125">URL Query Parameter</span></span> | <span data-ttu-id="52277-126">fromDate</span><span class="sxs-lookup"><span data-stu-id="52277-126">fromDate</span></span> | <span data-ttu-id="52277-127">DateTime (heure époque)</span><span class="sxs-lookup"><span data-stu-id="52277-127">DateTime (epoch time)</span></span> | <span data-ttu-id="52277-128">Oui</span><span class="sxs-lookup"><span data-stu-id="52277-128">Yes</span></span> | <span data-ttu-id="52277-129">Heure à partir de laquelle les actions doivent être extraites</span><span class="sxs-lookup"><span data-stu-id="52277-129">Time from which the actions need to be retrieved</span></span> |
| <span data-ttu-id="52277-130">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="52277-130">URL Query Parameter</span></span> | <span data-ttu-id="52277-131">count</span><span class="sxs-lookup"><span data-stu-id="52277-131">count</span></span> | <span data-ttu-id="52277-132">number</span><span class="sxs-lookup"><span data-stu-id="52277-132">number</span></span> | <span data-ttu-id="52277-133">Oui</span><span class="sxs-lookup"><span data-stu-id="52277-133">Yes</span></span> | <span data-ttu-id="52277-134">Nombre d’actions individuelles à renvoyer ; Par défaut = 30</span><span class="sxs-lookup"><span data-stu-id="52277-134">Count of individual actions to be returned; Default = 30</span></span> |

### <a name="response-body"></a><span data-ttu-id="52277-135">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="52277-135">Response body</span></span>

| <span data-ttu-id="52277-136">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-136">Parameter</span></span> | <span data-ttu-id="52277-137">Type</span><span class="sxs-lookup"><span data-stu-id="52277-137">Type</span></span> | <span data-ttu-id="52277-138">Description</span><span class="sxs-lookup"><span data-stu-id="52277-138">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-139">actions</span><span class="sxs-lookup"><span data-stu-id="52277-139">actions</span></span> | <span data-ttu-id="52277-140">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="52277-140">JSON Object Array</span></span> | <span data-ttu-id="52277-141">Tableau d’objets action</span><span class="sxs-lookup"><span data-stu-id="52277-141">Array of action objects</span></span> |
| <span data-ttu-id="52277-142">hasMore</span><span class="sxs-lookup"><span data-stu-id="52277-142">hasMore</span></span> | <span data-ttu-id="52277-143">bool?en</span><span class="sxs-lookup"><span data-stu-id="52277-143">boolean</span></span> | <span data-ttu-id="52277-144">Si le nombre maximal d’actions par réponse a atteint, cette variable est définie sur true</span><span class="sxs-lookup"><span data-stu-id="52277-144">If the max count of actions per response has reached, this variable will be set to true</span></span> |

<span data-ttu-id="52277-145">Structure de JSON pour chaque action individuelle dans les actions de tableau [] :</span><span class="sxs-lookup"><span data-stu-id="52277-145">JSON structure for each individual action in the array actions[]:</span></span>

| <span data-ttu-id="52277-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-146">Parameter</span></span> | <span data-ttu-id="52277-147">Type</span><span class="sxs-lookup"><span data-stu-id="52277-147">Type</span></span> | <span data-ttu-id="52277-148">Description</span><span class="sxs-lookup"><span data-stu-id="52277-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-149">referenceId</span><span class="sxs-lookup"><span data-stu-id="52277-149">referenceId</span></span> | <span data-ttu-id="52277-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-150">String</span></span> | <span data-ttu-id="52277-151">referenceID pour le message</span><span class="sxs-lookup"><span data-stu-id="52277-151">referenceID for the message</span></span> |
| <span data-ttu-id="52277-152">actionType</span><span class="sxs-lookup"><span data-stu-id="52277-152">actionType</span></span> | <span data-ttu-id="52277-153">String</span><span class="sxs-lookup"><span data-stu-id="52277-153">String</span></span> | <span data-ttu-id="52277-154">Type d’action renvoyée</span><span class="sxs-lookup"><span data-stu-id="52277-154">Type of action being returned</span></span> |
| <span data-ttu-id="52277-155">actionBody</span><span class="sxs-lookup"><span data-stu-id="52277-155">actionBody</span></span> | <span data-ttu-id="52277-156">Tableau d’objets JSON spécifique à l’actiontype</span><span class="sxs-lookup"><span data-stu-id="52277-156">JSON object array specific to the actiontype</span></span> | <span data-ttu-id="52277-157">Tableau avec des objets spécifiques à l’actiontype</span><span class="sxs-lookup"><span data-stu-id="52277-157">Array with objects specific to the actiontype</span></span> |
| <span data-ttu-id="52277-158">sender</span><span class="sxs-lookup"><span data-stu-id="52277-158">sender</span></span> | <span data-ttu-id="52277-159">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-159">String</span></span> | <span data-ttu-id="52277-160">Numéro de téléphone de l’utilisateur qui a envoyé l’action pour le groupe</span><span class="sxs-lookup"><span data-stu-id="52277-160">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="52277-161">sentAt</span><span class="sxs-lookup"><span data-stu-id="52277-161">sentAt</span></span> | <span data-ttu-id="52277-162">Date/heure</span><span class="sxs-lookup"><span data-stu-id="52277-162">DateTime</span></span> | <span data-ttu-id="52277-163">Publication de l’action pour le groupe</span><span class="sxs-lookup"><span data-stu-id="52277-163">Time when the action was posted to the group</span></span> |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a><span data-ttu-id="52277-164">structure d’objet actionBody de pièce jointe image/image :</span><span class="sxs-lookup"><span data-stu-id="52277-164">actionBody object structure for image/picture attachment:</span></span>

| <span data-ttu-id="52277-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-165">Parameter</span></span> | <span data-ttu-id="52277-166">Type</span><span class="sxs-lookup"><span data-stu-id="52277-166">Type</span></span> | <span data-ttu-id="52277-167">Description</span><span class="sxs-lookup"><span data-stu-id="52277-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-168">imageURL</span><span class="sxs-lookup"><span data-stu-id="52277-168">imageURL</span></span> | <span data-ttu-id="52277-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-169">String</span></span> | <span data-ttu-id="52277-170">Chaîne d’URL de l’image</span><span class="sxs-lookup"><span data-stu-id="52277-170">URL string for the picture</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-171">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-171">Sample JSON Response:</span></span>

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

####  <a name="actionbody-object-structure-for-the-action-share-location"></a><span data-ttu-id="52277-172">structure d’objet actionBody pour l’emplacement du partage de l’action :</span><span class="sxs-lookup"><span data-stu-id="52277-172">actionBody object structure for the action 'Share Location':</span></span>

| <span data-ttu-id="52277-173">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-173">Parameter</span></span> | <span data-ttu-id="52277-174">Type</span><span class="sxs-lookup"><span data-stu-id="52277-174">Type</span></span> | <span data-ttu-id="52277-175">Description</span><span class="sxs-lookup"><span data-stu-id="52277-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-176">latitude</span><span class="sxs-lookup"><span data-stu-id="52277-176">latitude</span></span> | <span data-ttu-id="52277-177">Double</span><span class="sxs-lookup"><span data-stu-id="52277-177">Double</span></span> | <span data-ttu-id="52277-178">Latitude coordonnées de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="52277-178">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="52277-179">longitude</span><span class="sxs-lookup"><span data-stu-id="52277-179">longitude</span></span> | <span data-ttu-id="52277-180">Double</span><span class="sxs-lookup"><span data-stu-id="52277-180">Double</span></span> | <span data-ttu-id="52277-181">Longitude coordonnées de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="52277-181">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-182">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-182">Sample JSON Response:</span></span>

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

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a><span data-ttu-id="52277-183">structure d’objet actionBody pour l’action « Photo avec emplacement » :</span><span class="sxs-lookup"><span data-stu-id="52277-183">actionBody object structure for the action 'Photo with Location':</span></span>

| <span data-ttu-id="52277-184">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-184">Parameter</span></span> | <span data-ttu-id="52277-185">Type</span><span class="sxs-lookup"><span data-stu-id="52277-185">Type</span></span> | <span data-ttu-id="52277-186">Description</span><span class="sxs-lookup"><span data-stu-id="52277-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-187">imageURL</span><span class="sxs-lookup"><span data-stu-id="52277-187">imageURL</span></span> | <span data-ttu-id="52277-188">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-188">String</span></span> | <span data-ttu-id="52277-189">Chaîne d’URL de l’image</span><span class="sxs-lookup"><span data-stu-id="52277-189">URL string for the picture</span></span> |
| <span data-ttu-id="52277-190">latitude</span><span class="sxs-lookup"><span data-stu-id="52277-190">latitude</span></span> | <span data-ttu-id="52277-191">Double</span><span class="sxs-lookup"><span data-stu-id="52277-191">Double</span></span> | <span data-ttu-id="52277-192">Latitude coordonnées de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="52277-192">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="52277-193">longitude</span><span class="sxs-lookup"><span data-stu-id="52277-193">longitude</span></span> | <span data-ttu-id="52277-194">Double</span><span class="sxs-lookup"><span data-stu-id="52277-194">Double</span></span> | <span data-ttu-id="52277-195">Longitude coordonnées de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="52277-195">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-196">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-196">Sample JSON Response:</span></span>

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

####  <a name="actionbody-object-structure-for-the-action-job"></a><span data-ttu-id="52277-197">structure d’objet actionBody pour l’action 'Job' :</span><span class="sxs-lookup"><span data-stu-id="52277-197">actionBody object structure for the action 'Job':</span></span>

| <span data-ttu-id="52277-198">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-198">Parameter</span></span> | <span data-ttu-id="52277-199">Type</span><span class="sxs-lookup"><span data-stu-id="52277-199">Type</span></span> | <span data-ttu-id="52277-200">Description</span><span class="sxs-lookup"><span data-stu-id="52277-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-201">actionId</span><span class="sxs-lookup"><span data-stu-id="52277-201">actionId</span></span> | <span data-ttu-id="52277-202">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-202">String</span></span> | <span data-ttu-id="52277-203">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="52277-203">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="52277-204">title</span><span class="sxs-lookup"><span data-stu-id="52277-204">title</span></span> | <span data-ttu-id="52277-205">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-205">String</span></span> | <span data-ttu-id="52277-206">Titre de la tâche</span><span class="sxs-lookup"><span data-stu-id="52277-206">Title of the Job</span></span> |
| <span data-ttu-id="52277-207">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="52277-207">assigneeCount</span></span> | <span data-ttu-id="52277-208">Numérique</span><span class="sxs-lookup"><span data-stu-id="52277-208">Numeric</span></span> | <span data-ttu-id="52277-209">Nombre de destinataires</span><span class="sxs-lookup"><span data-stu-id="52277-209">Number of assignees</span></span> |
| <span data-ttu-id="52277-210">responseCount</span><span class="sxs-lookup"><span data-stu-id="52277-210">responseCount</span></span> | <span data-ttu-id="52277-211">Numérique</span><span class="sxs-lookup"><span data-stu-id="52277-211">Numeric</span></span> | <span data-ttu-id="52277-212">Nombre d’intervenants a marqué le travail terminée</span><span class="sxs-lookup"><span data-stu-id="52277-212">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="52277-213">isCompleted</span><span class="sxs-lookup"><span data-stu-id="52277-213">isCompleted</span></span> | <span data-ttu-id="52277-214">Bool�en</span><span class="sxs-lookup"><span data-stu-id="52277-214">Boolean</span></span> | <span data-ttu-id="52277-215">True si tous les intervenants ont effectué le travail</span><span class="sxs-lookup"><span data-stu-id="52277-215">True when all assignees have completed the job</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-216">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-216">Sample JSON Response:</span></span>

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
####  <a name="actionbody-object-structure-for-the-action-poll"></a><span data-ttu-id="52277-217">structure d’objet actionBody pour l’action « Sondage » :</span><span class="sxs-lookup"><span data-stu-id="52277-217">actionBody object structure for the action 'Poll':</span></span>

| <span data-ttu-id="52277-218">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-218">Parameter</span></span> | <span data-ttu-id="52277-219">Type</span><span class="sxs-lookup"><span data-stu-id="52277-219">Type</span></span> | <span data-ttu-id="52277-220">Description</span><span class="sxs-lookup"><span data-stu-id="52277-220">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-221">actionId</span><span class="sxs-lookup"><span data-stu-id="52277-221">actionId</span></span> | <span data-ttu-id="52277-222">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-222">String</span></span> | <span data-ttu-id="52277-223">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="52277-223">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="52277-224">question</span><span class="sxs-lookup"><span data-stu-id="52277-224">question</span></span> | <span data-ttu-id="52277-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-225">String</span></span> | <span data-ttu-id="52277-226">Question du sondage</span><span class="sxs-lookup"><span data-stu-id="52277-226">Poll Question</span></span> |
| <span data-ttu-id="52277-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="52277-227">isSenderOnly</span></span> | <span data-ttu-id="52277-228">Bool�en</span><span class="sxs-lookup"><span data-stu-id="52277-228">Boolean</span></span> | <span data-ttu-id="52277-229">True lorsque le résumé de sondage est visible uniquement par l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="52277-229">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="52277-230">affichait</span><span class="sxs-lookup"><span data-stu-id="52277-230">expiryDate</span></span> | <span data-ttu-id="52277-231">Date/heure</span><span class="sxs-lookup"><span data-stu-id="52277-231">DateTime</span></span> | <span data-ttu-id="52277-232">DateTime de la date d’expiration de sondage</span><span class="sxs-lookup"><span data-stu-id="52277-232">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="52277-233">Choices</span><span class="sxs-lookup"><span data-stu-id="52277-233">Choices</span></span> | <span data-ttu-id="52277-234">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="52277-234">Json Array</span></span> | <span data-ttu-id="52277-235">Liste de Json objets avec le composant suivant</span><span class="sxs-lookup"><span data-stu-id="52277-235">List of Json objects with following component</span></span> <ol><li><span data-ttu-id="52277-236">titre - texte de l’Option</span><span class="sxs-lookup"><span data-stu-id="52277-236">title - Option Text</span></span></li><li><span data-ttu-id="52277-237">image - Option Image</span><span class="sxs-lookup"><span data-stu-id="52277-237">image - Option Image</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-238">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-238">Sample JSON Response:</span></span>

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
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a><span data-ttu-id="52277-239">structure d’objet actionBody pour l’action « Rendez-vous » :</span><span class="sxs-lookup"><span data-stu-id="52277-239">actionBody object structure for the action 'Let's Meet':</span></span>

| <span data-ttu-id="52277-240">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-240">Parameter</span></span> | <span data-ttu-id="52277-241">Type</span><span class="sxs-lookup"><span data-stu-id="52277-241">Type</span></span> | <span data-ttu-id="52277-242">Description</span><span class="sxs-lookup"><span data-stu-id="52277-242">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-243">actionId</span><span class="sxs-lookup"><span data-stu-id="52277-243">actionId</span></span> | <span data-ttu-id="52277-244">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-244">String</span></span> | <span data-ttu-id="52277-245">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="52277-245">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="52277-246">title</span><span class="sxs-lookup"><span data-stu-id="52277-246">title</span></span> | <span data-ttu-id="52277-247">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-247">String</span></span> | <span data-ttu-id="52277-248">Titre de la demande de réunion</span><span class="sxs-lookup"><span data-stu-id="52277-248">Title of the Meeting request</span></span> |
| <span data-ttu-id="52277-249">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="52277-249">isSenderOnly</span></span> | <span data-ttu-id="52277-250">Bool�en</span><span class="sxs-lookup"><span data-stu-id="52277-250">Boolean</span></span> | <span data-ttu-id="52277-251">True lorsque le résumé de sondage est visible uniquement par l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="52277-251">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="52277-252">duration</span><span class="sxs-lookup"><span data-stu-id="52277-252">duration</span></span> | <span data-ttu-id="52277-253">Entier</span><span class="sxs-lookup"><span data-stu-id="52277-253">Integer</span></span> | <span data-ttu-id="52277-254">Durée de la réunion (en minutes)</span><span class="sxs-lookup"><span data-stu-id="52277-254">Duration of the meeting (in mins)</span></span> |
| <span data-ttu-id="52277-255">ordre du jour</span><span class="sxs-lookup"><span data-stu-id="52277-255">agenda</span></span> | <span data-ttu-id="52277-256">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-256">String</span></span> | <span data-ttu-id="52277-257">Ordre du jour, la valeur de la réunion</span><span class="sxs-lookup"><span data-stu-id="52277-257">Agenda set for the meeting</span></span> |
| <span data-ttu-id="52277-258">startingTime</span><span class="sxs-lookup"><span data-stu-id="52277-258">startingTime</span></span> | <span data-ttu-id="52277-259">Date/heure</span><span class="sxs-lookup"><span data-stu-id="52277-259">DateTime</span></span> | <span data-ttu-id="52277-260">DateTime de la date d’expiration de sondage</span><span class="sxs-lookup"><span data-stu-id="52277-260">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="52277-261">Place</span><span class="sxs-lookup"><span data-stu-id="52277-261">Place</span></span> | <span data-ttu-id="52277-262">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="52277-262">Json Object</span></span> | <span data-ttu-id="52277-263">Données d’emplacement avec le composant suivant</span><span class="sxs-lookup"><span data-stu-id="52277-263">Location Data with following component</span></span> <ol><li><span data-ttu-id="52277-264">Latitude</span><span class="sxs-lookup"><span data-stu-id="52277-264">Latitude</span></span></li><li><span data-ttu-id="52277-265">Longitude</span><span class="sxs-lookup"><span data-stu-id="52277-265">Longitude</span></span></li><li><span data-ttu-id="52277-266">name</span><span class="sxs-lookup"><span data-stu-id="52277-266">name</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-267">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-267">Sample JSON Response:</span></span>

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


####  <a name="actionbody-object-structure-for-the-action-survey"></a><span data-ttu-id="52277-268">structure d’objet actionBody pour l’action « Enquête » :</span><span class="sxs-lookup"><span data-stu-id="52277-268">actionBody object structure for the action 'Survey':</span></span>

| <span data-ttu-id="52277-269">Paramètre</span><span class="sxs-lookup"><span data-stu-id="52277-269">Parameter</span></span> | <span data-ttu-id="52277-270">Type</span><span class="sxs-lookup"><span data-stu-id="52277-270">Type</span></span> | <span data-ttu-id="52277-271">Description</span><span class="sxs-lookup"><span data-stu-id="52277-271">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="52277-272">actionId</span><span class="sxs-lookup"><span data-stu-id="52277-272">actionId</span></span> | <span data-ttu-id="52277-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-273">String</span></span> | <span data-ttu-id="52277-274">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="52277-274">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="52277-275">title</span><span class="sxs-lookup"><span data-stu-id="52277-275">title</span></span> | <span data-ttu-id="52277-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="52277-276">String</span></span> | <span data-ttu-id="52277-277">Titre de l’enquête</span><span class="sxs-lookup"><span data-stu-id="52277-277">Title of the Survey</span></span> |
| <span data-ttu-id="52277-278">responseCount</span><span class="sxs-lookup"><span data-stu-id="52277-278">responseCount</span></span> | <span data-ttu-id="52277-279">Numérique</span><span class="sxs-lookup"><span data-stu-id="52277-279">Numeric</span></span> | <span data-ttu-id="52277-280">Nombre de personnes qui a répondu à l’enquête</span><span class="sxs-lookup"><span data-stu-id="52277-280">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="52277-281">affichait</span><span class="sxs-lookup"><span data-stu-id="52277-281">expiryDate</span></span> | <span data-ttu-id="52277-282">Date/heure</span><span class="sxs-lookup"><span data-stu-id="52277-282">DateTime</span></span> | <span data-ttu-id="52277-283">DateTime de délai d’expiration de l’enquête</span><span class="sxs-lookup"><span data-stu-id="52277-283">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="52277-284">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="52277-284">Sample JSON Response:</span></span>

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

<span data-ttu-id="52277-285">À suivre : Vous pouvez récupérer davantage les détails de chaque instance de l’action avec actionId correspondant.</span><span class="sxs-lookup"><span data-stu-id="52277-285">Next: You can retrieve further details of each action instance with the corresponding actionId.</span></span> [<span data-ttu-id="52277-286">API pour l’extraction des détails de l’instance Action</span><span class="sxs-lookup"><span data-stu-id="52277-286">API for retrieving Action instance Details</span></span>](actionDetails.md)
