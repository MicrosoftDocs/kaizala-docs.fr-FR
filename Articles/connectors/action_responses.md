---
title: /Responses
description: Article de référence de l’API obtenir des données de réponse pour les Actions Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 7eee4d159fa932bec1e949ea6fd2b558d2154e7b
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399370"
---
# <a name="post-response-to-an-action"></a><span data-ttu-id="1938d-103">Réponse à une Action</span><span class="sxs-lookup"><span data-stu-id="1938d-103">Post response to an Action</span></span>
## <a name="post-responses"></a><span data-ttu-id="1938d-104">/Responses POST</span><span class="sxs-lookup"><span data-stu-id="1938d-104">POST /responses</span></span>

    POST {endpoint-url}/groups/{groupId}/actions/{actionId}/responses

### <a name="request-parameters"></a><span data-ttu-id="1938d-105">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="1938d-105">Request Parameters</span></span>

|  | <span data-ttu-id="1938d-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-106">Parameter</span></span> | <span data-ttu-id="1938d-107">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-107">Type</span></span> | <span data-ttu-id="1938d-108">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="1938d-108">Optional?</span></span> | <span data-ttu-id="1938d-109">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="1938d-110">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="1938d-110">URL Path Parameter</span></span> | <span data-ttu-id="1938d-111">groupId</span><span class="sxs-lookup"><span data-stu-id="1938d-111">groupId</span></span> | <span data-ttu-id="1938d-112">String</span><span class="sxs-lookup"><span data-stu-id="1938d-112">String</span></span> | <span data-ttu-id="1938d-113">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-113">No</span></span> | <span data-ttu-id="1938d-114">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="1938d-114">Group Identifier</span></span> |
| <span data-ttu-id="1938d-115">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="1938d-115">URL Path Parameter</span></span> | <span data-ttu-id="1938d-116">actionId</span><span class="sxs-lookup"><span data-stu-id="1938d-116">actionId</span></span> | <span data-ttu-id="1938d-117">String</span><span class="sxs-lookup"><span data-stu-id="1938d-117">String</span></span> | <span data-ttu-id="1938d-118">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-118">No</span></span> | <span data-ttu-id="1938d-119">Identificateur d’action</span><span class="sxs-lookup"><span data-stu-id="1938d-119">Action Identifier</span></span> |
| <span data-ttu-id="1938d-120">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1938d-120">HTTP Header</span></span> | <span data-ttu-id="1938d-121">accessToken</span><span class="sxs-lookup"><span data-stu-id="1938d-121">accessToken</span></span> | <span data-ttu-id="1938d-122">String</span><span class="sxs-lookup"><span data-stu-id="1938d-122">String</span></span> | <span data-ttu-id="1938d-123">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-123">No</span></span> | <span data-ttu-id="1938d-124">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="1938d-124">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="1938d-125">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="1938d-125">HTTP Header</span></span> | <span data-ttu-id="1938d-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1938d-126">Content-Type</span></span> | <span data-ttu-id="1938d-127">String</span><span class="sxs-lookup"><span data-stu-id="1938d-127">String</span></span> | <span data-ttu-id="1938d-128">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-128">No</span></span> | <span data-ttu-id="1938d-129">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="1938d-129">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="1938d-130">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="1938d-130">Request body</span></span>

