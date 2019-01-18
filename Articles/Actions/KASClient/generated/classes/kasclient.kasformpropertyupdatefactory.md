---
ms.openlocfilehash: 01bf00e0a8aeca6f09a8243b297470606736d7ab
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727964"
---
<span data-ttu-id="00e41-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormPropertyUpdateFactory](../classes/kasclient.kasformpropertyupdatefactory.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormPropertyUpdateFactory](../classes/kasclient.kasformpropertyupdatefactory.md)</span></span>

# <a name="class-kasformpropertyupdatefactory"></a><span data-ttu-id="00e41-102">Classe : KASFormPropertyUpdateFactory</span><span class="sxs-lookup"><span data-stu-id="00e41-102">Class: KASFormPropertyUpdateFactory</span></span>

## <a name="hierarchy"></a><span data-ttu-id="00e41-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="00e41-103">Hierarchy</span></span>

<span data-ttu-id="00e41-104">**KASFormPropertyUpdateFactory**</span><span class="sxs-lookup"><span data-stu-id="00e41-104">**KASFormPropertyUpdateFactory**</span></span>

## <a name="index"></a><span data-ttu-id="00e41-105">Index</span><span class="sxs-lookup"><span data-stu-id="00e41-105">Index</span></span>

### <a name="methods"></a><span data-ttu-id="00e41-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00e41-106">Methods</span></span>

