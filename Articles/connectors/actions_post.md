---
title: /Actions_post
description: Article de référence pour l'API de publication d'une action sur un groupe Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 5ca7c92f76a0e0e18025dda2526b53515a003e90
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190741"
---
# <a name="post-a-action-in-a-group"></a><span data-ttu-id="f091a-103">Publier une action dans un groupe</span><span class="sxs-lookup"><span data-stu-id="f091a-103">Post a Action in a group</span></span>
## <a name="post-actions"></a><span data-ttu-id="f091a-104">POST/actions</span><span class="sxs-lookup"><span data-stu-id="f091a-104">POST /actions</span></span>

    POST {endpoint-url}/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="f091a-105">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="f091a-105">Request Parameters</span></span>

|  | <span data-ttu-id="f091a-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-106">Parameter</span></span> | <span data-ttu-id="f091a-107">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-107">Type</span></span> | <span data-ttu-id="f091a-108">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-108">Optional?</span></span> | <span data-ttu-id="f091a-109">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-110">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="f091a-110">URL Path Parameter</span></span> | <span data-ttu-id="f091a-111">groupId</span><span class="sxs-lookup"><span data-stu-id="f091a-111">groupId</span></span> | <span data-ttu-id="f091a-112">String</span><span class="sxs-lookup"><span data-stu-id="f091a-112">String</span></span> | <span data-ttu-id="f091a-113">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-113">No</span></span> | <span data-ttu-id="f091a-114">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="f091a-114">Group Identifier</span></span> |
| <span data-ttu-id="f091a-115">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="f091a-115">HTTP Header</span></span> | <span data-ttu-id="f091a-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="f091a-116">accessToken</span></span> | <span data-ttu-id="f091a-117">String</span><span class="sxs-lookup"><span data-stu-id="f091a-117">String</span></span> | <span data-ttu-id="f091a-118">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-118">No</span></span> | <span data-ttu-id="f091a-119">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="f091a-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="f091a-120">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="f091a-120">HTTP Header</span></span> | <span data-ttu-id="f091a-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f091a-121">Content-Type</span></span> | <span data-ttu-id="f091a-122">String</span><span class="sxs-lookup"><span data-stu-id="f091a-122">String</span></span> | <span data-ttu-id="f091a-123">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-123">No</span></span> | <span data-ttu-id="f091a-124">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="f091a-124">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="f091a-125">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f091a-125">Request body</span></span>

| <span data-ttu-id="f091a-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-126">Parameter</span></span> | <span data-ttu-id="f091a-127">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-127">Type</span></span> | <span data-ttu-id="f091a-128">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-128">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f091a-129">id</span><span class="sxs-lookup"><span data-stu-id="f091a-129">id</span></span> | <span data-ttu-id="f091a-130">String</span><span class="sxs-lookup"><span data-stu-id="f091a-130">String</span></span> | <span data-ttu-id="f091a-131">ID du package d'action Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f091a-131">Id of the Kaizala Action package.</span></span> <span data-ttu-id="f091a-132">L'un des actionType ou l'ID doit être spécifié</span><span class="sxs-lookup"><span data-stu-id="f091a-132">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="f091a-133">actionType</span><span class="sxs-lookup"><span data-stu-id="f091a-133">actionType</span></span> | <span data-ttu-id="f091a-134">String</span><span class="sxs-lookup"><span data-stu-id="f091a-134">String</span></span> | <span data-ttu-id="f091a-135">Enum «Survey»/«Job».</span><span class="sxs-lookup"><span data-stu-id="f091a-135">Enum "Survey"/"Job".</span></span> <span data-ttu-id="f091a-136">L'un des actionType ou l'ID doit être spécifié</span><span class="sxs-lookup"><span data-stu-id="f091a-136">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="f091a-137">actionBody</span><span class="sxs-lookup"><span data-stu-id="f091a-137">actionBody</span></span> | <span data-ttu-id="f091a-138">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="f091a-138">JSON Object</span></span> | <span data-ttu-id="f091a-139">Objet représentant les données nécessaires pour l'action correspondante.</span><span class="sxs-lookup"><span data-stu-id="f091a-139">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="f091a-140">Paramètres définis ci-dessous pour chacune des actions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f091a-140">Parameters defined below for each of the supported Actions.</span></span> |


