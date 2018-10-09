---
title: /webhooks
description: Article de référence de l’API gérer les abonnements Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 00cbca686e8948d61425f067356e8c7eadb1892c
ms.sourcegitcommit: 27dd3ded71b4a77258961a2fc93c1ec0d02f2980
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25450927"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="384a0-103">API pour inscrire et gérer des webhooks</span><span class="sxs-lookup"><span data-stu-id="384a0-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="384a0-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-104">/webhook</span></span>
<span data-ttu-id="384a0-105">Prévoit d’API pour gérer les abonnements aux événements à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="384a0-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="384a0-106">WebHooks est un modèle HTTP léger fournit un modèle d’éditeur/abonné simple pour câblage ensemble SaaS et les API de Web services.</span><span class="sxs-lookup"><span data-stu-id="384a0-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="384a0-107">Lorsqu’un événement se produit dans Kaizala, une notification est envoyée sous la forme d’une demande HTTP POST pour les abonnés.</span><span class="sxs-lookup"><span data-stu-id="384a0-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="384a0-108">La demande POST contient des informations sur l’événement qui rend possible pour le récepteur d’agir en conséquence.</span><span class="sxs-lookup"><span data-stu-id="384a0-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="384a0-109">À l’aide de WebHooks, vous pouvez vous abonner à différents événements qui se produisent dans un contexte de groupe de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="384a0-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="384a0-110">VALIDER /webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="384a0-111">Pour vérifier que votre point de terminaison de service webhook est authentique et qu’elle fonctionne nous allons maintenant vérifier votre URL de rappel avant de créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="384a0-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="384a0-112">Pour la vérification, nous vous enverrons un jeton de validation dont vous aurez besoin pour nous envoyer dans les 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="384a0-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="384a0-113">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="384a0-113">Read More</span></span>](WebHookValidaton.md)

#### <a name="request-parameters"></a><span data-ttu-id="384a0-114">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-114">Request Parameters</span></span>

|  | <span data-ttu-id="384a0-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-115">Parameter</span></span> | <span data-ttu-id="384a0-116">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-116">Type</span></span> | <span data-ttu-id="384a0-117">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-117">Optional?</span></span> | <span data-ttu-id="384a0-118">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-119">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="384a0-119">HTTP Header</span></span> | <span data-ttu-id="384a0-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="384a0-120">accessToken</span></span> | <span data-ttu-id="384a0-121">String</span><span class="sxs-lookup"><span data-stu-id="384a0-121">String</span></span> | <span data-ttu-id="384a0-122">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-122">No</span></span> | <span data-ttu-id="384a0-123">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="384a0-124">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="384a0-124">HTTP Header</span></span> | <span data-ttu-id="384a0-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="384a0-125">Content-Type</span></span> | <span data-ttu-id="384a0-126">String</span><span class="sxs-lookup"><span data-stu-id="384a0-126">String</span></span> | <span data-ttu-id="384a0-127">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-127">No</span></span> | <span data-ttu-id="384a0-128">« application/json »</span><span class="sxs-lookup"><span data-stu-id="384a0-128">"application/json"</span></span> |

#### <a name="request-body"></a><span data-ttu-id="384a0-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-129">Request body</span></span>

