---
title: / Actions_post
description: Article de référence de l’API de publier des actions sur un groupe Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 015a60bbef7be7108cc0edc10e81cc1f8b5636e2
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905129"
---
# <a name="post-a-action-in-a-group"></a><span data-ttu-id="d29e4-103">Publier une Action dans un groupe</span><span class="sxs-lookup"><span data-stu-id="d29e4-103">Post a Action in a group</span></span>
### <a name="post-actions"></a><span data-ttu-id="d29e4-104">/Actions POST</span><span class="sxs-lookup"><span data-stu-id="d29e4-104">POST /actions</span></span>

    POST {endpoint-url}/groups/{groupId}/actions

##### <a name="request-parameters"></a><span data-ttu-id="d29e4-105">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="d29e4-105">Request Parameters</span></span>

|  | <span data-ttu-id="d29e4-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-106">Parameter</span></span> | <span data-ttu-id="d29e4-107">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-107">Type</span></span> | <span data-ttu-id="d29e4-108">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-108">Optional?</span></span> | <span data-ttu-id="d29e4-109">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-110">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="d29e4-110">URL Path Parameter</span></span> | <span data-ttu-id="d29e4-111">groupId</span><span class="sxs-lookup"><span data-stu-id="d29e4-111">groupId</span></span> | <span data-ttu-id="d29e4-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-112">String</span></span> | <span data-ttu-id="d29e4-113">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-113">No</span></span> | <span data-ttu-id="d29e4-114">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="d29e4-114">Group Identifier</span></span> |
| <span data-ttu-id="d29e4-115">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d29e4-115">HTTP Header</span></span> | <span data-ttu-id="d29e4-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="d29e4-116">accessToken</span></span> | <span data-ttu-id="d29e4-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-117">String</span></span> | <span data-ttu-id="d29e4-118">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-118">No</span></span> | <span data-ttu-id="d29e4-119">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="d29e4-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="d29e4-120">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="d29e4-120">HTTP Header</span></span> | <span data-ttu-id="d29e4-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-121">Content-Type</span></span> | <span data-ttu-id="d29e4-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-122">String</span></span> | <span data-ttu-id="d29e4-123">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-123">No</span></span> | <span data-ttu-id="d29e4-124">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="d29e4-124">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="d29e4-125">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="d29e4-125">Request body</span></span>

| <span data-ttu-id="d29e4-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-126">Parameter</span></span> | <span data-ttu-id="d29e4-127">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-127">Type</span></span> | <span data-ttu-id="d29e4-128">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-128">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d29e4-129">id</span><span class="sxs-lookup"><span data-stu-id="d29e4-129">id</span></span> | <span data-ttu-id="d29e4-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-130">String</span></span> | <span data-ttu-id="d29e4-131">ID du package Kaizala Action.</span><span class="sxs-lookup"><span data-stu-id="d29e4-131">Id of the Kaizala Action package.</span></span> <span data-ttu-id="d29e4-132">ActionType ou Id doit être spécifiée</span><span class="sxs-lookup"><span data-stu-id="d29e4-132">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="d29e4-133">actionType</span><span class="sxs-lookup"><span data-stu-id="d29e4-133">actionType</span></span> | <span data-ttu-id="d29e4-134">String</span><span class="sxs-lookup"><span data-stu-id="d29e4-134">String</span></span> | <span data-ttu-id="d29e4-135">Enum « Enquête » / « Du travail ».</span><span class="sxs-lookup"><span data-stu-id="d29e4-135">Enum "Survey"/"Job".</span></span> <span data-ttu-id="d29e4-136">ActionType ou Id doit être spécifiée</span><span class="sxs-lookup"><span data-stu-id="d29e4-136">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="d29e4-137">actionBody</span><span class="sxs-lookup"><span data-stu-id="d29e4-137">actionBody</span></span> | <span data-ttu-id="d29e4-138">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="d29e4-138">JSON Object</span></span> | <span data-ttu-id="d29e4-139">Objet représentant les données nécessaires pour l’Action respectif.</span><span class="sxs-lookup"><span data-stu-id="d29e4-139">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="d29e4-140">Paramètres définis ci-dessous pour chacune des Actions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d29e4-140">Parameters defined below for each of the supported Actions.</span></span> |


