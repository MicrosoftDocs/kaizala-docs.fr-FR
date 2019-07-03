[](../README.md) > [KASClient](../modules/kasclient.md) > [KASRichImageAttachment](../classes/kasclient.kasrichimageattachment.md)

# <a name="class-kasrichimageattachment"></a>Classe: KASRichImageAttachment

## <a name="hierarchy"></a>Hierarchy

↳ [KASImageAttachment](kasclient.kasimageattachment.md)

**↳ KASRichImageAttachment**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentId](kasclient.kasrichimageattachment.md#attachmentid)
* [fileName](kasclient.kasrichimageattachment.md#filename)
* [generateThumbnailServerUrl](kasclient.kasrichimageattachment.md#generatethumbnailserverurl)
* [hasSetThumbnail](kasclient.kasrichimageattachment.md#hassetthumbnail)
* [height](kasclient.kasrichimageattachment.md#height)
* [id](kasclient.kasrichimageattachment.md#id)
* [localPath](kasclient.kasrichimageattachment.md#localpath)
* [metadataFetchState](kasclient.kasrichimageattachment.md#metadatafetchstate)
* [ocrData](kasclient.kasrichimageattachment.md#ocrdata)
* [processedOCRData](kasclient.kasrichimageattachment.md#processedocrdata)
* [requireHighResThumbnail](kasclient.kasrichimageattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasrichimageattachment.md#serverpath)
* [size](kasclient.kasrichimageattachment.md#size)
* [thumbnail](kasclient.kasrichimageattachment.md#thumbnail)
* [thumbnailServerUrl](kasclient.kasrichimageattachment.md#thumbnailserverurl)
* [type](kasclient.kasrichimageattachment.md#type)
* [width](kasclient.kasrichimageattachment.md#width)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasrichimageattachment.md#tojson)
* [fromJSON](kasclient.kasrichimageattachment.md#fromjson)
* [hasLocalPath](kasclient.kasrichimageattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasrichimageattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasrichimageattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Propriétés

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● attachmentId**: *`string`* = ""

___
<a id="filename"></a>

###  <a name="filename"></a>fileName

**● filename**: *`string`* = ""

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

**● hauteur**: *`number`* = 0

___
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = null

___
<a id="localpath"></a>

###  <a name="localpath"></a>localPath

**● LocalPath**: *`string`* = ""

___
<a id="metadatafetchstate"></a>

###  <a name="metadatafetchstate"></a>metadataFetchState

**● metadataFetchState**: *[ImageMetadataFetchState](../enums/kasclient.imagemetadatafetchstate.md)* = ImageMetadataFetchState. initié

___
<a id="ocrdata"></a>

###  <a name="ocrdata"></a>ocrData

**● ocrData**: *`string`* = null

___
<a id="processedocrdata"></a>

###  <a name="processedocrdata"></a>processedOCRData

**● processedOCRData**: *`string`* = null

___
<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a>requireHighResThumbnail

**● requireHighResThumbnail**: *`boolean`* = false

___
<a id="serverpath"></a>

###  <a name="serverpath"></a>serverPath

**● ServerPath**: *`string`* = ""

___
<a id="size"></a>

###  <a name="size"></a>size

**● taille**: *`number`* = 0

___
<a id="thumbnail"></a>

###  <a name="thumbnail"></a>icône

**● miniature**: *`string`* = ""

___
<a id="thumbnailserverurl"></a>

###  <a name="thumbnailserverurl"></a>thumbnailServerUrl

**● thumbnailServerUrl**: *`string`* = ""

___
<a id="type"></a>

###  <a name="type"></a>type

**● type**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. image

___
<a id="width"></a>

###  <a name="width"></a>width

**● largeur**: *`number`* = 0

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASRichImageAttachment](kasclient.kasrichimageattachment.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASRichImageAttachment](kasclient.kasrichimageattachment.md)

___
<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a>`<Static>`hasLocalPath

▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| 5.5 | [KASAttachment](kasclient.kasattachment.md) |

**Renvoie:**`boolean`

___
<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a>`<Static>`hasServerPath

▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| 5.5 | [KASAttachment](kasclient.kasattachment.md) |

**Renvoie:**`boolean`

___
<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a>`<Static>`populateModelFromJSON

▸ **populateModelFromJSON**(attachment: *[KASRichImageAttachment](kasclient.kasrichimageattachment.md)*, Object *`JSON`*:):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASRichImageAttachment](kasclient.kasrichimageattachment.md) |
| objet | `JSON` |

**Renvoie:**`void`

___

