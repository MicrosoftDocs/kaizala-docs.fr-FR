# <a name="webhook-response-schema-for-registered-events"></a><span data-ttu-id="cf2c2-101">Schéma de réponse Webhook pour les événements enregistrés</span><span class="sxs-lookup"><span data-stu-id="cf2c2-101">Webhook response schema for registered events</span></span>

<span data-ttu-id="cf2c2-102">Si un webhook est inscrit, Kaizala renvoie une réponse webHook pour chaque événement sur objectId inscrit, filtré pour les événements enregistrés.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-102">If a webhook is registered, Kaizala returns a webHook response for each event on the registered objectId, filtered for registered events.</span></span> <span data-ttu-id="cf2c2-103">Vous trouverez ci-dessous les détails du schéma de réponse webhook différentes pour différents événements.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-103">Below is schema details for different webhook response for different events.</span></span>

## <a name="response-body"></a><span data-ttu-id="cf2c2-104">Corps de réponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-104">Response Body</span></span>
| <span data-ttu-id="cf2c2-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-105">Parameter</span></span> | <span data-ttu-id="cf2c2-106">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-106">Type</span></span> | <span data-ttu-id="cf2c2-107">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-107">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-108">objectId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-108">objectId</span></span> | <span data-ttu-id="cf2c2-109">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-109">String</span></span> | <span data-ttu-id="cf2c2-110">Identificateur représentant l’objet dans le contexte dans lequel le webhook a été créé. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="cf2c2-110">Identifier representing the object in which context the webhook has been created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="cf2c2-111">objectType</span><span class="sxs-lookup"><span data-stu-id="cf2c2-111">objectType</span></span> | <span data-ttu-id="cf2c2-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-112">String</span></span> | <span data-ttu-id="cf2c2-113">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="cf2c2-113">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="cf2c2-114">eventType</span><span class="sxs-lookup"><span data-stu-id="cf2c2-114">eventType</span></span> | <span data-ttu-id="cf2c2-115">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-115">String</span></span> | <span data-ttu-id="cf2c2-116">Événements enregistrés qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-116">Registered event that has been invoked</span></span> |
| <span data-ttu-id="cf2c2-117">eventId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-117">eventId</span></span> | <span data-ttu-id="cf2c2-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-118">String</span></span> | <span data-ttu-id="cf2c2-119">Identificateur représentant l’événement</span><span class="sxs-lookup"><span data-stu-id="cf2c2-119">Identifier representing the event</span></span> |
| <span data-ttu-id="cf2c2-120">data</span><span class="sxs-lookup"><span data-stu-id="cf2c2-120">data</span></span> | <span data-ttu-id="cf2c2-121">Objet JSON</span><span class="sxs-lookup"><span data-stu-id="cf2c2-121">JSON Object</span></span> | <span data-ttu-id="cf2c2-122">Objet représentant les données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-122">Object representing data specific to that event.</span></span> <span data-ttu-id="cf2c2-123">Paramètres définis ci-dessous pour chacun de l’événement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-123">Parameters defined below for each of the supported event.</span></span> |
| <span data-ttu-id="cf2c2-124">context</span><span class="sxs-lookup"><span data-stu-id="cf2c2-124">context</span></span> | <span data-ttu-id="cf2c2-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-125">String</span></span> | <span data-ttu-id="cf2c2-126">Renvoie la valeur qui a été définie lors de l’enregistrement d’un webhook sous paramètre 'callbackContext'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-126">Returns value that has been set while registering a webhook under parameter 'callbackContext'</span></span>|
| <span data-ttu-id="cf2c2-127">fromUser</span><span class="sxs-lookup"><span data-stu-id="cf2c2-127">fromUser</span></span> | <span data-ttu-id="cf2c2-128">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-128">String</span></span> | <span data-ttu-id="cf2c2-129">Numéro de téléphone de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-129">Sender's phone number</span></span> |
| <span data-ttu-id="cf2c2-130">fromUserId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-130">fromUserId</span></span> | <span data-ttu-id="cf2c2-131">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-131">String</span></span> | <span data-ttu-id="cf2c2-132">UserId de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-132">Sender's userId</span></span> |
| <span data-ttu-id="cf2c2-133">fromUserName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-133">fromUserName</span></span> | <span data-ttu-id="cf2c2-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-134">String</span></span> | <span data-ttu-id="cf2c2-135">Nom de l’expéditeur enregistré avec Kaizala</span><span class="sxs-lookup"><span data-stu-id="cf2c2-135">Sender's registered name with Kaizala</span></span> |
| <span data-ttu-id="cf2c2-136">fromUserProfilePic</span><span class="sxs-lookup"><span data-stu-id="cf2c2-136">fromUserProfilePic</span></span> | <span data-ttu-id="cf2c2-137">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-137">url</span></span> | <span data-ttu-id="cf2c2-138">Pic de profil de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-138">Sender's Profile Pic</span></span> |

