# <a name="webhook-response-schema-for-registered-events"></a><span data-ttu-id="02bcd-101">Schéma de réponse webhook pour les événements inscrits</span><span class="sxs-lookup"><span data-stu-id="02bcd-101">Webhook response schema for registered events</span></span>

<span data-ttu-id="02bcd-102">Si un webhook est inscrit, Kaizala renvoie une réponse webHook pour chaque événement sur l'objectId enregistré, filtré pour les événements inscrits.</span><span class="sxs-lookup"><span data-stu-id="02bcd-102">If a webhook is registered, Kaizala returns a webHook response for each event on the registered objectId, filtered for registered events.</span></span> <span data-ttu-id="02bcd-103">Vous trouverez ci-dessous les détails du schéma de différentes réponses de webhook pour différents événements.</span><span class="sxs-lookup"><span data-stu-id="02bcd-103">Below is schema details for different webhook response for different events.</span></span>

## <a name="response-body"></a><span data-ttu-id="02bcd-104">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">Response Body</span></span>
| <span data-ttu-id="02bcd-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">Parameter</span></span> | <span data-ttu-id="02bcd-106">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">Type</span></span> | <span data-ttu-id="02bcd-107">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-108">objectId</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">objectId</span></span> | <span data-ttu-id="02bcd-109">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">String</span></span> | <span data-ttu-id="02bcd-110">Identificateur représentant l'objet dans lequel le webhook a été créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">Identifier representing the object in which context the webhook has been created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="02bcd-111">objectType</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">objectType</span></span> | <span data-ttu-id="02bcd-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">String</span></span> | <span data-ttu-id="02bcd-113">Énumération: «Group»/«action»/«ActionPackage»</span><span class="sxs-lookup"><span data-stu-id="02bcd-113">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="02bcd-114">Évènement</span><span class="sxs-lookup"><span data-stu-id="02bcd-114">eventType</span></span> | <span data-ttu-id="02bcd-115">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-115">String</span></span> | <span data-ttu-id="02bcd-116">Événement Registered qui a été appelé</span><span class="sxs-lookup"><span data-stu-id="02bcd-116">Registered event that has been invoked</span></span> |
| <span data-ttu-id="02bcd-117">eventId</span><span class="sxs-lookup"><span data-stu-id="02bcd-117">eventId</span></span> | <span data-ttu-id="02bcd-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-118">String</span></span> | <span data-ttu-id="02bcd-119">Identificateur représentant l'événement</span><span class="sxs-lookup"><span data-stu-id="02bcd-119">Identifier representing the event</span></span> |
| <span data-ttu-id="02bcd-120">données</span><span class="sxs-lookup"><span data-stu-id="02bcd-120">data</span></span> | <span data-ttu-id="02bcd-121">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="02bcd-121">JSON Object</span></span> | <span data-ttu-id="02bcd-122">Objet représentant des données spécifiques à cet événement.</span><span class="sxs-lookup"><span data-stu-id="02bcd-122">Object representing data specific to that event.</span></span> <span data-ttu-id="02bcd-123">Paramètres définis ci-dessous pour chacun des événements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02bcd-123">Parameters defined below for each of the supported event.</span></span> |
| <span data-ttu-id="02bcd-124">contexte</span><span class="sxs-lookup"><span data-stu-id="02bcd-124">context</span></span> | <span data-ttu-id="02bcd-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-125">String</span></span> | <span data-ttu-id="02bcd-126">Renvoie la valeur qui a été définie lors de l'inscription d'un webhook sous le paramètre «callbackContext»</span><span class="sxs-lookup"><span data-stu-id="02bcd-126">Returns value that has been set while registering a webhook under parameter 'callbackContext'</span></span>|
| <span data-ttu-id="02bcd-127">fromUser</span><span class="sxs-lookup"><span data-stu-id="02bcd-127">fromUser</span></span> | <span data-ttu-id="02bcd-128">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-128">String</span></span> | <span data-ttu-id="02bcd-129">Numéro de téléphone de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-129">Sender's phone number</span></span> |
| <span data-ttu-id="02bcd-130">fromUserId</span><span class="sxs-lookup"><span data-stu-id="02bcd-130">fromUserId</span></span> | <span data-ttu-id="02bcd-131">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-131">String</span></span> | <span data-ttu-id="02bcd-132">UserId de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-132">Sender's userId</span></span> |
| <span data-ttu-id="02bcd-133">fromUserName</span><span class="sxs-lookup"><span data-stu-id="02bcd-133">fromUserName</span></span> | <span data-ttu-id="02bcd-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-134">String</span></span> | <span data-ttu-id="02bcd-135">Nom enregistré de l'expéditeur avec Kaizala</span><span class="sxs-lookup"><span data-stu-id="02bcd-135">Sender's registered name with Kaizala</span></span> |
| <span data-ttu-id="02bcd-136">fromUserProfilePic</span><span class="sxs-lookup"><span data-stu-id="02bcd-136">fromUserProfilePic</span></span> | <span data-ttu-id="02bcd-137">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-137">url</span></span> | <span data-ttu-id="02bcd-138">Profil de l'expéditeur pic</span><span class="sxs-lookup"><span data-stu-id="02bcd-138">Sender's Profile Pic</span></span> |

