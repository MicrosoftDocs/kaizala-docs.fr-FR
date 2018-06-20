---
title: / Détails de l’action
description: Article de référence de l’API à la requête concernant les détails des Actions Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: a0871eec8a0247cea122bd14f968dd1e16936101
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905123"
---
# <a name="get-details-for-an-action-in-a-group"></a><span data-ttu-id="f4bf9-103">Obtenir plus d’informations pour une Action dans un groupe</span><span class="sxs-lookup"><span data-stu-id="f4bf9-103">Get details for an Action in a group</span></span>
## <a name="get-actionsactionid"></a><span data-ttu-id="f4bf9-104">GET /actions/ {actionId} /</span><span class="sxs-lookup"><span data-stu-id="f4bf9-104">GET /actions/{actionId}/</span></span>

<span data-ttu-id="f4bf9-105">Extraction l’API pour extraire la liste des instances de l’action envoyé à un groupe à l’aide de l' [API pour obtenir /actions ici](actions_get.md).</span><span class="sxs-lookup"><span data-stu-id="f4bf9-105">Check-out the API for retrieving the list of action instances sent to a group using the [API for get /actions here](actions_get.md).</span></span> <span data-ttu-id="f4bf9-106">Vous pouvez récupérer plus de détails sur une instance d’action spécifique référencé par un actionId.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-106">You can retrieve further details about a specific action instance referenced by an actionId.</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a><span data-ttu-id="f4bf9-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="f4bf9-107">Request Parameters</span></span>

|  | <span data-ttu-id="f4bf9-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f4bf9-108">Parameter</span></span> | <span data-ttu-id="f4bf9-109">Type</span><span class="sxs-lookup"><span data-stu-id="f4bf9-109">Type</span></span> | <span data-ttu-id="f4bf9-110">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="f4bf9-110">Optional?</span></span> | <span data-ttu-id="f4bf9-111">Description</span><span class="sxs-lookup"><span data-stu-id="f4bf9-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4bf9-112">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="f4bf9-112">URL Path Parameter</span></span> | <span data-ttu-id="f4bf9-113">groupId</span><span class="sxs-lookup"><span data-stu-id="f4bf9-113">groupId</span></span> | <span data-ttu-id="f4bf9-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-114">String</span></span> | <span data-ttu-id="f4bf9-115">Non</span><span class="sxs-lookup"><span data-stu-id="f4bf9-115">No</span></span> | <span data-ttu-id="f4bf9-116">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="f4bf9-117">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="f4bf9-117">URL Path Parameter</span></span> | <span data-ttu-id="f4bf9-118">actionId</span><span class="sxs-lookup"><span data-stu-id="f4bf9-118">actionId</span></span> | <span data-ttu-id="f4bf9-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-119">String</span></span> | <span data-ttu-id="f4bf9-120">Non</span><span class="sxs-lookup"><span data-stu-id="f4bf9-120">No</span></span> | <span data-ttu-id="f4bf9-121">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-121">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="f4bf9-122">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="f4bf9-122">HTTP Header</span></span> | <span data-ttu-id="f4bf9-123">accessToken</span><span class="sxs-lookup"><span data-stu-id="f4bf9-123">accessToken</span></span> | <span data-ttu-id="f4bf9-124">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-124">String</span></span> | <span data-ttu-id="f4bf9-125">Non</span><span class="sxs-lookup"><span data-stu-id="f4bf9-125">No</span></span> | <span data-ttu-id="f4bf9-126">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="f4bf9-126">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="f4bf9-127">Paramètre de requête URL</span><span class="sxs-lookup"><span data-stu-id="f4bf9-127">URL Query Parameter</span></span> | <span data-ttu-id="f4bf9-128">getDetails</span><span class="sxs-lookup"><span data-stu-id="f4bf9-128">getDetails</span></span> | <span data-ttu-id="f4bf9-129">Booléen</span><span class="sxs-lookup"><span data-stu-id="f4bf9-129">Boolean</span></span> | <span data-ttu-id="f4bf9-130">Oui</span><span class="sxs-lookup"><span data-stu-id="f4bf9-130">Yes</span></span> | <span data-ttu-id="f4bf9-131">Permet d’obtenir l’affichage des détails de l’action spécifique ; Valeur par défaut est False</span><span class="sxs-lookup"><span data-stu-id="f4bf9-131">Use to get drill-down details of the specific action; Default is False</span></span> |