|  <span data-ttu-id="384a0-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-130">Parameter</span></span> | <span data-ttu-id="384a0-131">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-131">Type</span></span> | <span data-ttu-id="384a0-132">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-132">Optional?</span></span> | <span data-ttu-id="384a0-133">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-134">objectId</span><span class="sxs-lookup"><span data-stu-id="384a0-134">objectId</span></span> | <span data-ttu-id="384a0-135">String</span><span class="sxs-lookup"><span data-stu-id="384a0-135">String</span></span> | <span data-ttu-id="384a0-136">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-136">No</span></span> | <span data-ttu-id="384a0-137">Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="384a0-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="384a0-138">objectType</span><span class="sxs-lookup"><span data-stu-id="384a0-138">objectType</span></span> | <span data-ttu-id="384a0-139">String</span><span class="sxs-lookup"><span data-stu-id="384a0-139">String</span></span> | <span data-ttu-id="384a0-140">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-140">No</span></span> | <span data-ttu-id="384a0-141">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="384a0-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="384a0-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="384a0-142">eventTypes</span></span> | <span data-ttu-id="384a0-143">Tableau</span><span class="sxs-lookup"><span data-stu-id="384a0-143">Array</span></span> | <span data-ttu-id="384a0-144">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-144">No</span></span> | <span data-ttu-id="384a0-145">Tableau de différents types d’événements, à que vous devez vous inscrire le webhook.</span><span class="sxs-lookup"><span data-stu-id="384a0-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="384a0-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="384a0-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="384a0-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="384a0-147">callBackUrl</span></span> | <span data-ttu-id="384a0-148">String</span><span class="sxs-lookup"><span data-stu-id="384a0-148">String</span></span> | <span data-ttu-id="384a0-149">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-149">No</span></span> | <span data-ttu-id="384a0-150">URL HTTPS vers lequel doivent être notifiés pour les événements auxquels vous êtes abonnés</span><span class="sxs-lookup"><span data-stu-id="384a0-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="384a0-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="384a0-151">callBackToken</span></span> | <span data-ttu-id="384a0-152">String</span><span class="sxs-lookup"><span data-stu-id="384a0-152">String</span></span> | <span data-ttu-id="384a0-153">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-153">Yes</span></span> | <span data-ttu-id="384a0-154">Paramètre facultatif vous pouvez définir qui seront envoyées dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-155">callBackContext</span><span class="sxs-lookup"><span data-stu-id="384a0-155">callBackContext</span></span> | <span data-ttu-id="384a0-156">String</span><span class="sxs-lookup"><span data-stu-id="384a0-156">String</span></span> | <span data-ttu-id="384a0-157">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-157">Yes</span></span> | <span data-ttu-id="384a0-158">Paramètre facultatif vous pouvez définir qui seront envoyées dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-159">validité</span><span class="sxs-lookup"><span data-stu-id="384a0-159">validity</span></span> | <span data-ttu-id="384a0-160">String</span><span class="sxs-lookup"><span data-stu-id="384a0-160">String</span></span> | <span data-ttu-id="384a0-161">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-161">Yes</span></span> | <span data-ttu-id="384a0-162">Validité pour le WebHook actif au format d’origine.</span><span class="sxs-lookup"><span data-stu-id="384a0-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="384a0-163">Valeur par défaut est de 2 ans</span><span class="sxs-lookup"><span data-stu-id="384a0-163">Default is 2 years</span></span> |


#### <a name="response-body"></a><span data-ttu-id="384a0-164">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="384a0-164">Response body</span></span>
| <span data-ttu-id="384a0-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-165">Parameter</span></span> | <span data-ttu-id="384a0-166">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-166">Type</span></span> | <span data-ttu-id="384a0-167">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="384a0-168">webhookId</span><span class="sxs-lookup"><span data-stu-id="384a0-168">webhookId</span></span> | <span data-ttu-id="384a0-169">String</span><span class="sxs-lookup"><span data-stu-id="384a0-169">String</span></span> | <span data-ttu-id="384a0-170">Identificateur représentant le webHook créé</span><span class="sxs-lookup"><span data-stu-id="384a0-170">Identifier representing the webHook created</span></span> |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="384a0-171">Corps - de requête s’abonner à tous les événements au niveau de groupe</span><span class="sxs-lookup"><span data-stu-id="384a0-171">Request Body - Subscribe to all events at group level</span></span>

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


