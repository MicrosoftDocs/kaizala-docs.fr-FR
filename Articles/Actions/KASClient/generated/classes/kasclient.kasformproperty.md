<span data-ttu-id="91caa-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="91caa-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)</span></span>

# <a name="class-kasformproperty"></a><span data-ttu-id="91caa-102">Classe: KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="91caa-102">Class: KASFormProperty</span></span>

## <a name="hierarchy"></a><span data-ttu-id="91caa-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="91caa-103">Hierarchy</span></span>

<span data-ttu-id="91caa-104">**KASFormProperty**</span><span class="sxs-lookup"><span data-stu-id="91caa-104">**KASFormProperty**</span></span>

## <a name="index"></a><span data-ttu-id="91caa-105">Index</span><span class="sxs-lookup"><span data-stu-id="91caa-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="91caa-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91caa-106">Properties</span></span>

* [<span data-ttu-id="91caa-107">name</span><span class="sxs-lookup"><span data-stu-id="91caa-107">name</span></span>](kasclient.kasformproperty.md#name)
* [<span data-ttu-id="91caa-108">type</span><span class="sxs-lookup"><span data-stu-id="91caa-108">type</span></span>](kasclient.kasformproperty.md#type)
* [<span data-ttu-id="91caa-109">value</span><span class="sxs-lookup"><span data-stu-id="91caa-109">value</span></span>](kasclient.kasformproperty.md#value)
### <a name="methods"></a><span data-ttu-id="91caa-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="91caa-110">Methods</span></span>

* [<span data-ttu-id="91caa-111">getAPICompatiblePropertyType</span><span class="sxs-lookup"><span data-stu-id="91caa-111">getAPICompatiblePropertyType</span></span>](kasclient.kasformproperty.md#getapicompatiblepropertytype)
* [<span data-ttu-id="91caa-112">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-112">toAPICompatibleJSON</span></span>](kasclient.kasformproperty.md#toapicompatiblejson)
* [<span data-ttu-id="91caa-113">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-113">toClientJSON</span></span>](kasclient.kasformproperty.md#toclientjson)
* [<span data-ttu-id="91caa-114">toJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-114">toJSON</span></span>](kasclient.kasformproperty.md#tojson)
* [<span data-ttu-id="91caa-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-115">fromJSON</span></span>](kasclient.kasformproperty.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="91caa-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91caa-116">Properties</span></span>

<a id="name"></a>

###  <a name="name"></a><span data-ttu-id="91caa-117">name</span><span class="sxs-lookup"><span data-stu-id="91caa-117">name</span></span>

<span data-ttu-id="91caa-118">**● nom**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="91caa-118">**● name**: *`string`* = ""</span></span>

<span data-ttu-id="91caa-119">Nom des métadonnées</span><span class="sxs-lookup"><span data-stu-id="91caa-119">Name of the metadata</span></span>

___
<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="91caa-120">type</span><span class="sxs-lookup"><span data-stu-id="91caa-120">type</span></span>

<span data-ttu-id="91caa-121">**● type**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* = KASFormPropertyType. Text</span><span class="sxs-lookup"><span data-stu-id="91caa-121">**● type**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* =  KASFormPropertyType.Text</span></span>

<span data-ttu-id="91caa-122">Type de métadonnées</span><span class="sxs-lookup"><span data-stu-id="91caa-122">Type of the metadata</span></span>

___
<a id="value"></a>

###  <a name="value"></a><span data-ttu-id="91caa-123">value</span><span class="sxs-lookup"><span data-stu-id="91caa-123">value</span></span>

<span data-ttu-id="91caa-124">**● valeur**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="91caa-124">**● value**: *`string`* = ""</span></span>

<span data-ttu-id="91caa-125">Valeur des métadonnées</span><span class="sxs-lookup"><span data-stu-id="91caa-125">Value of the metadata</span></span>

___

## <a name="methods"></a><span data-ttu-id="91caa-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="91caa-126">Methods</span></span>

<a id="getapicompatiblepropertytype"></a>

###  <a name="getapicompatiblepropertytype"></a><span data-ttu-id="91caa-127">getAPICompatiblePropertyType</span><span class="sxs-lookup"><span data-stu-id="91caa-127">getAPICompatiblePropertyType</span></span>

<span data-ttu-id="91caa-128">▸ **getAPICompatiblePropertyType**(type: *`string`*):`string`</span><span class="sxs-lookup"><span data-stu-id="91caa-128">▸ **getAPICompatiblePropertyType**(type: *`string`*): `string`</span></span>

<span data-ttu-id="91caa-129">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="91caa-129">**Parameters:**</span></span>

| <span data-ttu-id="91caa-130">Nom</span><span class="sxs-lookup"><span data-stu-id="91caa-130">Name</span></span> | <span data-ttu-id="91caa-131">Type</span><span class="sxs-lookup"><span data-stu-id="91caa-131">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="91caa-132">type</span><span class="sxs-lookup"><span data-stu-id="91caa-132">type</span></span> | `string` |

<span data-ttu-id="91caa-133">**Renvoie:**`string`</span><span class="sxs-lookup"><span data-stu-id="91caa-133">**Returns:** `string`</span></span>

___
<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a><span data-ttu-id="91caa-134">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-134">toAPICompatibleJSON</span></span>

<span data-ttu-id="91caa-135">▸ **toAPICompatibleJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-135">▸ **toAPICompatibleJSON**(): `JSON`</span></span>

<span data-ttu-id="91caa-136">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-136">**Returns:** `JSON`</span></span>

___
<a id="toclientjson"></a>

###  <a name="toclientjson"></a><span data-ttu-id="91caa-137">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-137">toClientJSON</span></span>

<span data-ttu-id="91caa-138">▸ **toClientJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-138">▸ **toClientJSON**(): `JSON`</span></span>

<span data-ttu-id="91caa-139">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-139">**Returns:** `JSON`</span></span>

___
<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="91caa-140">toJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-140">toJSON</span></span>

<span data-ttu-id="91caa-141">▸ **toJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-141">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="91caa-142">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="91caa-142">**Returns:** `JSON`</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="91caa-143">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="91caa-143">`<Static>` fromJSON</span></span>

<span data-ttu-id="91caa-144">▸ **fromJSON**(objet: *`JSON`*): [KASFormProperty](kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="91caa-144">▸ **fromJSON**(object: *`JSON`*): [KASFormProperty](kasclient.kasformproperty.md)</span></span>

<span data-ttu-id="91caa-145">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="91caa-145">**Parameters:**</span></span>

| <span data-ttu-id="91caa-146">Nom</span><span class="sxs-lookup"><span data-stu-id="91caa-146">Name</span></span> | <span data-ttu-id="91caa-147">Type</span><span class="sxs-lookup"><span data-stu-id="91caa-147">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="91caa-148">objet</span><span class="sxs-lookup"><span data-stu-id="91caa-148">object</span></span> | `JSON` |

<span data-ttu-id="91caa-149">**Renvoie:** [KASFormProperty](kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="91caa-149">**Returns:** [KASFormProperty](kasclient.kasformproperty.md)</span></span>

___