<span data-ttu-id="02bcd-139">Le paramètre «Data» varie en fonction de l'événement webHook.</span><span class="sxs-lookup"><span data-stu-id="02bcd-139">The parameter 'data' would vary depending on the webHook event.</span></span> <span data-ttu-id="02bcd-140">Vous pouvez trouver le schéma de chaque événement ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="02bcd-140">You can find schema for each event below.</span></span>

### <a name="data-for-event-textmessagecreated"></a><span data-ttu-id="02bcd-141">données de l'événement «TextMessageCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-141">data for event 'TextMessageCreated'</span></span>
| <span data-ttu-id="02bcd-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-142">Parameter</span></span> | <span data-ttu-id="02bcd-143">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-143">Type</span></span> | <span data-ttu-id="02bcd-144">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-144">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-145">text</span><span class="sxs-lookup"><span data-stu-id="02bcd-145">text</span></span> | <span data-ttu-id="02bcd-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-146">String</span></span> | <span data-ttu-id="02bcd-147">Message texte envoyé</span><span class="sxs-lookup"><span data-stu-id="02bcd-147">Text Message that has been sent</span></span> |

#### <a name="sample-webhook-response-for-textmessagecreated"></a><span data-ttu-id="02bcd-148">Exemple de réponse webHook pour «TextMessageCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-148">Sample webHook response for 'TextMessageCreated'</span></span>
```javascript
{
  "objectId": "8c2050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "TextMessageCreated",
  "eventId": "55ed01-02b5-491e-8e7e-484726da976b",
  "data": {
    "text": "Test Message"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-attachmentcreated"></a><span data-ttu-id="02bcd-149">données de l'événement «AttachmentCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-149">data for event 'AttachmentCreated'</span></span>
| <span data-ttu-id="02bcd-150">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-150">Parameter</span></span> | <span data-ttu-id="02bcd-151">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-151">Type</span></span> | <span data-ttu-id="02bcd-152">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-152">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-153">panne</span><span class="sxs-lookup"><span data-stu-id="02bcd-153">media</span></span> | <span data-ttu-id="02bcd-154">Tableau</span><span class="sxs-lookup"><span data-stu-id="02bcd-154">Array</span></span> | <span data-ttu-id="02bcd-155">Chaque élément contient mediaUrl et mediaFileName</span><span class="sxs-lookup"><span data-stu-id="02bcd-155">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="02bcd-156">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="02bcd-156">mediaUrl</span></span> | <span data-ttu-id="02bcd-157">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-157">url</span></span> | <span data-ttu-id="02bcd-158">URL de l'image</span><span class="sxs-lookup"><span data-stu-id="02bcd-158">url of the image</span></span> |
| <span data-ttu-id="02bcd-159">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="02bcd-159">mediaFileName</span></span> | <span data-ttu-id="02bcd-160">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-160">String</span></span> | <span data-ttu-id="02bcd-161">Filename</span><span class="sxs-lookup"><span data-stu-id="02bcd-161">Filename</span></span> |
| <span data-ttu-id="02bcd-162">actionType</span><span class="sxs-lookup"><span data-stu-id="02bcd-162">actionType</span></span> | <span data-ttu-id="02bcd-163">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-163">String</span></span> | <span data-ttu-id="02bcd-164">Valeur enum: 'image'</span><span class="sxs-lookup"><span data-stu-id="02bcd-164">Enum value : 'Image'</span></span> |
| <span data-ttu-id="02bcd-165">caption</span><span class="sxs-lookup"><span data-stu-id="02bcd-165">caption</span></span> | <span data-ttu-id="02bcd-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-166">String</span></span> | <span data-ttu-id="02bcd-167">légende associée à l'image</span><span class="sxs-lookup"><span data-stu-id="02bcd-167">caption attached with the image</span></span> |

#### <a name="sample-webhook-response-for-attachmentcreated"></a><span data-ttu-id="02bcd-168">Exemple de réponse webHook pour «AttachmentCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-168">Sample webHook response for 'AttachmentCreated'</span></span>
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "AttachmentCreated",
  "eventId": "59e2e9f9-9b10-4b67-8bc5-3f85a04f2d91",
  "data": {
    "media": [
      {
        "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/0ad142c52b30d797addebadb620c19bf6f018299ed4acdce5760e45e2e4bc4ae.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Thbp46wdgoqbDaAF06v2Y2ijzny0jx2fBDo1EZab%2BNY%3D&amp;st=2018-03-22T10:22:21Z&amp;se=2292-01-05T11:22:21Z&amp;sp=r",
        "mediaFileName": "IMG_18-03-22_165220084_1.jpg"
      }
    ],
    "actionType": "Image",
    "caption": "Testing."
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```
### <a name="data-for-event-announcement"></a><span data-ttu-id="02bcd-169">données de l'événement'annonce'</span><span class="sxs-lookup"><span data-stu-id="02bcd-169">data for event 'Announcement'</span></span>
| <span data-ttu-id="02bcd-170">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-170">Parameter</span></span> | <span data-ttu-id="02bcd-171">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-171">Type</span></span> | <span data-ttu-id="02bcd-172">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-172">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-173">title</span><span class="sxs-lookup"><span data-stu-id="02bcd-173">title</span></span> | <span data-ttu-id="02bcd-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-174">String</span></span> | <span data-ttu-id="02bcd-175">Titre de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-175">Title of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-176">text</span><span class="sxs-lookup"><span data-stu-id="02bcd-176">text</span></span> | <span data-ttu-id="02bcd-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-177">String</span></span> | <span data-ttu-id="02bcd-178">Corps du message de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-178">Message body of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-179">panne</span><span class="sxs-lookup"><span data-stu-id="02bcd-179">media</span></span> | <span data-ttu-id="02bcd-180">Tableau</span><span class="sxs-lookup"><span data-stu-id="02bcd-180">Array</span></span> | <span data-ttu-id="02bcd-181">Chaque élément contient mediaUrl et mediaFileName</span><span class="sxs-lookup"><span data-stu-id="02bcd-181">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="02bcd-182">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="02bcd-182">mediaUrl</span></span> | <span data-ttu-id="02bcd-183">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-183">url</span></span> | <span data-ttu-id="02bcd-184">URL de l'image</span><span class="sxs-lookup"><span data-stu-id="02bcd-184">url of the image</span></span> |
| <span data-ttu-id="02bcd-185">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="02bcd-185">mediaFileName</span></span> | <span data-ttu-id="02bcd-186">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-186">String</span></span> | <span data-ttu-id="02bcd-187">Filename</span><span class="sxs-lookup"><span data-stu-id="02bcd-187">Filename</span></span> |