* [<span data-ttu-id="00e41-107">addEntriesInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-107">addEntriesInPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#addentriesinpropertyvalue)
* [<span data-ttu-id="00e41-108">addProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-108">addProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#addproperty)
* [<span data-ttu-id="00e41-109">deleteEntriesFromPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-109">deleteEntriesFromPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#deleteentriesfrompropertyvalue)
* [<span data-ttu-id="00e41-110">deleteProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-110">deleteProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#deleteproperty)
* [<span data-ttu-id="00e41-111">replaceEntryInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-111">replaceEntryInPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#replaceentryinpropertyvalue)
* [<span data-ttu-id="00e41-112">updateValueInProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-112">updateValueInProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#updatevalueinproperty)

---

## <a name="methods"></a><span data-ttu-id="00e41-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00e41-113">Methods</span></span>

<a id="addentriesinpropertyvalue"></a>

### <a name="static-addentriesinpropertyvalue"></a><span data-ttu-id="00e41-114">`<Static>`addEntriesInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-114">`<Static>` addEntriesInPropertyValue</span></span>

<span data-ttu-id="00e41-115">▸ **addEntriesInPropertyValue**(entrées : \* `string`[]\*, propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-115">▸ **addEntriesInPropertyValue**(entries: *`string`[]*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-116">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-116">**Parameters:**</span></span>

| <span data-ttu-id="00e41-117">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-117">Name</span></span> | <span data-ttu-id="00e41-118">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-118">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-119">entrées</span><span class="sxs-lookup"><span data-stu-id="00e41-119">entries</span></span> | <span data-ttu-id="00e41-120">`string`[]</span><span class="sxs-lookup"><span data-stu-id="00e41-120"></span></span> |
| <span data-ttu-id="00e41-121">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-121">property</span></span> | [<span data-ttu-id="00e41-122">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-122">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-123">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-123">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="addproperty"></a>

### <a name="static-addproperty"></a><span data-ttu-id="00e41-124">`<Static>`addProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-124">`<Static>` addProperty</span></span>

<span data-ttu-id="00e41-125">▸ **addProperty**(propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-125">▸ **addProperty**(property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-126">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-126">**Parameters:**</span></span>

| <span data-ttu-id="00e41-127">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-127">Name</span></span> | <span data-ttu-id="00e41-128">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-128">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-129">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-129">property</span></span> | [<span data-ttu-id="00e41-130">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-130">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-131">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-131">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="deleteentriesfrompropertyvalue"></a>

### <a name="static-deleteentriesfrompropertyvalue"></a><span data-ttu-id="00e41-132">`<Static>`deleteEntriesFromPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-132">`<Static>` deleteEntriesFromPropertyValue</span></span>

<span data-ttu-id="00e41-133">▸ **deleteEntriesFromPropertyValue**(entrées : \* `string`[]\*, propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-133">▸ **deleteEntriesFromPropertyValue**(entries: *`string`[]*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-134">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-134">**Parameters:**</span></span>

| <span data-ttu-id="00e41-135">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-135">Name</span></span> | <span data-ttu-id="00e41-136">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-136">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-137">entrées</span><span class="sxs-lookup"><span data-stu-id="00e41-137">entries</span></span> | <span data-ttu-id="00e41-138">`string`[]</span><span class="sxs-lookup"><span data-stu-id="00e41-138"></span></span> |
| <span data-ttu-id="00e41-139">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-139">property</span></span> | [<span data-ttu-id="00e41-140">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-140">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-141">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-141">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="deleteproperty"></a>

### <a name="static-deleteproperty"></a><span data-ttu-id="00e41-142">`<Static>`deleteProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-142">`<Static>` deleteProperty</span></span>

<span data-ttu-id="00e41-143">▸ **deleteProperty**(propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-143">▸ **deleteProperty**(property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-144">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-144">**Parameters:**</span></span>

| <span data-ttu-id="00e41-145">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-145">Name</span></span> | <span data-ttu-id="00e41-146">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-146">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-147">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-147">property</span></span> | [<span data-ttu-id="00e41-148">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-148">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-149">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-149">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="replaceentryinpropertyvalue"></a>

### <a name="static-replaceentryinpropertyvalue"></a><span data-ttu-id="00e41-150">`<Static>`replaceEntryInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="00e41-150">`<Static>` replaceEntryInPropertyValue</span></span>

<span data-ttu-id="00e41-151">▸ **replaceEntryInPropertyValue**(oldEntry : *`string`*, newEntry : *`string`*, propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-151">▸ **replaceEntryInPropertyValue**(oldEntry: *`string`*, newEntry: *`string`*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-152">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-152">**Parameters:**</span></span>

| <span data-ttu-id="00e41-153">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-153">Name</span></span> | <span data-ttu-id="00e41-154">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-154">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-155">oldEntry</span><span class="sxs-lookup"><span data-stu-id="00e41-155">oldEntry</span></span> | `string` |
| <span data-ttu-id="00e41-156">newEntry</span><span class="sxs-lookup"><span data-stu-id="00e41-156">newEntry</span></span> | `string` |
| <span data-ttu-id="00e41-157">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-157">property</span></span> | [<span data-ttu-id="00e41-158">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-158">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-159">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-159">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="updatevalueinproperty"></a>

### <a name="static-updatevalueinproperty"></a><span data-ttu-id="00e41-160">`<Static>`updateValueInProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-160">`<Static>` updateValueInProperty</span></span>

<span data-ttu-id="00e41-161">▸ **updateValueInProperty**(newValue : *`string`*, propriété : *[KASFormProperty](kasclient.kasformproperty.md)*) : [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-161">▸ **updateValueInProperty**(newValue: *`string`*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="00e41-162">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="00e41-162">**Parameters:**</span></span>

| <span data-ttu-id="00e41-163">Nom</span><span class="sxs-lookup"><span data-stu-id="00e41-163">Name</span></span> | <span data-ttu-id="00e41-164">Type</span><span class="sxs-lookup"><span data-stu-id="00e41-164">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="00e41-165">newValue</span><span class="sxs-lookup"><span data-stu-id="00e41-165">newValue</span></span> | `string` |
| <span data-ttu-id="00e41-166">propriété</span><span class="sxs-lookup"><span data-stu-id="00e41-166">property</span></span> | [<span data-ttu-id="00e41-167">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="00e41-167">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="00e41-168">**Renvoie :** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="00e41-168">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

