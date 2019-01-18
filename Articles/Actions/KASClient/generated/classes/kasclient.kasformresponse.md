---
ms.openlocfilehash: 84e9530593e8850a0cf354ae2e07c77e0b68db75
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727909"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)

# <a name="class-kasformresponse"></a>Classe : KASFormResponse

## <a name="hierarchy"></a>Hierarchy

**KASFormResponse**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [groupId](kasclient.kasformresponse.md#groupid)
* [groupName](kasclient.kasformresponse.md#groupname)
* [id](kasclient.kasformresponse.md#id)
* [questionToAnswerMap](kasclient.kasformresponse.md#questiontoanswermap)
* [responderId](kasclient.kasformresponse.md#responderid)
* [responderName](kasclient.kasformresponse.md#respondername)
* [sendStatus](kasclient.kasformresponse.md#sendstatus)
* [sendTime](kasclient.kasformresponse.md#sendtime)
* [serverToLocalAssetUrlMap](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="groupid"></a>

###  <a name="groupid"></a>groupId

**● groupId**: *`string`* = « »

Id de groupe

___

<a id="groupname"></a>

###  <a name="groupname"></a>groupName

**● groupName**: *`string`* = « »

Nom du groupe

___

<a id="id"></a>

###  <a name="id"></a>id

**Id ●**: *`string`* = « »

Un id réponse unique, requis en cas de mise à jour d’une réponse existante

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a>questionToAnswerMap

**● questionToAnswerMap**:*`object`*

Un mappage d’id de question pour répondre aux Dictionary<QuestionId : nombre, réponse : string>
#### <a name="type-declaration"></a>Déclaration de type

___

<a id="responderid"></a>

###  <a name="responderid"></a>responderId

**● responderId**: *`string`* = « »

Identificateur de réponse

___

<a id="respondername"></a>

###  <a name="respondername"></a>responderName

**● responderName**: *`string`* = « »

Nom du répondeur

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a>sendStatus

**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus.Unknown

État d’envoyer de message de réponse

___

<a id="sendtime"></a>

###  <a name="sendtime"></a>sendTime

**● sendTime**: *`number`* = 0

Envoyer le temps de réponse

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a>serverToLocalAssetUrlMap

**● serverToLocalAssetUrlMap**:*`object`*

Un mappage pour la propriété serverUrl par rapport à localUrl de toutes les pièces jointes image pour une réponse Dictionary<ServerUrl : chaîne, LocalUrl : string>
#### <a name="type-declaration"></a>Déclaration de type

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASFormResponse](kasclient.kasformresponse.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASFormResponse](kasclient.kasformresponse.md)

___