#### <a name="sample-webhook-response-for-announcement"></a><span data-ttu-id="02bcd-188">Exemple de réponse webHook pour «Announcement»</span><span class="sxs-lookup"><span data-stu-id="02bcd-188">Sample webHook response for 'Announcement'</span></span>
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "Announcement",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "text": "Caption :Testing.",
    "title": "Sent by Robin Richard",
    "media": [
      {
        "url": "https://cdn.inc-000.kms.osi.office.net/contenthost/beb2cfef8732c6cc3b54652c1f6f99d64f529fd9be3d409e2966552639fb791f.jpeg",
        "fileName": "e3c145f1-5e6f-4ee9-bd83-49ec3a1c2550.jpeg"
      }
    ]
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobcreated"></a><span data-ttu-id="02bcd-189">données de l'événement «JobCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-189">data for event 'JobCreated'</span></span>
| <span data-ttu-id="02bcd-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-190">Parameter</span></span> | <span data-ttu-id="02bcd-191">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-191">Type</span></span> | <span data-ttu-id="02bcd-192">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-193">title</span><span class="sxs-lookup"><span data-stu-id="02bcd-193">title</span></span> | <span data-ttu-id="02bcd-194">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-194">String</span></span> | <span data-ttu-id="02bcd-195">Titre de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-195">Title of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-196">text</span><span class="sxs-lookup"><span data-stu-id="02bcd-196">text</span></span> | <span data-ttu-id="02bcd-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-197">String</span></span> | <span data-ttu-id="02bcd-198">Corps du message de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-198">Message body of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-199">actionId</span><span class="sxs-lookup"><span data-stu-id="02bcd-199">actionId</span></span> | <span data-ttu-id="02bcd-200">Id</span><span class="sxs-lookup"><span data-stu-id="02bcd-200">Id</span></span> | <span data-ttu-id="02bcd-201">Identificateur de cette instance particulière de l'action de travail</span><span class="sxs-lookup"><span data-stu-id="02bcd-201">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="02bcd-202">dueDate</span><span class="sxs-lookup"><span data-stu-id="02bcd-202">dueDate</span></span> | <span data-ttu-id="02bcd-203">Date</span><span class="sxs-lookup"><span data-stu-id="02bcd-203">Date</span></span> | <span data-ttu-id="02bcd-204">Date d'expiration de la tâche</span><span class="sxs-lookup"><span data-stu-id="02bcd-204">Date by which job would expire</span></span> |
| <span data-ttu-id="02bcd-205">assignedTo</span><span class="sxs-lookup"><span data-stu-id="02bcd-205">assignedTo</span></span> | <span data-ttu-id="02bcd-206">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02bcd-206">String Array</span></span> | <span data-ttu-id="02bcd-207">Tableau de numéros de téléphone</span><span class="sxs-lookup"><span data-stu-id="02bcd-207">Array of phone numbers</span></span> |


