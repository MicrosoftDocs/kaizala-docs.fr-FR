[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)

# <a name="class-kasformresponsenotificationmodel"></a>Classe: KASFormResponseNotificationModel

## <a name="hierarchy"></a>Hierarchy

**KASFormResponseNotificationModel**

## <a name="index"></a>Index

### <a name="constructors"></a>Constructeurs

* [constructeur](kasclient.kasformresponsenotificationmodel.md#constructor)
### <a name="properties"></a>Propriétés

* [messagePreview](kasclient.kasformresponsenotificationmodel.md#messagepreview)
* [messageTarget](kasclient.kasformresponsenotificationmodel.md#messagetarget)
* [pushTarget](kasclient.kasformresponsenotificationmodel.md#pushtarget)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasformresponsenotificationmodel.md#tojson)
* [fromJson](kasclient.kasformresponsenotificationmodel.md#fromjson)

---

## <a name="constructors"></a>Constructeurs

<a id="constructor"></a>

###  <a name="constructor"></a>constructeur

⊕ **New KASFormResponseNotificationModel**(MessageTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, pushTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, messagePreview?: *`String`*): [ KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| `Default value`messageTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`pushTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`messagePreview | `String` |  null |

**Renvoie:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

## <a name="properties"></a>Propriétés

<a id="messagepreview"></a>

###  <a name="messagepreview"></a>messagePreview

**● messagePreview**: *`String`* = ""

___

<a id="messagetarget"></a>

###  <a name="messagetarget"></a>messageTarget

**● messageTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*

___

<a id="pushtarget"></a>

###  <a name="pushtarget"></a>pushTarget

**● pushTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJson

▸ **fromJson**(objet: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

