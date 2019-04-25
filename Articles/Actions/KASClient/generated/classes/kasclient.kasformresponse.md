[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)

# <a name="class-kasformresponse"></a>Classe: KASFormResponse

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

**● GroupID**: *`string`* = ""

ID de groupe

___

<a id="groupname"></a>

###  <a name="groupname"></a>groupName

**● GroupName**: *`string`* = ""

Nom du groupe

___

<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

Un ID de réponse unique, requis en cas de mise à jour d'une réponse existante

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a>questionToAnswerMap

**● questionToAnswerMap**:*`object`*

Une carte de l'ID de question pour répondre à Dictionary<QuestionId: Number, Answer: string>
#### <a name="type-declaration"></a>Déclaration de type

___

<a id="responderid"></a>

###  <a name="responderid"></a>responderId

**● responderId**: *`string`* = ""

ID du répondeur

___

<a id="respondername"></a>

###  <a name="respondername"></a>responderName

**● responderName**: *`string`* = ""

Nom du répondeur

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a>sendStatus

**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus. Unknown

État de l'envoi du message de réponse

___

<a id="sendtime"></a>

###  <a name="sendtime"></a>sendTime

**● sendTime**: *`number`* = 0

Heure d'envoi de la réponse

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a>serverToLocalAssetUrlMap

**● serverToLocalAssetUrlMap**:*`object`*

Une carte pour l'localUrl de toutes les pièces jointes d'image à une réponse Dictionary<ServerUrl: chaîne, LocalUrl: string>
#### <a name="type-declaration"></a>Déclaration de type

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASFormResponse](kasclient.kasformresponse.md)

___

