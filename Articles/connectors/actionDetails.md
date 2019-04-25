---
title: Détails de l'/action
description: Article de référence pour l'API permettant de rechercher des détails sur les actions Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: a0871eec8a0247cea122bd14f968dd1e16936101
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190723"
---
# <a name="get-details-for-an-action-in-a-group"></a><span data-ttu-id="65bee-103">Obtenir les détails d'une action dans un groupe</span><span class="sxs-lookup"><span data-stu-id="65bee-103">Get details for an Action in a group</span></span>
## <a name="get-actionsactionid"></a><span data-ttu-id="65bee-104">OBTENIR/actions/{actionId}/</span><span class="sxs-lookup"><span data-stu-id="65bee-104">GET /actions/{actionId}/</span></span>

<span data-ttu-id="65bee-105">Extrayez l'API pour récupérer la liste des instances d'action envoyées à un groupe à l'aide [de l'API pour Get/actions ici](actions_get.md).</span><span class="sxs-lookup"><span data-stu-id="65bee-105">Check-out the API for retrieving the list of action instances sent to a group using the [API for get /actions here](actions_get.md).</span></span> <span data-ttu-id="65bee-106">Vous pouvez récupérer des informations supplémentaires sur une instance d'action spécifique référencée par un actionId.</span><span class="sxs-lookup"><span data-stu-id="65bee-106">You can retrieve further details about a specific action instance referenced by an actionId.</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a><span data-ttu-id="65bee-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="65bee-107">Request Parameters</span></span>

|  | <span data-ttu-id="65bee-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65bee-108">Parameter</span></span> | <span data-ttu-id="65bee-109">Type</span><span class="sxs-lookup"><span data-stu-id="65bee-109">Type</span></span> | <span data-ttu-id="65bee-110">Module?</span><span class="sxs-lookup"><span data-stu-id="65bee-110">Optional?</span></span> | <span data-ttu-id="65bee-111">Description</span><span class="sxs-lookup"><span data-stu-id="65bee-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="65bee-112">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="65bee-112">URL Path Parameter</span></span> | <span data-ttu-id="65bee-113">groupId</span><span class="sxs-lookup"><span data-stu-id="65bee-113">groupId</span></span> | <span data-ttu-id="65bee-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-114">String</span></span> | <span data-ttu-id="65bee-115">Non</span><span class="sxs-lookup"><span data-stu-id="65bee-115">No</span></span> | <span data-ttu-id="65bee-116">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="65bee-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="65bee-117">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="65bee-117">URL Path Parameter</span></span> | <span data-ttu-id="65bee-118">actionId</span><span class="sxs-lookup"><span data-stu-id="65bee-118">actionId</span></span> | <span data-ttu-id="65bee-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-119">String</span></span> | <span data-ttu-id="65bee-120">Non</span><span class="sxs-lookup"><span data-stu-id="65bee-120">No</span></span> | <span data-ttu-id="65bee-121">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="65bee-121">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="65bee-122">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="65bee-122">HTTP Header</span></span> | <span data-ttu-id="65bee-123">accessToken</span><span class="sxs-lookup"><span data-stu-id="65bee-123">accessToken</span></span> | <span data-ttu-id="65bee-124">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-124">String</span></span> | <span data-ttu-id="65bee-125">Non</span><span class="sxs-lookup"><span data-stu-id="65bee-125">No</span></span> | <span data-ttu-id="65bee-126">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="65bee-126">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="65bee-127">Paramètre de requête d'URL</span><span class="sxs-lookup"><span data-stu-id="65bee-127">URL Query Parameter</span></span> | <span data-ttu-id="65bee-128">getDetails</span><span class="sxs-lookup"><span data-stu-id="65bee-128">getDetails</span></span> | <span data-ttu-id="65bee-129">Booléen</span><span class="sxs-lookup"><span data-stu-id="65bee-129">Boolean</span></span> | <span data-ttu-id="65bee-130">Oui</span><span class="sxs-lookup"><span data-stu-id="65bee-130">Yes</span></span> | <span data-ttu-id="65bee-131">Utilisez pour obtenir des informations détaillées sur l'action spécifique; La valeur par défaut est false</span><span class="sxs-lookup"><span data-stu-id="65bee-131">Use to get drill-down details of the specific action; Default is False</span></span> |