###### <a name="actionbody-for-an-announcement-action"></a><span data-ttu-id="d29e4-141">actionBody pour une Action d’annonce</span><span class="sxs-lookup"><span data-stu-id="d29e4-141">actionBody for an Announcement Action</span></span>

| <span data-ttu-id="d29e4-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-142">Parameter</span></span> | <span data-ttu-id="d29e4-143">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-143">Type</span></span> | <span data-ttu-id="d29e4-144">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-144">Optional?</span></span> | <span data-ttu-id="d29e4-145">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-145">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-146">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-146">title</span></span> | <span data-ttu-id="d29e4-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-147">String</span></span> | <span data-ttu-id="d29e4-148">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-148">No</span></span> | <span data-ttu-id="d29e4-149">Titre de l’annonce</span><span class="sxs-lookup"><span data-stu-id="d29e4-149">Title of the Announcement</span></span> |
| <span data-ttu-id="d29e4-150">MediaResources</span><span class="sxs-lookup"><span data-stu-id="d29e4-150">MediaResources</span></span> | <span data-ttu-id="d29e4-151">String]</span><span class="sxs-lookup"><span data-stu-id="d29e4-151">String[]</span></span> | <span data-ttu-id="d29e4-152">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-152">Yes</span></span> | <span data-ttu-id="d29e4-153">Tableau des ressources multimédia</span><span class="sxs-lookup"><span data-stu-id="d29e4-153">Array of media resources</span></span> |
| <span data-ttu-id="d29e4-154">Message</span><span class="sxs-lookup"><span data-stu-id="d29e4-154">Message</span></span> | <span data-ttu-id="d29e4-155">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-155">String</span></span> | <span data-ttu-id="d29e4-156">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-156">No</span></span> | <span data-ttu-id="d29e4-157">Corps du message</span><span class="sxs-lookup"><span data-stu-id="d29e4-157">Message Body</span></span> |

###### <a name="sample-json-request-for-an-announcement-action"></a><span data-ttu-id="d29e4-158">Exemple de demande JSON pour une Action d’annonce</span><span class="sxs-lookup"><span data-stu-id="d29e4-158">Sample JSON Request for an Announcement Action</span></span>

```javascript
{
  "actionType" : "Announcement",
  "actionBody" : 
  {
    "Message":"Announcement from API Message text",
    "Title" : "Title text", 
    "MediaResources" : 
    [
      "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNV","eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VE"
    ]
  }
}

```

###### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="d29e4-159">actionBody pour une Action de tâche</span><span class="sxs-lookup"><span data-stu-id="d29e4-159">actionBody for a Job Action</span></span>

| <span data-ttu-id="d29e4-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-160">Parameter</span></span> | <span data-ttu-id="d29e4-161">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-161">Type</span></span> | <span data-ttu-id="d29e4-162">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-162">Optional?</span></span> | <span data-ttu-id="d29e4-163">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-164">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-164">title</span></span> | <span data-ttu-id="d29e4-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-165">String</span></span> | <span data-ttu-id="d29e4-166">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-166">No</span></span> | <span data-ttu-id="d29e4-167">Titre de la tâche</span><span class="sxs-lookup"><span data-stu-id="d29e4-167">Title of the Job</span></span> |
| <span data-ttu-id="d29e4-168">assignedTo</span><span class="sxs-lookup"><span data-stu-id="d29e4-168">assignedTo</span></span> | <span data-ttu-id="d29e4-169">String]</span><span class="sxs-lookup"><span data-stu-id="d29e4-169">String[]</span></span> | <span data-ttu-id="d29e4-170">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-170">No</span></span> | <span data-ttu-id="d29e4-171">Titre de la tâche</span><span class="sxs-lookup"><span data-stu-id="d29e4-171">Title of the Job</span></span> |
| <span data-ttu-id="d29e4-172">dueDate</span><span class="sxs-lookup"><span data-stu-id="d29e4-172">dueDate</span></span> | <span data-ttu-id="d29e4-173">long</span><span class="sxs-lookup"><span data-stu-id="d29e4-173">long</span></span> | <span data-ttu-id="d29e4-174">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-174">Yes</span></span> | <span data-ttu-id="d29e4-175">Par défaut : 24 heures.</span><span class="sxs-lookup"><span data-stu-id="d29e4-175">Default: 24hrs.</span></span> <span data-ttu-id="d29e4-176">Nombre d’heures avant laquelle le travail doit être terminé</span><span class="sxs-lookup"><span data-stu-id="d29e4-176">Number of hours before which job should be completed</span></span> |

###### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="d29e4-177">Exemple de demande JSON pour une Action de tâche</span><span class="sxs-lookup"><span data-stu-id="d29e4-177">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        title : "test job",
        assignedTo : ["+911111111111", "+911111111112"],
        dueDate : 10
    }
}

```

###### <a name="actionbody-for-a-poll-action"></a><span data-ttu-id="d29e4-178">actionBody pour une Action de sondage</span><span class="sxs-lookup"><span data-stu-id="d29e4-178">actionBody for a Poll Action</span></span>

| <span data-ttu-id="d29e4-179">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-179">Parameter</span></span> | <span data-ttu-id="d29e4-180">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-180">Type</span></span> | <span data-ttu-id="d29e4-181">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-181">Optional?</span></span> | <span data-ttu-id="d29e4-182">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-182">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-183">question</span><span class="sxs-lookup"><span data-stu-id="d29e4-183">question</span></span> | <span data-ttu-id="d29e4-184">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-184">String</span></span> | <span data-ttu-id="d29e4-185">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-185">No</span></span> | <span data-ttu-id="d29e4-186">Question du sondage</span><span class="sxs-lookup"><span data-stu-id="d29e4-186">Poll Question</span></span> |
| <span data-ttu-id="d29e4-187">Choices</span><span class="sxs-lookup"><span data-stu-id="d29e4-187">Choices</span></span> | <span data-ttu-id="d29e4-188">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="d29e4-188">Json Array</span></span> | <span data-ttu-id="d29e4-189">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-189">No</span></span> | <span data-ttu-id="d29e4-190">Options disponibles pour l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="d29e4-190">Choices available for the poll.</span></span> <span data-ttu-id="d29e4-191">Chaque choix ont ci-dessous composant :</span><span class="sxs-lookup"><span data-stu-id="d29e4-191">Each Choice have below component:</span></span> <ol><li><span data-ttu-id="d29e4-192">titre (obligatoire & sous forme de chaîne)</span><span class="sxs-lookup"><span data-stu-id="d29e4-192">title (Mandatory & in String format)</span></span> </li><li><span data-ttu-id="d29e4-193">image (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d29e4-193">image (optional)</span></span></li></ol> |
| <span data-ttu-id="d29e4-194">expiryInHours</span><span class="sxs-lookup"><span data-stu-id="d29e4-194">expiryInHours</span></span> | <span data-ttu-id="d29e4-195">Entier</span><span class="sxs-lookup"><span data-stu-id="d29e4-195">Integer</span></span> | <span data-ttu-id="d29e4-196">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-196">Yes</span></span> | <span data-ttu-id="d29e4-197">Par défaut : 720.</span><span class="sxs-lookup"><span data-stu-id="d29e4-197">Default:720.</span></span> <span data-ttu-id="d29e4-198">Nombre d’heures dans laquelle un sondage gven expire</span><span class="sxs-lookup"><span data-stu-id="d29e4-198">Number of hours in which a gven poll would expire</span></span> |

###### <a name="sample-json-request-for-a-poll-action"></a><span data-ttu-id="d29e4-199">Exemple de demande JSON pour une Action de sondage</span><span class="sxs-lookup"><span data-stu-id="d29e4-199">Sample JSON Request for a Poll Action</span></span>

```javascript
{actionType:"Poll", actionBody:{question:"Do you find Kaizala extensibility easy to use?", 
    choices:
        [
        {title:"Yes",image:"eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="},
        {title:"No"},
        {title:"Not at all"}
        ],
    expiryInHours:10}}