#### <a name="sample-webhook-response-for-jobcreated"></a><span data-ttu-id="02bcd-208">Exemple de réponse webHook pour «JobCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-208">Sample webHook response for 'JobCreated'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "assignedTo": [
      "+919740797266"
    ],
    "title": "Test Job",
    "dueDate": "2018-03-22T18:29:59Z",
    "actionId": "aeb012-31a0-477a-a131-8a1e2791b36e",
    "groupId": "8c291050-9be8-6-97f5-bb7013930027"
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobresponse"></a><span data-ttu-id="02bcd-209">données de l'événement «JobResponse»</span><span class="sxs-lookup"><span data-stu-id="02bcd-209">data for event 'JobResponse'</span></span>
| <span data-ttu-id="02bcd-210">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-210">Parameter</span></span> | <span data-ttu-id="02bcd-211">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-211">Type</span></span> | <span data-ttu-id="02bcd-212">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-212">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-213">title</span><span class="sxs-lookup"><span data-stu-id="02bcd-213">title</span></span> | <span data-ttu-id="02bcd-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-214">String</span></span> | <span data-ttu-id="02bcd-215">Titre de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-215">Title of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-216">text</span><span class="sxs-lookup"><span data-stu-id="02bcd-216">text</span></span> | <span data-ttu-id="02bcd-217">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-217">String</span></span> | <span data-ttu-id="02bcd-218">Corps du message de l'action d'annonce</span><span class="sxs-lookup"><span data-stu-id="02bcd-218">Message body of Announcement Action</span></span> |
| <span data-ttu-id="02bcd-219">actionId</span><span class="sxs-lookup"><span data-stu-id="02bcd-219">actionId</span></span> | <span data-ttu-id="02bcd-220">Id</span><span class="sxs-lookup"><span data-stu-id="02bcd-220">Id</span></span> | <span data-ttu-id="02bcd-221">Identificateur de cette instance particulière de l'action de travail</span><span class="sxs-lookup"><span data-stu-id="02bcd-221">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="02bcd-222">groupId</span><span class="sxs-lookup"><span data-stu-id="02bcd-222">groupId</span></span> | <span data-ttu-id="02bcd-223">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-223">String</span></span> | <span data-ttu-id="02bcd-224">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="02bcd-224">Group Identifier</span></span> |
| <span data-ttu-id="02bcd-225">responseId</span><span class="sxs-lookup"><span data-stu-id="02bcd-225">responseId</span></span> | <span data-ttu-id="02bcd-226">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-226">String</span></span> | <span data-ttu-id="02bcd-227">GUID permettant d'identifier cette réponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-227">GUID for identifying that Response</span></span> |
| <span data-ttu-id="02bcd-228">responseDetails</span><span class="sxs-lookup"><span data-stu-id="02bcd-228">responseDetails</span></span> | <span data-ttu-id="02bcd-229">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02bcd-229">String Array</span></span> | <span data-ttu-id="02bcd-230">Tableau d'objets Response</span><span class="sxs-lookup"><span data-stu-id="02bcd-230">Array of Response Objects</span></span> |
| <span data-ttu-id="02bcd-231">utilisateur</span><span class="sxs-lookup"><span data-stu-id="02bcd-231">assignee</span></span> | <span data-ttu-id="02bcd-232">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-232">String</span></span> | <span data-ttu-id="02bcd-233">Numéro de téléphone du destinataire</span><span class="sxs-lookup"><span data-stu-id="02bcd-233">Assignee's Phone Number</span></span> |
| <span data-ttu-id="02bcd-234">assigneeName</span><span class="sxs-lookup"><span data-stu-id="02bcd-234">assigneeName</span></span> | <span data-ttu-id="02bcd-235">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-235">String</span></span> | <span data-ttu-id="02bcd-236">Nom du cessionnaire</span><span class="sxs-lookup"><span data-stu-id="02bcd-236">Assignee's Name</span></span> |
| <span data-ttu-id="02bcd-237">assigneeProfilePic</span><span class="sxs-lookup"><span data-stu-id="02bcd-237">assigneeProfilePic</span></span> | <span data-ttu-id="02bcd-238">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-238">url</span></span> | <span data-ttu-id="02bcd-239">URL du profil de l'intervenant pic</span><span class="sxs-lookup"><span data-stu-id="02bcd-239">url of the assignee's profile pic</span></span> |
| <span data-ttu-id="02bcd-240">isCompleted</span><span class="sxs-lookup"><span data-stu-id="02bcd-240">isCompleted</span></span> | <span data-ttu-id="02bcd-241">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-241">Boolean</span></span> | <span data-ttu-id="02bcd-242">Le travail est-il terminé?</span><span class="sxs-lookup"><span data-stu-id="02bcd-242">Is the Job completed?</span></span> |




