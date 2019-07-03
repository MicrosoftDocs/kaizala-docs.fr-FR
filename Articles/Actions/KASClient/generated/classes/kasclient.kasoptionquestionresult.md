[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)

# <a name="class-kasoptionquestionresult"></a>Classe: KASOptionQuestionResult

## <a name="hierarchy"></a>Hierarchy

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASOptionQuestionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [optionResults](kasclient.kasoptionquestionresult.md#optionresults)
* [questionId](kasclient.kasoptionquestionresult.md#questionid)
* [questionTitle](kasclient.kasoptionquestionresult.md#questiontitle)
* [questionType](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a>Méthodes

* [getResultsOrder](kasclient.kasoptionquestionresult.md#getresultsorder)
* [fromJSON](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="optionresults"></a>

###  <a name="optionresults"></a>optionResults

**● optionResults**:*`object`*

Pour SingleSelect/MultiSelect, le résultat sera l’ID d’option et son dictionnaire de nombre<OptionId: nombre, OptionResult: KASOptionResult>
#### <a name="type-declaration"></a>Déclaration de type

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

## <a name="methods"></a>Méthodes

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a>getResultsOrder

▸ **getResultsOrder**(): `number`[]

Obtient tous les ID d’option triés dans le nombre total de réponses (décroissant).

**Renvoie:** `number`[] liste de tous les ID d’option

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

___