<span data-ttu-id="cf2c2-139">Le paramètre « données » serait varient en fonction de l’événement webHook.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-139">The parameter 'data' would vary depending on the webHook event.</span></span> <span data-ttu-id="cf2c2-140">Vous pouvez trouver le schéma pour chaque événement ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-140">You can find schema for each event below.</span></span>

### <a name="data-for-event-textmessagecreated"></a><span data-ttu-id="cf2c2-141">données pour l’événement 'TextMessageCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-141">data for event 'TextMessageCreated'</span></span>
| <span data-ttu-id="cf2c2-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-142">Parameter</span></span> | <span data-ttu-id="cf2c2-143">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-143">Type</span></span> | <span data-ttu-id="cf2c2-144">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-144">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-145">text</span><span class="sxs-lookup"><span data-stu-id="cf2c2-145">text</span></span> | <span data-ttu-id="cf2c2-146">String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-146">String</span></span> | <span data-ttu-id="cf2c2-147">Message texte qui a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-147">Text Message that has been sent</span></span> |

#### <a name="sample-webhook-response-for-textmessagecreated"></a><span data-ttu-id="cf2c2-148">Exemple de réponse webHook pour 'TextMessageCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-148">Sample webHook response for 'TextMessageCreated'</span></span>
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

### <a name="data-for-event-attachmentcreated"></a><span data-ttu-id="cf2c2-149">données pour l’événement 'AttachmentCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-149">data for event 'AttachmentCreated'</span></span>
| <span data-ttu-id="cf2c2-150">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-150">Parameter</span></span> | <span data-ttu-id="cf2c2-151">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-151">Type</span></span> | <span data-ttu-id="cf2c2-152">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-152">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-153">multimédia</span><span class="sxs-lookup"><span data-stu-id="cf2c2-153">media</span></span> | <span data-ttu-id="cf2c2-154">Tableau</span><span class="sxs-lookup"><span data-stu-id="cf2c2-154">Array</span></span> | <span data-ttu-id="cf2c2-155">Chaque élément contient mediaUrl et mediaFileName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-155">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="cf2c2-156">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="cf2c2-156">mediaUrl</span></span> | <span data-ttu-id="cf2c2-157">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-157">url</span></span> | <span data-ttu-id="cf2c2-158">URL de l’image</span><span class="sxs-lookup"><span data-stu-id="cf2c2-158">url of the image</span></span> |
| <span data-ttu-id="cf2c2-159">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-159">mediaFileName</span></span> | <span data-ttu-id="cf2c2-160">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-160">String</span></span> | <span data-ttu-id="cf2c2-161">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="cf2c2-161">Filename</span></span> |
| <span data-ttu-id="cf2c2-162">actionType</span><span class="sxs-lookup"><span data-stu-id="cf2c2-162">actionType</span></span> | <span data-ttu-id="cf2c2-163">String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-163">String</span></span> | <span data-ttu-id="cf2c2-164">Valeur enum : « Image »</span><span class="sxs-lookup"><span data-stu-id="cf2c2-164">Enum value : 'Image'</span></span> |
| <span data-ttu-id="cf2c2-165">légende</span><span class="sxs-lookup"><span data-stu-id="cf2c2-165">caption</span></span> | <span data-ttu-id="cf2c2-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-166">String</span></span> | <span data-ttu-id="cf2c2-167">légende attachée à l’image</span><span class="sxs-lookup"><span data-stu-id="cf2c2-167">caption attached with the image</span></span> |

