---
ms.openlocfilehash: 5ea10ec4a326c6ae1ceaae4db8a2994d25e17fce
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727928"
---
<span data-ttu-id="94d49-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span></span>

# <a name="class-kasattachment"></a><span data-ttu-id="94d49-102">Classe : KASAttachment</span><span class="sxs-lookup"><span data-stu-id="94d49-102">Class: KASAttachment</span></span>

## <a name="hierarchy"></a><span data-ttu-id="94d49-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="94d49-103">Hierarchy</span></span>

<span data-ttu-id="94d49-104">**KASAttachment**</span><span class="sxs-lookup"><span data-stu-id="94d49-104">**KASAttachment**</span></span>

<span data-ttu-id="94d49-105">↳ [KASAudioAttachment](kasclient.kasaudioattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-105">↳  [KASAudioAttachment](kasclient.kasaudioattachment.md)</span></span>

<span data-ttu-id="94d49-106">↳ [KASImageAttachment](kasclient.kasimageattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-106">↳  [KASImageAttachment](kasclient.kasimageattachment.md)</span></span>

<span data-ttu-id="94d49-107">↳ [KASVideoAttachment](kasclient.kasvideoattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-107">↳  [KASVideoAttachment](kasclient.kasvideoattachment.md)</span></span>

## <a name="index"></a><span data-ttu-id="94d49-108">Index</span><span class="sxs-lookup"><span data-stu-id="94d49-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="94d49-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94d49-109">Properties</span></span>

* [<span data-ttu-id="94d49-110">attachmentId</span><span class="sxs-lookup"><span data-stu-id="94d49-110">attachmentId</span></span>](kasclient.kasattachment.md#attachmentid)
* [<span data-ttu-id="94d49-111">fileName</span><span class="sxs-lookup"><span data-stu-id="94d49-111">fileName</span></span>](kasclient.kasattachment.md#filename)
* [<span data-ttu-id="94d49-112">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="94d49-112">hasSetThumbnail</span></span>](kasclient.kasattachment.md#hassetthumbnail)
* [<span data-ttu-id="94d49-113">localPath</span><span class="sxs-lookup"><span data-stu-id="94d49-113">localPath</span></span>](kasclient.kasattachment.md#localpath)
* [<span data-ttu-id="94d49-114">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="94d49-114">requireHighResThumbnail</span></span>](kasclient.kasattachment.md#requirehighresthumbnail)
* [<span data-ttu-id="94d49-115">serverPath</span><span class="sxs-lookup"><span data-stu-id="94d49-115">serverPath</span></span>](kasclient.kasattachment.md#serverpath)
* [<span data-ttu-id="94d49-116">size</span><span class="sxs-lookup"><span data-stu-id="94d49-116">size</span></span>](kasclient.kasattachment.md#size)
* [<span data-ttu-id="94d49-117">thumbnail</span><span class="sxs-lookup"><span data-stu-id="94d49-117">thumbnail</span></span>](kasclient.kasattachment.md#thumbnail)
* [<span data-ttu-id="94d49-118">type</span><span class="sxs-lookup"><span data-stu-id="94d49-118">type</span></span>](kasclient.kasattachment.md#type)
### <a name="methods"></a><span data-ttu-id="94d49-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94d49-119">Methods</span></span>

* [<span data-ttu-id="94d49-120">toJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-120">toJSON</span></span>](kasclient.kasattachment.md#tojson)
* [<span data-ttu-id="94d49-121">fromJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-121">fromJSON</span></span>](kasclient.kasattachment.md#fromjson)
* [<span data-ttu-id="94d49-122">hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="94d49-122">hasLocalPath</span></span>](kasclient.kasattachment.md#haslocalpath)
* [<span data-ttu-id="94d49-123">hasServerPath</span><span class="sxs-lookup"><span data-stu-id="94d49-123">hasServerPath</span></span>](kasclient.kasattachment.md#hasserverpath)
* [<span data-ttu-id="94d49-124">populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-124">populateModelFromJSON</span></span>](kasclient.kasattachment.md#populatemodelfromjson)

---

## <a name="properties"></a><span data-ttu-id="94d49-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94d49-125">Properties</span></span>

<a id="attachmentid"></a>

###  <a name="attachmentid"></a><span data-ttu-id="94d49-126">attachmentId</span><span class="sxs-lookup"><span data-stu-id="94d49-126">attachmentId</span></span>

<span data-ttu-id="94d49-127">**● attachmentId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="94d49-127">**● attachmentId**: *`string`* = ""</span></span>

___

<a id="filename"></a>

###  <a name="filename"></a><span data-ttu-id="94d49-128">fileName</span><span class="sxs-lookup"><span data-stu-id="94d49-128">fileName</span></span>

<span data-ttu-id="94d49-129">**● le nom de fichier**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="94d49-129">**● fileName**: *`string`* = ""</span></span>

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a><span data-ttu-id="94d49-130">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="94d49-130">hasSetThumbnail</span></span>

<span data-ttu-id="94d49-131">**● hasSetThumbnail**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="94d49-131">**● hasSetThumbnail**: *`boolean`* = false</span></span>

___

<a id="localpath"></a>

###  <a name="localpath"></a><span data-ttu-id="94d49-132">localPath</span><span class="sxs-lookup"><span data-stu-id="94d49-132">localPath</span></span>

<span data-ttu-id="94d49-133">**● localPath**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="94d49-133">**● localPath**: *`string`* = ""</span></span>

___

<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a><span data-ttu-id="94d49-134">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="94d49-134">requireHighResThumbnail</span></span>

<span data-ttu-id="94d49-135">**● requireHighResThumbnail**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="94d49-135">**● requireHighResThumbnail**: *`boolean`* = false</span></span>

___

<a id="serverpath"></a>

###  <a name="serverpath"></a><span data-ttu-id="94d49-136">serverPath</span><span class="sxs-lookup"><span data-stu-id="94d49-136">serverPath</span></span>

<span data-ttu-id="94d49-137">**● serverPath**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="94d49-137">**● serverPath**: *`string`* = ""</span></span>

___

<a id="size"></a>

###  <a name="size"></a><span data-ttu-id="94d49-138">size</span><span class="sxs-lookup"><span data-stu-id="94d49-138">size</span></span>

<span data-ttu-id="94d49-139">**Taille ●**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="94d49-139">**● size**: *`number`* = 0</span></span>

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a><span data-ttu-id="94d49-140">miniature</span><span class="sxs-lookup"><span data-stu-id="94d49-140">thumbnail</span></span>

<span data-ttu-id="94d49-141">**Miniature ●**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="94d49-141">**● thumbnail**: *`string`* = ""</span></span>

___

<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="94d49-142">type</span><span class="sxs-lookup"><span data-stu-id="94d49-142">type</span></span>

<span data-ttu-id="94d49-143">**Type ●**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image</span><span class="sxs-lookup"><span data-stu-id="94d49-143">**● type**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* =  KASAttachmentType.Image</span></span>

___

## <a name="methods"></a><span data-ttu-id="94d49-144">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94d49-144">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="94d49-145">toJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-145">toJSON</span></span>

<span data-ttu-id="94d49-146">▸ **toJSON**() :`JSON`</span><span class="sxs-lookup"><span data-stu-id="94d49-146">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="94d49-147">Les clés de chaîne suivantes (« ty », « bande afn », « asb », etc.) DOIT être synchronisée avec la représentation du modèle objet des pièces jointes dans iOS et Android code.</span><span class="sxs-lookup"><span data-stu-id="94d49-147">The following string keys("ty", "afn", "asb", etc.) MUST be in sync with the Attachment object model representation in iOS and Android code.</span></span> <span data-ttu-id="94d49-148">Ceci est essentiel appropriée sérialisation et la désérialisation sur le pont KAS.</span><span class="sxs-lookup"><span data-stu-id="94d49-148">This is vital for proper serialization and deserialization over the KAS bridge.</span></span>

<span data-ttu-id="94d49-149">**Renvoie :** `JSON`</span><span class="sxs-lookup"><span data-stu-id="94d49-149">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="94d49-150">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-150">`<Static>` fromJSON</span></span>

<span data-ttu-id="94d49-151">▸ **fromJSON**(objet : *`any`*) : [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-151">▸ **fromJSON**(object: *`any`*): [KASAttachment](kasclient.kasattachment.md)</span></span>

<span data-ttu-id="94d49-152">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="94d49-152">**Parameters:**</span></span>

| <span data-ttu-id="94d49-153">Nom</span><span class="sxs-lookup"><span data-stu-id="94d49-153">Name</span></span> | <span data-ttu-id="94d49-154">Type</span><span class="sxs-lookup"><span data-stu-id="94d49-154">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="94d49-155">objet</span><span class="sxs-lookup"><span data-stu-id="94d49-155">object</span></span> | `any` |

<span data-ttu-id="94d49-156">**Renvoie :** [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="94d49-156">**Returns:** [KASAttachment](kasclient.kasattachment.md)</span></span>

___

<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a><span data-ttu-id="94d49-157">`<Static>`hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="94d49-157">`<Static>` hasLocalPath</span></span>

<span data-ttu-id="94d49-158">▸ **hasLocalPath**(obj : *[KASAttachment](kasclient.kasattachment.md)*) :`boolean`</span><span class="sxs-lookup"><span data-stu-id="94d49-158">▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="94d49-159">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="94d49-159">**Parameters:**</span></span>

| <span data-ttu-id="94d49-160">Nom</span><span class="sxs-lookup"><span data-stu-id="94d49-160">Name</span></span> | <span data-ttu-id="94d49-161">Type</span><span class="sxs-lookup"><span data-stu-id="94d49-161">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="94d49-162">obj</span><span class="sxs-lookup"><span data-stu-id="94d49-162">obj</span></span> | [<span data-ttu-id="94d49-163">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="94d49-163">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="94d49-164">**Renvoie :** `boolean`</span><span class="sxs-lookup"><span data-stu-id="94d49-164">**Returns:** `boolean`</span></span>

___

<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a><span data-ttu-id="94d49-165">`<Static>`hasServerPath</span><span class="sxs-lookup"><span data-stu-id="94d49-165">`<Static>` hasServerPath</span></span>

<span data-ttu-id="94d49-166">▸ **hasServerPath**(obj : *[KASAttachment](kasclient.kasattachment.md)*) :`boolean`</span><span class="sxs-lookup"><span data-stu-id="94d49-166">▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="94d49-167">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="94d49-167">**Parameters:**</span></span>

| <span data-ttu-id="94d49-168">Nom</span><span class="sxs-lookup"><span data-stu-id="94d49-168">Name</span></span> | <span data-ttu-id="94d49-169">Type</span><span class="sxs-lookup"><span data-stu-id="94d49-169">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="94d49-170">obj</span><span class="sxs-lookup"><span data-stu-id="94d49-170">obj</span></span> | [<span data-ttu-id="94d49-171">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="94d49-171">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="94d49-172">**Renvoie :** `boolean`</span><span class="sxs-lookup"><span data-stu-id="94d49-172">**Returns:** `boolean`</span></span>

___

<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a><span data-ttu-id="94d49-173">`<Static>`populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="94d49-173">`<Static>` populateModelFromJSON</span></span>

<span data-ttu-id="94d49-174">▸ **populateModelFromJSON**(pièces jointes : *[KASAttachment](kasclient.kasattachment.md)*, l’objet : *`JSON`*) :`void`</span><span class="sxs-lookup"><span data-stu-id="94d49-174">▸ **populateModelFromJSON**(attachment: *[KASAttachment](kasclient.kasattachment.md)*, object: *`JSON`*): `void`</span></span>

<span data-ttu-id="94d49-175">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="94d49-175">**Parameters:**</span></span>

| <span data-ttu-id="94d49-176">Nom</span><span class="sxs-lookup"><span data-stu-id="94d49-176">Name</span></span> | <span data-ttu-id="94d49-177">Type</span><span class="sxs-lookup"><span data-stu-id="94d49-177">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="94d49-178">pièce jointe</span><span class="sxs-lookup"><span data-stu-id="94d49-178">attachment</span></span> | [<span data-ttu-id="94d49-179">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="94d49-179">KASAttachment</span></span>](kasclient.kasattachment.md) |
| <span data-ttu-id="94d49-180">objet</span><span class="sxs-lookup"><span data-stu-id="94d49-180">object</span></span> | `JSON` |

<span data-ttu-id="94d49-181">**Renvoie :** `void`</span><span class="sxs-lookup"><span data-stu-id="94d49-181">**Returns:** `void`</span></span>

___

