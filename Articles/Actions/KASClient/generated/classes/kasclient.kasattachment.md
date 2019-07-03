[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)

# <a name="class-kasattachment"></a>Classe: KASAttachment

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

**● attachmentId**: *`string`* = ""

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

Les clés de chaîne suivantes («Ty», «AFN», «ASB», etc.) DOIT être synchronisé avec la représentation du modèle objet pièce jointe dans iOS et le code Android. Cette étape est essentielle pour la sérialisation et la désérialisation appropriées sur le pont KAS.

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

▸ **populateModelFromJSON**(attachment: *[KASAttachment](kasclient.kasattachment.md)*, Object *`JSON`*:):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| pièce jointe | [KASAttachment](kasclient.kasattachment.md) |
| objet | `JSON` |

**Renvoie:**`void`

___

