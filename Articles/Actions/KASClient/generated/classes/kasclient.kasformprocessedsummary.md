[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)

# <a name="class-kasformprocessedsummary"></a>Classe: KASFormProcessedSummary

## <a name="hierarchy"></a>Hierarchy

**KASFormProcessedSummary**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [JSON](kasclient.kasformprocessedsummary.md#json)
* [nonRespondersInConversation](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [résultats](kasclient.kasformprocessedsummary.md#results)
* [targetResponderCount](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [totalResponseCount](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a>nonRespondersInConversation

**● nonRespondersInConversation**: * `string`[]* = []

Nombre de réponses dans la conversation

___

<a id="results"></a>

###  <a name="results"></a>results

**● résultats**:*`object`*

Résultat agrégé pour les questions agrégées Dictionary<QuestionId: Number, result: KASQuestionResult>
#### <a name="type-declaration"></a>Déclaration de type

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● targetResponderCount**: *`number`* = 0

Combien de fois dans la conversation ont été affectées pour répondre à ce formulaire

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● totalResponseCount**: *`number`* = 0

Le nombre total de réponses reçues pour le formulaire, en considérant plusieurs réponses d'une personne

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

___