### <a name="response-body"></a><span data-ttu-id="65bee-132">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="65bee-132">Response body</span></span>

| <span data-ttu-id="65bee-133">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65bee-133">Parameter</span></span> | <span data-ttu-id="65bee-134">Type</span><span class="sxs-lookup"><span data-stu-id="65bee-134">Type</span></span> | <span data-ttu-id="65bee-135">Description</span><span class="sxs-lookup"><span data-stu-id="65bee-135">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="65bee-136">actionType</span><span class="sxs-lookup"><span data-stu-id="65bee-136">actionType</span></span> | <span data-ttu-id="65bee-137">String</span><span class="sxs-lookup"><span data-stu-id="65bee-137">String</span></span> | <span data-ttu-id="65bee-138">Type d'action retourné</span><span class="sxs-lookup"><span data-stu-id="65bee-138">Type of action being returned</span></span> |
| <span data-ttu-id="65bee-139">actionDetails</span><span class="sxs-lookup"><span data-stu-id="65bee-139">actionDetails</span></span> | <span data-ttu-id="65bee-140">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="65bee-140">JSON object</span></span> | <span data-ttu-id="65bee-141">Onbject JSON spécifique au ActionType</span><span class="sxs-lookup"><span data-stu-id="65bee-141">JSON onbject specific to the actiontype</span></span> |
| <span data-ttu-id="65bee-142">expéditeur</span><span class="sxs-lookup"><span data-stu-id="65bee-142">sender</span></span> | <span data-ttu-id="65bee-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-143">String</span></span> | <span data-ttu-id="65bee-144">Numéro de téléphone de l'utilisateur qui a envoyé l'action au groupe</span><span class="sxs-lookup"><span data-stu-id="65bee-144">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="65bee-145">sentAt</span><span class="sxs-lookup"><span data-stu-id="65bee-145">sentAt</span></span> | <span data-ttu-id="65bee-146">DateTime
</span><span class="sxs-lookup"><span data-stu-id="65bee-146">DateTime</span></span> | <span data-ttu-id="65bee-147">Heure à laquelle l'action a été publiée dans le groupe</span><span class="sxs-lookup"><span data-stu-id="65bee-147">Time when the action was posted to the group</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-job"></a><span data-ttu-id="65bee-148">structure d'objet actionDetails pour l'action «Job»:</span><span class="sxs-lookup"><span data-stu-id="65bee-148">actionDetails object structure for the action 'Job':</span></span>