<span data-ttu-id="384a0-172">Vous pouvez trouver le schéma de réponse webhook les événements inscrits dans Kaizala [**ici**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="384a0-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

### <a name="get-webhook"></a><span data-ttu-id="384a0-173">Obtenir /webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-173">Get /webhook</span></span>

    GET {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a><span data-ttu-id="384a0-174">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-174">Request Parameters</span></span>


|  | <span data-ttu-id="384a0-175">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-175">Parameter</span></span> | <span data-ttu-id="384a0-176">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-176">Type</span></span> | <span data-ttu-id="384a0-177">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-177">Optional?</span></span> | <span data-ttu-id="384a0-178">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-178">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-179">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="384a0-179">HTTP Header</span></span> | <span data-ttu-id="384a0-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="384a0-180">accessToken</span></span> | <span data-ttu-id="384a0-181">String</span><span class="sxs-lookup"><span data-stu-id="384a0-181">String</span></span> | <span data-ttu-id="384a0-182">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-182">No</span></span> | <span data-ttu-id="384a0-183">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-183">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="384a0-184">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="384a0-184">Query parameter</span></span> | <span data-ttu-id="384a0-185">objectId</span><span class="sxs-lookup"><span data-stu-id="384a0-185">objectId</span></span> | <span data-ttu-id="384a0-186">String</span><span class="sxs-lookup"><span data-stu-id="384a0-186">String</span></span> | <span data-ttu-id="384a0-187">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-187">No</span></span> | <span data-ttu-id="384a0-188">Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="384a0-188">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="384a0-189">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="384a0-189">Query parameter</span></span> | <span data-ttu-id="384a0-190">objectType</span><span class="sxs-lookup"><span data-stu-id="384a0-190">objectType</span></span> | <span data-ttu-id="384a0-191">String</span><span class="sxs-lookup"><span data-stu-id="384a0-191">String</span></span> | <span data-ttu-id="384a0-192">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-192">No</span></span> | <span data-ttu-id="384a0-193">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="384a0-193">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

#### <a name="response-body"></a><span data-ttu-id="384a0-194">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="384a0-194">Response body</span></span>

| <span data-ttu-id="384a0-195">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-195">Parameter</span></span> | <span data-ttu-id="384a0-196">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-196">Type</span></span> | <span data-ttu-id="384a0-197">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-197">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="384a0-198">webhooks</span><span class="sxs-lookup"><span data-stu-id="384a0-198">webhooks</span></span> | <span data-ttu-id="384a0-199">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="384a0-199">JSON Object Array</span></span> | <span data-ttu-id="384a0-200">Tableau de webhooks souscrit sur objectId</span><span class="sxs-lookup"><span data-stu-id="384a0-200">Array of webhooks subscribed on the objectId</span></span> |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="384a0-201">Structure de JSON pour chaque webhook individuel dans le tableau webhooks [-] :</span><span class="sxs-lookup"><span data-stu-id="384a0-201">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="384a0-202">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-202">Parameter</span></span> | <span data-ttu-id="384a0-203">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-203">Type</span></span> | <span data-ttu-id="384a0-204">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="384a0-205">id</span><span class="sxs-lookup"><span data-stu-id="384a0-205">id</span></span> | <span data-ttu-id="384a0-206">String</span><span class="sxs-lookup"><span data-stu-id="384a0-206">String</span></span> | <span data-ttu-id="384a0-207">Identificateur Webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-207">Webhook Identifier</span></span> |
| <span data-ttu-id="384a0-208">objectId</span><span class="sxs-lookup"><span data-stu-id="384a0-208">objectId</span></span> | <span data-ttu-id="384a0-209">String</span><span class="sxs-lookup"><span data-stu-id="384a0-209">String</span></span> | <span data-ttu-id="384a0-210">Identificateur d’objet</span><span class="sxs-lookup"><span data-stu-id="384a0-210">Object Identifier</span></span> |
| <span data-ttu-id="384a0-211">objectType</span><span class="sxs-lookup"><span data-stu-id="384a0-211">objectType</span></span> | <span data-ttu-id="384a0-212">String</span><span class="sxs-lookup"><span data-stu-id="384a0-212">String</span></span> | <span data-ttu-id="384a0-213">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="384a0-213">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="384a0-214">events</span><span class="sxs-lookup"><span data-stu-id="384a0-214">events</span></span> | <span data-ttu-id="384a0-215">String]</span><span class="sxs-lookup"><span data-stu-id="384a0-215">String[]</span></span> | <span data-ttu-id="384a0-216">Liste des événements avec chaque valeur comme « ActionCreated », « ActionResponse », « SurveyCreated », « JobCreated », « SurveyResponse », « JobResponse », « TextMessageCreated », « AttachmentCreated », « Announcement », « MemberAdded », « MemberRemoved », « GroupAdded » » GroupRemoved »</span><span class="sxs-lookup"><span data-stu-id="384a0-216">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="384a0-217">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="384a0-217">callBackUrl</span></span> | <span data-ttu-id="384a0-218">String</span><span class="sxs-lookup"><span data-stu-id="384a0-218">String</span></span> | <span data-ttu-id="384a0-219">URL de rappel à laquelle doivent être notifiés pour les événements auxquels vous êtes abonnés</span><span class="sxs-lookup"><span data-stu-id="384a0-219">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="384a0-220">callBackToken</span><span class="sxs-lookup"><span data-stu-id="384a0-220">callBackToken</span></span> | <span data-ttu-id="384a0-221">String</span><span class="sxs-lookup"><span data-stu-id="384a0-221">String</span></span> | <span data-ttu-id="384a0-222">Paramètre qui sera envoyé dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-222">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-223">callBackContext</span><span class="sxs-lookup"><span data-stu-id="384a0-223">callBackContext</span></span> | <span data-ttu-id="384a0-224">String</span><span class="sxs-lookup"><span data-stu-id="384a0-224">String</span></span> | <span data-ttu-id="384a0-225">Paramètre envoyé dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-225">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-226">validité</span><span class="sxs-lookup"><span data-stu-id="384a0-226">validity</span></span> | <span data-ttu-id="384a0-227">String</span><span class="sxs-lookup"><span data-stu-id="384a0-227">String</span></span> | <span data-ttu-id="384a0-228">Validité pour le WebHook actif au format d’origine.</span><span class="sxs-lookup"><span data-stu-id="384a0-228">Validity for the WebHook to be active in EPOCH format.</span></span> |
| <span data-ttu-id="384a0-229">Active</span><span class="sxs-lookup"><span data-stu-id="384a0-229">active</span></span> | <span data-ttu-id="384a0-230">Boolean</span><span class="sxs-lookup"><span data-stu-id="384a0-230">Boolean</span></span> | <span data-ttu-id="384a0-231">Valeur True, si l’état de webhook est actif</span><span class="sxs-lookup"><span data-stu-id="384a0-231">True, if the state of webhook is active</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="384a0-232">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="384a0-232">Sample JSON Response</span></span>

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

### <a name="delete-webhook"></a><span data-ttu-id="384a0-233">Supprimer /webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-233">Delete /webhook</span></span>

    DELETE {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a><span data-ttu-id="384a0-234">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-234">Request Parameters</span></span>
|  | <span data-ttu-id="384a0-235">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-235">Parameter</span></span> | <span data-ttu-id="384a0-236">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-236">Type</span></span> | <span data-ttu-id="384a0-237">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-237">Optional?</span></span> | <span data-ttu-id="384a0-238">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-238">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-239">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="384a0-239">HTTP Header</span></span> | <span data-ttu-id="384a0-240">accessToken</span><span class="sxs-lookup"><span data-stu-id="384a0-240">accessToken</span></span> | <span data-ttu-id="384a0-241">String</span><span class="sxs-lookup"><span data-stu-id="384a0-241">String</span></span> | <span data-ttu-id="384a0-242">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-242">No</span></span> | <span data-ttu-id="384a0-243">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-243">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="384a0-244">Paramètre de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-244">Path parameter</span></span> | <span data-ttu-id="384a0-245">webhookId</span><span class="sxs-lookup"><span data-stu-id="384a0-245">webhookId</span></span> | <span data-ttu-id="384a0-246">String</span><span class="sxs-lookup"><span data-stu-id="384a0-246">String</span></span> | <span data-ttu-id="384a0-247">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-247">No</span></span> | <span data-ttu-id="384a0-248">Identificateur Webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-248">Webhook Identifier</span></span> |

### <a name="put-webhook"></a><span data-ttu-id="384a0-249">Placez /webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-249">PUT /webhook</span></span>

    PUT {endpoint-url}/v1/webhook/{webhookId}

<span data-ttu-id="384a0-250">N’importe quel paramètre pour la webhook peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="384a0-250">Any parameter for the webhook can be updated.</span></span> <span data-ttu-id="384a0-251">Corps de la requête peut contenir des paramètres 1 ou plus, selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="384a0-251">Request Body may contain 1 or more parameters, as needed.</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="384a0-252">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-252">Request Parameters</span></span>

|  | <span data-ttu-id="384a0-253">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-253">Parameter</span></span> | <span data-ttu-id="384a0-254">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-254">Type</span></span> | <span data-ttu-id="384a0-255">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-255">Optional?</span></span> | <span data-ttu-id="384a0-256">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-257">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="384a0-257">HTTP Header</span></span> | <span data-ttu-id="384a0-258">accessToken</span><span class="sxs-lookup"><span data-stu-id="384a0-258">accessToken</span></span> | <span data-ttu-id="384a0-259">String</span><span class="sxs-lookup"><span data-stu-id="384a0-259">String</span></span> | <span data-ttu-id="384a0-260">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-260">No</span></span> | <span data-ttu-id="384a0-261">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-261">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="384a0-262">Paramètre de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="384a0-262">Path parameter</span></span> | <span data-ttu-id="384a0-263">webhookId</span><span class="sxs-lookup"><span data-stu-id="384a0-263">webhookId</span></span> | <span data-ttu-id="384a0-264">String</span><span class="sxs-lookup"><span data-stu-id="384a0-264">String</span></span> | <span data-ttu-id="384a0-265">Non</span><span class="sxs-lookup"><span data-stu-id="384a0-265">No</span></span> | <span data-ttu-id="384a0-266">Identificateur Webhook</span><span class="sxs-lookup"><span data-stu-id="384a0-266">Webhook Identifier</span></span> |

#### <a name="request-body"></a><span data-ttu-id="384a0-267">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="384a0-267">Request body</span></span>

|  <span data-ttu-id="384a0-268">Paramètre</span><span class="sxs-lookup"><span data-stu-id="384a0-268">Parameter</span></span> | <span data-ttu-id="384a0-269">Type</span><span class="sxs-lookup"><span data-stu-id="384a0-269">Type</span></span> | <span data-ttu-id="384a0-270">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="384a0-270">Optional?</span></span> | <span data-ttu-id="384a0-271">Description</span><span class="sxs-lookup"><span data-stu-id="384a0-271">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="384a0-272">objectId</span><span class="sxs-lookup"><span data-stu-id="384a0-272">objectId</span></span> | <span data-ttu-id="384a0-273">String</span><span class="sxs-lookup"><span data-stu-id="384a0-273">String</span></span> | <span data-ttu-id="384a0-274">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-274">Yes</span></span> | <span data-ttu-id="384a0-275">Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="384a0-275">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="384a0-276">objectType</span><span class="sxs-lookup"><span data-stu-id="384a0-276">objectType</span></span> | <span data-ttu-id="384a0-277">String</span><span class="sxs-lookup"><span data-stu-id="384a0-277">String</span></span> | <span data-ttu-id="384a0-278">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-278">Yes</span></span> | <span data-ttu-id="384a0-279">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="384a0-279">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="384a0-280">eventTypes</span><span class="sxs-lookup"><span data-stu-id="384a0-280">eventTypes</span></span> | <span data-ttu-id="384a0-281">Tableau</span><span class="sxs-lookup"><span data-stu-id="384a0-281">Array</span></span> | <span data-ttu-id="384a0-282">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-282">Yes</span></span> | <span data-ttu-id="384a0-283">Tableau de différents types d’événements, à que vous devez vous inscrire le webhook.</span><span class="sxs-lookup"><span data-stu-id="384a0-283">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="384a0-284">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="384a0-284">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="384a0-285">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="384a0-285">callBackUrl</span></span> | <span data-ttu-id="384a0-286">String</span><span class="sxs-lookup"><span data-stu-id="384a0-286">String</span></span> | <span data-ttu-id="384a0-287">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-287">Yes</span></span> | <span data-ttu-id="384a0-288">URL HTTPS vers lequel doivent être notifiés pour les événements auxquels vous êtes abonnés</span><span class="sxs-lookup"><span data-stu-id="384a0-288">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="384a0-289">callBackToken</span><span class="sxs-lookup"><span data-stu-id="384a0-289">callBackToken</span></span> | <span data-ttu-id="384a0-290">String</span><span class="sxs-lookup"><span data-stu-id="384a0-290">String</span></span> | <span data-ttu-id="384a0-291">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-291">Yes</span></span> | <span data-ttu-id="384a0-292">Paramètre facultatif vous pouvez définir qui seront envoyées dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-292">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-293">callBackContext</span><span class="sxs-lookup"><span data-stu-id="384a0-293">callBackContext</span></span> | <span data-ttu-id="384a0-294">String</span><span class="sxs-lookup"><span data-stu-id="384a0-294">String</span></span> | <span data-ttu-id="384a0-295">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-295">Yes</span></span> | <span data-ttu-id="384a0-296">Paramètre facultatif vous pouvez définir qui seront envoyées dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook</span><span class="sxs-lookup"><span data-stu-id="384a0-296">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="384a0-297">validité</span><span class="sxs-lookup"><span data-stu-id="384a0-297">validity</span></span> | <span data-ttu-id="384a0-298">String</span><span class="sxs-lookup"><span data-stu-id="384a0-298">String</span></span> | <span data-ttu-id="384a0-299">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-299">Yes</span></span> | <span data-ttu-id="384a0-300">Validité pour le WebHook actif au format d’origine.</span><span class="sxs-lookup"><span data-stu-id="384a0-300">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="384a0-301">Valeur par défaut est de 2 ans</span><span class="sxs-lookup"><span data-stu-id="384a0-301">Default is 2 years</span></span> |
| <span data-ttu-id="384a0-302">Actif</span><span class="sxs-lookup"><span data-stu-id="384a0-302">Active</span></span> | <span data-ttu-id="384a0-303">Booléen</span><span class="sxs-lookup"><span data-stu-id="384a0-303">Boolean</span></span> | <span data-ttu-id="384a0-304">Oui</span><span class="sxs-lookup"><span data-stu-id="384a0-304">Yes</span></span> | <span data-ttu-id="384a0-305">Modifier l’état de webhook actif, si la valeur est true</span><span class="sxs-lookup"><span data-stu-id="384a0-305">Change the state of webhook to Active, if the value is true</span></span> |


#### <a name="sample-request-body"></a><span data-ttu-id="384a0-306">Corps de demande d’exemple</span><span class="sxs-lookup"><span data-stu-id="384a0-306">Sample Request Body</span></span>

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

## <a name="auto-disable-of-webhooks"></a><span data-ttu-id="384a0-307">Désactivation automatique de Webhooks</span><span class="sxs-lookup"><span data-stu-id="384a0-307">Auto-Disable of Webhooks</span></span>

<span data-ttu-id="384a0-308">Pour améliorer la fiabilité de nos Webhooks, nous avons récemment ajouté la logique de désactivation et de réessayer.</span><span class="sxs-lookup"><span data-stu-id="384a0-308">To improve the Reliability of our Webhooks, we recently have added the Retry and Disabling Logic.</span></span> <span data-ttu-id="384a0-309">Le rappel Url/point de terminaison auprès d’un webhook, si elle est inaccessible ou ne répond pas avec un code d’état autre que 2xx (> = 3xx), puis notre Service essaiera de portée/réessayer il de 6 fois de manière exponentielle dans une plage de 2 jours.</span><span class="sxs-lookup"><span data-stu-id="384a0-309">The Callback Url/Endpoint registered with a webhook, if not reachable or does not respond with a status code other than 2xx (>=3xx), then our Service will try to reach/retry it for 6 times in an exponential way within a span of 2 Days.</span></span> 

<span data-ttu-id="384a0-310">Si elle échoue encore pour 2 jours, puis le Webhook correspondant sera désactivé et le propriétaire doit mettre à jour avec l’API de /webhook Put avant le début de votre travail.</span><span class="sxs-lookup"><span data-stu-id="384a0-310">If it is still failing for 2 days, then the corresponding Webhook will be disabled, and the owner needs to update it with the Put /webhook API before it starts working again.</span></span> <span data-ttu-id="384a0-311">Pour, par exemple</span><span class="sxs-lookup"><span data-stu-id="384a0-311">For e.g.</span></span>

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a><span data-ttu-id="384a0-312">Corps de la demande :</span><span class="sxs-lookup"><span data-stu-id="384a0-312">Request Body:</span></span>
````javascript
{ 
  "Active": "true" 
} 
````