#### <a name="sample-webhook-response-for-attachmentcreated"></a><span data-ttu-id="cf2c2-168">Exemple de réponse webHook pour 'AttachmentCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-168">Sample webHook response for 'AttachmentCreated'</span></span>
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
### <a name="data-for-event-announcement"></a><span data-ttu-id="cf2c2-169">données pour l’événement « Annonce »</span><span class="sxs-lookup"><span data-stu-id="cf2c2-169">data for event 'Announcement'</span></span>
| <span data-ttu-id="cf2c2-170">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-170">Parameter</span></span> | <span data-ttu-id="cf2c2-171">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-171">Type</span></span> | <span data-ttu-id="cf2c2-172">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-172">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-173">title</span><span class="sxs-lookup"><span data-stu-id="cf2c2-173">title</span></span> | <span data-ttu-id="cf2c2-174">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-174">String</span></span> | <span data-ttu-id="cf2c2-175">Titre de l’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-175">Title of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-176">text</span><span class="sxs-lookup"><span data-stu-id="cf2c2-176">text</span></span> | <span data-ttu-id="cf2c2-177">String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-177">String</span></span> | <span data-ttu-id="cf2c2-178">Corps du message d’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-178">Message body of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-179">multimédia</span><span class="sxs-lookup"><span data-stu-id="cf2c2-179">media</span></span> | <span data-ttu-id="cf2c2-180">Tableau</span><span class="sxs-lookup"><span data-stu-id="cf2c2-180">Array</span></span> | <span data-ttu-id="cf2c2-181">Chaque élément contient mediaUrl et mediaFileName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-181">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="cf2c2-182">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="cf2c2-182">mediaUrl</span></span> | <span data-ttu-id="cf2c2-183">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-183">url</span></span> | <span data-ttu-id="cf2c2-184">URL de l’image</span><span class="sxs-lookup"><span data-stu-id="cf2c2-184">url of the image</span></span> |
| <span data-ttu-id="cf2c2-185">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-185">mediaFileName</span></span> | <span data-ttu-id="cf2c2-186">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-186">String</span></span> | <span data-ttu-id="cf2c2-187">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="cf2c2-187">Filename</span></span> |


#### <a name="sample-webhook-response-for-announcement"></a><span data-ttu-id="cf2c2-188">Exemple de réponse webHook pour « Annonce »</span><span class="sxs-lookup"><span data-stu-id="cf2c2-188">Sample webHook response for 'Announcement'</span></span>
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