#### <a name="actionbody-for-an-announcement-action"></a><span data-ttu-id="f091a-141">actionBody pour une action d'annonce</span><span class="sxs-lookup"><span data-stu-id="f091a-141">actionBody for an Announcement Action</span></span>

| <span data-ttu-id="f091a-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-142">Parameter</span></span> | <span data-ttu-id="f091a-143">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-143">Type</span></span> | <span data-ttu-id="f091a-144">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-144">Optional?</span></span> | <span data-ttu-id="f091a-145">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-145">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-146">title</span><span class="sxs-lookup"><span data-stu-id="f091a-146">title</span></span> | <span data-ttu-id="f091a-147">String</span><span class="sxs-lookup"><span data-stu-id="f091a-147">String</span></span> | <span data-ttu-id="f091a-148">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-148">No</span></span> | <span data-ttu-id="f091a-149">Titre de l'annonce</span><span class="sxs-lookup"><span data-stu-id="f091a-149">Title of the Announcement</span></span> |
| <span data-ttu-id="f091a-150">MediaResources</span><span class="sxs-lookup"><span data-stu-id="f091a-150">MediaResources</span></span> | <span data-ttu-id="f091a-151">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="f091a-151">String[]</span></span> | <span data-ttu-id="f091a-152">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-152">Yes</span></span> | <span data-ttu-id="f091a-153">Tableau des ressources multimédias</span><span class="sxs-lookup"><span data-stu-id="f091a-153">Array of media resources</span></span> |
| <span data-ttu-id="f091a-154">Message</span><span class="sxs-lookup"><span data-stu-id="f091a-154">Message</span></span> | <span data-ttu-id="f091a-155">String</span><span class="sxs-lookup"><span data-stu-id="f091a-155">String</span></span> | <span data-ttu-id="f091a-156">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-156">No</span></span> | <span data-ttu-id="f091a-157">Corps du message</span><span class="sxs-lookup"><span data-stu-id="f091a-157">Message Body</span></span> |

#### <a name="sample-json-request-for-an-announcement-action"></a><span data-ttu-id="f091a-158">Exemple de demande JSON pour une action d'annonce</span><span class="sxs-lookup"><span data-stu-id="f091a-158">Sample JSON Request for an Announcement Action</span></span>

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

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="f091a-159">actionBody pour une action de travail</span><span class="sxs-lookup"><span data-stu-id="f091a-159">actionBody for a Job Action</span></span>

| <span data-ttu-id="f091a-160">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-160">Parameter</span></span> | <span data-ttu-id="f091a-161">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-161">Type</span></span> | <span data-ttu-id="f091a-162">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-162">Optional?</span></span> | <span data-ttu-id="f091a-163">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-164">title</span><span class="sxs-lookup"><span data-stu-id="f091a-164">title</span></span> | <span data-ttu-id="f091a-165">String</span><span class="sxs-lookup"><span data-stu-id="f091a-165">String</span></span> | <span data-ttu-id="f091a-166">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-166">No</span></span> | <span data-ttu-id="f091a-167">Titre du travail</span><span class="sxs-lookup"><span data-stu-id="f091a-167">Title of the Job</span></span> |
| <span data-ttu-id="f091a-168">assignedTo</span><span class="sxs-lookup"><span data-stu-id="f091a-168">assignedTo</span></span> | <span data-ttu-id="f091a-169">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="f091a-169">String[]</span></span> | <span data-ttu-id="f091a-170">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-170">No</span></span> | <span data-ttu-id="f091a-171">Titre du travail</span><span class="sxs-lookup"><span data-stu-id="f091a-171">Title of the Job</span></span> |
| <span data-ttu-id="f091a-172">dueDate</span><span class="sxs-lookup"><span data-stu-id="f091a-172">dueDate</span></span> | <span data-ttu-id="f091a-173">long</span><span class="sxs-lookup"><span data-stu-id="f091a-173">long</span></span> | <span data-ttu-id="f091a-174">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-174">Yes</span></span> | <span data-ttu-id="f091a-175">Valeur par défaut: 24 heures.</span><span class="sxs-lookup"><span data-stu-id="f091a-175">Default: 24hrs.</span></span> <span data-ttu-id="f091a-176">Nombre d'heures avant laquelle le travail doit être effectué</span><span class="sxs-lookup"><span data-stu-id="f091a-176">Number of hours before which job should be completed</span></span> |

