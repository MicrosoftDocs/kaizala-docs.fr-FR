<span data-ttu-id="85f2b-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="85f2b-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span></span>

# <a name="class-kasoptionresult"></a><span data-ttu-id="85f2b-102">Classe: KASOptionResult</span><span class="sxs-lookup"><span data-stu-id="85f2b-102">Class: KASOptionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="85f2b-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="85f2b-103">Hierarchy</span></span>

<span data-ttu-id="85f2b-104">**KASOptionResult**</span><span class="sxs-lookup"><span data-stu-id="85f2b-104">**KASOptionResult**</span></span>

## <a name="index"></a><span data-ttu-id="85f2b-105">Index</span><span class="sxs-lookup"><span data-stu-id="85f2b-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="85f2b-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85f2b-106">Properties</span></span>

* [<span data-ttu-id="85f2b-107">optionId</span><span class="sxs-lookup"><span data-stu-id="85f2b-107">optionId</span></span>](kasclient.kasoptionresult.md#optionid)
* [<span data-ttu-id="85f2b-108">optionTitle</span><span class="sxs-lookup"><span data-stu-id="85f2b-108">optionTitle</span></span>](kasclient.kasoptionresult.md#optiontitle)
* [<span data-ttu-id="85f2b-109">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="85f2b-109">responderToResponseCount</span></span>](kasclient.kasoptionresult.md#respondertoresponsecount)
* [<span data-ttu-id="85f2b-110">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="85f2b-110">totalResponsesCount</span></span>](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a><span data-ttu-id="85f2b-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="85f2b-111">Methods</span></span>

* [<span data-ttu-id="85f2b-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="85f2b-112">fromJSON</span></span>](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="85f2b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85f2b-113">Properties</span></span>

<a id="optionid"></a>

###  <a name="optionid"></a><span data-ttu-id="85f2b-114">optionId</span><span class="sxs-lookup"><span data-stu-id="85f2b-114">optionId</span></span>

<span data-ttu-id="85f2b-115">**● optionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="85f2b-115">**● optionId**: *`number`* = 0</span></span>

<span data-ttu-id="85f2b-116">Index de l'option</span><span class="sxs-lookup"><span data-stu-id="85f2b-116">Index of the option</span></span>

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a><span data-ttu-id="85f2b-117">optionTitle</span><span class="sxs-lookup"><span data-stu-id="85f2b-117">optionTitle</span></span>

<span data-ttu-id="85f2b-118">**● optionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="85f2b-118">**● optionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="85f2b-119">Titre de l'option</span><span class="sxs-lookup"><span data-stu-id="85f2b-119">Title of the option</span></span>

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a><span data-ttu-id="85f2b-120">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="85f2b-120">responderToResponseCount</span></span>

<span data-ttu-id="85f2b-121">**● responderToResponseCount**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="85f2b-121">**● responderToResponseCount**: *`object`*</span></span>

<span data-ttu-id="85f2b-122">Une carte des ID d'utilisateur par rapport à leur nombre de réponses Dictionary<UserId: String, ResponseCount: number></span><span class="sxs-lookup"><span data-stu-id="85f2b-122">A map of user ids against their response count Dictionary<UserId: string, ResponseCount: number></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="85f2b-123">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="85f2b-123">Type declaration</span></span>

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a><span data-ttu-id="85f2b-124">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="85f2b-124">totalResponsesCount</span></span>

<span data-ttu-id="85f2b-125">**● totalResponsesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="85f2b-125">**● totalResponsesCount**: *`number`* = 0</span></span>

<span data-ttu-id="85f2b-126">Combien d'entre elles ont choisi cette option?</span><span class="sxs-lookup"><span data-stu-id="85f2b-126">How many have chosen this option</span></span>

___

## <a name="methods"></a><span data-ttu-id="85f2b-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="85f2b-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="85f2b-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="85f2b-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="85f2b-129">▸ **fromJSON**(objet: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="85f2b-129">▸ **fromJSON**(object: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

<span data-ttu-id="85f2b-130">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="85f2b-130">**Parameters:**</span></span>

| <span data-ttu-id="85f2b-131">Nom</span><span class="sxs-lookup"><span data-stu-id="85f2b-131">Name</span></span> | <span data-ttu-id="85f2b-132">Type</span><span class="sxs-lookup"><span data-stu-id="85f2b-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="85f2b-133">objet</span><span class="sxs-lookup"><span data-stu-id="85f2b-133">object</span></span> | `any` |

<span data-ttu-id="85f2b-134">**Renvoie:** [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="85f2b-134">**Returns:** [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

___