### <a name="data-for-event-jobcreated"></a><span data-ttu-id="cf2c2-189">données pour l’événement 'JobCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-189">data for event 'JobCreated'</span></span>
| <span data-ttu-id="cf2c2-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-190">Parameter</span></span> | <span data-ttu-id="cf2c2-191">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-191">Type</span></span> | <span data-ttu-id="cf2c2-192">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-193">title</span><span class="sxs-lookup"><span data-stu-id="cf2c2-193">title</span></span> | <span data-ttu-id="cf2c2-194">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-194">String</span></span> | <span data-ttu-id="cf2c2-195">Titre de l’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-195">Title of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-196">text</span><span class="sxs-lookup"><span data-stu-id="cf2c2-196">text</span></span> | <span data-ttu-id="cf2c2-197">String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-197">String</span></span> | <span data-ttu-id="cf2c2-198">Corps du message d’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-198">Message body of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-199">actionId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-199">actionId</span></span> | <span data-ttu-id="cf2c2-200">ID</span><span class="sxs-lookup"><span data-stu-id="cf2c2-200">Id</span></span> | <span data-ttu-id="cf2c2-201">Identificateur pour cette instance particulière d’une Action de la tâche</span><span class="sxs-lookup"><span data-stu-id="cf2c2-201">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="cf2c2-202">dueDate</span><span class="sxs-lookup"><span data-stu-id="cf2c2-202">dueDate</span></span> | <span data-ttu-id="cf2c2-203">Date</span><span class="sxs-lookup"><span data-stu-id="cf2c2-203">Date</span></span> | <span data-ttu-id="cf2c2-204">Date par projet expire</span><span class="sxs-lookup"><span data-stu-id="cf2c2-204">Date by which job would expire</span></span> |
| <span data-ttu-id="cf2c2-205">assignedTo</span><span class="sxs-lookup"><span data-stu-id="cf2c2-205">assignedTo</span></span> | <span data-ttu-id="cf2c2-206">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="cf2c2-206">String Array</span></span> | <span data-ttu-id="cf2c2-207">Tableau des numéros de téléphone</span><span class="sxs-lookup"><span data-stu-id="cf2c2-207">Array of phone numbers</span></span> |


#### <a name="sample-webhook-response-for-jobcreated"></a><span data-ttu-id="cf2c2-208">Exemple de réponse webHook pour 'JobCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-208">Sample webHook response for 'JobCreated'</span></span>
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

### <a name="data-for-event-jobresponse"></a><span data-ttu-id="cf2c2-209">données pour l’événement 'JobResponse'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-209">data for event 'JobResponse'</span></span>
| <span data-ttu-id="cf2c2-210">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-210">Parameter</span></span> | <span data-ttu-id="cf2c2-211">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-211">Type</span></span> | <span data-ttu-id="cf2c2-212">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-212">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-213">title</span><span class="sxs-lookup"><span data-stu-id="cf2c2-213">title</span></span> | <span data-ttu-id="cf2c2-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-214">String</span></span> | <span data-ttu-id="cf2c2-215">Titre de l’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-215">Title of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-216">text</span><span class="sxs-lookup"><span data-stu-id="cf2c2-216">text</span></span> | <span data-ttu-id="cf2c2-217">String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-217">String</span></span> | <span data-ttu-id="cf2c2-218">Corps du message d’Action de l’annonce</span><span class="sxs-lookup"><span data-stu-id="cf2c2-218">Message body of Announcement Action</span></span> |
| <span data-ttu-id="cf2c2-219">actionId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-219">actionId</span></span> | <span data-ttu-id="cf2c2-220">ID</span><span class="sxs-lookup"><span data-stu-id="cf2c2-220">Id</span></span> | <span data-ttu-id="cf2c2-221">Identificateur pour cette instance particulière d’une Action de la tâche</span><span class="sxs-lookup"><span data-stu-id="cf2c2-221">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="cf2c2-222">groupId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-222">groupId</span></span> | <span data-ttu-id="cf2c2-223">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-223">String</span></span> | <span data-ttu-id="cf2c2-224">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="cf2c2-224">Group Identifier</span></span> |
| <span data-ttu-id="cf2c2-225">responseId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-225">responseId</span></span> | <span data-ttu-id="cf2c2-226">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-226">String</span></span> | <span data-ttu-id="cf2c2-227">GUID de l’identification de réponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-227">GUID for identifying that Response</span></span> |
| <span data-ttu-id="cf2c2-228">responseDetails</span><span class="sxs-lookup"><span data-stu-id="cf2c2-228">responseDetails</span></span> | <span data-ttu-id="cf2c2-229">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="cf2c2-229">String Array</span></span> | <span data-ttu-id="cf2c2-230">Tableau d’objets de réponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-230">Array of Response Objects</span></span> |
| <span data-ttu-id="cf2c2-231">intervenant</span><span class="sxs-lookup"><span data-stu-id="cf2c2-231">assignee</span></span> | <span data-ttu-id="cf2c2-232">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-232">String</span></span> | <span data-ttu-id="cf2c2-233">Numéro de téléphone du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-233">Assignee's Phone Number</span></span> |
| <span data-ttu-id="cf2c2-234">assigneeName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-234">assigneeName</span></span> | <span data-ttu-id="cf2c2-235">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-235">String</span></span> | <span data-ttu-id="cf2c2-236">Nom de la personne affectée</span><span class="sxs-lookup"><span data-stu-id="cf2c2-236">Assignee's Name</span></span> |
| <span data-ttu-id="cf2c2-237">assigneeProfilePic</span><span class="sxs-lookup"><span data-stu-id="cf2c2-237">assigneeProfilePic</span></span> | <span data-ttu-id="cf2c2-238">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-238">url</span></span> | <span data-ttu-id="cf2c2-239">URL de pic de profil de la personne affectée au</span><span class="sxs-lookup"><span data-stu-id="cf2c2-239">url of the assignee's profile pic</span></span> |
| <span data-ttu-id="cf2c2-240">isCompleted</span><span class="sxs-lookup"><span data-stu-id="cf2c2-240">isCompleted</span></span> | <span data-ttu-id="cf2c2-241">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-241">Boolean</span></span> | <span data-ttu-id="cf2c2-242">La tâche est terminée ?</span><span class="sxs-lookup"><span data-stu-id="cf2c2-242">Is the Job completed?</span></span> |