### <a name="response-body"></a><span data-ttu-id="f4bf9-132">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="f4bf9-132">Response body</span></span>

| <span data-ttu-id="f4bf9-133">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f4bf9-133">Parameter</span></span> | <span data-ttu-id="f4bf9-134">Type</span><span class="sxs-lookup"><span data-stu-id="f4bf9-134">Type</span></span> | <span data-ttu-id="f4bf9-135">Description</span><span class="sxs-lookup"><span data-stu-id="f4bf9-135">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f4bf9-136">actionType</span><span class="sxs-lookup"><span data-stu-id="f4bf9-136">actionType</span></span> | <span data-ttu-id="f4bf9-137">String</span><span class="sxs-lookup"><span data-stu-id="f4bf9-137">String</span></span> | <span data-ttu-id="f4bf9-138">Type d’action renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4bf9-138">Type of action being returned</span></span> |
| <span data-ttu-id="f4bf9-139">actionDetails</span><span class="sxs-lookup"><span data-stu-id="f4bf9-139">actionDetails</span></span> | <span data-ttu-id="f4bf9-140">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="f4bf9-140">JSON object</span></span> | <span data-ttu-id="f4bf9-141">JSON onbject spécifique à l’actiontype</span><span class="sxs-lookup"><span data-stu-id="f4bf9-141">JSON onbject specific to the actiontype</span></span> |
| <span data-ttu-id="f4bf9-142">sender</span><span class="sxs-lookup"><span data-stu-id="f4bf9-142">sender</span></span> | <span data-ttu-id="f4bf9-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-143">String</span></span> | <span data-ttu-id="f4bf9-144">Numéro de téléphone de l’utilisateur qui a envoyé l’action pour le groupe</span><span class="sxs-lookup"><span data-stu-id="f4bf9-144">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="f4bf9-145">sentAt</span><span class="sxs-lookup"><span data-stu-id="f4bf9-145">sentAt</span></span> | <span data-ttu-id="f4bf9-146">Date/heure</span><span class="sxs-lookup"><span data-stu-id="f4bf9-146">DateTime</span></span> | <span data-ttu-id="f4bf9-147">Publication de l’action pour le groupe</span><span class="sxs-lookup"><span data-stu-id="f4bf9-147">Time when the action was posted to the group</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-job"></a><span data-ttu-id="f4bf9-148">structure d’objet actionDetails pour l’action 'Job' :</span><span class="sxs-lookup"><span data-stu-id="f4bf9-148">actionDetails object structure for the action 'Job':</span></span>