```
###### <a name="actionbody-for-a-lets-meet-action"></a><span data-ttu-id="d29e4-200">actionBody pour une Action répondent aux jetons</span><span class="sxs-lookup"><span data-stu-id="d29e4-200">actionBody for a Let's Meet Action</span></span>

| <span data-ttu-id="d29e4-201">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-201">Parameter</span></span> | <span data-ttu-id="d29e4-202">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-202">Type</span></span> | <span data-ttu-id="d29e4-203">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-203">Optional?</span></span> | <span data-ttu-id="d29e4-204">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-204">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-205">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-205">title</span></span> | <span data-ttu-id="d29e4-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-206">String</span></span> | <span data-ttu-id="d29e4-207">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-207">No</span></span> | <span data-ttu-id="d29e4-208">Titre de la demande de réunion</span><span class="sxs-lookup"><span data-stu-id="d29e4-208">Title of the Meeting Request</span></span>  |
| <span data-ttu-id="d29e4-209">startingTime</span><span class="sxs-lookup"><span data-stu-id="d29e4-209">startingTime</span></span> | <span data-ttu-id="d29e4-210">Date/heure</span><span class="sxs-lookup"><span data-stu-id="d29e4-210">DateTime</span></span> | <span data-ttu-id="d29e4-211">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-211">No</span></span> | <span data-ttu-id="d29e4-212">Heure de début de la réunion</span><span class="sxs-lookup"><span data-stu-id="d29e4-212">Starting time for the meeting</span></span> |
| <span data-ttu-id="d29e4-213">DurationInMins</span><span class="sxs-lookup"><span data-stu-id="d29e4-213">DurationInMins</span></span> | <span data-ttu-id="d29e4-214">Entier</span><span class="sxs-lookup"><span data-stu-id="d29e4-214">Integer</span></span> | <span data-ttu-id="d29e4-215">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-215">No</span></span> | <span data-ttu-id="d29e4-216">Valeur par défaut : 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="d29e4-216">Default: 30 mins.</span></span> <span data-ttu-id="d29e4-217">Nombre de minutes pour laquelle une réunion est effectuée</span><span class="sxs-lookup"><span data-stu-id="d29e4-217">Number of minutes for which a meeting would be conducted</span></span> |
| <span data-ttu-id="d29e4-218">place</span><span class="sxs-lookup"><span data-stu-id="d29e4-218">place</span></span> | <span data-ttu-id="d29e4-219">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="d29e4-219">JSON object</span></span> | <span data-ttu-id="d29e4-220">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-220">Yes</span></span> | <span data-ttu-id="d29e4-221">Emplacement de la réunion.</span><span class="sxs-lookup"><span data-stu-id="d29e4-221">Meeting Location.</span></span> <span data-ttu-id="d29e4-222">Contient les 3 composants : latitude, longitude, nom</span><span class="sxs-lookup"><span data-stu-id="d29e4-222">Contains 3 components: latitude, longitude, name</span></span>  |
| <span data-ttu-id="d29e4-223">ordre du jour</span><span class="sxs-lookup"><span data-stu-id="d29e4-223">agenda</span></span> | <span data-ttu-id="d29e4-224">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-224">String</span></span> | <span data-ttu-id="d29e4-225">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-225">Yes</span></span> | <span data-ttu-id="d29e4-226">L’ordre du jour de la réunion / Description de la réunion</span><span class="sxs-lookup"><span data-stu-id="d29e4-226">Agenda for the Meeting / Description for the meeting</span></span> |
| <span data-ttu-id="d29e4-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="d29e4-227">isSenderOnly</span></span> | <span data-ttu-id="d29e4-228">Bool</span><span class="sxs-lookup"><span data-stu-id="d29e4-228">Bool</span></span> | <span data-ttu-id="d29e4-229">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-229">Yes</span></span> | <span data-ttu-id="d29e4-230">Pour autoriser uniquement l’expéditeur afficher les rendez-vous résumé.</span><span class="sxs-lookup"><span data-stu-id="d29e4-230">For allowing only sender to view Let's Meet summary.</span></span> <span data-ttu-id="d29e4-231">Par défaut : false</span><span class="sxs-lookup"><span data-stu-id="d29e4-231">Default: false</span></span> |

###### <a name="sample-json-request-for-a-lets-meet-action"></a><span data-ttu-id="d29e4-232">Exemple de demande JSON pour un rendez-vous Action</span><span class="sxs-lookup"><span data-stu-id="d29e4-232">Sample JSON Request for a Let's Meet Action</span></span>

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

###### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="d29e4-233">actionBody pour un instance(id) de package enquête Action ou Action :</span><span class="sxs-lookup"><span data-stu-id="d29e4-233">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="d29e4-234">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-234">Parameter</span></span> | <span data-ttu-id="d29e4-235">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-235">Type</span></span> | <span data-ttu-id="d29e4-236">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-236">Optional?</span></span> | <span data-ttu-id="d29e4-237">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-237">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-238">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-238">title</span></span> | <span data-ttu-id="d29e4-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-239">String</span></span> | <span data-ttu-id="d29e4-240">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-240">No</span></span> | <span data-ttu-id="d29e4-241">Titre de la tâche</span><span class="sxs-lookup"><span data-stu-id="d29e4-241">Title of the Job</span></span> |
| <span data-ttu-id="d29e4-242">dueDate</span><span class="sxs-lookup"><span data-stu-id="d29e4-242">dueDate</span></span> | <span data-ttu-id="d29e4-243">long</span><span class="sxs-lookup"><span data-stu-id="d29e4-243">long</span></span> | <span data-ttu-id="d29e4-244">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-244">Yes</span></span> | <span data-ttu-id="d29e4-245">Par défaut : 24 heures.</span><span class="sxs-lookup"><span data-stu-id="d29e4-245">Default: 24hrs.</span></span> <span data-ttu-id="d29e4-246">Nombre d’heures avant laquelle le travail doit être terminé</span><span class="sxs-lookup"><span data-stu-id="d29e4-246">Number of hours before which job should be completed</span></span> |
| <span data-ttu-id="d29e4-247">é anonyme</span><span class="sxs-lookup"><span data-stu-id="d29e4-247">isAnonymous</span></span> | <span data-ttu-id="d29e4-248">Bool</span><span class="sxs-lookup"><span data-stu-id="d29e4-248">Bool</span></span> | <span data-ttu-id="d29e4-249">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-249">Yes</span></span> | <span data-ttu-id="d29e4-250">Pour autoriser les réponses de l’enquête anonyme.</span><span class="sxs-lookup"><span data-stu-id="d29e4-250">For allowing anonymous survey responses.</span></span> <span data-ttu-id="d29e4-251">Par défaut : false</span><span class="sxs-lookup"><span data-stu-id="d29e4-251">Default: false</span></span> |
| <span data-ttu-id="d29e4-252">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="d29e4-252">isSenderOnly</span></span> | <span data-ttu-id="d29e4-253">Bool</span><span class="sxs-lookup"><span data-stu-id="d29e4-253">Bool</span></span> | <span data-ttu-id="d29e4-254">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-254">Yes</span></span> | <span data-ttu-id="d29e4-255">Pour autoriser uniquement l’expéditeur afficher le résumé enquête.</span><span class="sxs-lookup"><span data-stu-id="d29e4-255">For allowing only sender to view survey summary.</span></span> <span data-ttu-id="d29e4-256">Par défaut : false</span><span class="sxs-lookup"><span data-stu-id="d29e4-256">Default: false</span></span> |
| <span data-ttu-id="d29e4-257">acceptMultipleResponses</span><span class="sxs-lookup"><span data-stu-id="d29e4-257">acceptMultipleResponses</span></span> | <span data-ttu-id="d29e4-258">Bool</span><span class="sxs-lookup"><span data-stu-id="d29e4-258">Bool</span></span> | <span data-ttu-id="d29e4-259">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-259">Yes</span></span> | <span data-ttu-id="d29e4-260">Pour autoriser plusieurs réponses à partir de la même répondeur.</span><span class="sxs-lookup"><span data-stu-id="d29e4-260">For allowing multiple responses from same responder.</span></span> <span data-ttu-id="d29e4-261">Par défaut : false</span><span class="sxs-lookup"><span data-stu-id="d29e4-261">Default: false</span></span> |
| <span data-ttu-id="d29e4-262">questions</span><span class="sxs-lookup"><span data-stu-id="d29e4-262">questions</span></span> | <span data-ttu-id="d29e4-263">object[]</span><span class="sxs-lookup"><span data-stu-id="d29e4-263">object[]</span></span> | <span data-ttu-id="d29e4-264">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-264">No</span></span> | <span data-ttu-id="d29e4-265">Chaque élément d’object [] est décrit ci-dessous en tant qu’objet Question</span><span class="sxs-lookup"><span data-stu-id="d29e4-265">Each element of object[] is described below as Question object</span></span> |
| <span data-ttu-id="d29e4-266">properties</span><span class="sxs-lookup"><span data-stu-id="d29e4-266">properties</span></span> | <span data-ttu-id="d29e4-267">object[]</span><span class="sxs-lookup"><span data-stu-id="d29e4-267">object[]</span></span> | <span data-ttu-id="d29e4-268">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-268">No</span></span> | <span data-ttu-id="d29e4-269">Chaque élément d’object [] est décrit ci-dessous en tant qu’objet Property.</span><span class="sxs-lookup"><span data-stu-id="d29e4-269">Each element of object[] is described below as Property Object.</span></span> <span data-ttu-id="d29e4-270">Valide uniquement pour la création d’Instance de Package de l’Action</span><span class="sxs-lookup"><span data-stu-id="d29e4-270">Only valid for creating Action Package Instance</span></span> |

###### <a name="structure-for-question-object"></a><span data-ttu-id="d29e4-271">Structure de l’objet Question</span><span class="sxs-lookup"><span data-stu-id="d29e4-271">Structure for Question object</span></span>

| <span data-ttu-id="d29e4-272">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-272">Parameter</span></span> | <span data-ttu-id="d29e4-273">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-273">Type</span></span> | <span data-ttu-id="d29e4-274">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-274">Optional?</span></span> | <span data-ttu-id="d29e4-275">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-276">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-276">title</span></span> | <span data-ttu-id="d29e4-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-277">String</span></span> | <span data-ttu-id="d29e4-278">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-278">No</span></span> | <span data-ttu-id="d29e4-279">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="d29e4-279">Title of the question</span></span> |
| <span data-ttu-id="d29e4-280">type</span><span class="sxs-lookup"><span data-stu-id="d29e4-280">type</span></span> | <span data-ttu-id="d29e4-281">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-281">String</span></span> | <span data-ttu-id="d29e4-282">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-282">No</span></span> | <span data-ttu-id="d29e4-283">Type de la question.</span><span class="sxs-lookup"><span data-stu-id="d29e4-283">Type of the question.</span></span> <span data-ttu-id="d29e4-284">Enum : SingleOption/MultiOption/texte/Image/numérique/Date/emplacement/AttachmentList</span><span class="sxs-lookup"><span data-stu-id="d29e4-284">Enum: SingleOption/MultiOption/Text/Image/Numeric/Date/Location/AttachmentList</span></span> |
| <span data-ttu-id="d29e4-285">isInvisible</span><span class="sxs-lookup"><span data-stu-id="d29e4-285">isInvisible</span></span> | <span data-ttu-id="d29e4-286">Bool</span><span class="sxs-lookup"><span data-stu-id="d29e4-286">Bool</span></span> | <span data-ttu-id="d29e4-287">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-287">Yes</span></span> | <span data-ttu-id="d29e4-288">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="d29e4-288">Default: false.</span></span> <span data-ttu-id="d29e4-289">Pour contrôler la visibilité de la question</span><span class="sxs-lookup"><span data-stu-id="d29e4-289">To control the visibility of the question</span></span> |
| <span data-ttu-id="d29e4-290">options</span><span class="sxs-lookup"><span data-stu-id="d29e4-290">options</span></span> | <span data-ttu-id="d29e4-291">object[]</span><span class="sxs-lookup"><span data-stu-id="d29e4-291">object[]</span></span> | <span data-ttu-id="d29e4-292">Oui</span><span class="sxs-lookup"><span data-stu-id="d29e4-292">Yes</span></span> | <span data-ttu-id="d29e4-293">Obligatoire pour le type de question SingleOption et MultiOption.</span><span class="sxs-lookup"><span data-stu-id="d29e4-293">Mandatory for SingleOption and MultiOption question type.</span></span> <span data-ttu-id="d29e4-294">chaque élément d’object [] est décrit ci-dessous en tant qu’Option, objet</span><span class="sxs-lookup"><span data-stu-id="d29e4-294">each element of object[] is described below as Option object</span></span> |

###### <a name="structure-for-option-object"></a><span data-ttu-id="d29e4-295">Structure d’Option, objet</span><span class="sxs-lookup"><span data-stu-id="d29e4-295">Structure for Option object</span></span>

| <span data-ttu-id="d29e4-296">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-296">Parameter</span></span> | <span data-ttu-id="d29e4-297">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-297">Type</span></span> | <span data-ttu-id="d29e4-298">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-298">Optional?</span></span> | <span data-ttu-id="d29e4-299">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-299">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-300">title</span><span class="sxs-lookup"><span data-stu-id="d29e4-300">title</span></span> | <span data-ttu-id="d29e4-301">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-301">String</span></span> | <span data-ttu-id="d29e4-302">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-302">No</span></span> | <span data-ttu-id="d29e4-303">Titre de l’Option</span><span class="sxs-lookup"><span data-stu-id="d29e4-303">Title of the Option</span></span> |

###### <a name="structure-for-property-object"></a><span data-ttu-id="d29e4-304">Structure de l’objet Property</span><span class="sxs-lookup"><span data-stu-id="d29e4-304">Structure for Property object</span></span>

| <span data-ttu-id="d29e4-305">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-305">Parameter</span></span> | <span data-ttu-id="d29e4-306">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-306">Type</span></span> | <span data-ttu-id="d29e4-307">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="d29e4-307">Optional?</span></span> | <span data-ttu-id="d29e4-308">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-308">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="d29e4-309">name</span><span class="sxs-lookup"><span data-stu-id="d29e4-309">name</span></span> | <span data-ttu-id="d29e4-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-310">String</span></span> | <span data-ttu-id="d29e4-311">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-311">No</span></span> | <span data-ttu-id="d29e4-312">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="d29e4-312">Name of the property</span></span> |
| <span data-ttu-id="d29e4-313">type</span><span class="sxs-lookup"><span data-stu-id="d29e4-313">type</span></span> | <span data-ttu-id="d29e4-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-314">String</span></span> | <span data-ttu-id="d29e4-315">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-315">No</span></span> | <span data-ttu-id="d29e4-316">Type de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d29e4-316">Type of the property.</span></span> <span data-ttu-id="d29e4-317">Enum : Texte, numérique, emplacement, DateTime, StringList, pièce jointe, StringSet, AttachmentList</span><span class="sxs-lookup"><span data-stu-id="d29e4-317">Enum: Text, Numeric, Location, DateTime, StringList, Attachment, StringSet, AttachmentList</span></span> |
| <span data-ttu-id="d29e4-318">value</span><span class="sxs-lookup"><span data-stu-id="d29e4-318">value</span></span> | <span data-ttu-id="d29e4-319">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-319">String</span></span> | <span data-ttu-id="d29e4-320">Non</span><span class="sxs-lookup"><span data-stu-id="d29e4-320">No</span></span> | <span data-ttu-id="d29e4-321">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d29e4-321">Value of the property</span></span> |

###### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="d29e4-322">Exemple de demande JSON pour une Action de l’enquête</span><span class="sxs-lookup"><span data-stu-id="d29e4-322">Sample JSON Request for a Survey Action</span></span>

```javascript
{
  actionType: "Survey",
  actionBody: {
    isAnonymous:false,
    isSenderOnly:false,
    acceptMultipleResponses:true,
    dueDate:10,
    title: "A test survey!!",
    questions: [
        {
            title: "a test question written here",
            type: "Text"
        },
        {
            title: "Single select question",
            type: "SingleOption",
            options: [{title:"Opt1"},{title:"Opt2"}]
        },
        {
            title: "Multi select question",
            type: "MultiOption",
            options: [{title:"MOpt1"},{title:"MOpt2"},{title:"MOpt3"}]
        },
        {
            title: "Numeric question",
            type: "Numeric"
        },
        {
            title: "Location question",
            type: "Location"
        },
        {
            title: "DateTime question",
            type: "DateTime"
        },
        {
            title: "Image question",
            type: "Image"
        }
        ]
  }
}
```

###### <a name="response-body"></a><span data-ttu-id="d29e4-323">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="d29e4-323">Response body</span></span>

| <span data-ttu-id="d29e4-324">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d29e4-324">Parameter</span></span> | <span data-ttu-id="d29e4-325">Type</span><span class="sxs-lookup"><span data-stu-id="d29e4-325">Type</span></span> | <span data-ttu-id="d29e4-326">Description</span><span class="sxs-lookup"><span data-stu-id="d29e4-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d29e4-327">referenceId</span><span class="sxs-lookup"><span data-stu-id="d29e4-327">referenceId</span></span> | <span data-ttu-id="d29e4-328">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-328">String</span></span> | <span data-ttu-id="d29e4-329">Identificateur de demande</span><span class="sxs-lookup"><span data-stu-id="d29e4-329">Request identifier</span></span> |
| <span data-ttu-id="d29e4-330">actionId</span><span class="sxs-lookup"><span data-stu-id="d29e4-330">actionId</span></span> | <span data-ttu-id="d29e4-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29e4-331">String</span></span> | <span data-ttu-id="d29e4-332">Identificateur d’action</span><span class="sxs-lookup"><span data-stu-id="d29e4-332">Action identifier</span></span> |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
