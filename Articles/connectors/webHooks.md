---
title: /webhooks
description: Article de référence de l’API gérer les abonnements Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 8b78449ba41042de262bed7e3317771ef33c8031
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905188"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="7ecbf-103">API pour inscrire et gérer des webhooks</span><span class="sxs-lookup"><span data-stu-id="7ecbf-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="7ecbf-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-104">/webhook</span></span>
<span data-ttu-id="7ecbf-105">Prévoit d’API pour gérer les abonnements aux événements à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="7ecbf-106">WebHooks est un modèle HTTP léger fournit un modèle d’éditeur/abonné simple pour câblage ensemble SaaS et les API de Web services.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="7ecbf-107">Lorsqu’un événement se produit dans Kaizala, une notification est envoyée sous la forme d’une demande HTTP POST pour les abonnés.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="7ecbf-108">La demande POST contient des informations sur l’événement qui rend possible pour le récepteur d’agir en conséquence.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="7ecbf-109">À l’aide de WebHooks, vous pouvez vous abonner à différents événements qui se produisent dans un contexte de groupe de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="7ecbf-110">VALIDER /webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="7ecbf-111">Pour vérifier que votre point de terminaison de service webhook est authentique et qu’elle fonctionne nous allons maintenant vérifier votre URL de rappel avant de créer l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="7ecbf-112">Pour la vérification, nous vous enverrons un jeton de validation dont vous aurez besoin pour nous envoyer dans les 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="7ecbf-113">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="7ecbf-113">Read More</span></span>](WebHookValidaton.md)

##### <a name="request-parameters"></a><span data-ttu-id="7ecbf-114">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7ecbf-114">Request Parameters</span></span>

|  | <span data-ttu-id="7ecbf-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-115">Parameter</span></span> | <span data-ttu-id="7ecbf-116">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-116">Type</span></span> | <span data-ttu-id="7ecbf-117">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7ecbf-117">Optional?</span></span> | <span data-ttu-id="7ecbf-118">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-119">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7ecbf-119">HTTP Header</span></span> | <span data-ttu-id="7ecbf-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-120">accessToken</span></span> | <span data-ttu-id="7ecbf-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-121">String</span></span> | <span data-ttu-id="7ecbf-122">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-122">No</span></span> | <span data-ttu-id="7ecbf-123">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7ecbf-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="7ecbf-124">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7ecbf-124">HTTP Header</span></span> | <span data-ttu-id="7ecbf-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-125">Content-Type</span></span> | <span data-ttu-id="7ecbf-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-126">String</span></span> | <span data-ttu-id="7ecbf-127">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-127">No</span></span> | <span data-ttu-id="7ecbf-128">« application/json »</span><span class="sxs-lookup"><span data-stu-id="7ecbf-128">"application/json"</span></span> |

##### <a name="request-body"></a><span data-ttu-id="7ecbf-129">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="7ecbf-129">Request body</span></span>

|  <span data-ttu-id="7ecbf-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-130">Parameter</span></span> | <span data-ttu-id="7ecbf-131">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-131">Type</span></span> | <span data-ttu-id="7ecbf-132">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7ecbf-132">Optional?</span></span> | <span data-ttu-id="7ecbf-133">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-134">objectId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-134">objectId</span></span> | <span data-ttu-id="7ecbf-135">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-135">String</span></span> | <span data-ttu-id="7ecbf-136">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-136">No</span></span> | <span data-ttu-id="7ecbf-137">Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="7ecbf-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="7ecbf-138">objectType</span><span class="sxs-lookup"><span data-stu-id="7ecbf-138">objectType</span></span> | <span data-ttu-id="7ecbf-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-139">String</span></span> | <span data-ttu-id="7ecbf-140">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-140">No</span></span> | <span data-ttu-id="7ecbf-141">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="7ecbf-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="7ecbf-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="7ecbf-142">eventTypes</span></span> | <span data-ttu-id="7ecbf-143">Tableau</span><span class="sxs-lookup"><span data-stu-id="7ecbf-143">Array</span></span> | <span data-ttu-id="7ecbf-144">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-144">No</span></span> | <span data-ttu-id="7ecbf-145">Tableau de différents types d’événements, à que vous devez vous inscrire le webhook.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="7ecbf-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="7ecbf-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="7ecbf-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="7ecbf-147">callBackUrl</span></span> | <span data-ttu-id="7ecbf-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-148">String</span></span> | <span data-ttu-id="7ecbf-149">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-149">No</span></span> | <span data-ttu-id="7ecbf-150">URL HTTPS vers lequel doivent être notifiés pour les événements auxquels vous êtes abonnés</span><span class="sxs-lookup"><span data-stu-id="7ecbf-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="7ecbf-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-151">callBackToken</span></span> | <span data-ttu-id="7ecbf-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-152">String</span></span> | <span data-ttu-id="7ecbf-153">Oui</span><span class="sxs-lookup"><span data-stu-id="7ecbf-153">Yes</span></span> | <span data-ttu-id="7ecbf-154">Paramètre facultatif vous pouvez définir qui seront envoyées dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="7ecbf-155">callBackContext</span><span class="sxs-lookup"><span data-stu-id="7ecbf-155">callBackContext</span></span> | <span data-ttu-id="7ecbf-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-156">String</span></span> | <span data-ttu-id="7ecbf-157">Oui</span><span class="sxs-lookup"><span data-stu-id="7ecbf-157">Yes</span></span> | <span data-ttu-id="7ecbf-158">Paramètre facultatif vous pouvez définir qui seront envoyées dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="7ecbf-159">validité</span><span class="sxs-lookup"><span data-stu-id="7ecbf-159">validity</span></span> | <span data-ttu-id="7ecbf-160">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-160">String</span></span> | <span data-ttu-id="7ecbf-161">Oui</span><span class="sxs-lookup"><span data-stu-id="7ecbf-161">Yes</span></span> | <span data-ttu-id="7ecbf-162">Validité pour le WebHook actif au format d’origine.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="7ecbf-163">Valeur par défaut est de 2 ans</span><span class="sxs-lookup"><span data-stu-id="7ecbf-163">Default is 2 years</span></span> |


