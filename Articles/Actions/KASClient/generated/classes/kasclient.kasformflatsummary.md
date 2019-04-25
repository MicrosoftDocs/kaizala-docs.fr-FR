[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)

# <a name="class-kasformflatsummary"></a>Classe: KASFormFlatSummary

## <a name="hierarchy"></a>Hierarchy

**KASFormFlatSummary**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [conversationId](kasclient.kasformflatsummary.md#conversationid)
* [formId](kasclient.kasformflatsummary.md#formid)
* [JSON](kasclient.kasformflatsummary.md#json)
### <a name="methods"></a>Méthodes

* [getAllResponses](kasclient.kasformflatsummary.md#getallresponses)
* [getQuestionResponsesForUserId](kasclient.kasformflatsummary.md#getquestionresponsesforuserid)
* [getRespondedUserIds](kasclient.kasformflatsummary.md#getrespondeduserids)
* [getResponsesForUserId](kasclient.kasformflatsummary.md#getresponsesforuserid)
* [getTotalResponseCount](kasclient.kasformflatsummary.md#gettotalresponsecount)
* [fromJSON](kasclient.kasformflatsummary.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● conversationId**: *`string`* = ""

L'ID de la conversation associée ne doit pas être modifié.

___

<a id="formid"></a>

###  <a name="formid"></a>formId

**● formid**: *`string`* = ""

L'ID du formulaire associé ne doit pas être modifié.

___

<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___

## <a name="methods"></a>Méthodes

<a id="getallresponses"></a>

###  <a name="getallresponses"></a>getAllResponses

▸ **getAllResponses**():`__type`

Obtient toutes les réponses de tous les utilisateurs

**Renvoie:**`__type`

___

<a id="getquestionresponsesforuserid"></a>

###  <a name="getquestionresponsesforuserid"></a>getQuestionResponsesForUserId

▸ **getQuestionResponsesForUserId**(UserID: *`string`*, questionId: *`number`*): `string`[]

Obtient toutes les réponses d'un utilisateur par rapport à une question spécifique.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  ID unique de l'utilisateur |
| questionId | `number` |  ID de la question |

**Renvoie:** `string`[] liste de toutes les réponses fournies par l'utilisateur pour cette question

___

<a id="getrespondeduserids"></a>

###  <a name="getrespondeduserids"></a>getRespondedUserIds

▸ **getRespondedUserIds**(): `string`[]

Obtient tous les ID d'utilisateur qui ont répondu au formulaire.

**Renvoie:** `string`[] liste de tous les ID d'utilisateur ayant répondu

___

<a id="getresponsesforuserid"></a>

###  <a name="getresponsesforuserid"></a>getResponsesForUserId

▸ **getResponsesForUserId**(UserID: *`string`*):`__type`

Obtient toutes les réponses d'un utilisateur à un formulaire.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  ID unique de l'utilisateur |

**Renvoie:** `__type` ID de la question à la liste des réponses

___

<a id="gettotalresponsecount"></a>

###  <a name="gettotalresponsecount"></a>getTotalResponseCount

▸ **getTotalResponseCount**():`number`

Obtient le nombre de réponses de tous les utilisateurs

**Renvoie:** `number` nombre de réponses

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*, isResponseAppended: *`boolean`*): [KASFormFlatSummary](kasclient.kasformflatsummary.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |
| isResponseAppended | `boolean` |

**Renvoie:** [KASFormFlatSummary](kasclient.kasformflatsummary.md)

___

