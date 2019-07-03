[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)

# <a name="class-kaserror"></a>Classe: KASError

## <a name="hierarchy"></a>Hierarchy

**KASError**

## <a name="index"></a>Index

### <a name="constructors"></a>Constructeurs

* [constructeur](kasclient.kaserror.md#constructor)
### <a name="properties"></a>Propriétés

* [description](kasclient.kaserror.md#description)
* [errorCode](kasclient.kaserror.md#errorcode)
### <a name="methods"></a>Méthodes

* [Méthode](kasclient.kaserror.md#tostring)
* [fromErrorString](kasclient.kaserror.md#fromerrorstring)
* [fromString](kasclient.kaserror.md#fromstring)

---

## <a name="constructors"></a>Constructeurs

<a id="constructor"></a>

###  <a name="constructor"></a>constructeur

⊕ **New KASError**(ErrorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, Description: *`string`*): [KASError](kasclient.kaserror.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| errorCode | [KASErrorCode](../enums/kasclient.kaserrorcode.md) |
| description | `string` |

**Renvoie:** [KASError](kasclient.kaserror.md)

___

## <a name="properties"></a>Propriétés

<a id="description"></a>

###  <a name="description"></a>description

**● Description**: *`String`* = ""

___
<a id="errorcode"></a>

###  <a name="errorcode"></a>errorCode

**● ErrorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode. None

___

## <a name="methods"></a>Méthodes

<a id="tostring"></a>

###  <a name="tostring"></a>Méthode

▸ **ToString**():`string`

**Renvoie:**`string`

___
<a id="fromerrorstring"></a>

### <a name="static-fromerrorstring"></a>`<Static>`fromErrorString

▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| stringifyError | `string` |  JSON dictionnaire d’erreurs avec code et description |

**Renvoie:** [KASError](kasclient.kaserror.md) renvoie l’objet KASError créé à partir d’une erreur JSON. Pour la chaîne NULL, NULL est renvoyé.

___
<a id="fromstring"></a>

### <a name="static-fromstring"></a>`<Static>`fromString

▸ **FromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| stringifyError | `string` |  JSON dictionnaire d’erreurs avec code et description |

**Renvoie:** [KASError](kasclient.kaserror.md) renvoie l’objet KASError créé à partir d’une erreur JSON. Pour une chaîne de valeur null, le code d’erreur non null est également renvoyé.

___

