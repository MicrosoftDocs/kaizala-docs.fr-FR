---
ms.openlocfilehash: 9384cc245b6c5c3d8889e6c9025eae7f31802469
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727943"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)

# <a name="class-kasnumericquestionresult"></a>Classe : KASNumericQuestionResult

## <a name="hierarchy"></a>Hierarchy

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASNumericQuestionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [moyenne](kasclient.kasnumericquestionresult.md#average)
* [questionId](kasclient.kasnumericquestionresult.md#questionid)
* [questionTitle](kasclient.kasnumericquestionresult.md#questiontitle)
* [questionType](kasclient.kasnumericquestionresult.md#questiontype)
* [somme](kasclient.kasnumericquestionresult.md#sum)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasnumericquestionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="average"></a>

###  <a name="average"></a>average

**Moyenne ●**: *`number`* = 0

___

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

<a id="sum"></a>

###  <a name="sum"></a>sum

**Somme ●**: *`number`* = 0

Pour des questions numériques sera le résultat agrégé somme et moyenne de toutes les réponses

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

___

