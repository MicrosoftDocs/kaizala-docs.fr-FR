[](../README.md) > [KASClient](../modules/kasclient.md) > [KASConversationDetails](../classes/kasclient.kasconversationdetails.md)

# <a name="class-kasconversationdetails"></a>Classe: KASConversationDetails

Définit les détails de la conversation de l’hôte et de la source
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
* [isHostGroupDiscoverable](kasclient.kasconversationdetails.md#ishostgroupdiscoverable)
* [isSourceGroupDiscoverable](kasclient.kasconversationdetails.md#issourcegroupdiscoverable)
* [sourceConversationId](kasclient.kasconversationdetails.md#sourceconversationid)
* [sourceConversationTitle](kasclient.kasconversationdetails.md#sourceconversationtitle)
* [sourceConversationType](kasclient.kasconversationdetails.md#sourceconversationtype)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasconversationdetails.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="currentuserid"></a>

###  <a name="currentuserid"></a>currentUserId

**● currentUserId**: *`string`* = ""

___
<a id="currentuserroleinhostconversation"></a>

###  <a name="currentuserroleinhostconversation"></a>currentUserRoleInHostConversation

**● currentUserRoleInHostConversation**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole. None

___
<a id="hostconversationid"></a>

###  <a name="hostconversationid"></a>hostConversationId

**● hostConversationId**: *`string`* = ""

___
<a id="hostconversationparticipantsmap"></a>

###  <a name="hostconversationparticipantsmap"></a>hostConversationParticipantsMap

**● hostConversationParticipantsMap**:*`object`*

#### <a name="type-declaration"></a>Déclaration de type

___
<a id="hostconversationtitle"></a>

###  <a name="hostconversationtitle"></a>hostConversationTitle

**● hostConversationTitle**: *`string`* = ""

___
<a id="hostconversationtype"></a>

###  <a name="hostconversationtype"></a>hostConversationType

**● hostConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType. None

___
<a id="ishostgroupdiscoverable"></a>

###  <a name="ishostgroupdiscoverable"></a>isHostGroupDiscoverable

**● isHostGroupDiscoverable**: *`boolean`* = false

___
<a id="issourcegroupdiscoverable"></a>

###  <a name="issourcegroupdiscoverable"></a>isSourceGroupDiscoverable

**● isSourceGroupDiscoverable**: *`boolean`* = false

___
<a id="sourceconversationid"></a>

###  <a name="sourceconversationid"></a>sourceConversationId

**● sourceConversationId**: *`string`* = ""

___
<a id="sourceconversationtitle"></a>

###  <a name="sourceconversationtitle"></a>sourceConversationTitle

**● sourceConversationTitle**: *`string`* = ""

___
<a id="sourceconversationtype"></a>

###  <a name="sourceconversationtype"></a>sourceConversationType

**● sourceConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType. None

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASConversationDetails](kasclient.kasconversationdetails.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASConversationDetails](kasclient.kasconversationdetails.md)

___