| <span data-ttu-id="1938d-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-131">Parameter</span></span> | <span data-ttu-id="1938d-132">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-132">Type</span></span> | <span data-ttu-id="1938d-133">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1938d-134">id</span><span class="sxs-lookup"><span data-stu-id="1938d-134">id</span></span> | <span data-ttu-id="1938d-135">String</span><span class="sxs-lookup"><span data-stu-id="1938d-135">String</span></span> | <span data-ttu-id="1938d-136">ID du package Kaizala Action.</span><span class="sxs-lookup"><span data-stu-id="1938d-136">Id of the Kaizala Action package.</span></span> <span data-ttu-id="1938d-137">ActionType ou Id doit être spécifiée</span><span class="sxs-lookup"><span data-stu-id="1938d-137">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="1938d-138">actionType</span><span class="sxs-lookup"><span data-stu-id="1938d-138">actionType</span></span> | <span data-ttu-id="1938d-139">String</span><span class="sxs-lookup"><span data-stu-id="1938d-139">String</span></span> | <span data-ttu-id="1938d-140">Enum « Enquête » / « Du travail ».</span><span class="sxs-lookup"><span data-stu-id="1938d-140">Enum "Survey"/"Job".</span></span> <span data-ttu-id="1938d-141">ActionType ou Id doit être spécifiée</span><span class="sxs-lookup"><span data-stu-id="1938d-141">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="1938d-142">responseId</span><span class="sxs-lookup"><span data-stu-id="1938d-142">responseId</span></span> | <span data-ttu-id="1938d-143">String</span><span class="sxs-lookup"><span data-stu-id="1938d-143">String</span></span> | <span data-ttu-id="1938d-144">Pour mettre à jour la réponse existante</span><span class="sxs-lookup"><span data-stu-id="1938d-144">For updating existing response</span></span> |
| <span data-ttu-id="1938d-145">actionBody</span><span class="sxs-lookup"><span data-stu-id="1938d-145">actionBody</span></span> | <span data-ttu-id="1938d-146">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="1938d-146">JSON Object</span></span> | <span data-ttu-id="1938d-147">Objet représentant les données nécessaires pour l’Action respectif.</span><span class="sxs-lookup"><span data-stu-id="1938d-147">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="1938d-148">Paramètres définis ci-dessous pour chacune des Actions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1938d-148">Parameters defined below for each of the supported Actions.</span></span> |

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="1938d-149">actionBody pour une Action de tâche</span><span class="sxs-lookup"><span data-stu-id="1938d-149">actionBody for a Job Action</span></span>

| <span data-ttu-id="1938d-150">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-150">Parameter</span></span> | <span data-ttu-id="1938d-151">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-151">Type</span></span> | <span data-ttu-id="1938d-152">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="1938d-152">Optional?</span></span> | <span data-ttu-id="1938d-153">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-153">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="1938d-154">isCompleted</span><span class="sxs-lookup"><span data-stu-id="1938d-154">isCompleted</span></span> | <span data-ttu-id="1938d-155">Bool</span><span class="sxs-lookup"><span data-stu-id="1938d-155">Bool</span></span> | <span data-ttu-id="1938d-156">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-156">No</span></span> | <span data-ttu-id="1938d-157">Marque la tâche comme étant achevée</span><span class="sxs-lookup"><span data-stu-id="1938d-157">Mark the job as completed</span></span> |


