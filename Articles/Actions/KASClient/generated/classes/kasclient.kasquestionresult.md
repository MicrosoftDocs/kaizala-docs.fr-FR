<span data-ttu-id="8ddca-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span></span>

# <a name="class-kasquestionresult"></a><span data-ttu-id="8ddca-102">Classe: KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="8ddca-102">Class: KASQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="8ddca-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8ddca-103">Hierarchy</span></span>

<span data-ttu-id="8ddca-104">**KASQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="8ddca-104">**KASQuestionResult**</span></span>

<span data-ttu-id="8ddca-105">↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-105">↳  [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span></span>

<span data-ttu-id="8ddca-106">↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-106">↳  [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="8ddca-107">↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-107">↳  [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

## <a name="index"></a><span data-ttu-id="8ddca-108">Index</span><span class="sxs-lookup"><span data-stu-id="8ddca-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="8ddca-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ddca-109">Properties</span></span>

* [<span data-ttu-id="8ddca-110">questionId</span><span class="sxs-lookup"><span data-stu-id="8ddca-110">questionId</span></span>](kasclient.kasquestionresult.md#questionid)
* [<span data-ttu-id="8ddca-111">questionTitle</span><span class="sxs-lookup"><span data-stu-id="8ddca-111">questionTitle</span></span>](kasclient.kasquestionresult.md#questiontitle)
* [<span data-ttu-id="8ddca-112">questionType</span><span class="sxs-lookup"><span data-stu-id="8ddca-112">questionType</span></span>](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="8ddca-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8ddca-113">Methods</span></span>

* [<span data-ttu-id="8ddca-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="8ddca-114">fromJSON</span></span>](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="8ddca-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ddca-115">Properties</span></span>

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="8ddca-116">questionId</span><span class="sxs-lookup"><span data-stu-id="8ddca-116">questionId</span></span>

<span data-ttu-id="8ddca-117">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="8ddca-117">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="8ddca-118">Index de la question</span><span class="sxs-lookup"><span data-stu-id="8ddca-118">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="8ddca-119">questionTitle</span><span class="sxs-lookup"><span data-stu-id="8ddca-119">questionTitle</span></span>

<span data-ttu-id="8ddca-120">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8ddca-120">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="8ddca-121">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="8ddca-121">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="8ddca-122">questionType</span><span class="sxs-lookup"><span data-stu-id="8ddca-122">questionType</span></span>

<span data-ttu-id="8ddca-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="8ddca-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="8ddca-124">Type de la question</span><span class="sxs-lookup"><span data-stu-id="8ddca-124">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="8ddca-125">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8ddca-125">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="8ddca-126">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="8ddca-126">`<Static>` fromJSON</span></span>

<span data-ttu-id="8ddca-127">▸ **fromJSON**(objet: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-127">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="8ddca-128">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="8ddca-128">**Parameters:**</span></span>

| <span data-ttu-id="8ddca-129">Nom</span><span class="sxs-lookup"><span data-stu-id="8ddca-129">Name</span></span> | <span data-ttu-id="8ddca-130">Type</span><span class="sxs-lookup"><span data-stu-id="8ddca-130">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="8ddca-131">objet</span><span class="sxs-lookup"><span data-stu-id="8ddca-131">object</span></span> | `any` |

<span data-ttu-id="8ddca-132">**Renvoie:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8ddca-132">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