#### <a name="sample-webhook-response-for-jobresponse"></a><span data-ttu-id="cf2c2-243">Exemple de réponse webHook pour 'JobResponse'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-243">Sample webHook response for 'JobResponse'</span></span>
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

### <a name="data-for-event-actioncreated--surveycreated"></a><span data-ttu-id="cf2c2-244">données pour l’événement 'ActionCreated' / 'SurveyCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-244">data for event 'ActionCreated' / 'SurveyCreated'</span></span>
| <span data-ttu-id="cf2c2-245">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-245">Parameter</span></span> | <span data-ttu-id="cf2c2-246">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-246">Type</span></span> | <span data-ttu-id="cf2c2-247">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-247">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-248">actionId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-248">actionId</span></span> | <span data-ttu-id="cf2c2-249">ID</span><span class="sxs-lookup"><span data-stu-id="cf2c2-249">Id</span></span> | <span data-ttu-id="cf2c2-250">Identificateur pour cette instance particulière d’une Action de la tâche</span><span class="sxs-lookup"><span data-stu-id="cf2c2-250">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="cf2c2-251">groupId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-251">groupId</span></span> | <span data-ttu-id="cf2c2-252">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-252">String</span></span> | <span data-ttu-id="cf2c2-253">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="cf2c2-253">Group Identifier</span></span> |
| <span data-ttu-id="cf2c2-254">responseId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-254">responseId</span></span> | <span data-ttu-id="cf2c2-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-255">String</span></span> | <span data-ttu-id="cf2c2-256">GUID de l’identification de réponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-256">GUID for identifying that Response</span></span> |
| <span data-ttu-id="cf2c2-257">questions</span><span class="sxs-lookup"><span data-stu-id="cf2c2-257">questions</span></span> | <span data-ttu-id="cf2c2-258">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="cf2c2-258">String Array</span></span> | <span data-ttu-id="cf2c2-259">Tableau d’objets</span><span class="sxs-lookup"><span data-stu-id="cf2c2-259">Array of Objects</span></span> |
| <span data-ttu-id="cf2c2-260">répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-260">responder</span></span> | <span data-ttu-id="cf2c2-261">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-261">String</span></span> | <span data-ttu-id="cf2c2-262">Numéro de téléphone du répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-262">responder's Phone Number</span></span> |
| <span data-ttu-id="cf2c2-263">responderName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-263">responderName</span></span> | <span data-ttu-id="cf2c2-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-264">String</span></span> | <span data-ttu-id="cf2c2-265">Nom de l’auteur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-265">responder's Name</span></span> |
| <span data-ttu-id="cf2c2-266">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="cf2c2-266">responderProfilePic</span></span> | <span data-ttu-id="cf2c2-267">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-267">url</span></span> | <span data-ttu-id="cf2c2-268">URL de pic de profil du répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-268">url of the responder's profile pic</span></span> |
| <span data-ttu-id="cf2c2-269">é anonyme</span><span class="sxs-lookup"><span data-stu-id="cf2c2-269">isAnonymous</span></span> | <span data-ttu-id="cf2c2-270">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-270">Boolean</span></span> | <span data-ttu-id="cf2c2-271">Est la réponse d’enquête été présentée de manière anonyme</span><span class="sxs-lookup"><span data-stu-id="cf2c2-271">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="cf2c2-272">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-272">isUpdateResponse</span></span> | <span data-ttu-id="cf2c2-273">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-273">Boolean</span></span> | <span data-ttu-id="cf2c2-274">A la réponse été mis à jour par le répondeur, étant donné que la réponse a été précédemment envoyée</span><span class="sxs-lookup"><span data-stu-id="cf2c2-274">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="cf2c2-275">Détails du schéma pour l’objet 'responseWithQuestions'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-275">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="cf2c2-276">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-276">Parameter</span></span> | <span data-ttu-id="cf2c2-277">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-277">Type</span></span> | <span data-ttu-id="cf2c2-278">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-278">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-279">title</span><span class="sxs-lookup"><span data-stu-id="cf2c2-279">title</span></span> | <span data-ttu-id="cf2c2-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-280">String</span></span> | <span data-ttu-id="cf2c2-281">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="cf2c2-281">Question Title</span></span> |
| <span data-ttu-id="cf2c2-282">type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-282">type</span></span> | <span data-ttu-id="cf2c2-283">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-283">String</span></span> | <span data-ttu-id="cf2c2-284">QuestionType</span><span class="sxs-lookup"><span data-stu-id="cf2c2-284">QuestionType</span></span> |
| <span data-ttu-id="cf2c2-285">options</span><span class="sxs-lookup"><span data-stu-id="cf2c2-285">options</span></span> | <span data-ttu-id="cf2c2-286">Tableau</span><span class="sxs-lookup"><span data-stu-id="cf2c2-286">Array</span></span> | <span data-ttu-id="cf2c2-287">Liste d’options (paire clé-valeur) applicables aux questions choice multiple</span><span class="sxs-lookup"><span data-stu-id="cf2c2-287">List of options (key-value pair) applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="cf2c2-288">isInvisible</span><span class="sxs-lookup"><span data-stu-id="cf2c2-288">isInvisible</span></span> | <span data-ttu-id="cf2c2-289">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-289">Boolean</span></span> | <span data-ttu-id="cf2c2-290">La question est masquée dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-290">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a><span data-ttu-id="cf2c2-291">Exemple de réponse webHook pour 'ActionCreated' / 'SurveyCreated'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-291">Sample webHook response for 'ActionCreated' / 'SurveyCreated'</span></span>
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



