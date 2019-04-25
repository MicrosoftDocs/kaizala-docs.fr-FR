---
title: /webhooks
description: Article de référence pour l'API permettant de gérer les abonnements Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: a2cdb74284f6980644366cf3b61740ea46389512
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190731"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="23e84-103">API pour inscrire & gérer les webhooks</span><span class="sxs-lookup"><span data-stu-id="23e84-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="23e84-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-104">/webhook</span></span>
<span data-ttu-id="23e84-105">Point de terminaison de l'API pour gérer les abonnements aux événements dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="23e84-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="23e84-106">Les webHooks sont un modèle HTTP léger qui fournit un modèle d'éditeur/d'abonné simple pour le câblage des API Web et des services SaaS.</span><span class="sxs-lookup"><span data-stu-id="23e84-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="23e84-107">Lorsqu'un événement se produit dans Kaizala, une notification est envoyée sous la forme d'une demande HTTP POST aux abonnés inscrits.</span><span class="sxs-lookup"><span data-stu-id="23e84-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="23e84-108">La requête POST contient des informations sur l'événement, ce qui permet au destinataire d'agir en conséquence.</span><span class="sxs-lookup"><span data-stu-id="23e84-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="23e84-109">À l'aide des webHooks, vous pouvez vous abonner à différents événements qui se produisent dans un contexte de groupe de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="23e84-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="23e84-110">POST/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="23e84-111">Pour vérifier que votre point de terminaison de service webhook est authentique et que nous travaillons, nous allons vérifier votre URL de rappel avant de créer un abonnement.</span><span class="sxs-lookup"><span data-stu-id="23e84-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="23e84-112">Pour la vérification, nous vous enverrons un jeton de validation dont vous avez besoin pour nous envoyer vos commentaires dans un délai de 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="23e84-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="23e84-113">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="23e84-113">Read More</span></span>](WebHookValidaton.md)

#### <a name="request-parameters"></a><span data-ttu-id="23e84-114">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-114">Request Parameters</span></span>

|  | <span data-ttu-id="23e84-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-115">Parameter</span></span> | <span data-ttu-id="23e84-116">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-116">Type</span></span> | <span data-ttu-id="23e84-117">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-117">Optional?</span></span> | <span data-ttu-id="23e84-118">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-119">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="23e84-119">HTTP Header</span></span> | <span data-ttu-id="23e84-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="23e84-120">accessToken</span></span> | <span data-ttu-id="23e84-121">String</span><span class="sxs-lookup"><span data-stu-id="23e84-121">String</span></span> | <span data-ttu-id="23e84-122">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-122">No</span></span> | <span data-ttu-id="23e84-123">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="23e84-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="23e84-124">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="23e84-124">HTTP Header</span></span> | <span data-ttu-id="23e84-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="23e84-125">Content-Type</span></span> | <span data-ttu-id="23e84-126">String</span><span class="sxs-lookup"><span data-stu-id="23e84-126">String</span></span> | <span data-ttu-id="23e84-127">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-127">No</span></span> | <span data-ttu-id="23e84-128">«application/JSON»</span><span class="sxs-lookup"><span data-stu-id="23e84-128">"application/json"</span></span> |

#### <a name="request-body"></a><span data-ttu-id="23e84-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-129">Request body</span></span>

