<span data-ttu-id="fbce1-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fbce1-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span></span>

# <a name="class-kasformprocessedsummary"></a><span data-ttu-id="fbce1-102">Classe: KASFormProcessedSummary</span><span class="sxs-lookup"><span data-stu-id="fbce1-102">Class: KASFormProcessedSummary</span></span>

## <a name="hierarchy"></a><span data-ttu-id="fbce1-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fbce1-103">Hierarchy</span></span>

<span data-ttu-id="fbce1-104">**KASFormProcessedSummary**</span><span class="sxs-lookup"><span data-stu-id="fbce1-104">**KASFormProcessedSummary**</span></span>

## <a name="index"></a><span data-ttu-id="fbce1-105">Index</span><span class="sxs-lookup"><span data-stu-id="fbce1-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="fbce1-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fbce1-106">Properties</span></span>

* [<span data-ttu-id="fbce1-107">JSON</span><span class="sxs-lookup"><span data-stu-id="fbce1-107">json</span></span>](kasclient.kasformprocessedsummary.md#json)
* [<span data-ttu-id="fbce1-108">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="fbce1-108">nonRespondersInConversation</span></span>](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [<span data-ttu-id="fbce1-109">résultats</span><span class="sxs-lookup"><span data-stu-id="fbce1-109">results</span></span>](kasclient.kasformprocessedsummary.md#results)
* [<span data-ttu-id="fbce1-110">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="fbce1-110">targetResponderCount</span></span>](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [<span data-ttu-id="fbce1-111">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="fbce1-111">totalResponseCount</span></span>](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a><span data-ttu-id="fbce1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbce1-112">Methods</span></span>

* [<span data-ttu-id="fbce1-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="fbce1-113">fromJSON</span></span>](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="fbce1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fbce1-114">Properties</span></span>

<a id="json"></a>

###  <a name="json"></a><span data-ttu-id="fbce1-115">json</span><span class="sxs-lookup"><span data-stu-id="fbce1-115">json</span></span>

<span data-ttu-id="fbce1-116">**● JSON**:*`JSON`*</span><span class="sxs-lookup"><span data-stu-id="fbce1-116">**● json**: *`JSON`*</span></span>

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a><span data-ttu-id="fbce1-117">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="fbce1-117">nonRespondersInConversation</span></span>

<span data-ttu-id="fbce1-118">**● nonRespondersInConversation**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="fbce1-118">**● nonRespondersInConversation**: *`string`[]* =  []</span></span>

<span data-ttu-id="fbce1-119">Nombre de réponses dans la conversation</span><span class="sxs-lookup"><span data-stu-id="fbce1-119">How many in the conversation did not respond</span></span>

___

<a id="results"></a>

###  <a name="results"></a><span data-ttu-id="fbce1-120">results</span><span class="sxs-lookup"><span data-stu-id="fbce1-120">results</span></span>

<span data-ttu-id="fbce1-121">**● résultats**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="fbce1-121">**● results**: *`object`*</span></span>

<span data-ttu-id="fbce1-122">Résultat agrégé pour les questions agrégées Dictionary<QuestionId: Number, result: KASQuestionResult></span><span class="sxs-lookup"><span data-stu-id="fbce1-122">Aggregated result for aggregative questions Dictionary<QuestionId: number, Result: KASQuestionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="fbce1-123">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="fbce1-123">Type declaration</span></span>

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a><span data-ttu-id="fbce1-124">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="fbce1-124">targetResponderCount</span></span>

<span data-ttu-id="fbce1-125">**● targetResponderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="fbce1-125">**● targetResponderCount**: *`number`* = 0</span></span>

<span data-ttu-id="fbce1-126">Combien de fois dans la conversation ont été affectées pour répondre à ce formulaire</span><span class="sxs-lookup"><span data-stu-id="fbce1-126">How many in the conversation were assigned to respond to this form</span></span>

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a><span data-ttu-id="fbce1-127">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="fbce1-127">totalResponseCount</span></span>

<span data-ttu-id="fbce1-128">**● totalResponseCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="fbce1-128">**● totalResponseCount**: *`number`* = 0</span></span>

<span data-ttu-id="fbce1-129">Le nombre total de réponses reçues pour le formulaire, en considérant plusieurs réponses d'une personne</span><span class="sxs-lookup"><span data-stu-id="fbce1-129">How many total responses were received for the form, considering multiple responses from one person</span></span>

___

## <a name="methods"></a><span data-ttu-id="fbce1-130">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbce1-130">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="fbce1-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="fbce1-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="fbce1-132">▸ **fromJSON**(objet: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fbce1-132">▸ **fromJSON**(object: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

<span data-ttu-id="fbce1-133">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="fbce1-133">**Parameters:**</span></span>

| <span data-ttu-id="fbce1-134">Nom</span><span class="sxs-lookup"><span data-stu-id="fbce1-134">Name</span></span> | <span data-ttu-id="fbce1-135">Type</span><span class="sxs-lookup"><span data-stu-id="fbce1-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="fbce1-136">objet</span><span class="sxs-lookup"><span data-stu-id="fbce1-136">object</span></span> | `JSON` |

<span data-ttu-id="fbce1-137">**Renvoie:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fbce1-137">**Returns:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

___

