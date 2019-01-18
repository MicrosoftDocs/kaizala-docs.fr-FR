---
ms.openlocfilehash: 6433ecb385d38db201ec8e2733768e9fc095ae8e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727923"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)

# <a name="class-kasformproperty"></a>Classe : KASFormProperty

## <a name="hierarchy"></a>Hierarchy

**KASFormProperty**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [Nom](kasclient.kasformproperty.md#name)
* [type](kasclient.kasformproperty.md#type)
* [value](kasclient.kasformproperty.md#value)
### <a name="methods"></a>Méthodes

* [getAPICompatiblePropertyType](kasclient.kasformproperty.md#getapicompatiblepropertytype)
* [toAPICompatibleJSON](kasclient.kasformproperty.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasformproperty.md#toclientjson)
* [toJSON](kasclient.kasformproperty.md#tojson)
* [fromJSON](kasclient.kasformproperty.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="name"></a>

###  <a name="name"></a>name

**Nom ●**: *`string`* = « »

Nom des métadonnées

___

<a id="type"></a>

###  <a name="type"></a>type

**Type ●**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* = KASFormPropertyType.Text

Type de métadonnées

___

<a id="value"></a>

###  <a name="value"></a>value

**Valeur ●**: *`string`* = « »

Valeur des métadonnées

___

## <a name="methods"></a>Méthodes

<a id="getapicompatiblepropertytype"></a>

###  <a name="getapicompatiblepropertytype"></a>getAPICompatiblePropertyType

▸ **getAPICompatiblePropertyType**(type : *`string`*) :`string`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| type | `string` |

**Renvoie :** `string`

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **toAPICompatibleJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **toClientJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`JSON`*) : [KASFormProperty](kasclient.kasformproperty.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie :** [KASFormProperty](kasclient.kasformproperty.md)

___