#### <a name="sample-webhook-response-for-jobresponse"></a><span data-ttu-id="02bcd-243">Exemple de réponse webHook pour «JobResponse»</span><span class="sxs-lookup"><span data-stu-id="02bcd-243">Sample webHook response for 'JobResponse'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "actionId": "2ce34820-3d67-4807-9a1d-7cf099c2e7ae",
    "groupId": "8c291050-9be8-45d6-97f5-bb7013930027",
    "responseId": "80a883ec-e6c7-4dc8-979d-d268bbeeee8b",
    "responseDetails": {
      "response": {
        "assignee": "++91xxxxxxxx",
        "assigneeName": "Robin Richard",
        "assigneeProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d536285d08e6409e416.jpg",
        "isCompleted": true
      }
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-actioncreated--surveycreated"></a><span data-ttu-id="02bcd-244">données pour l'événement «ActionCreated»/«SurveyCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-244">data for event 'ActionCreated' / 'SurveyCreated'</span></span>
| <span data-ttu-id="02bcd-245">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-245">Parameter</span></span> | <span data-ttu-id="02bcd-246">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-246">Type</span></span> | <span data-ttu-id="02bcd-247">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-247">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-248">actionId</span><span class="sxs-lookup"><span data-stu-id="02bcd-248">actionId</span></span> | <span data-ttu-id="02bcd-249">Id</span><span class="sxs-lookup"><span data-stu-id="02bcd-249">Id</span></span> | <span data-ttu-id="02bcd-250">Identificateur de cette instance particulière de l'action de travail</span><span class="sxs-lookup"><span data-stu-id="02bcd-250">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="02bcd-251">groupId</span><span class="sxs-lookup"><span data-stu-id="02bcd-251">groupId</span></span> | <span data-ttu-id="02bcd-252">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-252">String</span></span> | <span data-ttu-id="02bcd-253">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="02bcd-253">Group Identifier</span></span> |
| <span data-ttu-id="02bcd-254">responseId</span><span class="sxs-lookup"><span data-stu-id="02bcd-254">responseId</span></span> | <span data-ttu-id="02bcd-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-255">String</span></span> | <span data-ttu-id="02bcd-256">GUID permettant d'identifier cette réponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-256">GUID for identifying that Response</span></span> |
| <span data-ttu-id="02bcd-257">questions</span><span class="sxs-lookup"><span data-stu-id="02bcd-257">questions</span></span> | <span data-ttu-id="02bcd-258">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02bcd-258">String Array</span></span> | <span data-ttu-id="02bcd-259">Tableau d'objets</span><span class="sxs-lookup"><span data-stu-id="02bcd-259">Array of Objects</span></span> |
| <span data-ttu-id="02bcd-260">répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-260">responder</span></span> | <span data-ttu-id="02bcd-261">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-261">String</span></span> | <span data-ttu-id="02bcd-262">Numéro de téléphone du répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-262">responder's Phone Number</span></span> |
| <span data-ttu-id="02bcd-263">responderName</span><span class="sxs-lookup"><span data-stu-id="02bcd-263">responderName</span></span> | <span data-ttu-id="02bcd-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-264">String</span></span> | <span data-ttu-id="02bcd-265">Nom du répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-265">responder's Name</span></span> |
| <span data-ttu-id="02bcd-266">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="02bcd-266">responderProfilePic</span></span> | <span data-ttu-id="02bcd-267">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-267">url</span></span> | <span data-ttu-id="02bcd-268">URL du profil du répondeur pic</span><span class="sxs-lookup"><span data-stu-id="02bcd-268">url of the responder's profile pic</span></span> |
| <span data-ttu-id="02bcd-269">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="02bcd-269">isAnonymous</span></span> | <span data-ttu-id="02bcd-270">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-270">Boolean</span></span> | <span data-ttu-id="02bcd-271">La réponse de l'enquête a-t-elle été soumise de manière anonyme?</span><span class="sxs-lookup"><span data-stu-id="02bcd-271">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="02bcd-272">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-272">isUpdateResponse</span></span> | <span data-ttu-id="02bcd-273">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-273">Boolean</span></span> | <span data-ttu-id="02bcd-274">La réponse a-t-elle été mise à jour par un répondeur, car la réponse a été envoyée plus tôt</span><span class="sxs-lookup"><span data-stu-id="02bcd-274">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="02bcd-275">Détails du schéma pour l'objet «responseWithQuestions»</span><span class="sxs-lookup"><span data-stu-id="02bcd-275">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="02bcd-276">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-276">Parameter</span></span> | <span data-ttu-id="02bcd-277">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-277">Type</span></span> | <span data-ttu-id="02bcd-278">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-278">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-279">title</span><span class="sxs-lookup"><span data-stu-id="02bcd-279">title</span></span> | <span data-ttu-id="02bcd-280">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-280">String</span></span> | <span data-ttu-id="02bcd-281">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="02bcd-281">Question Title</span></span> |
| <span data-ttu-id="02bcd-282">type</span><span class="sxs-lookup"><span data-stu-id="02bcd-282">type</span></span> | <span data-ttu-id="02bcd-283">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-283">String</span></span> | <span data-ttu-id="02bcd-284">QuestionType</span><span class="sxs-lookup"><span data-stu-id="02bcd-284">QuestionType</span></span> |
| <span data-ttu-id="02bcd-285">options</span><span class="sxs-lookup"><span data-stu-id="02bcd-285">options</span></span> | <span data-ttu-id="02bcd-286">Tableau</span><span class="sxs-lookup"><span data-stu-id="02bcd-286">Array</span></span> | <span data-ttu-id="02bcd-287">Liste d'options (paire clé-valeur) applicable aux questions à choix multiples</span><span class="sxs-lookup"><span data-stu-id="02bcd-287">List of options (key-value pair) applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="02bcd-288">isInvisible</span><span class="sxs-lookup"><span data-stu-id="02bcd-288">isInvisible</span></span> | <span data-ttu-id="02bcd-289">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-289">Boolean</span></span> | <span data-ttu-id="02bcd-290">Est la question cachée de l'interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="02bcd-290">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a><span data-ttu-id="02bcd-291">Exemple de réponse webHook pour «ActionCreated»/«SurveyCreated»</span><span class="sxs-lookup"><span data-stu-id="02bcd-291">Sample webHook response for 'ActionCreated' / 'SurveyCreated'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "ActionCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```



### <a name="data-for-event-surveyresponse-actionresponse"></a><span data-ttu-id="02bcd-292">données pour l'événement «SurveyResponse»/«ActionResponse»</span><span class="sxs-lookup"><span data-stu-id="02bcd-292">data for event 'SurveyResponse'/ 'ActionResponse'</span></span>
| <span data-ttu-id="02bcd-293">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-293">Parameter</span></span> | <span data-ttu-id="02bcd-294">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-294">Type</span></span> | <span data-ttu-id="02bcd-295">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-295">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-296">actionId</span><span class="sxs-lookup"><span data-stu-id="02bcd-296">actionId</span></span> | <span data-ttu-id="02bcd-297">Id</span><span class="sxs-lookup"><span data-stu-id="02bcd-297">Id</span></span> | <span data-ttu-id="02bcd-298">Identificateur de cette instance particulière de l'action de travail</span><span class="sxs-lookup"><span data-stu-id="02bcd-298">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="02bcd-299">groupId</span><span class="sxs-lookup"><span data-stu-id="02bcd-299">groupId</span></span> | <span data-ttu-id="02bcd-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-300">String</span></span> | <span data-ttu-id="02bcd-301">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="02bcd-301">Group Identifier</span></span> |
| <span data-ttu-id="02bcd-302">responseId</span><span class="sxs-lookup"><span data-stu-id="02bcd-302">responseId</span></span> | <span data-ttu-id="02bcd-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-303">String</span></span> | <span data-ttu-id="02bcd-304">GUID permettant d'identifier cette réponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-304">GUID for identifying that Response</span></span> |
| <span data-ttu-id="02bcd-305">responseDetails</span><span class="sxs-lookup"><span data-stu-id="02bcd-305">responseDetails</span></span> | <span data-ttu-id="02bcd-306">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02bcd-306">String Array</span></span> | <span data-ttu-id="02bcd-307">Tableau d'objets «responseWithQuestions»</span><span class="sxs-lookup"><span data-stu-id="02bcd-307">Array of 'responseWithQuestions' Objects</span></span> |
| <span data-ttu-id="02bcd-308">répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-308">responder</span></span> | <span data-ttu-id="02bcd-309">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-309">String</span></span> | <span data-ttu-id="02bcd-310">Numéro de téléphone du répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-310">responder's Phone Number</span></span> |
| <span data-ttu-id="02bcd-311">responderName</span><span class="sxs-lookup"><span data-stu-id="02bcd-311">responderName</span></span> | <span data-ttu-id="02bcd-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-312">String</span></span> | <span data-ttu-id="02bcd-313">Nom du répondeur</span><span class="sxs-lookup"><span data-stu-id="02bcd-313">responder's Name</span></span> |
| <span data-ttu-id="02bcd-314">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="02bcd-314">responderProfilePic</span></span> | <span data-ttu-id="02bcd-315">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-315">url</span></span> | <span data-ttu-id="02bcd-316">URL du profil du répondeur pic</span><span class="sxs-lookup"><span data-stu-id="02bcd-316">url of the responder's profile pic</span></span> |
| <span data-ttu-id="02bcd-317">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="02bcd-317">isAnonymous</span></span> | <span data-ttu-id="02bcd-318">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-318">Boolean</span></span> | <span data-ttu-id="02bcd-319">La réponse de l'enquête a-t-elle été soumise de manière anonyme?</span><span class="sxs-lookup"><span data-stu-id="02bcd-319">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="02bcd-320">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="02bcd-320">isUpdateResponse</span></span> | <span data-ttu-id="02bcd-321">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-321">Boolean</span></span> | <span data-ttu-id="02bcd-322">La réponse a-t-elle été mise à jour par un répondeur, car la réponse a été envoyée plus tôt</span><span class="sxs-lookup"><span data-stu-id="02bcd-322">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="02bcd-323">Détails du schéma pour l'objet «responseWithQuestions»</span><span class="sxs-lookup"><span data-stu-id="02bcd-323">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="02bcd-324">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-324">Parameter</span></span> | <span data-ttu-id="02bcd-325">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-325">Type</span></span> | <span data-ttu-id="02bcd-326">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-327">title</span><span class="sxs-lookup"><span data-stu-id="02bcd-327">title</span></span> | <span data-ttu-id="02bcd-328">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-328">String</span></span> | <span data-ttu-id="02bcd-329">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="02bcd-329">Question Title</span></span> |
| <span data-ttu-id="02bcd-330">type</span><span class="sxs-lookup"><span data-stu-id="02bcd-330">type</span></span> | <span data-ttu-id="02bcd-331">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-331">String</span></span> | <span data-ttu-id="02bcd-332">QuestionType</span><span class="sxs-lookup"><span data-stu-id="02bcd-332">QuestionType</span></span> |
| <span data-ttu-id="02bcd-333">options</span><span class="sxs-lookup"><span data-stu-id="02bcd-333">options</span></span> | <span data-ttu-id="02bcd-334">Tableau</span><span class="sxs-lookup"><span data-stu-id="02bcd-334">Array</span></span> | <span data-ttu-id="02bcd-335">Liste des options applicables aux questions à choix multiples</span><span class="sxs-lookup"><span data-stu-id="02bcd-335">List of options applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="02bcd-336">répondre</span><span class="sxs-lookup"><span data-stu-id="02bcd-336">answer</span></span> | <span data-ttu-id="02bcd-337">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="02bcd-337">Array of Json Object</span></span> | <span data-ttu-id="02bcd-338">Réponses</span><span class="sxs-lookup"><span data-stu-id="02bcd-338">Answers</span></span> |
| <span data-ttu-id="02bcd-339">isInvisible</span><span class="sxs-lookup"><span data-stu-id="02bcd-339">isInvisible</span></span> | <span data-ttu-id="02bcd-340">Booléen</span><span class="sxs-lookup"><span data-stu-id="02bcd-340">Boolean</span></span> | <span data-ttu-id="02bcd-341">Est la question cachée de l'interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="02bcd-341">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a><span data-ttu-id="02bcd-342">Exemple de réponse webHook pour «SurveyResponse» «ActionResponse»</span><span class="sxs-lookup"><span data-stu-id="02bcd-342">Sample webHook response for 'SurveyResponse' 'ActionResponse'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "SurveyResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```


### <a name="data-for-event-memberadded--memberremoved"></a><span data-ttu-id="02bcd-343">données pour l'événement «MemberAdded»/«MemberRemoved»</span><span class="sxs-lookup"><span data-stu-id="02bcd-343">data for event 'MemberAdded' / 'MemberRemoved'</span></span>
| <span data-ttu-id="02bcd-344">Paramètre</span><span class="sxs-lookup"><span data-stu-id="02bcd-344">Parameter</span></span> | <span data-ttu-id="02bcd-345">Type</span><span class="sxs-lookup"><span data-stu-id="02bcd-345">Type</span></span> | <span data-ttu-id="02bcd-346">Description</span><span class="sxs-lookup"><span data-stu-id="02bcd-346">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="02bcd-347">membre</span><span class="sxs-lookup"><span data-stu-id="02bcd-347">member</span></span> | <span data-ttu-id="02bcd-348">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-348">String</span></span> | <span data-ttu-id="02bcd-349">Numéro de téléphone du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="02bcd-349">Phone Number of the added Member</span></span> |
| <span data-ttu-id="02bcd-350">NomMembre</span><span class="sxs-lookup"><span data-stu-id="02bcd-350">memberName</span></span> | <span data-ttu-id="02bcd-351">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02bcd-351">String</span></span> | <span data-ttu-id="02bcd-352">Nom du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="02bcd-352">Name of the added Member</span></span> |
| <span data-ttu-id="02bcd-353">type</span><span class="sxs-lookup"><span data-stu-id="02bcd-353">type</span></span> | <span data-ttu-id="02bcd-354">String</span><span class="sxs-lookup"><span data-stu-id="02bcd-354">String</span></span> | <span data-ttu-id="02bcd-355">Rôle d'appartenance du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="02bcd-355">Membership role of the added member</span></span> |
| <span data-ttu-id="02bcd-356">memberProfilePic</span><span class="sxs-lookup"><span data-stu-id="02bcd-356">memberProfilePic</span></span> | <span data-ttu-id="02bcd-357">url</span><span class="sxs-lookup"><span data-stu-id="02bcd-357">url</span></span> | <span data-ttu-id="02bcd-358">URL du profil de l'intervenant pic</span><span class="sxs-lookup"><span data-stu-id="02bcd-358">url of the assignee's profile pic</span></span> |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a><span data-ttu-id="02bcd-359">Exemple de réponse webHook pour «MemberAdded»/«MemberRemoved»</span><span class="sxs-lookup"><span data-stu-id="02bcd-359">Sample webHook response for 'MemberAdded' /'MemberRemoved'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "member": "+91xxxxxxxx",
    "memberName": "Jan Decker",
    "memberProfilePic": "https://mobileonlyapps.blob.core.windows.net/polymer-7ebb8d90e1324b5cbd61d1e10a30ada7/bbac582a4364860679d40fda7c6b.jpg",
    "type": "Member"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