##### <a name="response-body"></a><span data-ttu-id="7ecbf-164">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="7ecbf-164">Response body</span></span>
| <span data-ttu-id="7ecbf-165">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-165">Parameter</span></span> | <span data-ttu-id="7ecbf-166">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-166">Type</span></span> | <span data-ttu-id="7ecbf-167">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-168">webhookId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-168">webhookId</span></span> | <span data-ttu-id="7ecbf-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-169">String</span></span> | <span data-ttu-id="7ecbf-170">Identificateur représentant le webHook créé</span><span class="sxs-lookup"><span data-stu-id="7ecbf-170">Identifier representing the webHook created</span></span> |

##### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="7ecbf-171">Corps - de requête s’abonner à tous les événements au niveau de groupe</span><span class="sxs-lookup"><span data-stu-id="7ecbf-171">Request Body - Subscribe to all events at group level</span></span>

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


<span data-ttu-id="7ecbf-172">Vous pouvez trouver le schéma de réponse webhook les événements inscrits dans Kaizala [**ici**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="7ecbf-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

### <a name="get-webhook"></a><span data-ttu-id="7ecbf-173">Obtenir /webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-173">Get /webhook</span></span>

    GET {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a><span data-ttu-id="7ecbf-174">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7ecbf-174">Request Parameters</span></span>


|  | <span data-ttu-id="7ecbf-175">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-175">Parameter</span></span> | <span data-ttu-id="7ecbf-176">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-176">Type</span></span> | <span data-ttu-id="7ecbf-177">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7ecbf-177">Optional?</span></span> | <span data-ttu-id="7ecbf-178">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-178">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-179">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7ecbf-179">HTTP Header</span></span> | <span data-ttu-id="7ecbf-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-180">accessToken</span></span> | <span data-ttu-id="7ecbf-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-181">String</span></span> | <span data-ttu-id="7ecbf-182">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-182">No</span></span> | <span data-ttu-id="7ecbf-183">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7ecbf-183">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7ecbf-184">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="7ecbf-184">Query parameter</span></span> | <span data-ttu-id="7ecbf-185">objectId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-185">objectId</span></span> | <span data-ttu-id="7ecbf-186">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-186">String</span></span> | <span data-ttu-id="7ecbf-187">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-187">No</span></span> | <span data-ttu-id="7ecbf-188">Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action</span><span class="sxs-lookup"><span data-stu-id="7ecbf-188">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="7ecbf-189">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="7ecbf-189">Query parameter</span></span> | <span data-ttu-id="7ecbf-190">objectType</span><span class="sxs-lookup"><span data-stu-id="7ecbf-190">objectType</span></span> | <span data-ttu-id="7ecbf-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-191">String</span></span> | <span data-ttu-id="7ecbf-192">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-192">No</span></span> | <span data-ttu-id="7ecbf-193">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="7ecbf-193">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

##### <a name="response-body"></a><span data-ttu-id="7ecbf-194">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="7ecbf-194">Response body</span></span>

| <span data-ttu-id="7ecbf-195">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-195">Parameter</span></span> | <span data-ttu-id="7ecbf-196">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-196">Type</span></span> | <span data-ttu-id="7ecbf-197">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-197">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-198">webhooks</span><span class="sxs-lookup"><span data-stu-id="7ecbf-198">webhooks</span></span> | <span data-ttu-id="7ecbf-199">Tableau d’objets JSON</span><span class="sxs-lookup"><span data-stu-id="7ecbf-199">JSON Object Array</span></span> | <span data-ttu-id="7ecbf-200">Tableau de webhooks souscrit sur objectId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-200">Array of webhooks subscribed on the objectId</span></span> |

######  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="7ecbf-201">Structure de JSON pour chaque webhook individuel dans le tableau webhooks [-] :</span><span class="sxs-lookup"><span data-stu-id="7ecbf-201">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="7ecbf-202">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-202">Parameter</span></span> | <span data-ttu-id="7ecbf-203">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-203">Type</span></span> | <span data-ttu-id="7ecbf-204">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-205">id</span><span class="sxs-lookup"><span data-stu-id="7ecbf-205">id</span></span> | <span data-ttu-id="7ecbf-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-206">String</span></span> | <span data-ttu-id="7ecbf-207">Identificateur Webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-207">Webhook Identifier</span></span> |
| <span data-ttu-id="7ecbf-208">objectId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-208">objectId</span></span> | <span data-ttu-id="7ecbf-209">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-209">String</span></span> | <span data-ttu-id="7ecbf-210">Identificateur d’objet</span><span class="sxs-lookup"><span data-stu-id="7ecbf-210">Object Identifier</span></span> |
| <span data-ttu-id="7ecbf-211">objectType</span><span class="sxs-lookup"><span data-stu-id="7ecbf-211">objectType</span></span> | <span data-ttu-id="7ecbf-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-212">String</span></span> | <span data-ttu-id="7ecbf-213">Enum : « groupe » / « Action » / « ActionPackage »</span><span class="sxs-lookup"><span data-stu-id="7ecbf-213">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="7ecbf-214">events</span><span class="sxs-lookup"><span data-stu-id="7ecbf-214">events</span></span> | <span data-ttu-id="7ecbf-215">String]</span><span class="sxs-lookup"><span data-stu-id="7ecbf-215">String[]</span></span> | <span data-ttu-id="7ecbf-216">Liste des événements avec chaque valeur comme « ActionCreated », « ActionResponse », « SurveyCreated », « JobCreated », « SurveyResponse », « JobResponse », « TextMessageCreated », « AttachmentCreated », « Announcement », « MemberAdded », « MemberRemoved », « GroupAdded » » GroupRemoved »</span><span class="sxs-lookup"><span data-stu-id="7ecbf-216">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="7ecbf-217">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="7ecbf-217">callBackUrl</span></span> | <span data-ttu-id="7ecbf-218">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-218">String</span></span> | <span data-ttu-id="7ecbf-219">URL de rappel à laquelle doivent être notifiés pour les événements auxquels vous êtes abonnés</span><span class="sxs-lookup"><span data-stu-id="7ecbf-219">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="7ecbf-220">callBackToken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-220">callBackToken</span></span> | <span data-ttu-id="7ecbf-221">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-221">String</span></span> | <span data-ttu-id="7ecbf-222">Paramètre qui sera envoyé dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-222">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="7ecbf-223">callBackContext</span><span class="sxs-lookup"><span data-stu-id="7ecbf-223">callBackContext</span></span> | <span data-ttu-id="7ecbf-224">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-224">String</span></span> | <span data-ttu-id="7ecbf-225">Paramètre envoyé dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-225">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="7ecbf-226">validité</span><span class="sxs-lookup"><span data-stu-id="7ecbf-226">validity</span></span> | <span data-ttu-id="7ecbf-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-227">String</span></span> | <span data-ttu-id="7ecbf-228">Validité pour le WebHook actif au format d’origine.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-228">Validity for the WebHook to be active in EPOCH format.</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="7ecbf-229">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="7ecbf-229">Sample JSON Response</span></span>

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
        }
    ]
}
```

### <a name="delete-webhook"></a><span data-ttu-id="7ecbf-230">Supprimer /webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-230">Delete /webhook</span></span>

    DELETE {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a><span data-ttu-id="7ecbf-231">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="7ecbf-231">Request Parameters</span></span>
|  | <span data-ttu-id="7ecbf-232">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7ecbf-232">Parameter</span></span> | <span data-ttu-id="7ecbf-233">Type</span><span class="sxs-lookup"><span data-stu-id="7ecbf-233">Type</span></span> | <span data-ttu-id="7ecbf-234">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="7ecbf-234">Optional?</span></span> | <span data-ttu-id="7ecbf-235">Description</span><span class="sxs-lookup"><span data-stu-id="7ecbf-235">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7ecbf-236">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7ecbf-236">HTTP Header</span></span> | <span data-ttu-id="7ecbf-237">accessToken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-237">accessToken</span></span> | <span data-ttu-id="7ecbf-238">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-238">String</span></span> | <span data-ttu-id="7ecbf-239">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-239">No</span></span> | <span data-ttu-id="7ecbf-240">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="7ecbf-240">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7ecbf-241">Paramètre de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="7ecbf-241">Path parameter</span></span> | <span data-ttu-id="7ecbf-242">webhookId</span><span class="sxs-lookup"><span data-stu-id="7ecbf-242">webhookId</span></span> | <span data-ttu-id="7ecbf-243">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7ecbf-243">String</span></span> | <span data-ttu-id="7ecbf-244">Non</span><span class="sxs-lookup"><span data-stu-id="7ecbf-244">No</span></span> | <span data-ttu-id="7ecbf-245">Identificateur Webhook</span><span class="sxs-lookup"><span data-stu-id="7ecbf-245">Webhook Identifier</span></span> |
