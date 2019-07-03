<span data-ttu-id="b2e77-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="b2e77-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span></span>

# <a name="class-kaserror"></a><span data-ttu-id="b2e77-102">Classe: KASError</span><span class="sxs-lookup"><span data-stu-id="b2e77-102">Class: KASError</span></span>

## <a name="hierarchy"></a><span data-ttu-id="b2e77-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b2e77-103">Hierarchy</span></span>

<span data-ttu-id="b2e77-104">**KASError**</span><span class="sxs-lookup"><span data-stu-id="b2e77-104">**KASError**</span></span>

## <a name="index"></a><span data-ttu-id="b2e77-105">Index</span><span class="sxs-lookup"><span data-stu-id="b2e77-105">Index</span></span>

### <a name="constructors"></a><span data-ttu-id="b2e77-106">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="b2e77-106">Constructors</span></span>

* [<span data-ttu-id="b2e77-107">constructeur</span><span class="sxs-lookup"><span data-stu-id="b2e77-107">constructor</span></span>](kasclient.kaserror.md#constructor)
### <a name="properties"></a><span data-ttu-id="b2e77-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2e77-108">Properties</span></span>

* [<span data-ttu-id="b2e77-109">description</span><span class="sxs-lookup"><span data-stu-id="b2e77-109">description</span></span>](kasclient.kaserror.md#description)
* [<span data-ttu-id="b2e77-110">errorCode</span><span class="sxs-lookup"><span data-stu-id="b2e77-110">errorCode</span></span>](kasclient.kaserror.md#errorcode)
### <a name="methods"></a><span data-ttu-id="b2e77-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b2e77-111">Methods</span></span>

* [<span data-ttu-id="b2e77-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="b2e77-112">toString</span></span>](kasclient.kaserror.md#tostring)
* [<span data-ttu-id="b2e77-113">fromErrorString</span><span class="sxs-lookup"><span data-stu-id="b2e77-113">fromErrorString</span></span>](kasclient.kaserror.md#fromerrorstring)
* [<span data-ttu-id="b2e77-114">fromString</span><span class="sxs-lookup"><span data-stu-id="b2e77-114">fromString</span></span>](kasclient.kaserror.md#fromstring)

---

## <a name="constructors"></a><span data-ttu-id="b2e77-115">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="b2e77-115">Constructors</span></span>

<a id="constructor"></a>

###  <a name="constructor"></a><span data-ttu-id="b2e77-116">constructeur</span><span class="sxs-lookup"><span data-stu-id="b2e77-116">constructor</span></span>

<span data-ttu-id="b2e77-117">⊕ **New KASError**(ErrorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, Description: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="b2e77-117">⊕ **new KASError**(errorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, description: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="b2e77-118">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="b2e77-118">**Parameters:**</span></span>

| <span data-ttu-id="b2e77-119">Nom</span><span class="sxs-lookup"><span data-stu-id="b2e77-119">Name</span></span> | <span data-ttu-id="b2e77-120">Type</span><span class="sxs-lookup"><span data-stu-id="b2e77-120">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="b2e77-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="b2e77-121">errorCode</span></span> | [<span data-ttu-id="b2e77-122">KASErrorCode</span><span class="sxs-lookup"><span data-stu-id="b2e77-122">KASErrorCode</span></span>](../enums/kasclient.kaserrorcode.md) |
| <span data-ttu-id="b2e77-123">description</span><span class="sxs-lookup"><span data-stu-id="b2e77-123">description</span></span> | `string` |

<span data-ttu-id="b2e77-124">**Renvoie:** [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="b2e77-124">**Returns:** [KASError](kasclient.kaserror.md)</span></span>

___

## <a name="properties"></a><span data-ttu-id="b2e77-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2e77-125">Properties</span></span>

<a id="description"></a>

###  <a name="description"></a><span data-ttu-id="b2e77-126">description</span><span class="sxs-lookup"><span data-stu-id="b2e77-126">description</span></span>

<span data-ttu-id="b2e77-127">**● Description**: *`String`* = ""</span><span class="sxs-lookup"><span data-stu-id="b2e77-127">**● description**: *`String`* = ""</span></span>

___
<a id="errorcode"></a>

###  <a name="errorcode"></a><span data-ttu-id="b2e77-128">errorCode</span><span class="sxs-lookup"><span data-stu-id="b2e77-128">errorCode</span></span>

<span data-ttu-id="b2e77-129">**● ErrorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode. None</span><span class="sxs-lookup"><span data-stu-id="b2e77-129">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* =  KASErrorCode.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="b2e77-130">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b2e77-130">Methods</span></span>

<a id="tostring"></a>

###  <a name="tostring"></a><span data-ttu-id="b2e77-131">Méthode</span><span class="sxs-lookup"><span data-stu-id="b2e77-131">toString</span></span>

<span data-ttu-id="b2e77-132">▸ **ToString**():`string`</span><span class="sxs-lookup"><span data-stu-id="b2e77-132">▸ **toString**(): `string`</span></span>

<span data-ttu-id="b2e77-133">**Renvoie:**`string`</span><span class="sxs-lookup"><span data-stu-id="b2e77-133">**Returns:** `string`</span></span>

___
<a id="fromerrorstring"></a>

### <a name="static-fromerrorstring"></a><span data-ttu-id="b2e77-134">`<Static>`fromErrorString</span><span class="sxs-lookup"><span data-stu-id="b2e77-134">`<Static>` fromErrorString</span></span>

<span data-ttu-id="b2e77-135">▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="b2e77-135">▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="b2e77-136">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="b2e77-136">**Parameters:**</span></span>

| <span data-ttu-id="b2e77-137">Nom</span><span class="sxs-lookup"><span data-stu-id="b2e77-137">Name</span></span> | <span data-ttu-id="b2e77-138">Type</span><span class="sxs-lookup"><span data-stu-id="b2e77-138">Type</span></span> | <span data-ttu-id="b2e77-139">Description</span><span class="sxs-lookup"><span data-stu-id="b2e77-139">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="b2e77-140">stringifyError</span><span class="sxs-lookup"><span data-stu-id="b2e77-140">stringifyError</span></span> | `string` |  <span data-ttu-id="b2e77-141">JSON dictionnaire d’erreurs avec code et description</span><span class="sxs-lookup"><span data-stu-id="b2e77-141">stringified dictionary of error with code and description</span></span> |

<span data-ttu-id="b2e77-142">**Renvoie:** [KASError](kasclient.kaserror.md) renvoie l’objet KASError créé à partir d’une erreur JSON.</span><span class="sxs-lookup"><span data-stu-id="b2e77-142">**Returns:** [KASError](kasclient.kaserror.md) returns KASError object made from stringified error.</span></span> <span data-ttu-id="b2e77-143">Pour la chaîne NULL, NULL est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b2e77-143">For null string, null object is returned.</span></span>

___
<a id="fromstring"></a>

### <a name="static-fromstring"></a><span data-ttu-id="b2e77-144">`<Static>`fromString</span><span class="sxs-lookup"><span data-stu-id="b2e77-144">`<Static>` fromString</span></span>

<span data-ttu-id="b2e77-145">▸ **FromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="b2e77-145">▸ **fromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="b2e77-146">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="b2e77-146">**Parameters:**</span></span>

| <span data-ttu-id="b2e77-147">Nom</span><span class="sxs-lookup"><span data-stu-id="b2e77-147">Name</span></span> | <span data-ttu-id="b2e77-148">Type</span><span class="sxs-lookup"><span data-stu-id="b2e77-148">Type</span></span> | <span data-ttu-id="b2e77-149">Description</span><span class="sxs-lookup"><span data-stu-id="b2e77-149">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="b2e77-150">stringifyError</span><span class="sxs-lookup"><span data-stu-id="b2e77-150">stringifyError</span></span> | `string` |  <span data-ttu-id="b2e77-151">JSON dictionnaire d’erreurs avec code et description</span><span class="sxs-lookup"><span data-stu-id="b2e77-151">stringified dictionary of error with code and description</span></span> |

<span data-ttu-id="b2e77-152">**Renvoie:** [KASError](kasclient.kaserror.md) renvoie l’objet KASError créé à partir d’une erreur JSON.</span><span class="sxs-lookup"><span data-stu-id="b2e77-152">**Returns:** [KASError](kasclient.kaserror.md) returns KASError object made from stringified error.</span></span> <span data-ttu-id="b2e77-153">Pour une chaîne de valeur null, le code d’erreur non null est également renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b2e77-153">For null string also, non-null error code is returned</span></span>

___

