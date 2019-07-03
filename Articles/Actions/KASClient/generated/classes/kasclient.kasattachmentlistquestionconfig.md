[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionConfig](../classes/kasclient.kasattachmentlistquestionconfig.md)

# <a name="class-kasattachmentlistquestionconfig"></a>Classe: KASAttachmentListQuestionConfig

## <a name="hierarchy"></a>Hierarchy

 [KASQuestionConfig](kasclient.kasquestionconfig.md)

**↳ KASAttachmentListQuestionConfig**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentListType](kasclient.kasattachmentlistquestionconfig.md#attachmentlisttype)
* [defaultCameraFilterMode](kasclient.kasattachmentlistquestionconfig.md#defaultcamerafiltermode)
* [imageSource](kasclient.kasattachmentlistquestionconfig.md#imagesource)
* [maxImageCount](kasclient.kasattachmentlistquestionconfig.md#maximagecount)
* [pageBreakEnabled](kasclient.kasattachmentlistquestionconfig.md#pagebreakenabled)
* [ATTACHMENT_LIST_TYPE](kasclient.kasattachmentlistquestionconfig.md#attachment_list_type)
* [DEFAULT_CAMERA_FILTER_MODE](kasclient.kasattachmentlistquestionconfig.md#default_camera_filter_mode)
* [IMAGE_SOURCE_KEY](kasclient.kasattachmentlistquestionconfig.md#image_source_key)
* [MAX_IMAGE_COUNT_KEY](kasclient.kasattachmentlistquestionconfig.md#max_image_count_key)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasattachmentlistquestionconfig.md#tojson)
* [fromJSON](kasclient.kasattachmentlistquestionconfig.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a>attachmentListType

**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic

___
<a id="defaultcamerafiltermode"></a>

###  <a name="defaultcamerafiltermode"></a>defaultCameraFilterMode

**● defaultCameraFilterMode**: *[CameraFilterMode](../enums/kasclient.camerafiltermode.md)* = CameraFilterMode. photo

___
<a id="imagesource"></a>

###  <a name="imagesource"></a>imageSource

**● imageSource**: *[ImagePickerSource](../enums/kasclient.imagepickersource.md)* = ImagePickerSource. All

___
<a id="maximagecount"></a>

###  <a name="maximagecount"></a>maxImageCount

**● maxImageCount**: *`number`* = 10

___
<a id="pagebreakenabled"></a>

###  <a name="pagebreakenabled"></a>pageBreakEnabled

**● pageBreakEnabled**: *`boolean`* = true

___
<a id="attachment_list_type"></a>

### <a name="static-attachmentlisttype"></a>`<Static>`ATTACHMENT_LIST_TYPE

**● ATTACHMENT_LIST_TYPE**: *`string`* = "alt"

___
<a id="default_camera_filter_mode"></a>

### <a name="static-defaultcamerafiltermode"></a>`<Static>`DEFAULT_CAMERA_FILTER_MODE

**● DEFAULT_CAMERA_FILTER_MODE**: *`string`* = "DCFM"

___
<a id="image_source_key"></a>

### <a name="static-imagesourcekey"></a>`<Static>`IMAGE_SOURCE_KEY

**● IMAGE_SOURCE_KEY**: *`string`* = "is"

___
<a id="max_image_count_key"></a>

### <a name="static-maximagecountkey"></a>`<Static>`MAX_IMAGE_COUNT_KEY

**● MAX_IMAGE_COUNT_KEY**: *`string`* = "MIC"

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASAttachmentListQuestionConfig](kasclient.kasattachmentlistquestionconfig.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASAttachmentListQuestionConfig](kasclient.kasattachmentlistquestionconfig.md)

___

