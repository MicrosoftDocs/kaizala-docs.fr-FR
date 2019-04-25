[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)

# <a name="class-kasnumericquestionresult"></a>Classe: KASNumericQuestionResult

## <a name="hierarchy"></a>Hierarchy

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASNumericQuestionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [temps](kasclient.kasnumericquestionresult.md#average)
* [questionId](kasclient.kasnumericquestionresult.md#questionid)
* [questionTitle](kasclient.kasnumericquestionresult.md#questiontitle)
* [questionType](kasclient.kasnumericquestionresult.md#questiontype)
* [synthèse](kasclient.kasnumericquestionresult.md#sum)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasnumericquestionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="average"></a>

###  <a name="average"></a>temps

**● moyenne**: *`number`* = 0

___

<a id="questionid"></a>

###  <a name="questionid"></a>questionId

**● questionId**: *`number`* = 0

Index de la question

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = ""

Titre de la question

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questionType

**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Type de la question

___

<a id="sum"></a>

###  <a name="sum"></a>synthèse

**● Sum**: *`number`* = 0

Pour les questions numériques, le résultat agrégé est Sum et la moyenne de toutes les réponses

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

___