| <span data-ttu-id="65bee-149">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65bee-149">Parameter</span></span> | <span data-ttu-id="65bee-150">Type</span><span class="sxs-lookup"><span data-stu-id="65bee-150">Type</span></span> | <span data-ttu-id="65bee-151">Description</span><span class="sxs-lookup"><span data-stu-id="65bee-151">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="65bee-152">dueDate</span><span class="sxs-lookup"><span data-stu-id="65bee-152">dueDate</span></span> | <span data-ttu-id="65bee-153">DateTime
</span><span class="sxs-lookup"><span data-stu-id="65bee-153">DateTime</span></span> | <span data-ttu-id="65bee-154">Date d'échéance de la tâche</span><span class="sxs-lookup"><span data-stu-id="65bee-154">Due date for the Job</span></span> |
| <span data-ttu-id="65bee-155">title</span><span class="sxs-lookup"><span data-stu-id="65bee-155">title</span></span> | <span data-ttu-id="65bee-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-156">String</span></span> | <span data-ttu-id="65bee-157">Titre du travail</span><span class="sxs-lookup"><span data-stu-id="65bee-157">Title of the Job</span></span> |
| <span data-ttu-id="65bee-158">status</span><span class="sxs-lookup"><span data-stu-id="65bee-158">status</span></span> | <span data-ttu-id="65bee-159">Booléen</span><span class="sxs-lookup"><span data-stu-id="65bee-159">Boolean</span></span> | <span data-ttu-id="65bee-160">True lorsque tous les utilisateurs ont effectué le travail</span><span class="sxs-lookup"><span data-stu-id="65bee-160">True when all assignees have completed the job</span></span> |
| <span data-ttu-id="65bee-161">responseCount</span><span class="sxs-lookup"><span data-stu-id="65bee-161">responseCount</span></span> | <span data-ttu-id="65bee-162">Numérique</span><span class="sxs-lookup"><span data-stu-id="65bee-162">Numeric</span></span> | <span data-ttu-id="65bee-163">Nombre d'utilisateurs ayant marqué le travail comme terminé</span><span class="sxs-lookup"><span data-stu-id="65bee-163">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="65bee-164">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="65bee-164">assigneeCount</span></span> | <span data-ttu-id="65bee-165">Numérique</span><span class="sxs-lookup"><span data-stu-id="65bee-165">Numeric</span></span> | <span data-ttu-id="65bee-166">Nombre de personnes affectées</span><span class="sxs-lookup"><span data-stu-id="65bee-166">Number of assignees</span></span> |
| <span data-ttu-id="65bee-167">renvoyé</span><span class="sxs-lookup"><span data-stu-id="65bee-167">responses</span></span> | <span data-ttu-id="65bee-168">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="65bee-168">JSON Array</span></span> | <span data-ttu-id="65bee-169">Tableau JSON de réponses aux travaux individuels</span><span class="sxs-lookup"><span data-stu-id="65bee-169">JSON Array of individual Job responses</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a><span data-ttu-id="65bee-170">structure d'objet actionDetails pour l'action «Survey»:</span><span class="sxs-lookup"><span data-stu-id="65bee-170">actionDetails object structure for the action 'Survey':</span></span>

| <span data-ttu-id="65bee-171">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65bee-171">Parameter</span></span> | <span data-ttu-id="65bee-172">Type</span><span class="sxs-lookup"><span data-stu-id="65bee-172">Type</span></span> | <span data-ttu-id="65bee-173">Description</span><span class="sxs-lookup"><span data-stu-id="65bee-173">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="65bee-174">actionId</span><span class="sxs-lookup"><span data-stu-id="65bee-174">actionId</span></span> | <span data-ttu-id="65bee-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-175">String</span></span> | <span data-ttu-id="65bee-176">GUID représentant l'instance d'action spécifique</span><span class="sxs-lookup"><span data-stu-id="65bee-176">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="65bee-177">title</span><span class="sxs-lookup"><span data-stu-id="65bee-177">title</span></span> | <span data-ttu-id="65bee-178">Chaîne</span><span class="sxs-lookup"><span data-stu-id="65bee-178">String</span></span> | <span data-ttu-id="65bee-179">Titre de l'enquête</span><span class="sxs-lookup"><span data-stu-id="65bee-179">Title of the Survey</span></span> |
| <span data-ttu-id="65bee-180">responseCount</span><span class="sxs-lookup"><span data-stu-id="65bee-180">responseCount</span></span> | <span data-ttu-id="65bee-181">Numérique</span><span class="sxs-lookup"><span data-stu-id="65bee-181">Numeric</span></span> | <span data-ttu-id="65bee-182">Nombre de personnes ayant répondu à l'enquête</span><span class="sxs-lookup"><span data-stu-id="65bee-182">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="65bee-183">expiryDate</span><span class="sxs-lookup"><span data-stu-id="65bee-183">expiryDate</span></span> | <span data-ttu-id="65bee-184">DateTime
</span><span class="sxs-lookup"><span data-stu-id="65bee-184">DateTime</span></span> | <span data-ttu-id="65bee-185">Date et heure de l'expiration de l'enquête</span><span class="sxs-lookup"><span data-stu-id="65bee-185">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="65bee-186">Exemple de réponse JSON:</span><span class="sxs-lookup"><span data-stu-id="65bee-186">Sample JSON Response:</span></span>

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
