[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAudioAttachment](../classes/kasclient.kasaudioattachment.md)

# <a name="class-kasaudioattachment"></a>Classe: KASAudioAttachment

## <a name="hierarchy"></a>Hierarchy

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASAudioAttachment**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentId](kasclient.kasaudioattachment.md#attachmentid)
* [duration](kasclient.kasaudioattachment.md#duration)
* [fileName](kasclient.kasaudioattachment.md#filename)
* [hasSetThumbnail](kasclient.kasaudioattachment.md#hassetthumbnail)
* [localPath](kasclient.kasaudioattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasaudioattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasaudioattachment.md#serverpath)
* [size](kasclient.kasaudioattachment.md#size)
* [thumbnail](kasclient.kasaudioattachment.md#thumbnail)
* [type](kasclient.kasaudioattachment.md#type)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasaudioattachment.md#tojson)
* [fromJSON](kasclient.kasaudioattachment.md#fromjson)
* [hasLocalPath](kasclient.kasaudioattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasaudioattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasaudioattachment.md#populatemodelfromjson)

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

###  <a name="size"></a>taille

**● taille**: *`number`* = 0

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

▸ **populateModelFromJSON**(attachment: *[KASAudioAttachment](kasclient.kasaudioattachment.md)*, Object *`JSON`*:):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASAudioAttachment](kasclient.kasaudioattachment.md) |
| objet | `JSON` |

**Renvoie:**`void`

___

