---
ms.openlocfilehash: 2462effb40cd9759a8822cc8dcc09834fcef727b
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727952"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASConversationDetails](../classes/kasclient.kasconversationdetails.md)

# <a name="class-kasconversationdetails"></a>Classe : KASConversationDetails

Définit les détails de l’hôte et la source de conversation
## <a name="hierarchy"></a>Hierarchy

**KASConversationDetails**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [currentUserId](kasclient.kasconversationdetails.md#currentuserid)
* [currentUserRoleInHostConversation](kasclient.kasconversationdetails.md#currentuserroleinhostconversation)
* [hostConversationId](kasclient.kasconversationdetails.md#hostconversationid)
* [hostConversationParticipantsMap](kasclient.kasconversationdetails.md#hostconversationparticipantsmap)
* [hostConversationTitle](kasclient.kasconversationdetails.md#hostconversationtitle)
* [hostConversationType](kasclient.kasconversationdetails.md#hostconversationtype)
* [sourceConversationId](kasclient.kasconversationdetails.md#sourceconversationid)
* [sourceConversationTitle](kasclient.kasconversationdetails.md#sourceconversationtitle)
* [sourceConversationType](kasclient.kasconversationdetails.md#sourceconversationtype)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasconversationdetails.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="currentuserid"></a>

###  <a name="currentuserid"></a>currentUserId

**● currentUserId**: *`string`* = « »

___

<a id="currentuserroleinhostconversation"></a>

###  <a name="currentuserroleinhostconversation"></a>currentUserRoleInHostConversation

**● currentUserRoleInHostConversation**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole.NONE

___

<a id="hostconversationid"></a>

###  <a name="hostconversationid"></a>hostConversationId

**● hostConversationId**: *`string`* = « »

___

<a id="hostconversationparticipantsmap"></a>

###  <a name="hostconversationparticipantsmap"></a>hostConversationParticipantsMap

**● hostConversationParticipantsMap**:*`object`*

#### <a name="type-declaration"></a>Déclaration de type

___

<a id="hostconversationtitle"></a>

###  <a name="hostconversationtitle"></a>hostConversationTitle

**● hostConversationTitle**: *`string`* = « »

___

<a id="hostconversationtype"></a>

###  <a name="hostconversationtype"></a>hostConversationType

**● hostConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType.NONE

___

<a id="sourceconversationid"></a>

###  <a name="sourceconversationid"></a>sourceConversationId

**● sourceConversationId**: *`string`* = « »

___

<a id="sourceconversationtitle"></a>

###  <a name="sourceconversationtitle"></a>sourceConversationTitle

**● sourceConversationTitle**: *`string`* = « »

___

<a id="sourceconversationtype"></a>

###  <a name="sourceconversationtype"></a>sourceConversationType

**● sourceConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType.NONE

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASConversationDetails](kasclient.kasconversationdetails.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASConversationDetails](kasclient.kasconversationdetails.md)

___