##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="1938d-158">Exemple de demande JSON pour une Action de tâche</span><span class="sxs-lookup"><span data-stu-id="1938d-158">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        isCompleted : true
    }
}
```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="1938d-159">actionBody pour un instance(id) de package enquête Action ou Action :</span><span class="sxs-lookup"><span data-stu-id="1938d-159">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="1938d-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-160">Parameter</span></span> | <span data-ttu-id="1938d-161">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-161">Type</span></span> | <span data-ttu-id="1938d-162">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="1938d-162">Optional?</span></span> | <span data-ttu-id="1938d-163">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="1938d-164">responseName</span><span class="sxs-lookup"><span data-stu-id="1938d-164">responseName</span></span> | <span data-ttu-id="1938d-165">String</span><span class="sxs-lookup"><span data-stu-id="1938d-165">String</span></span> | <span data-ttu-id="1938d-166">Oui</span><span class="sxs-lookup"><span data-stu-id="1938d-166">Yes</span></span> | <span data-ttu-id="1938d-167">Pour identifier une réponse</span><span class="sxs-lookup"><span data-stu-id="1938d-167">For uniquely identifying a response</span></span> |
| <span data-ttu-id="1938d-168">responseLocation</span><span class="sxs-lookup"><span data-stu-id="1938d-168">responseLocation</span></span> | <span data-ttu-id="1938d-169">Objet Location</span><span class="sxs-lookup"><span data-stu-id="1938d-169">Location object</span></span> | <span data-ttu-id="1938d-170">Oui</span><span class="sxs-lookup"><span data-stu-id="1938d-170">Yes</span></span> | <span data-ttu-id="1938d-171">Pour identifier l’emplacement de la réponse</span><span class="sxs-lookup"><span data-stu-id="1938d-171">For identifying response's location</span></span> |
| <span data-ttu-id="1938d-172">réponses</span><span class="sxs-lookup"><span data-stu-id="1938d-172">answers</span></span> | <span data-ttu-id="1938d-173">object[]</span><span class="sxs-lookup"><span data-stu-id="1938d-173">object[]</span></span> | <span data-ttu-id="1938d-174">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-174">No</span></span> | <span data-ttu-id="1938d-175">Réponse de chaque question (basée sur un index).</span><span class="sxs-lookup"><span data-stu-id="1938d-175">Answer of each question(based on index).</span></span> <span data-ttu-id="1938d-176">objet sera de type chaîne pour le type de question : Text/SingleOption/Image, objet sera de type string [] type de question : MultiOption/AttachmentList, objet sera de type double pour le type de question : numérique/Date</span><span class="sxs-lookup"><span data-stu-id="1938d-176">object will be of type string for question type: SingleOption/Text/Image, object will be of type string[] for question type: MultiOption/AttachmentList, object will be of type double for question type: Numeric/Date</span></span> |

##### <a name="structure-for-location-object"></a><span data-ttu-id="1938d-177">Structure de l’objet d’emplacement</span><span class="sxs-lookup"><span data-stu-id="1938d-177">Structure for Location object</span></span>

| <span data-ttu-id="1938d-178">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-178">Parameter</span></span> | <span data-ttu-id="1938d-179">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-179">Type</span></span> | <span data-ttu-id="1938d-180">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="1938d-180">Optional?</span></span> | <span data-ttu-id="1938d-181">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-181">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="1938d-182">latitude</span><span class="sxs-lookup"><span data-stu-id="1938d-182">latitude</span></span> | <span data-ttu-id="1938d-183">Double</span><span class="sxs-lookup"><span data-stu-id="1938d-183">Double</span></span> | <span data-ttu-id="1938d-184">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-184">No</span></span> | <span data-ttu-id="1938d-185">Latitude de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="1938d-185">Latitude of the location</span></span> |
| <span data-ttu-id="1938d-186">longitude</span><span class="sxs-lookup"><span data-stu-id="1938d-186">longitude</span></span> | <span data-ttu-id="1938d-187">Double</span><span class="sxs-lookup"><span data-stu-id="1938d-187">Double</span></span> | <span data-ttu-id="1938d-188">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-188">No</span></span> | <span data-ttu-id="1938d-189">Longitude de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="1938d-189">Longitude of the location</span></span> |
| <span data-ttu-id="1938d-190">name</span><span class="sxs-lookup"><span data-stu-id="1938d-190">name</span></span> | <span data-ttu-id="1938d-191">String</span><span class="sxs-lookup"><span data-stu-id="1938d-191">String</span></span> | <span data-ttu-id="1938d-192">Non</span><span class="sxs-lookup"><span data-stu-id="1938d-192">No</span></span> | <span data-ttu-id="1938d-193">Nom de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="1938d-193">Name of the location</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="1938d-194">Exemple de demande JSON pour une Action de l’enquête</span><span class="sxs-lookup"><span data-stu-id="1938d-194">Sample JSON Request for a Survey Action</span></span>

```javascript
{
  "actionType" : "Survey",
  "actionBody" : 
  {
    "responseName" : "API response",
    "responseLocation" : 
    {
      "latitude" : 1, 
      "longitude" : 1, 
      "name" : "locationName234"
    },
    "Answers" : ["Response from API", "Opt1", ["MOpt1","MOpt2"],123,{"lt" : 1, "lg" : 1, "n":"cool"}, 1500377471, "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="]
  }
}
```
<span data-ttu-id="1938d-195">Vous devez télécharger l’image (v1/support api), puis utiliser mediaResource de la réponse comme réponse à la question de type Image.</span><span class="sxs-lookup"><span data-stu-id="1938d-195">You need to upload image (v1/media api) and then use mediaResource of the response as answer to Image type question.</span></span>

#### <a name="response-body"></a><span data-ttu-id="1938d-196">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="1938d-196">Response body</span></span>

| <span data-ttu-id="1938d-197">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1938d-197">Parameter</span></span> | <span data-ttu-id="1938d-198">Type</span><span class="sxs-lookup"><span data-stu-id="1938d-198">Type</span></span> | <span data-ttu-id="1938d-199">Description</span><span class="sxs-lookup"><span data-stu-id="1938d-199">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="1938d-200">responseId</span><span class="sxs-lookup"><span data-stu-id="1938d-200">responseId</span></span> | <span data-ttu-id="1938d-201">String</span><span class="sxs-lookup"><span data-stu-id="1938d-201">String</span></span> | <span data-ttu-id="1938d-202">Identificateur de réponse.</span><span class="sxs-lookup"><span data-stu-id="1938d-202">Response Identifier.</span></span> <span data-ttu-id="1938d-203">Vous permet de réponse de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1938d-203">Can you be used for updating response</span></span> |

```javascript
{
    "responseId": "bbcf469e-4027-40b7-a80b-a961a48619e7"
}
```
