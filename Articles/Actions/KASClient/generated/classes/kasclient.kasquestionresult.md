---
ms.openlocfilehash: 1e51f3aa34eb9a0a229cae1d4fd25be002447a1e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727940"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)

# <a name="class-kasquestionresult"></a>Classe : KASQuestionResult

## <a name="hierarchy"></a>Hierarchy

**KASQuestionResult**

↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)

↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [questionId](kasclient.kasquestionresult.md#questionid)
* [questionTitle](kasclient.kasquestionresult.md#questiontitle)
* [questionType](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="questionid"></a>

###  <a name="questionid"></a>questionId

**● questionId**: *`number`* = 0

Index de la question

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = « »

Titre de la question

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questionType

**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None

Type de la question

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASQuestionResult](kasclient.kasquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASQuestionResult](kasclient.kasquestionresult.md)

___

