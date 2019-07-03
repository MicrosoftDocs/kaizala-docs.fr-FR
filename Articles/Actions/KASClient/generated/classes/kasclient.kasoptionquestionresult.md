<span data-ttu-id="5a7e5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span></span>

# <a name="class-kasoptionquestionresult"></a><span data-ttu-id="5a7e5-102">Classe: KASOptionQuestionResult</span><span class="sxs-lookup"><span data-stu-id="5a7e5-102">Class: KASOptionQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="5a7e5-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="5a7e5-103">Hierarchy</span></span>

 [<span data-ttu-id="5a7e5-104">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="5a7e5-104">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="5a7e5-105">**↳ KASOptionQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="5a7e5-105">**↳ KASOptionQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="5a7e5-106">Index</span><span class="sxs-lookup"><span data-stu-id="5a7e5-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="5a7e5-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a7e5-107">Properties</span></span>

* [<span data-ttu-id="5a7e5-108">optionResults</span><span class="sxs-lookup"><span data-stu-id="5a7e5-108">optionResults</span></span>](kasclient.kasoptionquestionresult.md#optionresults)
* [<span data-ttu-id="5a7e5-109">questionId</span><span class="sxs-lookup"><span data-stu-id="5a7e5-109">questionId</span></span>](kasclient.kasoptionquestionresult.md#questionid)
* [<span data-ttu-id="5a7e5-110">questionTitle</span><span class="sxs-lookup"><span data-stu-id="5a7e5-110">questionTitle</span></span>](kasclient.kasoptionquestionresult.md#questiontitle)
* [<span data-ttu-id="5a7e5-111">questionType</span><span class="sxs-lookup"><span data-stu-id="5a7e5-111">questionType</span></span>](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="5a7e5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a7e5-112">Methods</span></span>

* [<span data-ttu-id="5a7e5-113">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="5a7e5-113">getResultsOrder</span></span>](kasclient.kasoptionquestionresult.md#getresultsorder)
* [<span data-ttu-id="5a7e5-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="5a7e5-114">fromJSON</span></span>](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="5a7e5-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a7e5-115">Properties</span></span>

<a id="optionresults"></a>

###  <a name="optionresults"></a><span data-ttu-id="5a7e5-116">optionResults</span><span class="sxs-lookup"><span data-stu-id="5a7e5-116">optionResults</span></span>

<span data-ttu-id="5a7e5-117">**● optionResults**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="5a7e5-117">**● optionResults**: *`object`*</span></span>

<span data-ttu-id="5a7e5-118">Pour SingleSelect/MultiSelect, le résultat sera l’ID d’option et son dictionnaire de nombre<OptionId: nombre, OptionResult: KASOptionResult></span><span class="sxs-lookup"><span data-stu-id="5a7e5-118">For SingleSelect/MultiSelect question, the result will be option id versus their counts Dictionary<OptionId: number, OptionResult: KASOptionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="5a7e5-119">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="5a7e5-119">Type declaration</span></span>

___
<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="5a7e5-120">questionId</span><span class="sxs-lookup"><span data-stu-id="5a7e5-120">questionId</span></span>

<span data-ttu-id="5a7e5-121">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="5a7e5-121">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="5a7e5-122">Index de la question</span><span class="sxs-lookup"><span data-stu-id="5a7e5-122">Index of the question</span></span>

___
<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="5a7e5-123">questionTitle</span><span class="sxs-lookup"><span data-stu-id="5a7e5-123">questionTitle</span></span>

<span data-ttu-id="5a7e5-124">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="5a7e5-124">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="5a7e5-125">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="5a7e5-125">Title of the question</span></span>

___
<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="5a7e5-126">questionType</span><span class="sxs-lookup"><span data-stu-id="5a7e5-126">questionType</span></span>

<span data-ttu-id="5a7e5-127">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="5a7e5-127">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="5a7e5-128">Type de la question</span><span class="sxs-lookup"><span data-stu-id="5a7e5-128">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="5a7e5-129">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a7e5-129">Methods</span></span>

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a><span data-ttu-id="5a7e5-130">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="5a7e5-130">getResultsOrder</span></span>

<span data-ttu-id="5a7e5-131">▸ **getResultsOrder**(): `number`[]</span><span class="sxs-lookup"><span data-stu-id="5a7e5-131">▸ **getResultsOrder**(): `number`[]</span></span>

<span data-ttu-id="5a7e5-132">Obtient tous les ID d’option triés dans le nombre total de réponses (décroissant).</span><span class="sxs-lookup"><span data-stu-id="5a7e5-132">Gets all the option ids sorted in their total responses count (descending)</span></span>

<span data-ttu-id="5a7e5-133">**Renvoie:** `number`[] liste de tous les ID d’option</span><span class="sxs-lookup"><span data-stu-id="5a7e5-133">**Returns:** `number`[] list of all the option ids</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="5a7e5-134">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="5a7e5-134">`<Static>` fromJSON</span></span>

<span data-ttu-id="5a7e5-135">▸ **fromJSON**(objet: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-135">▸ **fromJSON**(object: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

<span data-ttu-id="5a7e5-136">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="5a7e5-136">**Parameters:**</span></span>

| <span data-ttu-id="5a7e5-137">Nom</span><span class="sxs-lookup"><span data-stu-id="5a7e5-137">Name</span></span> | <span data-ttu-id="5a7e5-138">Type</span><span class="sxs-lookup"><span data-stu-id="5a7e5-138">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="5a7e5-139">objet</span><span class="sxs-lookup"><span data-stu-id="5a7e5-139">object</span></span> | `any` |

<span data-ttu-id="5a7e5-140">**Renvoie:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-140">**Returns:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

___

