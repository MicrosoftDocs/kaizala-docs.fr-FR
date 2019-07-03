[](../README.md) > [KASClient](../modules/kasclient.md) > [KASVideoAttachment](../classes/kasclient.kasvideoattachment.md)

# <a name="class-kasvideoattachment"></a>Classe: KASVideoAttachment

## <a name="hierarchy"></a>Hierarchy

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASVideoAttachment**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentId](kasclient.kasvideoattachment.md#attachmentid)
* [duration](kasclient.kasvideoattachment.md#duration)
* [fileName](kasclient.kasvideoattachment.md#filename)
* [hasSetThumbnail](kasclient.kasvideoattachment.md#hassetthumbnail)
* [localPath](kasclient.kasvideoattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasvideoattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasvideoattachment.md#serverpath)
* [size](kasclient.kasvideoattachment.md#size)
* [streamingPath](kasclient.kasvideoattachment.md#streamingpath)
* [thumbnail](kasclient.kasvideoattachment.md#thumbnail)
* [type](kasclient.kasvideoattachment.md#type)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasvideoattachment.md#tojson)
* [fromJSON](kasclient.kasvideoattachment.md#fromjson)
* [hasLocalPath](kasclient.kasvideoattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasvideoattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasvideoattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Propriétés

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● attachmentId**: *`string`* = ""

___
<a id="duration"></a>

###  <a name="duration"></a>duration

**● durée**: *`number`* = 0

___
<a id="filename"></a>

###  <a name="filename"></a>fileName

**● filename**: *`string`* = ""

___
<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● hasSetThumbnail**: *`boolean`* = false

___
<a id="localpath"></a>

###  <a name="localpath"></a>localPath

**● LocalPath**: *`string`* = ""

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
<a id="streamingpath"></a>

###  <a name="streamingpath"></a>streamingPath

**● streamingPath**: *`string`* = ""

___
<a id="thumbnail"></a>

###  <a name="thumbnail"></a>icône

**● miniature**: *`string`* = ""

___
<a id="type"></a>

###  <a name="type"></a>type

**● type**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. image

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASAttachment](kasclient.kasattachment.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASAttachment](kasclient.kasattachment.md)

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

▸ **populateModelFromJSON**(attachment: *[KASVideoAttachment](kasclient.kasvideoattachment.md)*, Object *`JSON`*:):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASVideoAttachment](kasclient.kasvideoattachment.md) |
| objet | `JSON` |

**Renvoie:**`void`

___