| <span data-ttu-id="f4bf9-149">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f4bf9-149">Parameter</span></span> | <span data-ttu-id="f4bf9-150">Type</span><span class="sxs-lookup"><span data-stu-id="f4bf9-150">Type</span></span> | <span data-ttu-id="f4bf9-151">Description</span><span class="sxs-lookup"><span data-stu-id="f4bf9-151">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f4bf9-152">dueDate</span><span class="sxs-lookup"><span data-stu-id="f4bf9-152">dueDate</span></span> | <span data-ttu-id="f4bf9-153">Date/heure</span><span class="sxs-lookup"><span data-stu-id="f4bf9-153">DateTime</span></span> | <span data-ttu-id="f4bf9-154">Date d’échéance de la tâche</span><span class="sxs-lookup"><span data-stu-id="f4bf9-154">Due date for the Job</span></span> |
| <span data-ttu-id="f4bf9-155">title</span><span class="sxs-lookup"><span data-stu-id="f4bf9-155">title</span></span> | <span data-ttu-id="f4bf9-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-156">String</span></span> | <span data-ttu-id="f4bf9-157">Titre de la tâche</span><span class="sxs-lookup"><span data-stu-id="f4bf9-157">Title of the Job</span></span> |
| <span data-ttu-id="f4bf9-158">status</span><span class="sxs-lookup"><span data-stu-id="f4bf9-158">status</span></span> | <span data-ttu-id="f4bf9-159">Bool�en</span><span class="sxs-lookup"><span data-stu-id="f4bf9-159">Boolean</span></span> | <span data-ttu-id="f4bf9-160">True si tous les intervenants ont effectué le travail</span><span class="sxs-lookup"><span data-stu-id="f4bf9-160">True when all assignees have completed the job</span></span> |
| <span data-ttu-id="f4bf9-161">responseCount</span><span class="sxs-lookup"><span data-stu-id="f4bf9-161">responseCount</span></span> | <span data-ttu-id="f4bf9-162">Numérique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-162">Numeric</span></span> | <span data-ttu-id="f4bf9-163">Nombre d’intervenants a marqué le travail terminée</span><span class="sxs-lookup"><span data-stu-id="f4bf9-163">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="f4bf9-164">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="f4bf9-164">assigneeCount</span></span> | <span data-ttu-id="f4bf9-165">Numérique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-165">Numeric</span></span> | <span data-ttu-id="f4bf9-166">Nombre de destinataires</span><span class="sxs-lookup"><span data-stu-id="f4bf9-166">Number of assignees</span></span> |
| <span data-ttu-id="f4bf9-167">réponses</span><span class="sxs-lookup"><span data-stu-id="f4bf9-167">responses</span></span> | <span data-ttu-id="f4bf9-168">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f4bf9-168">JSON Array</span></span> | <span data-ttu-id="f4bf9-169">Tableau JSON de réponses individuelles de travail</span><span class="sxs-lookup"><span data-stu-id="f4bf9-169">JSON Array of individual Job responses</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a><span data-ttu-id="f4bf9-170">structure d’objet actionDetails pour l’action « Enquête » :</span><span class="sxs-lookup"><span data-stu-id="f4bf9-170">actionDetails object structure for the action 'Survey':</span></span>

| <span data-ttu-id="f4bf9-171">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f4bf9-171">Parameter</span></span> | <span data-ttu-id="f4bf9-172">Type</span><span class="sxs-lookup"><span data-stu-id="f4bf9-172">Type</span></span> | <span data-ttu-id="f4bf9-173">Description</span><span class="sxs-lookup"><span data-stu-id="f4bf9-173">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f4bf9-174">actionId</span><span class="sxs-lookup"><span data-stu-id="f4bf9-174">actionId</span></span> | <span data-ttu-id="f4bf9-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-175">String</span></span> | <span data-ttu-id="f4bf9-176">GUID représentant l’instance de l’action spécifique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-176">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="f4bf9-177">title</span><span class="sxs-lookup"><span data-stu-id="f4bf9-177">title</span></span> | <span data-ttu-id="f4bf9-178">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f4bf9-178">String</span></span> | <span data-ttu-id="f4bf9-179">Titre de l’enquête</span><span class="sxs-lookup"><span data-stu-id="f4bf9-179">Title of the Survey</span></span> |
| <span data-ttu-id="f4bf9-180">responseCount</span><span class="sxs-lookup"><span data-stu-id="f4bf9-180">responseCount</span></span> | <span data-ttu-id="f4bf9-181">Numérique</span><span class="sxs-lookup"><span data-stu-id="f4bf9-181">Numeric</span></span> | <span data-ttu-id="f4bf9-182">Nombre de personnes qui a répondu à l’enquête</span><span class="sxs-lookup"><span data-stu-id="f4bf9-182">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="f4bf9-183">affichait</span><span class="sxs-lookup"><span data-stu-id="f4bf9-183">expiryDate</span></span> | <span data-ttu-id="f4bf9-184">Date/heure</span><span class="sxs-lookup"><span data-stu-id="f4bf9-184">DateTime</span></span> | <span data-ttu-id="f4bf9-185">DateTime de délai d’expiration de l’enquête</span><span class="sxs-lookup"><span data-stu-id="f4bf9-185">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="f4bf9-186">Exemple de réponse JSON :</span><span class="sxs-lookup"><span data-stu-id="f4bf9-186">Sample JSON Response:</span></span>

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