### <a name="data-for-event-surveyresponse-actionresponse"></a><span data-ttu-id="cf2c2-292">données pour l’événement 'SurveyResponse' / 'ActionResponse'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-292">data for event 'SurveyResponse'/ 'ActionResponse'</span></span>
| <span data-ttu-id="cf2c2-293">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-293">Parameter</span></span> | <span data-ttu-id="cf2c2-294">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-294">Type</span></span> | <span data-ttu-id="cf2c2-295">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-295">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-296">actionId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-296">actionId</span></span> | <span data-ttu-id="cf2c2-297">ID</span><span class="sxs-lookup"><span data-stu-id="cf2c2-297">Id</span></span> | <span data-ttu-id="cf2c2-298">Identificateur pour cette instance particulière d’une Action de la tâche</span><span class="sxs-lookup"><span data-stu-id="cf2c2-298">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="cf2c2-299">groupId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-299">groupId</span></span> | <span data-ttu-id="cf2c2-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-300">String</span></span> | <span data-ttu-id="cf2c2-301">Identificateur de groupe</span><span class="sxs-lookup"><span data-stu-id="cf2c2-301">Group Identifier</span></span> |
| <span data-ttu-id="cf2c2-302">responseId</span><span class="sxs-lookup"><span data-stu-id="cf2c2-302">responseId</span></span> | <span data-ttu-id="cf2c2-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-303">String</span></span> | <span data-ttu-id="cf2c2-304">GUID de l’identification de réponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-304">GUID for identifying that Response</span></span> |
| <span data-ttu-id="cf2c2-305">responseDetails</span><span class="sxs-lookup"><span data-stu-id="cf2c2-305">responseDetails</span></span> | <span data-ttu-id="cf2c2-306">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="cf2c2-306">String Array</span></span> | <span data-ttu-id="cf2c2-307">Tableau d’objets 'responseWithQuestions'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-307">Array of 'responseWithQuestions' Objects</span></span> |
| <span data-ttu-id="cf2c2-308">répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-308">responder</span></span> | <span data-ttu-id="cf2c2-309">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-309">String</span></span> | <span data-ttu-id="cf2c2-310">Numéro de téléphone du répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-310">responder's Phone Number</span></span> |
| <span data-ttu-id="cf2c2-311">responderName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-311">responderName</span></span> | <span data-ttu-id="cf2c2-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-312">String</span></span> | <span data-ttu-id="cf2c2-313">Nom de l’auteur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-313">responder's Name</span></span> |
| <span data-ttu-id="cf2c2-314">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="cf2c2-314">responderProfilePic</span></span> | <span data-ttu-id="cf2c2-315">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-315">url</span></span> | <span data-ttu-id="cf2c2-316">URL de pic de profil du répondeur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-316">url of the responder's profile pic</span></span> |
| <span data-ttu-id="cf2c2-317">é anonyme</span><span class="sxs-lookup"><span data-stu-id="cf2c2-317">isAnonymous</span></span> | <span data-ttu-id="cf2c2-318">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-318">Boolean</span></span> | <span data-ttu-id="cf2c2-319">Est la réponse d’enquête été présentée de manière anonyme</span><span class="sxs-lookup"><span data-stu-id="cf2c2-319">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="cf2c2-320">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="cf2c2-320">isUpdateResponse</span></span> | <span data-ttu-id="cf2c2-321">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-321">Boolean</span></span> | <span data-ttu-id="cf2c2-322">A la réponse été mis à jour par le répondeur, étant donné que la réponse a été précédemment envoyée</span><span class="sxs-lookup"><span data-stu-id="cf2c2-322">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="cf2c2-323">Détails du schéma pour l’objet 'responseWithQuestions'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-323">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="cf2c2-324">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-324">Parameter</span></span> | <span data-ttu-id="cf2c2-325">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-325">Type</span></span> | <span data-ttu-id="cf2c2-326">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-327">title</span><span class="sxs-lookup"><span data-stu-id="cf2c2-327">title</span></span> | <span data-ttu-id="cf2c2-328">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-328">String</span></span> | <span data-ttu-id="cf2c2-329">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="cf2c2-329">Question Title</span></span> |
| <span data-ttu-id="cf2c2-330">type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-330">type</span></span> | <span data-ttu-id="cf2c2-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-331">String</span></span> | <span data-ttu-id="cf2c2-332">QuestionType</span><span class="sxs-lookup"><span data-stu-id="cf2c2-332">QuestionType</span></span> |
| <span data-ttu-id="cf2c2-333">options</span><span class="sxs-lookup"><span data-stu-id="cf2c2-333">options</span></span> | <span data-ttu-id="cf2c2-334">Tableau</span><span class="sxs-lookup"><span data-stu-id="cf2c2-334">Array</span></span> | <span data-ttu-id="cf2c2-335">Liste d’options applicables aux questions choice multiple</span><span class="sxs-lookup"><span data-stu-id="cf2c2-335">List of options applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="cf2c2-336">answer</span><span class="sxs-lookup"><span data-stu-id="cf2c2-336">answer</span></span> | <span data-ttu-id="cf2c2-337">Tableau de l’objet Json</span><span class="sxs-lookup"><span data-stu-id="cf2c2-337">Array of Json Object</span></span> | <span data-ttu-id="cf2c2-338">Réponses</span><span class="sxs-lookup"><span data-stu-id="cf2c2-338">Answers</span></span> |
| <span data-ttu-id="cf2c2-339">isInvisible</span><span class="sxs-lookup"><span data-stu-id="cf2c2-339">isInvisible</span></span> | <span data-ttu-id="cf2c2-340">Bool�en</span><span class="sxs-lookup"><span data-stu-id="cf2c2-340">Boolean</span></span> | <span data-ttu-id="cf2c2-341">La question est masquée dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf2c2-341">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a><span data-ttu-id="cf2c2-342">Exemple de réponse webHook pour 'SurveyResponse' 'ActionResponse'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-342">Sample webHook response for 'SurveyResponse' 'ActionResponse'</span></span>
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


