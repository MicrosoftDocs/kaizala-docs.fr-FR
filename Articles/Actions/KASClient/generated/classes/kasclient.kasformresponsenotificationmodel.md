---
ms.openlocfilehash: 94efbe6f80d643bdc930e2c23de6197d8b20d7ad
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727922"
---
<span data-ttu-id="46e42-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)</span></span>

# <a name="class-kasformresponsenotificationmodel"></a><span data-ttu-id="46e42-102">Classe : KASFormResponseNotificationModel</span><span class="sxs-lookup"><span data-stu-id="46e42-102">Class: KASFormResponseNotificationModel</span></span>

## <a name="hierarchy"></a><span data-ttu-id="46e42-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="46e42-103">Hierarchy</span></span>

<span data-ttu-id="46e42-104">**KASFormResponseNotificationModel**</span><span class="sxs-lookup"><span data-stu-id="46e42-104">**KASFormResponseNotificationModel**</span></span>

## <a name="index"></a><span data-ttu-id="46e42-105">Index</span><span class="sxs-lookup"><span data-stu-id="46e42-105">Index</span></span>

### <a name="constructors"></a><span data-ttu-id="46e42-106">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="46e42-106">Constructors</span></span>

* [<span data-ttu-id="46e42-107">constructeur</span><span class="sxs-lookup"><span data-stu-id="46e42-107">constructor</span></span>](kasclient.kasformresponsenotificationmodel.md#constructor)
### <a name="properties"></a><span data-ttu-id="46e42-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46e42-108">Properties</span></span>

* [<span data-ttu-id="46e42-109">messagePreview</span><span class="sxs-lookup"><span data-stu-id="46e42-109">messagePreview</span></span>](kasclient.kasformresponsenotificationmodel.md#messagepreview)
* [<span data-ttu-id="46e42-110">messageTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-110">messageTarget</span></span>](kasclient.kasformresponsenotificationmodel.md#messagetarget)
* [<span data-ttu-id="46e42-111">pushTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-111">pushTarget</span></span>](kasclient.kasformresponsenotificationmodel.md#pushtarget)
### <a name="methods"></a><span data-ttu-id="46e42-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46e42-112">Methods</span></span>

* [<span data-ttu-id="46e42-113">toJSON</span><span class="sxs-lookup"><span data-stu-id="46e42-113">toJSON</span></span>](kasclient.kasformresponsenotificationmodel.md#tojson)
* [<span data-ttu-id="46e42-114">fromJson</span><span class="sxs-lookup"><span data-stu-id="46e42-114">fromJson</span></span>](kasclient.kasformresponsenotificationmodel.md#fromjson)

---

## <a name="constructors"></a><span data-ttu-id="46e42-115">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="46e42-115">Constructors</span></span>

<a id="constructor"></a>

###  <a name="constructor"></a><span data-ttu-id="46e42-116">constructeur</span><span class="sxs-lookup"><span data-stu-id="46e42-116">constructor</span></span>

<span data-ttu-id="46e42-117">⊕ **KASFormResponseNotificationModel nouveau**(messageTarget? : *[] [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)*, pushTarget? : *[] [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)*, messagePreview? : *`String`*) : [ KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-117">⊕ **new KASFormResponseNotificationModel**(messageTarget?: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, pushTarget?: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, messagePreview?: *`String`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

<span data-ttu-id="46e42-118">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="46e42-118">**Parameters:**</span></span>

| <span data-ttu-id="46e42-119">Nom</span><span class="sxs-lookup"><span data-stu-id="46e42-119">Name</span></span> | <span data-ttu-id="46e42-120">Type</span><span class="sxs-lookup"><span data-stu-id="46e42-120">Type</span></span> | <span data-ttu-id="46e42-121">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="46e42-121">Default value</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="46e42-122">`Default value`messageTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-122">`Default value` messageTarget</span></span> | <span data-ttu-id="46e42-123">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) []</span><span class="sxs-lookup"><span data-stu-id="46e42-123">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]</span></span> |  <span data-ttu-id="46e42-124">null</span><span class="sxs-lookup"><span data-stu-id="46e42-124">null</span></span> |
| <span data-ttu-id="46e42-125">`Default value`pushTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-125">`Default value` pushTarget</span></span> | <span data-ttu-id="46e42-126">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) []</span><span class="sxs-lookup"><span data-stu-id="46e42-126">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]</span></span> |  <span data-ttu-id="46e42-127">null</span><span class="sxs-lookup"><span data-stu-id="46e42-127">null</span></span> |
| <span data-ttu-id="46e42-128">`Default value`messagePreview</span><span class="sxs-lookup"><span data-stu-id="46e42-128">`Default value` messagePreview</span></span> | `String` |  <span data-ttu-id="46e42-129">null</span><span class="sxs-lookup"><span data-stu-id="46e42-129">null</span></span> |

<span data-ttu-id="46e42-130">**Renvoie :** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-130">**Returns:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

___

## <a name="properties"></a><span data-ttu-id="46e42-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46e42-131">Properties</span></span>

<a id="messagepreview"></a>

###  <a name="messagepreview"></a><span data-ttu-id="46e42-132">messagePreview</span><span class="sxs-lookup"><span data-stu-id="46e42-132">messagePreview</span></span>

<span data-ttu-id="46e42-133">**● messagePreview**: *`String`* = « »</span><span class="sxs-lookup"><span data-stu-id="46e42-133">**● messagePreview**: *`String`* = ""</span></span>

___

<a id="messagetarget"></a>

###  <a name="messagetarget"></a><span data-ttu-id="46e42-134">messageTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-134">messageTarget</span></span>

<span data-ttu-id="46e42-135">**● messageTarget**: *[] [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)*</span><span class="sxs-lookup"><span data-stu-id="46e42-135">**● messageTarget**: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*</span></span>

___

<a id="pushtarget"></a>

###  <a name="pushtarget"></a><span data-ttu-id="46e42-136">pushTarget</span><span class="sxs-lookup"><span data-stu-id="46e42-136">pushTarget</span></span>

<span data-ttu-id="46e42-137">**● pushTarget**: *[] [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)*</span><span class="sxs-lookup"><span data-stu-id="46e42-137">**● pushTarget**: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*</span></span>

___

## <a name="methods"></a><span data-ttu-id="46e42-138">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46e42-138">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="46e42-139">toJSON</span><span class="sxs-lookup"><span data-stu-id="46e42-139">toJSON</span></span>

<span data-ttu-id="46e42-140">▸ **toJSON**() :`JSON`</span><span class="sxs-lookup"><span data-stu-id="46e42-140">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="46e42-141">**Renvoie :** `JSON`</span><span class="sxs-lookup"><span data-stu-id="46e42-141">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="46e42-142">`<Static>`fromJson</span><span class="sxs-lookup"><span data-stu-id="46e42-142">`<Static>` fromJson</span></span>

<span data-ttu-id="46e42-143">▸ **fromJson**(objet : *`JSON`*) : [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-143">▸ **fromJson**(object: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

<span data-ttu-id="46e42-144">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="46e42-144">**Parameters:**</span></span>

| <span data-ttu-id="46e42-145">Nom</span><span class="sxs-lookup"><span data-stu-id="46e42-145">Name</span></span> | <span data-ttu-id="46e42-146">Type</span><span class="sxs-lookup"><span data-stu-id="46e42-146">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="46e42-147">objet</span><span class="sxs-lookup"><span data-stu-id="46e42-147">object</span></span> | `JSON` |

<span data-ttu-id="46e42-148">**Renvoie :** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-148">**Returns:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

___