##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="f091a-177">Exemple de demande JSON pour une action de travail</span><span class="sxs-lookup"><span data-stu-id="f091a-177">Sample JSON Request for a Job Action</span></span>

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

#### <a name="actionbody-for-a-poll-action"></a><span data-ttu-id="f091a-178">actionBody pour une action de sondage</span><span class="sxs-lookup"><span data-stu-id="f091a-178">actionBody for a Poll Action</span></span>

| <span data-ttu-id="f091a-179">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-179">Parameter</span></span> | <span data-ttu-id="f091a-180">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-180">Type</span></span> | <span data-ttu-id="f091a-181">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-181">Optional?</span></span> | <span data-ttu-id="f091a-182">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-182">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-183">relative</span><span class="sxs-lookup"><span data-stu-id="f091a-183">question</span></span> | <span data-ttu-id="f091a-184">String</span><span class="sxs-lookup"><span data-stu-id="f091a-184">String</span></span> | <span data-ttu-id="f091a-185">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-185">No</span></span> | <span data-ttu-id="f091a-186">Question de sondage</span><span class="sxs-lookup"><span data-stu-id="f091a-186">Poll Question</span></span> |
| <span data-ttu-id="f091a-187">Choix</span><span class="sxs-lookup"><span data-stu-id="f091a-187">Choices</span></span> | <span data-ttu-id="f091a-188">Tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f091a-188">Json Array</span></span> | <span data-ttu-id="f091a-189">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-189">No</span></span> | <span data-ttu-id="f091a-190">Options disponibles pour le sondage.</span><span class="sxs-lookup"><span data-stu-id="f091a-190">Choices available for the poll.</span></span> <span data-ttu-id="f091a-191">Chaque choix comporte le composant suivant:</span><span class="sxs-lookup"><span data-stu-id="f091a-191">Each Choice have below component:</span></span> <ol><li><span data-ttu-id="f091a-192">title (obligatoire & dans le format de chaîne)</span><span class="sxs-lookup"><span data-stu-id="f091a-192">title (Mandatory & in String format)</span></span> </li><li><span data-ttu-id="f091a-193">image (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f091a-193">image (optional)</span></span></li></ol> |
| <span data-ttu-id="f091a-194">expiryInHours</span><span class="sxs-lookup"><span data-stu-id="f091a-194">expiryInHours</span></span> | <span data-ttu-id="f091a-195">Entier</span><span class="sxs-lookup"><span data-stu-id="f091a-195">Integer</span></span> | <span data-ttu-id="f091a-196">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-196">Yes</span></span> | <span data-ttu-id="f091a-197">Valeur par défaut: 720.</span><span class="sxs-lookup"><span data-stu-id="f091a-197">Default:720.</span></span> <span data-ttu-id="f091a-198">Nombre d'heures pendant lesquelles une interrogation gven a expiré.</span><span class="sxs-lookup"><span data-stu-id="f091a-198">Number of hours in which a gven poll would expire</span></span> |

##### <a name="sample-json-request-for-a-poll-action"></a><span data-ttu-id="f091a-199">Exemple de requête JSON pour une action de sondage</span><span class="sxs-lookup"><span data-stu-id="f091a-199">Sample JSON Request for a Poll Action</span></span>

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
#### <a name="actionbody-for-a-lets-meet-action"></a><span data-ttu-id="f091a-200">actionBody pour une action de réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-200">actionBody for a Let's Meet Action</span></span>

| <span data-ttu-id="f091a-201">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-201">Parameter</span></span> | <span data-ttu-id="f091a-202">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-202">Type</span></span> | <span data-ttu-id="f091a-203">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-203">Optional?</span></span> | <span data-ttu-id="f091a-204">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-204">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-205">title</span><span class="sxs-lookup"><span data-stu-id="f091a-205">title</span></span> | <span data-ttu-id="f091a-206">String</span><span class="sxs-lookup"><span data-stu-id="f091a-206">String</span></span> | <span data-ttu-id="f091a-207">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-207">No</span></span> | <span data-ttu-id="f091a-208">Titre de la demande de réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-208">Title of the Meeting Request</span></span>  |
| <span data-ttu-id="f091a-209">startingTime</span><span class="sxs-lookup"><span data-stu-id="f091a-209">startingTime</span></span> | <span data-ttu-id="f091a-210">DateTime
</span><span class="sxs-lookup"><span data-stu-id="f091a-210">DateTime</span></span> | <span data-ttu-id="f091a-211">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-211">No</span></span> | <span data-ttu-id="f091a-212">Heure de début de la réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-212">Starting time for the meeting</span></span> |
| <span data-ttu-id="f091a-213">DurationInMins</span><span class="sxs-lookup"><span data-stu-id="f091a-213">DurationInMins</span></span> | <span data-ttu-id="f091a-214">Entier</span><span class="sxs-lookup"><span data-stu-id="f091a-214">Integer</span></span> | <span data-ttu-id="f091a-215">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-215">No</span></span> | <span data-ttu-id="f091a-216">Valeur par défaut: 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="f091a-216">Default: 30 mins.</span></span> <span data-ttu-id="f091a-217">Nombre de minutes pendant lesquelles une réunion est effectuée</span><span class="sxs-lookup"><span data-stu-id="f091a-217">Number of minutes for which a meeting would be conducted</span></span> |
| <span data-ttu-id="f091a-218">positionnement</span><span class="sxs-lookup"><span data-stu-id="f091a-218">place</span></span> | <span data-ttu-id="f091a-219">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="f091a-219">JSON object</span></span> | <span data-ttu-id="f091a-220">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-220">Yes</span></span> | <span data-ttu-id="f091a-221">Emplacement de la réunion.</span><span class="sxs-lookup"><span data-stu-id="f091a-221">Meeting Location.</span></span> <span data-ttu-id="f091a-222">Contient 3 composants: Latitude, longitude, nom</span><span class="sxs-lookup"><span data-stu-id="f091a-222">Contains 3 components: latitude, longitude, name</span></span>  |
| <span data-ttu-id="f091a-223">réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-223">agenda</span></span> | <span data-ttu-id="f091a-224">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-224">String</span></span> | <span data-ttu-id="f091a-225">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-225">Yes</span></span> | <span data-ttu-id="f091a-226">Ordre du jour de la réunion/Description de la réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-226">Agenda for the Meeting / Description for the meeting</span></span> |
| <span data-ttu-id="f091a-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="f091a-227">isSenderOnly</span></span> | <span data-ttu-id="f091a-228">Bool</span><span class="sxs-lookup"><span data-stu-id="f091a-228">Bool</span></span> | <span data-ttu-id="f091a-229">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-229">Yes</span></span> | <span data-ttu-id="f091a-230">Pour autoriser uniquement l'expéditeur à consulter le résumé de la réunion.</span><span class="sxs-lookup"><span data-stu-id="f091a-230">For allowing only sender to view Let's Meet summary.</span></span> <span data-ttu-id="f091a-231">Valeur par défaut: false</span><span class="sxs-lookup"><span data-stu-id="f091a-231">Default: false</span></span> |

##### <a name="sample-json-request-for-a-lets-meet-action"></a><span data-ttu-id="f091a-232">Exemple de demande JSON pour une action de réunion</span><span class="sxs-lookup"><span data-stu-id="f091a-232">Sample JSON Request for a Let's Meet Action</span></span>

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="f091a-233">actionBody pour une action d'enquête ou une instance de package d'action (ID):</span><span class="sxs-lookup"><span data-stu-id="f091a-233">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="f091a-234">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-234">Parameter</span></span> | <span data-ttu-id="f091a-235">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-235">Type</span></span> | <span data-ttu-id="f091a-236">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-236">Optional?</span></span> | <span data-ttu-id="f091a-237">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-237">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-238">title</span><span class="sxs-lookup"><span data-stu-id="f091a-238">title</span></span> | <span data-ttu-id="f091a-239">String</span><span class="sxs-lookup"><span data-stu-id="f091a-239">String</span></span> | <span data-ttu-id="f091a-240">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-240">No</span></span> | <span data-ttu-id="f091a-241">Titre du travail</span><span class="sxs-lookup"><span data-stu-id="f091a-241">Title of the Job</span></span> |
| <span data-ttu-id="f091a-242">dueDate</span><span class="sxs-lookup"><span data-stu-id="f091a-242">dueDate</span></span> | <span data-ttu-id="f091a-243">long</span><span class="sxs-lookup"><span data-stu-id="f091a-243">long</span></span> | <span data-ttu-id="f091a-244">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-244">Yes</span></span> | <span data-ttu-id="f091a-245">Valeur par défaut: 24 heures.</span><span class="sxs-lookup"><span data-stu-id="f091a-245">Default: 24hrs.</span></span> <span data-ttu-id="f091a-246">Nombre d'heures avant laquelle le travail doit être effectué</span><span class="sxs-lookup"><span data-stu-id="f091a-246">Number of hours before which job should be completed</span></span> |
| <span data-ttu-id="f091a-247">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="f091a-247">isAnonymous</span></span> | <span data-ttu-id="f091a-248">Bool</span><span class="sxs-lookup"><span data-stu-id="f091a-248">Bool</span></span> | <span data-ttu-id="f091a-249">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-249">Yes</span></span> | <span data-ttu-id="f091a-250">Pour autoriser les réponses d'enquête anonymes.</span><span class="sxs-lookup"><span data-stu-id="f091a-250">For allowing anonymous survey responses.</span></span> <span data-ttu-id="f091a-251">Valeur par défaut: false</span><span class="sxs-lookup"><span data-stu-id="f091a-251">Default: false</span></span> |
| <span data-ttu-id="f091a-252">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="f091a-252">isSenderOnly</span></span> | <span data-ttu-id="f091a-253">Bool</span><span class="sxs-lookup"><span data-stu-id="f091a-253">Bool</span></span> | <span data-ttu-id="f091a-254">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-254">Yes</span></span> | <span data-ttu-id="f091a-255">Pour autoriser uniquement l'expéditeur à afficher le résumé de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="f091a-255">For allowing only sender to view survey summary.</span></span> <span data-ttu-id="f091a-256">Valeur par défaut: false</span><span class="sxs-lookup"><span data-stu-id="f091a-256">Default: false</span></span> |
| <span data-ttu-id="f091a-257">acceptMultipleResponses</span><span class="sxs-lookup"><span data-stu-id="f091a-257">acceptMultipleResponses</span></span> | <span data-ttu-id="f091a-258">Bool</span><span class="sxs-lookup"><span data-stu-id="f091a-258">Bool</span></span> | <span data-ttu-id="f091a-259">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-259">Yes</span></span> | <span data-ttu-id="f091a-260">Pour autoriser plusieurs réponses du même répondeur.</span><span class="sxs-lookup"><span data-stu-id="f091a-260">For allowing multiple responses from same responder.</span></span> <span data-ttu-id="f091a-261">Valeur par défaut: false</span><span class="sxs-lookup"><span data-stu-id="f091a-261">Default: false</span></span> |
| <span data-ttu-id="f091a-262">questions</span><span class="sxs-lookup"><span data-stu-id="f091a-262">questions</span></span> | <span data-ttu-id="f091a-263">object[]</span><span class="sxs-lookup"><span data-stu-id="f091a-263">object[]</span></span> | <span data-ttu-id="f091a-264">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-264">No</span></span> | <span data-ttu-id="f091a-265">Chaque élément de l'objet [] est décrit ci-dessous en tant qu'objet question.</span><span class="sxs-lookup"><span data-stu-id="f091a-265">Each element of object[] is described below as Question object</span></span> |
| <span data-ttu-id="f091a-266">properties</span><span class="sxs-lookup"><span data-stu-id="f091a-266">properties</span></span> | <span data-ttu-id="f091a-267">object[]</span><span class="sxs-lookup"><span data-stu-id="f091a-267">object[]</span></span> | <span data-ttu-id="f091a-268">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-268">No</span></span> | <span data-ttu-id="f091a-269">Chaque élément de l'objet [] est décrit ci-dessous en tant qu'objet Property.</span><span class="sxs-lookup"><span data-stu-id="f091a-269">Each element of object[] is described below as Property Object.</span></span> <span data-ttu-id="f091a-270">Valide uniquement pour la création d'une instance de package d'action</span><span class="sxs-lookup"><span data-stu-id="f091a-270">Only valid for creating Action Package Instance</span></span> |

##### <a name="structure-for-question-object"></a><span data-ttu-id="f091a-271">Structure de l'objet question</span><span class="sxs-lookup"><span data-stu-id="f091a-271">Structure for Question object</span></span>

| <span data-ttu-id="f091a-272">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-272">Parameter</span></span> | <span data-ttu-id="f091a-273">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-273">Type</span></span> | <span data-ttu-id="f091a-274">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-274">Optional?</span></span> | <span data-ttu-id="f091a-275">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-276">title</span><span class="sxs-lookup"><span data-stu-id="f091a-276">title</span></span> | <span data-ttu-id="f091a-277">String</span><span class="sxs-lookup"><span data-stu-id="f091a-277">String</span></span> | <span data-ttu-id="f091a-278">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-278">No</span></span> | <span data-ttu-id="f091a-279">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="f091a-279">Title of the question</span></span> |
| <span data-ttu-id="f091a-280">type</span><span class="sxs-lookup"><span data-stu-id="f091a-280">type</span></span> | <span data-ttu-id="f091a-281">String</span><span class="sxs-lookup"><span data-stu-id="f091a-281">String</span></span> | <span data-ttu-id="f091a-282">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-282">No</span></span> | <span data-ttu-id="f091a-283">Type de la question.</span><span class="sxs-lookup"><span data-stu-id="f091a-283">Type of the question.</span></span> <span data-ttu-id="f091a-284">Énumération: SingleOption/multiOption/Text/Image/Numeric/date/location/AttachmentList</span><span class="sxs-lookup"><span data-stu-id="f091a-284">Enum: SingleOption/MultiOption/Text/Image/Numeric/Date/Location/AttachmentList</span></span> |
| <span data-ttu-id="f091a-285">isInvisible</span><span class="sxs-lookup"><span data-stu-id="f091a-285">isInvisible</span></span> | <span data-ttu-id="f091a-286">Bool</span><span class="sxs-lookup"><span data-stu-id="f091a-286">Bool</span></span> | <span data-ttu-id="f091a-287">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-287">Yes</span></span> | <span data-ttu-id="f091a-288">Valeur par défaut: false.</span><span class="sxs-lookup"><span data-stu-id="f091a-288">Default: false.</span></span> <span data-ttu-id="f091a-289">Pour contrôler la visibilité de la question</span><span class="sxs-lookup"><span data-stu-id="f091a-289">To control the visibility of the question</span></span> |
| <span data-ttu-id="f091a-290">options</span><span class="sxs-lookup"><span data-stu-id="f091a-290">options</span></span> | <span data-ttu-id="f091a-291">object[]</span><span class="sxs-lookup"><span data-stu-id="f091a-291">object[]</span></span> | <span data-ttu-id="f091a-292">Oui</span><span class="sxs-lookup"><span data-stu-id="f091a-292">Yes</span></span> | <span data-ttu-id="f091a-293">Obligatoire pour SingleOption et le type de question multiOption.</span><span class="sxs-lookup"><span data-stu-id="f091a-293">Mandatory for SingleOption and MultiOption question type.</span></span> <span data-ttu-id="f091a-294">chaque élément de l'objet [] est décrit ci-dessous comme objet option</span><span class="sxs-lookup"><span data-stu-id="f091a-294">each element of object[] is described below as Option object</span></span> |

###### <a name="structure-for-option-object"></a><span data-ttu-id="f091a-295">Structure de l'objet option</span><span class="sxs-lookup"><span data-stu-id="f091a-295">Structure for Option object</span></span>

| <span data-ttu-id="f091a-296">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-296">Parameter</span></span> | <span data-ttu-id="f091a-297">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-297">Type</span></span> | <span data-ttu-id="f091a-298">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-298">Optional?</span></span> | <span data-ttu-id="f091a-299">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-299">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-300">title</span><span class="sxs-lookup"><span data-stu-id="f091a-300">title</span></span> | <span data-ttu-id="f091a-301">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-301">String</span></span> | <span data-ttu-id="f091a-302">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-302">No</span></span> | <span data-ttu-id="f091a-303">Titre de l'option</span><span class="sxs-lookup"><span data-stu-id="f091a-303">Title of the Option</span></span> |

###### <a name="structure-for-property-object"></a><span data-ttu-id="f091a-304">Structure de l'objet Property</span><span class="sxs-lookup"><span data-stu-id="f091a-304">Structure for Property object</span></span>

| <span data-ttu-id="f091a-305">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-305">Parameter</span></span> | <span data-ttu-id="f091a-306">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-306">Type</span></span> | <span data-ttu-id="f091a-307">Module?</span><span class="sxs-lookup"><span data-stu-id="f091a-307">Optional?</span></span> | <span data-ttu-id="f091a-308">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-308">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f091a-309">name</span><span class="sxs-lookup"><span data-stu-id="f091a-309">name</span></span> | <span data-ttu-id="f091a-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-310">String</span></span> | <span data-ttu-id="f091a-311">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-311">No</span></span> | <span data-ttu-id="f091a-312">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="f091a-312">Name of the property</span></span> |
| <span data-ttu-id="f091a-313">type</span><span class="sxs-lookup"><span data-stu-id="f091a-313">type</span></span> | <span data-ttu-id="f091a-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-314">String</span></span> | <span data-ttu-id="f091a-315">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-315">No</span></span> | <span data-ttu-id="f091a-316">Type de la propriété.</span><span class="sxs-lookup"><span data-stu-id="f091a-316">Type of the property.</span></span> <span data-ttu-id="f091a-317">Énumération: Text, Numeric, location, DateTime, StringList, Attachment, StringSet, AttachmentList</span><span class="sxs-lookup"><span data-stu-id="f091a-317">Enum: Text, Numeric, Location, DateTime, StringList, Attachment, StringSet, AttachmentList</span></span> |
| <span data-ttu-id="f091a-318">value</span><span class="sxs-lookup"><span data-stu-id="f091a-318">value</span></span> | <span data-ttu-id="f091a-319">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-319">String</span></span> | <span data-ttu-id="f091a-320">Non</span><span class="sxs-lookup"><span data-stu-id="f091a-320">No</span></span> | <span data-ttu-id="f091a-321">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f091a-321">Value of the property</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="f091a-322">Exemple de demande JSON pour une action d'enquête</span><span class="sxs-lookup"><span data-stu-id="f091a-322">Sample JSON Request for a Survey Action</span></span>

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

##### <a name="response-body"></a><span data-ttu-id="f091a-323">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="f091a-323">Response body</span></span>

| <span data-ttu-id="f091a-324">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f091a-324">Parameter</span></span> | <span data-ttu-id="f091a-325">Type</span><span class="sxs-lookup"><span data-stu-id="f091a-325">Type</span></span> | <span data-ttu-id="f091a-326">Description</span><span class="sxs-lookup"><span data-stu-id="f091a-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f091a-327">ID</span><span class="sxs-lookup"><span data-stu-id="f091a-327">referenceId</span></span> | <span data-ttu-id="f091a-328">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-328">String</span></span> | <span data-ttu-id="f091a-329">Identificateur de demande</span><span class="sxs-lookup"><span data-stu-id="f091a-329">Request identifier</span></span> |
| <span data-ttu-id="f091a-330">actionId</span><span class="sxs-lookup"><span data-stu-id="f091a-330">actionId</span></span> | <span data-ttu-id="f091a-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f091a-331">String</span></span> | <span data-ttu-id="f091a-332">Identificateur d'action</span><span class="sxs-lookup"><span data-stu-id="f091a-332">Action identifier</span></span> |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
