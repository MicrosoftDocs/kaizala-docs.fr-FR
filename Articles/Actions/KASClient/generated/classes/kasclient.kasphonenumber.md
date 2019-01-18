---
ms.openlocfilehash: 83bf0eada0674bea5a6cbe1e346a5f6aefac8121
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727904"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASPhoneNumber](../classes/kasclient.kasphonenumber.md)

# <a name="class-kasphonenumber"></a>Classe : KASPhoneNumber

## <a name="hierarchy"></a>Hierarchy

**KASPhoneNumber**

## <a name="index"></a>Index

### <a name="constructors"></a>Constructeurs

* [constructeur](kasclient.kasphonenumber.md#constructor)
### <a name="properties"></a>Propriétés

* [countryPhoneCode](kasclient.kasphonenumber.md#countryphonecode)
* [phoneNumber](kasclient.kasphonenumber.md#phonenumber)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasphonenumber.md#tojson)
* [toString](kasclient.kasphonenumber.md#tostring)
* [fromJSON](kasclient.kasphonenumber.md#fromjson)

---

## <a name="constructors"></a>Constructeurs

<a id="constructor"></a>

###  <a name="constructor"></a>constructeur

⊕ **KASPhoneNumber nouveau**(countryPhoneCode? : *`number`*, phoneNumber? : *`string`*) : [KASPhoneNumber](kasclient.kasphonenumber.md)

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| `Default value`countryPhoneCode | `number` | 0 |
| `Default value`phoneNumber | `string` | &quot;&quot; |

**Renvoie :** [KASPhoneNumber](kasclient.kasphonenumber.md)

___

## <a name="properties"></a>Propriétés

<a id="countryphonecode"></a>

###  <a name="countryphonecode"></a>countryPhoneCode

**● countryPhoneCode**: *`number`* = 0

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a>phoneNumber

**● phoneNumber**: *`string`* = « »

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="tostring"></a>

###  <a name="tostring"></a>toString

▸ **toString**() :`string`

**Renvoie :** `string`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(phoneNumberReponseJSON : *`any`*) : [KASPhoneNumber](kasclient.kasphonenumber.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| phoneNumberReponseJSON | `any` |

**Renvoie :** [KASPhoneNumber](kasclient.kasphonenumber.md)

___

