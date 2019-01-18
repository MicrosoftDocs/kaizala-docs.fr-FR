---
ms.openlocfilehash: a9a9a2cd7e5b561360668982dfcbba4e74bfe834
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727929"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASImageAttachment](../classes/kasclient.kasimageattachment.md)

# <a name="class-kasimageattachment"></a>Classe : KASImageAttachment

## <a name="hierarchy"></a>Hierarchy

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASImageAttachment**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentId](kasclient.kasimageattachment.md#attachmentid)
* [fileName](kasclient.kasimageattachment.md#filename)
* [generateThumbnailServerUrl](kasclient.kasimageattachment.md#generatethumbnailserverurl)
* [hasSetThumbnail](kasclient.kasimageattachment.md#hassetthumbnail)
* [height](kasclient.kasimageattachment.md#height)
* [localPath](kasclient.kasimageattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasimageattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasimageattachment.md#serverpath)
* [size](kasclient.kasimageattachment.md#size)
* [thumbnail](kasclient.kasimageattachment.md#thumbnail)
* [thumbnailServerUrl](kasclient.kasimageattachment.md#thumbnailserverurl)
* [type](kasclient.kasimageattachment.md#type)
* [width](kasclient.kasimageattachment.md#width)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasimageattachment.md#tojson)
* [fromJSON](kasclient.kasimageattachment.md#fromjson)
* [hasLocalPath](kasclient.kasimageattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasimageattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasimageattachment.md#populatemodelfromjson)

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

<a id="generatethumbnailserverurl"></a>

###  <a name="generatethumbnailserverurl"></a>generateThumbnailServerUrl

**● generateThumbnailServerUrl**: *`boolean`* = false

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● hasSetThumbnail**: *`boolean`* = false

___

<a id="height"></a>

###  <a name="height"></a>height

**Hauteur ●**: *`number`* = 0

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

<a id="thumbnailserverurl"></a>

###  <a name="thumbnailserverurl"></a>thumbnailServerUrl

**● thumbnailServerUrl**: *`string`* = « »

___

<a id="type"></a>

###  <a name="type"></a>type

**Type ●**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image

___

<a id="width"></a>

###  <a name="width"></a>width

**Largeur ●**: *`number`* = 0

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASImageAttachment](kasclient.kasimageattachment.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASImageAttachment](kasclient.kasimageattachment.md)

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

▸ **populateModelFromJSON**(pièces jointes : *[KASImageAttachment](kasclient.kasimageattachment.md)*, l’objet : *`JSON`*) :`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASImageAttachment](kasclient.kasimageattachment.md) |
| objet | `JSON` |

**Renvoie :** `void`

___

