---
ms.openlocfilehash: 1b4a3a6805310a9a0eb7c63701c367d96aa5fe61
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727927"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormAggregatedSummary](../classes/kasclient.kasformaggregatedsummary.md)

# <a name="class-kasformaggregatedsummary"></a>Classe : KASFormAggregatedSummary

## <a name="hierarchy"></a>Hierarchy

**KASFormAggregatedSummary**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [formId](kasclient.kasformaggregatedsummary.md#formid)
* [formStatus](kasclient.kasformaggregatedsummary.md#formstatus)
* [JSON](kasclient.kasformaggregatedsummary.md#json)
* [result](kasclient.kasformaggregatedsummary.md#result)
* [targetResponderCount](kasclient.kasformaggregatedsummary.md#targetrespondercount)
* [totalParticipantsCount](kasclient.kasformaggregatedsummary.md#totalparticipantscount)
* [totalResponseCount](kasclient.kasformaggregatedsummary.md#totalresponsecount)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasformaggregatedsummary.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="formid"></a>

###  <a name="formid"></a>formId

**● formId**: *`string`* = « »

___

<a id="formstatus"></a>

###  <a name="formstatus"></a>formStatus

**● formStatus**: *[FormStatus](../enums/kasclient.formstatus.md)* = FormStatus.Active

___

<a id="json"></a>

###  <a name="json"></a>json

**● json**:*`JSON`*

___

<a id="result"></a>

###  <a name="result"></a>résultat

**Résultat ●**: * `any`[]* =]

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● targetResponderCount**: *`number`* = 0

___

<a id="totalparticipantscount"></a>

###  <a name="totalparticipantscount"></a>totalParticipantsCount

**● totalParticipantsCount**: *`number`* = 0

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● totalResponseCount**: *`number`* = 0

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`JSON`*, questions : *[] [KASQuestion](kasclient.kasquestion.md)*) : [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |
| questions | [KASQuestion](kasclient.kasquestion.md) [] |

**Renvoie :** [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

___

