[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)

# <a name="class-kasoptionresult"></a>Classe: KASOptionResult

## <a name="hierarchy"></a>Hierarchy

**KASOptionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [optionId](kasclient.kasoptionresult.md#optionid)
* [optionTitle](kasclient.kasoptionresult.md#optiontitle)
* [responderToResponseCount](kasclient.kasoptionresult.md#respondertoresponsecount)
* [totalResponsesCount](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="optionid"></a>

###  <a name="optionid"></a>optionId

**● optionId**: *`number`* = 0

Index de l’option

___
<a id="optiontitle"></a>

###  <a name="optiontitle"></a>optionTitle

**● optionTitle**: *`string`* = ""

Titre de l’option

___
<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a>responderToResponseCount

**● responderToResponseCount**:*`object`*

Mappage des ID d’utilisateur par rapport au dictionnaire de nombre de réponses<UserId: String, ResponseCount: Number>
#### <a name="type-declaration"></a>Déclaration de type

___
<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a>totalResponsesCount

**● totalResponsesCount**: *`number`* = 0

Combien d’entre elles ont choisi cette option?

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASOptionResult](kasclient.kasoptionresult.md)

___

