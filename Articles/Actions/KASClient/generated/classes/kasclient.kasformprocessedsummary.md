---
ms.openlocfilehash: 7d76c2a5eae67bd6c1063b2595561e299f9f9160
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727902"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)

# <a name="class-kasformprocessedsummary"></a>Classe : KASFormProcessedSummary

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

**● json**:*`JSON`*

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a>nonRespondersInConversation

**● nonRespondersInConversation**: * `string`[]* =]

Combien de la conversation n’a pas répondu

___

<a id="results"></a>

###  <a name="results"></a>résultats

**Résultats ●**:*`object`*

Agrégation des résultats pour les questions aggregative Dictionary<QuestionId : nombre, le résultat : KASQuestionResult>
#### <a name="type-declaration"></a>Déclaration de type

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● targetResponderCount**: *`number`* = 0

Combien de la conversation ont été attribués pour répondre à ce formulaire

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● totalResponseCount**: *`number`* = 0

Nombre total de réponses ont été reçus pour le formulaire, en tenant compte des réponses multiples d’une personne

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`JSON`*) : [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie :** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

___

