# <a name="breaking-changes-communication"></a><span data-ttu-id="7c632-101">Communication avec interruption des modifications</span><span class="sxs-lookup"><span data-stu-id="7c632-101">Breaking Changes communication</span></span>

<span data-ttu-id="7c632-102">S'abonner au [développeur Kaizala Connectez-vous](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) à partir de votre application mobile pour recevoir la communication avec des modifications critiques dans la plateforme de développement Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7c632-102">Subscribe to [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) from your mobile app to receive Breaking changes communication in Kaizala Developer Platform.</span></span>

<!---

## Deprecating Mobile Number data from Kaizala APIs & Webhooks
||Details|
|--|--|
|**Impact Area**| APIs & Webhooks |
|**Impact Summary**|Kaizala APIs & Webhooks will stop returning Mobile Number as part of reponse. It will return Kaizala userIDs, which can be used to identify unique users. List of APIs & Webhook impacted:<br> <ol><li></li>|
|**Requires Action**|3rd party developers should make necessary changes to avoid break in their solutions. During the time period between 'Date of communication' & 'Date of Impact', Kaizala APIs will return both Mobile numbers and User IDs|
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 15-05-2018|

-->

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a><span data-ttu-id="7c632-103">Les groupes publics gérés peuvent uniquement être créés à l'aide du jeton d'utilisateur au niveau du client dans l'API «créer un groupe»</span><span class="sxs-lookup"><span data-stu-id="7c632-103">Managed Public groups can only be created using Tenant-level user token in 'Create Group' API</span></span>

||<span data-ttu-id="7c632-104">Détails</span><span class="sxs-lookup"><span data-stu-id="7c632-104">Details</span></span>|
|--|--|
|<span data-ttu-id="7c632-105">**Zone d'impact**</span><span class="sxs-lookup"><span data-stu-id="7c632-105">**Impact Area**</span></span>| <span data-ttu-id="7c632-106">API</span><span class="sxs-lookup"><span data-stu-id="7c632-106">APIs</span></span> |
|<span data-ttu-id="7c632-107">**Synthèse des impacts**</span><span class="sxs-lookup"><span data-stu-id="7c632-107">**Impact Summary**</span></span>| <span data-ttu-id="7c632-108">Un groupe public antérieur a été autorisé à être créé sans être mappé à une organisation.</span><span class="sxs-lookup"><span data-stu-id="7c632-108">Earlier Public group was allowed to be created without it being mapped to an Organization.</span></span> <span data-ttu-id="7c632-109">Désormais, les groupes publics gérés peuvent être créés via «[créer un groupe](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)», uniquement lorsque le jeton de l'utilisateur au niveau du client est utilisé dans l'API.</span><span class="sxs-lookup"><span data-stu-id="7c632-109">Henceforth, Managed Public Groups can be created through '[Create group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', only when tenant-level user token is used in API.</span></span> <span data-ttu-id="7c632-110">En [](connectors/UserToken.md) savoir plus pour le processus de génération du jeton d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="7c632-110">Read [here](connectors/UserToken.md) more for the process to generate user token</span></span> |
|<span data-ttu-id="7c632-111">**Date de communication**</span><span class="sxs-lookup"><span data-stu-id="7c632-111">**Date of Communication**</span></span>|<span data-ttu-id="7c632-112">06-06-2018</span><span class="sxs-lookup"><span data-stu-id="7c632-112">06-06-2018</span></span>|
|<span data-ttu-id="7c632-113">**Date de l'impact**</span><span class="sxs-lookup"><span data-stu-id="7c632-113">**Date of Impact**</span></span>|<span data-ttu-id="7c632-114">22-06-2018</span><span class="sxs-lookup"><span data-stu-id="7c632-114">22-06-2018</span></span>|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a><span data-ttu-id="7c632-115">Validation des callBackUrl enregistrées lors de la création du webhook</span><span class="sxs-lookup"><span data-stu-id="7c632-115">Validation of registered callBackUrl when webhook is created</span></span>

||<span data-ttu-id="7c632-116">Détails</span><span class="sxs-lookup"><span data-stu-id="7c632-116">Details</span></span>|
|--|--|
|<span data-ttu-id="7c632-117">**Zone d'impact**</span><span class="sxs-lookup"><span data-stu-id="7c632-117">**Impact Area**</span></span>| <span data-ttu-id="7c632-118">Webhooks</span><span class="sxs-lookup"><span data-stu-id="7c632-118">Webhooks</span></span> |
|<span data-ttu-id="7c632-119">**Synthèse des impacts**</span><span class="sxs-lookup"><span data-stu-id="7c632-119">**Impact Summary**</span></span>| <span data-ttu-id="7c632-120">À l'avance, lors de la création du webhook ([post/webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), les callBackUrl inscrits seront validés.</span><span class="sxs-lookup"><span data-stu-id="7c632-120">Going ahead, during creation of Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), registered callBackUrl would be validated.</span></span> <span data-ttu-id="7c632-121">Une fois la validation réussie, un webhook est créé.</span><span class="sxs-lookup"><span data-stu-id="7c632-121">After successful validation, a webhook would be created</span></span> |
|<span data-ttu-id="7c632-122">**Action requise**</span><span class="sxs-lookup"><span data-stu-id="7c632-122">**Required Action**</span></span>| <span data-ttu-id="7c632-123">Les abonnements de webhook plus anciens continueront de fonctionner au-delà de la date d'impact.</span><span class="sxs-lookup"><span data-stu-id="7c632-123">Older Webhook subscriptions will continue to work beyond the Date of Impact.</span></span> <span data-ttu-id="7c632-124">Les nouvelles demandes d'abonnement webhook vous obligent à vous assurer que votre service suit le processus mentionné [ici](connectors/WebHookValidaton.md) .</span><span class="sxs-lookup"><span data-stu-id="7c632-124">New Webhook subscription requests would require you to ensure your service follows the process mentioned [here](connectors/WebHookValidaton.md)</span></span> |
|<span data-ttu-id="7c632-125">**Date de communication**</span><span class="sxs-lookup"><span data-stu-id="7c632-125">**Date of Communication**</span></span>|<span data-ttu-id="7c632-126">09-05-2018</span><span class="sxs-lookup"><span data-stu-id="7c632-126">09-05-2018</span></span>|
|<span data-ttu-id="7c632-127">**Date de l'impact**</span><span class="sxs-lookup"><span data-stu-id="7c632-127">**Date of Impact**</span></span>|<span data-ttu-id="7c632-128">15-06-2018</span><span class="sxs-lookup"><span data-stu-id="7c632-128">15-06-2018</span></span>|

<!---

## Webhook subscription will be cancelled, if 10 consecutive failures are received

||Details|
|--|--|
|**Impact Area**| Webhooks |
|**Impact Summary**| Subscription of WebHooks would be suspended, if Kaizala server doesn't receive success for 10 consecutive attempts. Developer will get communication regarding the same on Kaizala Developer Connect. Click here to join [Kaizala Developer Connect]()|
|**Required Action**||
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 01-06-2018 |
-->


