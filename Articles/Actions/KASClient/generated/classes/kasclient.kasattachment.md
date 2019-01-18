---
ms.openlocfilehash: 5ea10ec4a326c6ae1ceaae4db8a2994d25e17fce
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727928"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)

# <a name="class-kasattachment"></a>Classe : KASAttachment

## <a name="hierarchy"></a>Hierarchy

**KASAttachment**

↳ [KASAudioAttachment](kasclient.kasaudioattachment.md)

↳ [KASImageAttachment](kasclient.kasimageattachment.md)

↳ [KASVideoAttachment](kasclient.kasvideoattachment.md)

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentId](kasclient.kasattachment.md#attachmentid)
* [fileName](kasclient.kasattachment.md#filename)
* [hasSetThumbnail](kasclient.kasattachment.md#hassetthumbnail)
* [localPath](kasclient.kasattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasattachment.md#serverpath)
* [size](kasclient.kasattachment.md#size)
* [thumbnail](kasclient.kasattachment.md#thumbnail)
* [type](kasclient.kasattachment.md#type)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasattachment.md#tojson)
* [fromJSON](kasclient.kasattachment.md#fromjson)
* [hasLocalPath](kasclient.kasattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Propriétés

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● attachmentId**: *`string`* = « »

___

<a id="filename"></a>

###  <a name="filename"></a>fileName

**● le nom de fichier**: *`string`* = « »

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● hasSetThumbnail**: *`boolean`* = false

___

<a id="localpath"></a>

###  <a name="localpath"></a>localPath

**● localPath**: *`string`* = « »

___

<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a>requireHighResThumbnail

**● requireHighResThumbnail**: *`boolean`* = false

___

<a id="serverpath"></a>

###  <a name="serverpath"></a>serverPath

**● serverPath**: *`string`* = « »

___

<a id="size"></a>

###  <a name="size"></a>size

**Taille ●**: *`number`* = 0

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a>miniature

**Miniature ●**: *`string`* = « »

___

<a id="type"></a>

###  <a name="type"></a>type

**Type ●**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**() :`JSON`

Les clés de chaîne suivantes (« ty », « bande afn », « asb », etc.) DOIT être synchronisée avec la représentation du modèle objet des pièces jointes dans iOS et Android code. Ceci est essentiel appropriée sérialisation et la désérialisation sur le pont KAS.

**Renvoie :** `JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASAttachment](kasclient.kasattachment.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASAttachment](kasclient.kasattachment.md)

___

<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a>`<Static>`hasLocalPath

▸ **hasLocalPath**(obj : *[KASAttachment](kasclient.kasattachment.md)*) :`boolean`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Renvoie :** `boolean`

___

<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a>`<Static>`hasServerPath

▸ **hasServerPath**(obj : *[KASAttachment](kasclient.kasattachment.md)*) :`boolean`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Renvoie :** `boolean`

___

<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a>`<Static>`populateModelFromJSON

▸ **populateModelFromJSON**(pièces jointes : *[KASAttachment](kasclient.kasattachment.md)*, l’objet : *`JSON`*) :`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASAttachment](kasclient.kasattachment.md) |
| objet | `JSON` |

**Renvoie :** `void`

___