|  <span data-ttu-id="23e84-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-130">Parameter</span></span> | <span data-ttu-id="23e84-131">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-131">Type</span></span> | <span data-ttu-id="23e84-132">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-132">Optional?</span></span> | <span data-ttu-id="23e84-133">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-134">objectId</span><span class="sxs-lookup"><span data-stu-id="23e84-134">objectId</span></span> | <span data-ttu-id="23e84-135">String</span><span class="sxs-lookup"><span data-stu-id="23e84-135">String</span></span> | <span data-ttu-id="23e84-136">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-136">No</span></span> | <span data-ttu-id="23e84-137">Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID</span><span class="sxs-lookup"><span data-stu-id="23e84-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="23e84-138">objectType</span><span class="sxs-lookup"><span data-stu-id="23e84-138">objectType</span></span> | <span data-ttu-id="23e84-139">String</span><span class="sxs-lookup"><span data-stu-id="23e84-139">String</span></span> | <span data-ttu-id="23e84-140">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-140">No</span></span> | <span data-ttu-id="23e84-141">Énumération: «Group»/«action»/«ActionPackage»</span><span class="sxs-lookup"><span data-stu-id="23e84-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="23e84-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="23e84-142">eventTypes</span></span> | <span data-ttu-id="23e84-143">Tableau</span><span class="sxs-lookup"><span data-stu-id="23e84-143">Array</span></span> | <span data-ttu-id="23e84-144">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-144">No</span></span> | <span data-ttu-id="23e84-145">Tableau des différents types d'événements dont vous avez besoin pour abonner le webhook.</span><span class="sxs-lookup"><span data-stu-id="23e84-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="23e84-146">Les événements pris en charge sont: «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «GroupRemoved», «»</span><span class="sxs-lookup"><span data-stu-id="23e84-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="23e84-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="23e84-147">callBackUrl</span></span> | <span data-ttu-id="23e84-148">String</span><span class="sxs-lookup"><span data-stu-id="23e84-148">String</span></span> | <span data-ttu-id="23e84-149">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-149">No</span></span> | <span data-ttu-id="23e84-150">URL HTTPs à laquelle les événements abonnés doivent être notifiés</span><span class="sxs-lookup"><span data-stu-id="23e84-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="23e84-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="23e84-151">callBackToken</span></span> | <span data-ttu-id="23e84-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-152">String</span></span> | <span data-ttu-id="23e84-153">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-153">Yes</span></span> | <span data-ttu-id="23e84-154">Paramètre facultatif que vous pouvez définir qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-155">callBackContext</span><span class="sxs-lookup"><span data-stu-id="23e84-155">callBackContext</span></span> | <span data-ttu-id="23e84-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-156">String</span></span> | <span data-ttu-id="23e84-157">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-157">Yes</span></span> | <span data-ttu-id="23e84-158">Paramètre facultatif que vous pouvez définir qui sera envoyé dans la charge utile JSON en tant que «Context» avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-159">validité</span><span class="sxs-lookup"><span data-stu-id="23e84-159">validity</span></span> | <span data-ttu-id="23e84-160">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-160">String</span></span> | <span data-ttu-id="23e84-161">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-161">Yes</span></span> | <span data-ttu-id="23e84-162">La validité du webHook est active au format d'époque.</span><span class="sxs-lookup"><span data-stu-id="23e84-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="23e84-163">La valeur par défaut est 2 ans</span><span class="sxs-lookup"><span data-stu-id="23e84-163">Default is 2 years</span></span> |


#### <a name="response-body"></a><span data-ttu-id="23e84-164">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="23e84-164">Response body</span></span>
| <span data-ttu-id="23e84-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-165">Parameter</span></span> | <span data-ttu-id="23e84-166">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-166">Type</span></span> | <span data-ttu-id="23e84-167">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="23e84-168">webhookId</span><span class="sxs-lookup"><span data-stu-id="23e84-168">webhookId</span></span> | <span data-ttu-id="23e84-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-169">String</span></span> | <span data-ttu-id="23e84-170">Identificateur représentant le webHook créé</span><span class="sxs-lookup"><span data-stu-id="23e84-170">Identifier representing the webHook created</span></span> |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="23e84-171">Corps de la demande: s'abonner à tous les événements au niveau du groupe</span><span class="sxs-lookup"><span data-stu-id="23e84-171">Request Body - Subscribe to all events at group level</span></span>