### <a name="data-for-event-memberadded--memberremoved"></a><span data-ttu-id="cf2c2-343">données pour l’événement 'MemberAdded' / 'MemberRemoved'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-343">data for event 'MemberAdded' / 'MemberRemoved'</span></span>
| <span data-ttu-id="cf2c2-344">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-344">Parameter</span></span> | <span data-ttu-id="cf2c2-345">Type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-345">Type</span></span> | <span data-ttu-id="cf2c2-346">Description</span><span class="sxs-lookup"><span data-stu-id="cf2c2-346">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="cf2c2-347">membre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-347">member</span></span> | <span data-ttu-id="cf2c2-348">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-348">String</span></span> | <span data-ttu-id="cf2c2-349">Numéro de téléphone du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="cf2c2-349">Phone Number of the added Member</span></span> |
| <span data-ttu-id="cf2c2-350">NomMembre</span><span class="sxs-lookup"><span data-stu-id="cf2c2-350">memberName</span></span> | <span data-ttu-id="cf2c2-351">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-351">String</span></span> | <span data-ttu-id="cf2c2-352">Nom du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="cf2c2-352">Name of the added Member</span></span> |
| <span data-ttu-id="cf2c2-353">type</span><span class="sxs-lookup"><span data-stu-id="cf2c2-353">type</span></span> | <span data-ttu-id="cf2c2-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="cf2c2-354">String</span></span> | <span data-ttu-id="cf2c2-355">L’appartenance au rôle du membre ajouté</span><span class="sxs-lookup"><span data-stu-id="cf2c2-355">Membership role of the added member</span></span> |
| <span data-ttu-id="cf2c2-356">memberProfilePic</span><span class="sxs-lookup"><span data-stu-id="cf2c2-356">memberProfilePic</span></span> | <span data-ttu-id="cf2c2-357">url</span><span class="sxs-lookup"><span data-stu-id="cf2c2-357">url</span></span> | <span data-ttu-id="cf2c2-358">URL de pic de profil de la personne affectée au</span><span class="sxs-lookup"><span data-stu-id="cf2c2-358">url of the assignee's profile pic</span></span> |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a><span data-ttu-id="cf2c2-359">Exemple de réponse webHook pour 'MemberAdded' / 'MemberRemoved'</span><span class="sxs-lookup"><span data-stu-id="cf2c2-359">Sample webHook response for 'MemberAdded' /'MemberRemoved'</span></span>
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

