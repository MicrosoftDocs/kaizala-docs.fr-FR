---
ms.openlocfilehash: 35a77307e603499ebf73881ff861b61cb7d41e76
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727947"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)

# <a name="class-kasformflatsummary"></a>Classe : KASFormFlatSummary

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

**● conversationId**: *`string`* = « »

L’id de la conversation associée, ne doit pas être modifié.

___

<a id="formid"></a>

###  <a name="formid"></a>formId

**● formId**: *`string`* = « »

L’id du formulaire associé, ne doit pas être modifié.

___

<a id="json"></a>

###  <a name="json"></a>json

**● json**:*`JSON`*

___

## <a name="methods"></a>Méthodes

<a id="getallresponses"></a>

###  <a name="getallresponses"></a>getAllResponses

▸ **getAllResponses**() :`__type`

Obtient toutes les réponses de tous les utilisateurs

**Renvoie :** `__type`

___

<a id="getquestionresponsesforuserid"></a>

###  <a name="getquestionresponsesforuserid"></a>getQuestionResponsesForUserId

▸ **getQuestionResponsesForUserId**(userId : *`string`*, questionId : *`number`*) : `string`]

Obtient toutes les réponses d’un utilisateur par rapport à une question spécifique

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  l’id unique de l’utilisateur |
| questionId | `number` |  l’id de la question |

**Renvoie :** `string`[] liste de toutes les réponses indiquée par l’utilisateur pour cette question

___

<a id="getrespondeduserids"></a>

###  <a name="getrespondeduserids"></a>getRespondedUserIds

▸ **getRespondedUserIds**() : `string`]

Obtient tous les ID d’utilisateur qui a répondu à l’écran

**Renvoie :** `string`[] liste de tous les codes de réponse utilisateur

___

<a id="getresponsesforuserid"></a>

###  <a name="getresponsesforuserid"></a>getResponsesForUserId

▸ **getResponsesForUserId**(userId : *`string`*) :`__type`

Obtient toutes les réponses d’un utilisateur à un formulaire

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  l’id unique de l’utilisateur |

**Renvoie :** `__type` id de question à la liste de réponses

___

<a id="gettotalresponsecount"></a>

###  <a name="gettotalresponsecount"></a>getTotalResponseCount

▸ **getTotalResponseCount**() :`number`

Nombre d’Obtient de toutes les réponses à tous les utilisateurs

**Renvoie :** `number` nombre de toutes les réponses

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*, isResponseAppended : *`boolean`*) : [KASFormFlatSummary](kasclient.kasformflatsummary.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |
| isResponseAppended | `boolean` |

**Renvoie :** [KASFormFlatSummary](kasclient.kasformflatsummary.md)

___