```javascript
{  
   "objectId":"74943849802190eaea3810",
   "objectType":"Group",
   "eventTypes":[
      "ActionCreated",
      "ActionResponse",
      "SurveyCreated",
      "JobCreated",
      "SurveyResponse",
      "JobResponse",
      "TextMessageCreated",
      "AttachmentCreated",
      "Announcement",
      "MemberAdded",
      "MemberRemoved",
      "GroupAdded",
      "GroupRemoved"
   ],
   "callBackUrl":"https://requestb.in/123",
   "callBackToken":"tokenToBeVerifiedByCallback",
   "callBackContext":"Any data which is required to be returned in callback"
}

```


<span data-ttu-id="23e84-172">Vous pouvez trouver le schéma de réponse webhook pour les événements inscrits dans Kaizala [**ici**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="23e84-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

> <span data-ttu-id="23e84-173">**Remarque:** Kaizala garantit au moins une fois la remise de la réponse webhook.</span><span class="sxs-lookup"><span data-stu-id="23e84-173">**Note:** Kaizala guarantees at-least once delivery of webhook response.</span></span> <span data-ttu-id="23e84-174">Cela peut se produire, dans certains cas, que Kaizala peut envoyer une réponse webhook en double pour le même événement.</span><span class="sxs-lookup"><span data-stu-id="23e84-174">It may happen, in certain cases, that Kaizala may send duplicate webhook response for the same event.</span></span>

### <a name="get-webhook"></a><span data-ttu-id="23e84-175">Obtenir/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-175">Get /webhook</span></span>

    <span data-ttu-id="23e84-176">OBTENIR {Endpoint-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-176">GET {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="23e84-177">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-177">Request Parameters</span></span>


|  | <span data-ttu-id="23e84-178">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-178">Parameter</span></span> | <span data-ttu-id="23e84-179">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-179">Type</span></span> | <span data-ttu-id="23e84-180">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-180">Optional?</span></span> | <span data-ttu-id="23e84-181">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-181">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-182">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="23e84-182">HTTP Header</span></span> | <span data-ttu-id="23e84-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="23e84-183">accessToken</span></span> | <span data-ttu-id="23e84-184">String</span><span class="sxs-lookup"><span data-stu-id="23e84-184">String</span></span> | <span data-ttu-id="23e84-185">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-185">No</span></span> | <span data-ttu-id="23e84-186">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="23e84-186">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="23e84-187">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="23e84-187">Query parameter</span></span> | <span data-ttu-id="23e84-188">objectId</span><span class="sxs-lookup"><span data-stu-id="23e84-188">objectId</span></span> | <span data-ttu-id="23e84-189">String</span><span class="sxs-lookup"><span data-stu-id="23e84-189">String</span></span> | <span data-ttu-id="23e84-190">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-190">No</span></span> | <span data-ttu-id="23e84-191">Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID</span><span class="sxs-lookup"><span data-stu-id="23e84-191">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="23e84-192">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="23e84-192">Query parameter</span></span> | <span data-ttu-id="23e84-193">objectType</span><span class="sxs-lookup"><span data-stu-id="23e84-193">objectType</span></span> | <span data-ttu-id="23e84-194">String</span><span class="sxs-lookup"><span data-stu-id="23e84-194">String</span></span> | <span data-ttu-id="23e84-195">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-195">No</span></span> | <span data-ttu-id="23e84-196">Énumération: «Group»/«action»/«ActionPackage»</span><span class="sxs-lookup"><span data-stu-id="23e84-196">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

#### <a name="response-body"></a><span data-ttu-id="23e84-197">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="23e84-197">Response body</span></span>

| <span data-ttu-id="23e84-198">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-198">Parameter</span></span> | <span data-ttu-id="23e84-199">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-199">Type</span></span> | <span data-ttu-id="23e84-200">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="23e84-201">webhooks</span><span class="sxs-lookup"><span data-stu-id="23e84-201">webhooks</span></span> | <span data-ttu-id="23e84-202">Tableau d'objets JSON</span><span class="sxs-lookup"><span data-stu-id="23e84-202">JSON Object Array</span></span> | <span data-ttu-id="23e84-203">Tableau de webhooks abonnés sur objectId</span><span class="sxs-lookup"><span data-stu-id="23e84-203">Array of webhooks subscribed on the objectId</span></span> |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="23e84-204">Structure JSON pour chaque webhook individuel dans le groupe webhooks []:</span><span class="sxs-lookup"><span data-stu-id="23e84-204">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="23e84-205">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-205">Parameter</span></span> | <span data-ttu-id="23e84-206">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-206">Type</span></span> | <span data-ttu-id="23e84-207">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-207">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="23e84-208">id</span><span class="sxs-lookup"><span data-stu-id="23e84-208">id</span></span> | <span data-ttu-id="23e84-209">String</span><span class="sxs-lookup"><span data-stu-id="23e84-209">String</span></span> | <span data-ttu-id="23e84-210">Identificateur de webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-210">Webhook Identifier</span></span> |
| <span data-ttu-id="23e84-211">objectId</span><span class="sxs-lookup"><span data-stu-id="23e84-211">objectId</span></span> | <span data-ttu-id="23e84-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-212">String</span></span> | <span data-ttu-id="23e84-213">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="23e84-213">Object Identifier</span></span> |
| <span data-ttu-id="23e84-214">objectType</span><span class="sxs-lookup"><span data-stu-id="23e84-214">objectType</span></span> | <span data-ttu-id="23e84-215">String</span><span class="sxs-lookup"><span data-stu-id="23e84-215">String</span></span> | <span data-ttu-id="23e84-216">Énumération: «Group»/«action»/«ActionPackage»</span><span class="sxs-lookup"><span data-stu-id="23e84-216">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="23e84-217">events</span><span class="sxs-lookup"><span data-stu-id="23e84-217">events</span></span> | <span data-ttu-id="23e84-218">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="23e84-218">String[]</span></span> | <span data-ttu-id="23e84-219">Liste d'événements avec chaque valeur «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «», « GroupRemoved»</span><span class="sxs-lookup"><span data-stu-id="23e84-219">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="23e84-220">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="23e84-220">callBackUrl</span></span> | <span data-ttu-id="23e84-221">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-221">String</span></span> | <span data-ttu-id="23e84-222">URL de rappel à laquelle les événements abonnés doivent être notifiés</span><span class="sxs-lookup"><span data-stu-id="23e84-222">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="23e84-223">callBackToken</span><span class="sxs-lookup"><span data-stu-id="23e84-223">callBackToken</span></span> | <span data-ttu-id="23e84-224">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-224">String</span></span> | <span data-ttu-id="23e84-225">Paramètre qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-225">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-226">callBackContext</span><span class="sxs-lookup"><span data-stu-id="23e84-226">callBackContext</span></span> | <span data-ttu-id="23e84-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-227">String</span></span> | <span data-ttu-id="23e84-228">Paramètre envoyé dans la charge utile JSON comme «Context» avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-228">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-229">validité</span><span class="sxs-lookup"><span data-stu-id="23e84-229">validity</span></span> | <span data-ttu-id="23e84-230">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-230">String</span></span> | <span data-ttu-id="23e84-231">La validité du webHook est active au format d'époque.</span><span class="sxs-lookup"><span data-stu-id="23e84-231">Validity for the WebHook to be active in EPOCH format.</span></span> |
| <span data-ttu-id="23e84-232">Active</span><span class="sxs-lookup"><span data-stu-id="23e84-232">active</span></span> | <span data-ttu-id="23e84-233">Booléen</span><span class="sxs-lookup"><span data-stu-id="23e84-233">Boolean</span></span> | <span data-ttu-id="23e84-234">True si l'état du webhook est actif</span><span class="sxs-lookup"><span data-stu-id="23e84-234">True, if the state of webhook is active</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="23e84-235">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="23e84-235">Sample JSON Response</span></span>

```javascript
{
    "webhooks": [
        {
            "id": "dac6fccf-f2e9-4abc-94d7-793037e99da7",
            "objectId": "b21405d1-4b10-4c46-bfa9-8338592f3782",
            "objectType": "Group",
            "events": [
                "ActionCreated",
                "ActionResponse",
                "SurveyCreated",
                "JobCreated",
                "SurveyResponse",
                "JobResponse",
                "TextMessageCreated",
                "AttachmentCreated",
                "Announcement",
                "MemberAdded",
                "MemberRemoved",
                "GroupAdded",
                "GroupRemoved"
            ],
            "filters": [],
            "callbackUrl": "https://requestb.in/12786un1",
            "callbackToken": "tokenToBeVerifiedByCallback",
            "ts": 1505491564677,
            "validity": 1568605416677
            "active": true
        }
    ]
}
```

### <a name="delete-webhook"></a><span data-ttu-id="23e84-236">Supprimer/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-236">Delete /webhook</span></span>

    <span data-ttu-id="23e84-237">DELETE {Endpoint-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-237">DELETE {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="23e84-238">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-238">Request Parameters</span></span>
|  | <span data-ttu-id="23e84-239">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-239">Parameter</span></span> | <span data-ttu-id="23e84-240">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-240">Type</span></span> | <span data-ttu-id="23e84-241">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-241">Optional?</span></span> | <span data-ttu-id="23e84-242">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-242">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-243">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="23e84-243">HTTP Header</span></span> | <span data-ttu-id="23e84-244">accessToken</span><span class="sxs-lookup"><span data-stu-id="23e84-244">accessToken</span></span> | <span data-ttu-id="23e84-245">String</span><span class="sxs-lookup"><span data-stu-id="23e84-245">String</span></span> | <span data-ttu-id="23e84-246">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-246">No</span></span> | <span data-ttu-id="23e84-247">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="23e84-247">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="23e84-248">Paramètre Path</span><span class="sxs-lookup"><span data-stu-id="23e84-248">Path parameter</span></span> | <span data-ttu-id="23e84-249">webhookId</span><span class="sxs-lookup"><span data-stu-id="23e84-249">webhookId</span></span> | <span data-ttu-id="23e84-250">String</span><span class="sxs-lookup"><span data-stu-id="23e84-250">String</span></span> | <span data-ttu-id="23e84-251">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-251">No</span></span> | <span data-ttu-id="23e84-252">Identificateur de webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-252">Webhook Identifier</span></span> |

### <a name="put-webhook"></a><span data-ttu-id="23e84-253">PUT/webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-253">PUT /webhook</span></span>

    PUT {endpoint-url}/v1/webhook/{webhookId}

<span data-ttu-id="23e84-254">Tout paramètre du webhook peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="23e84-254">Any parameter for the webhook can be updated.</span></span> <span data-ttu-id="23e84-255">Le corps de la demande peut contenir un ou plusieurs paramètres, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="23e84-255">Request Body may contain 1 or more parameters, as needed.</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="23e84-256">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-256">Request Parameters</span></span>

|  | <span data-ttu-id="23e84-257">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-257">Parameter</span></span> | <span data-ttu-id="23e84-258">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-258">Type</span></span> | <span data-ttu-id="23e84-259">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-259">Optional?</span></span> | <span data-ttu-id="23e84-260">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-260">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-261">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="23e84-261">HTTP Header</span></span> | <span data-ttu-id="23e84-262">accessToken</span><span class="sxs-lookup"><span data-stu-id="23e84-262">accessToken</span></span> | <span data-ttu-id="23e84-263">String</span><span class="sxs-lookup"><span data-stu-id="23e84-263">String</span></span> | <span data-ttu-id="23e84-264">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-264">No</span></span> | <span data-ttu-id="23e84-265">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="23e84-265">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="23e84-266">Paramètre Path</span><span class="sxs-lookup"><span data-stu-id="23e84-266">Path parameter</span></span> | <span data-ttu-id="23e84-267">webhookId</span><span class="sxs-lookup"><span data-stu-id="23e84-267">webhookId</span></span> | <span data-ttu-id="23e84-268">String</span><span class="sxs-lookup"><span data-stu-id="23e84-268">String</span></span> | <span data-ttu-id="23e84-269">Non</span><span class="sxs-lookup"><span data-stu-id="23e84-269">No</span></span> | <span data-ttu-id="23e84-270">Identificateur de webhook</span><span class="sxs-lookup"><span data-stu-id="23e84-270">Webhook Identifier</span></span> |

#### <a name="request-body"></a><span data-ttu-id="23e84-271">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="23e84-271">Request body</span></span>

|  <span data-ttu-id="23e84-272">Paramètre</span><span class="sxs-lookup"><span data-stu-id="23e84-272">Parameter</span></span> | <span data-ttu-id="23e84-273">Type</span><span class="sxs-lookup"><span data-stu-id="23e84-273">Type</span></span> | <span data-ttu-id="23e84-274">Module?</span><span class="sxs-lookup"><span data-stu-id="23e84-274">Optional?</span></span> | <span data-ttu-id="23e84-275">Description</span><span class="sxs-lookup"><span data-stu-id="23e84-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="23e84-276">objectId</span><span class="sxs-lookup"><span data-stu-id="23e84-276">objectId</span></span> | <span data-ttu-id="23e84-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-277">String</span></span> | <span data-ttu-id="23e84-278">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-278">Yes</span></span> | <span data-ttu-id="23e84-279">Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID</span><span class="sxs-lookup"><span data-stu-id="23e84-279">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="23e84-280">objectType</span><span class="sxs-lookup"><span data-stu-id="23e84-280">objectType</span></span> | <span data-ttu-id="23e84-281">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-281">String</span></span> | <span data-ttu-id="23e84-282">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-282">Yes</span></span> | <span data-ttu-id="23e84-283">Énumération: «Group»/«action»/«ActionPackage»</span><span class="sxs-lookup"><span data-stu-id="23e84-283">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="23e84-284">eventTypes</span><span class="sxs-lookup"><span data-stu-id="23e84-284">eventTypes</span></span> | <span data-ttu-id="23e84-285">Tableau</span><span class="sxs-lookup"><span data-stu-id="23e84-285">Array</span></span> | <span data-ttu-id="23e84-286">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-286">Yes</span></span> | <span data-ttu-id="23e84-287">Tableau des différents types d'événements dont vous avez besoin pour abonner le webhook.</span><span class="sxs-lookup"><span data-stu-id="23e84-287">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="23e84-288">Les événements pris en charge sont: «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «GroupRemoved», «»</span><span class="sxs-lookup"><span data-stu-id="23e84-288">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="23e84-289">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="23e84-289">callBackUrl</span></span> | <span data-ttu-id="23e84-290">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-290">String</span></span> | <span data-ttu-id="23e84-291">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-291">Yes</span></span> | <span data-ttu-id="23e84-292">URL HTTPs à laquelle les événements abonnés doivent être notifiés</span><span class="sxs-lookup"><span data-stu-id="23e84-292">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="23e84-293">callBackToken</span><span class="sxs-lookup"><span data-stu-id="23e84-293">callBackToken</span></span> | <span data-ttu-id="23e84-294">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-294">String</span></span> | <span data-ttu-id="23e84-295">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-295">Yes</span></span> | <span data-ttu-id="23e84-296">Paramètre facultatif que vous pouvez définir qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-296">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-297">callBackContext</span><span class="sxs-lookup"><span data-stu-id="23e84-297">callBackContext</span></span> | <span data-ttu-id="23e84-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-298">String</span></span> | <span data-ttu-id="23e84-299">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-299">Yes</span></span> | <span data-ttu-id="23e84-300">Paramètre facultatif que vous pouvez définir qui sera envoyé dans la charge utile JSON en tant que «Context» avec chaque rappel effectué par le webHook</span><span class="sxs-lookup"><span data-stu-id="23e84-300">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="23e84-301">validité</span><span class="sxs-lookup"><span data-stu-id="23e84-301">validity</span></span> | <span data-ttu-id="23e84-302">Chaîne</span><span class="sxs-lookup"><span data-stu-id="23e84-302">String</span></span> | <span data-ttu-id="23e84-303">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-303">Yes</span></span> | <span data-ttu-id="23e84-304">La validité du webHook est active au format d'époque.</span><span class="sxs-lookup"><span data-stu-id="23e84-304">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="23e84-305">La valeur par défaut est 2 ans</span><span class="sxs-lookup"><span data-stu-id="23e84-305">Default is 2 years</span></span> |
| <span data-ttu-id="23e84-306">Actif</span><span class="sxs-lookup"><span data-stu-id="23e84-306">Active</span></span> | <span data-ttu-id="23e84-307">Booléen</span><span class="sxs-lookup"><span data-stu-id="23e84-307">Boolean</span></span> | <span data-ttu-id="23e84-308">Oui</span><span class="sxs-lookup"><span data-stu-id="23e84-308">Yes</span></span> | <span data-ttu-id="23e84-309">Définir l'état du webhook sur actif si la valeur est true</span><span class="sxs-lookup"><span data-stu-id="23e84-309">Change the state of webhook to Active, if the value is true</span></span> |


#### <a name="sample-request-body"></a><span data-ttu-id="23e84-310">Exemple de corps de requête</span><span class="sxs-lookup"><span data-stu-id="23e84-310">Sample Request Body</span></span>

````javascript
    { 
       "objectId":"74943849802190eaea3810",
       "objectType":"Group",
       "eventTypes":[
          "ActionCreated",
          "ActionResponse",
          "SurveyCreated",
          "JobCreated",
          "SurveyResponse",
          "JobResponse",
          "TextMessageCreated",
          "AttachmentCreated",
          "Announcement",
          "MemberAdded",
          "MemberRemoved",
          "GroupAdded",
          "GroupRemoved"
       ],
       "callBackUrl":"https://requestb.in/123",
       "callBackToken":"tokenToBeVerifiedByCallback",
      "Active": "true" 
    } 

````

## <a name="auto-disable-of-webhooks"></a><span data-ttu-id="23e84-311">DésActivation automatique des webhooks</span><span class="sxs-lookup"><span data-stu-id="23e84-311">Auto-Disable of Webhooks</span></span>

<span data-ttu-id="23e84-312">Pour améliorer la fiabilité de nos webhooks, nous avons récemment ajouté la nouvelle tentative et la logique de désActivation.</span><span class="sxs-lookup"><span data-stu-id="23e84-312">To improve the Reliability of our Webhooks, we recently have added the Retry and Disabling Logic.</span></span> <span data-ttu-id="23e84-313">L'URL/le point de terminaison de rappel enregistré avec un webhook, s'il n'est pas accessible ou ne répond pas avec un code d'État autre que 2xx (> = 3xx), notre service tentera de l'atteindre/le retenter de 6 fois de manière exponentielle dans un délai de 2 jours.</span><span class="sxs-lookup"><span data-stu-id="23e84-313">The Callback Url/Endpoint registered with a webhook, if not reachable or does not respond with a status code other than 2xx (>=3xx), then our Service will try to reach/retry it for 6 times in an exponential way within a span of 2 Days.</span></span> 

<span data-ttu-id="23e84-314">En cas de défaillance continue pendant 2 jours, le webhook correspondant est désactivé et le propriétaire doit le mettre à jour avec l'API put/webhook avant de commencer à fonctionner à nouveau.</span><span class="sxs-lookup"><span data-stu-id="23e84-314">If it is still failing for 2 days, then the corresponding Webhook will be disabled, and the owner needs to update it with the Put /webhook API before it starts working again.</span></span> <span data-ttu-id="23e84-315">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="23e84-315">For e.g.</span></span>

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a><span data-ttu-id="23e84-316">Corps de la demande:</span><span class="sxs-lookup"><span data-stu-id="23e84-316">Request Body:</span></span>
````javascript
{ 
  "Active": "true" 
} 
````
