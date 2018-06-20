# <a name="breaking-changes-communication"></a><span data-ttu-id="77674-101">Annulation de communication des modifications</span><span class="sxs-lookup"><span data-stu-id="77674-101">Breaking Changes communication</span></span>

<span data-ttu-id="77674-102">S’abonner à [Se connecter pour les développeurs de Kaizala](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) à partir de votre application mobile pour recevoir les dernières modifications communication dans la plateforme de développement Kaizala.</span><span class="sxs-lookup"><span data-stu-id="77674-102">Subscribe to [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) from your mobile app to receive Breaking changes communication in Kaizala Developer Platform.</span></span>

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

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a><span data-ttu-id="77674-103">Des groupes publics gérés ne peuvent être créés à l’aide du jeton de l’utilisateur au niveau du client dans « créer un groupe' API</span><span class="sxs-lookup"><span data-stu-id="77674-103">Managed Public groups can only be created using Tenant-level user token in 'Create Group' API</span></span>

||<span data-ttu-id="77674-104">Détails</span><span class="sxs-lookup"><span data-stu-id="77674-104">Details</span></span>|
|--|--|
|<span data-ttu-id="77674-105">**Zone d’impact**</span><span class="sxs-lookup"><span data-stu-id="77674-105">**Impact Area**</span></span>| <span data-ttu-id="77674-106">API</span><span class="sxs-lookup"><span data-stu-id="77674-106">APIs</span></span> |
|<span data-ttu-id="77674-107">**Résumé de l’impact**</span><span class="sxs-lookup"><span data-stu-id="77674-107">**Impact Summary**</span></span>| <span data-ttu-id="77674-108">Groupe Public antérieur a été autorisée à être créée sans qu’il est mappée à une organisation.</span><span class="sxs-lookup"><span data-stu-id="77674-108">Earlier Public group was allowed to be created without it being mapped to an Organization.</span></span> <span data-ttu-id="77674-109">Désormais, groupes publics gérés peuvent être créés par le biais de «[créer le groupe](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)», uniquement lorsque le jeton de l’utilisateur au niveau du client est utilisé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="77674-109">Henceforth, Managed Public Groups can be created through '[Create group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', only when tenant-level user token is used in API.</span></span> <span data-ttu-id="77674-110">Lecture [ici](connectors/UserToken.md) plus pour le processus à générer le jeton de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="77674-110">Read [here](connectors/UserToken.md) more for the process to generate user token</span></span> |
|<span data-ttu-id="77674-111">**Date de Communication**</span><span class="sxs-lookup"><span data-stu-id="77674-111">**Date of Communication**</span></span>|<span data-ttu-id="77674-112">06-06-2018</span><span class="sxs-lookup"><span data-stu-id="77674-112">06-06-2018</span></span>|
|<span data-ttu-id="77674-113">**Date de l’Impact**</span><span class="sxs-lookup"><span data-stu-id="77674-113">**Date of Impact**</span></span>|<span data-ttu-id="77674-114">22-06-2018</span><span class="sxs-lookup"><span data-stu-id="77674-114">22-06-2018</span></span>|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a><span data-ttu-id="77674-115">Validation de callBackUrl inscrit lorsque webhook est créé.</span><span class="sxs-lookup"><span data-stu-id="77674-115">Validation of registered callBackUrl when webhook is created</span></span>

||<span data-ttu-id="77674-116">Détails</span><span class="sxs-lookup"><span data-stu-id="77674-116">Details</span></span>|
|--|--|
|<span data-ttu-id="77674-117">**Zone d’impact**</span><span class="sxs-lookup"><span data-stu-id="77674-117">**Impact Area**</span></span>| <span data-ttu-id="77674-118">Webhooks</span><span class="sxs-lookup"><span data-stu-id="77674-118">Webhooks</span></span> |
|<span data-ttu-id="77674-119">**Résumé de l’impact**</span><span class="sxs-lookup"><span data-stu-id="77674-119">**Impact Summary**</span></span>| <span data-ttu-id="77674-120">Si vous continuez, lors de la création de Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), callBackUrl enregistré est validé.</span><span class="sxs-lookup"><span data-stu-id="77674-120">Going ahead, during creation of Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), registered callBackUrl would be validated.</span></span> <span data-ttu-id="77674-121">Après une validation réussie, un webhook serait créée</span><span class="sxs-lookup"><span data-stu-id="77674-121">After successful validation, a webhook would be created</span></span> |
|<span data-ttu-id="77674-122">**Action requise**</span><span class="sxs-lookup"><span data-stu-id="77674-122">**Required Action**</span></span>| <span data-ttu-id="77674-123">Ancienne Webhook abonnements continueront de fonctionner au-delà de la Date de l’Impact.</span><span class="sxs-lookup"><span data-stu-id="77674-123">Older Webhook subscriptions will continue to work beyond the Date of Impact.</span></span> <span data-ttu-id="77674-124">Nouvelles demandes d’abonnement Webhook nécessite que vous vérifiez votre service suit le processus mentionné [ici](connectors/WebHookValidaton.md)</span><span class="sxs-lookup"><span data-stu-id="77674-124">New Webhook subscription requests would require you to ensure your service follows the process mentioned [here](connectors/WebHookValidaton.md)</span></span> |
|<span data-ttu-id="77674-125">**Date de Communication**</span><span class="sxs-lookup"><span data-stu-id="77674-125">**Date of Communication**</span></span>|<span data-ttu-id="77674-126">09-05-2018</span><span class="sxs-lookup"><span data-stu-id="77674-126">09-05-2018</span></span>|
|<span data-ttu-id="77674-127">**Date de l’Impact**</span><span class="sxs-lookup"><span data-stu-id="77674-127">**Date of Impact**</span></span>|<span data-ttu-id="77674-128">15-06-2018</span><span class="sxs-lookup"><span data-stu-id="77674-128">15-06-2018</span></span>|

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


