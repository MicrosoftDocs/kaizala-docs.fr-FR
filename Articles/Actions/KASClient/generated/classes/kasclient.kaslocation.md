---
ms.openlocfilehash: f9866ba870c065df049ffcde8b36feac23a3b3d0
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727941"
---
<span data-ttu-id="a7908-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASLocation](../classes/kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="a7908-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASLocation](../classes/kasclient.kaslocation.md)</span></span>

# <a name="class-kaslocation"></a><span data-ttu-id="a7908-102">Classe : KASLocation</span><span class="sxs-lookup"><span data-stu-id="a7908-102">Class: KASLocation</span></span>

## <a name="hierarchy"></a><span data-ttu-id="a7908-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a7908-103">Hierarchy</span></span>

<span data-ttu-id="a7908-104">**KASLocation**</span><span class="sxs-lookup"><span data-stu-id="a7908-104">**KASLocation**</span></span>

## <a name="index"></a><span data-ttu-id="a7908-105">Index</span><span class="sxs-lookup"><span data-stu-id="a7908-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="a7908-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7908-106">Properties</span></span>

* [<span data-ttu-id="a7908-107">latitude</span><span class="sxs-lookup"><span data-stu-id="a7908-107">latitude</span></span>](kasclient.kaslocation.md#latitude)
* [<span data-ttu-id="a7908-108">longitude</span><span class="sxs-lookup"><span data-stu-id="a7908-108">longitude</span></span>](kasclient.kaslocation.md#longitude)
* [<span data-ttu-id="a7908-109">placeAddress</span><span class="sxs-lookup"><span data-stu-id="a7908-109">placeAddress</span></span>](kasclient.kaslocation.md#placeaddress)
* [<span data-ttu-id="a7908-110">placeName</span><span class="sxs-lookup"><span data-stu-id="a7908-110">placeName</span></span>](kasclient.kaslocation.md#placename)
### <a name="methods"></a><span data-ttu-id="a7908-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7908-111">Methods</span></span>

* [<span data-ttu-id="a7908-112">toJSON</span><span class="sxs-lookup"><span data-stu-id="a7908-112">toJSON</span></span>](kasclient.kaslocation.md#tojson)
* [<span data-ttu-id="a7908-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="a7908-113">fromJSON</span></span>](kasclient.kaslocation.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="a7908-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7908-114">Properties</span></span>

<a id="latitude"></a>

###  <a name="latitude"></a><span data-ttu-id="a7908-115">latitude</span><span class="sxs-lookup"><span data-stu-id="a7908-115">latitude</span></span>

<span data-ttu-id="a7908-116">**Latitude ●**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a7908-116">**● latitude**: *`number`* = 0</span></span>

<span data-ttu-id="a7908-117">Latitude de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="a7908-117">Latitude of the location</span></span>

___

<a id="longitude"></a>

###  <a name="longitude"></a><span data-ttu-id="a7908-118">longitude</span><span class="sxs-lookup"><span data-stu-id="a7908-118">longitude</span></span>

<span data-ttu-id="a7908-119">**Longitude ●**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a7908-119">**● longitude**: *`number`* = 0</span></span>

<span data-ttu-id="a7908-120">Longitude de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="a7908-120">Longitude of the location</span></span>

___

<a id="placeaddress"></a>

###  <a name="placeaddress"></a><span data-ttu-id="a7908-121">placeAddress</span><span class="sxs-lookup"><span data-stu-id="a7908-121">placeAddress</span></span>

<span data-ttu-id="a7908-122">**● placeAddress**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="a7908-122">**● placeAddress**: *`string`* = ""</span></span>

<span data-ttu-id="a7908-123">Adresse de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="a7908-123">Address of the location</span></span>

___

<a id="placename"></a>

###  <a name="placename"></a><span data-ttu-id="a7908-124">placeName</span><span class="sxs-lookup"><span data-stu-id="a7908-124">placeName</span></span>

<span data-ttu-id="a7908-125">**● placeName**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="a7908-125">**● placeName**: *`string`* = ""</span></span>

<span data-ttu-id="a7908-126">Nom de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="a7908-126">Name of the location</span></span>

___

## <a name="methods"></a><span data-ttu-id="a7908-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7908-127">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="a7908-128">toJSON</span><span class="sxs-lookup"><span data-stu-id="a7908-128">toJSON</span></span>

<span data-ttu-id="a7908-129">▸ **toJSON**() :`JSON`</span><span class="sxs-lookup"><span data-stu-id="a7908-129">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="a7908-130">**Renvoie :** `JSON`</span><span class="sxs-lookup"><span data-stu-id="a7908-130">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="a7908-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="a7908-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="a7908-132">▸ **fromJSON**(objet : *`JSON`*) : [KASLocation](kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="a7908-132">▸ **fromJSON**(object: *`JSON`*): [KASLocation](kasclient.kaslocation.md)</span></span>

<span data-ttu-id="a7908-133">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="a7908-133">**Parameters:**</span></span>

| <span data-ttu-id="a7908-134">Nom</span><span class="sxs-lookup"><span data-stu-id="a7908-134">Name</span></span> | <span data-ttu-id="a7908-135">Type</span><span class="sxs-lookup"><span data-stu-id="a7908-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="a7908-136">objet</span><span class="sxs-lookup"><span data-stu-id="a7908-136">object</span></span> | `JSON` |

<span data-ttu-id="a7908-137">**Renvoie :** [KASLocation](kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="a7908-137">**Returns:** [KASLocation](kasclient.kaslocation.md)</span></span>

___

