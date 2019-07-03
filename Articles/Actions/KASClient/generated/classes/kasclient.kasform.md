[](../README.md) > [KASClient](../modules/kasclient.md) > [KASForm](../classes/kasclient.kasform.md)

# <a name="class-kasform"></a>Classe: KASForm

## <a name="hierarchy"></a>Hierarchy

**KASForm**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [allowSendReminder](kasclient.kasform.md#allowsendreminder)
* [canFetchAnonymousShareLink](kasclient.kasform.md#canfetchanonymoussharelink)
* [conversationId](kasclient.kasform.md#conversationid)
* [creatorId](kasclient.kasform.md#creatorid)
* [expiration](kasclient.kasform.md#expiry)
* [id](kasclient.kasform.md#id)
* [isAnonymous](kasclient.kasform.md#isanonymous)
* [isGroupLevelAggregationRequired](kasclient.kasform.md#isgrouplevelaggregationrequired)
* [isLocationRequested](kasclient.kasform.md#islocationrequested)
* [isResponseAppended](kasclient.kasform.md#isresponseappended)
* [JSON](kasclient.kasform.md#json)
* [packageId](kasclient.kasform.md#packageid)
* [packageMinorVersion](kasclient.kasform.md#packageminorversion)
* [properties](kasclient.kasform.md#properties)
* [questions](kasclient.kasform.md#questions)
* [reportType](kasclient.kasform.md#reporttype)
* [title](kasclient.kasform.md#title)
* [type](kasclient.kasform.md#type)
* [version](kasclient.kasform.md#version)
* [excellente](kasclient.kasform.md#visibility)
### <a name="methods"></a>Méthodes

* [getAPICompatibleVisibilityType](kasclient.kasform.md#getapicompatiblevisibilitytype)
* [toAPICompatibleJSON](kasclient.kasform.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasform.md#toclientjson)
* [toJSON](kasclient.kasform.md#tojson)
* [addResponseNotificationForAddRow](kasclient.kasform.md#addresponsenotificationforaddrow)
* [fromJSON](kasclient.kasform.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="allowsendreminder"></a>

###  <a name="allowsendreminder"></a>allowSendReminder

**● allowSendReminder**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. sender

Qui peut envoyer un rappel, la valeur par défaut est sender

___
<a id="canfetchanonymoussharelink"></a>

###  <a name="canfetchanonymoussharelink"></a>canFetchAnonymousShareLink

**● canFetchAnonymousShareLink**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. MembersAndSubscribers

Qui peut extraire le lien de partage de réponse anonyme, la valeur par défaut est tout le monde

___
<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● conversationId**: *`string`* = ""

ID de conversation associé, ne doit pas être modifié

___
<a id="creatorid"></a>

###  <a name="creatorid"></a>creatorId

**● creatorId**: *`string`* = ""

Le nom d’utilisateur qui a créé le formulaire ne doit pas être modifié

___
<a id="expiry"></a>

###  <a name="expiry"></a>expiration

**● expiration**: *`number`* = 0

Date d’expiration du formulaire

___
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

ID de formulaire, ne doit pas être modifié

___
<a id="isanonymous"></a>

###  <a name="isanonymous"></a>isAnonymous

**● isAnonymous**: *`boolean`* = false

Si le formulaire est anonyme, la valeur par défaut est false.

___
<a id="isgrouplevelaggregationrequired"></a>

###  <a name="isgrouplevelaggregationrequired"></a>isGroupLevelAggregationRequired

**● isGroupLevelAggregationRequired**: *`boolean`* = false

Si le serveur doit effectuer une agrégation de niveau sous-groupe sur les résultats pour cette instance d’action

___
<a id="islocationrequested"></a>

###  <a name="islocationrequested"></a>isLocationRequested

**● isLocationRequested**: *`boolean`* = false

Indique si l’emplacement des participants est joint à la réponse ou non, la valeur par défaut est false.

___
<a id="isresponseappended"></a>

###  <a name="isresponseappended"></a>isResponseAppended

**● isResponseAppended**: *`boolean`* = false

Indique si plusieurs réponses d’un utilisateur sont autorisées ou non; la valeur par défaut est false

___
<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___
<a id="packageid"></a>

###  <a name="packageid"></a>packageId

**● packageId**: *`string`* = ""

L’ID de package du MiniApp ne doit pas être modifié.

___
<a id="packageminorversion"></a>

###  <a name="packageminorversion"></a>packageMinorVersion

**● packageMinorVersion**: *`number`* =-1

Version mineure de package

___
<a id="properties"></a>

###  <a name="properties"></a>propriétés

**● Propriétés**: * [KASFormProperty](kasclient.kasformproperty.md)[]* = []

Une liste des métadonnées associées au formulaire

___
<a id="questions"></a>

###  <a name="questions"></a>questions

**● questions**: * [KASQuestion](kasclient.kasquestion.md)[]* = []

Toutes les questions associées au formulaire

___
<a id="reporttype"></a>

###  <a name="reporttype"></a>reportType

**● reportType**: *`number`* = 0

Type de rapport d’enquête, la valeur par défaut est 0, ce qui doit être de 1 pour le travail.

___
<a id="title"></a>

###  <a name="title"></a>title

**● titre**: *`string`* = ""

Titre du formulaire

___
<a id="type"></a>

###  <a name="type"></a>type

**● type**: *`number`* = 20

Type du formulaire, la valeur par défaut est 20, ne doit pas être modifiée.

___
<a id="version"></a>

###  <a name="version"></a>version

**● version**: *`number`* = 2

Version du formulaire, la valeur par défaut est 2, ne doit pas être modifiée.

___
<a id="visibility"></a>

###  <a name="visibility"></a>visibility

**● visibilité**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. All

Qui peut voir le résumé du formulaire, la valeur par défaut est All

___

## <a name="methods"></a>Méthodes

<a id="getapicompatiblevisibilitytype"></a>

###  <a name="getapicompatiblevisibilitytype"></a>getAPICompatibleVisibilityType

▸ **getAPICompatibleVisibilityType**(VisibilityType: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)*):`string`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| visibilityType | [KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md) |

**Renvoie:**`string`

___
<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **toAPICompatibleJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **toClientJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="addresponsenotificationforaddrow"></a>

### <a name="static-addresponsenotificationforaddrow"></a>`<Static>`addResponseNotificationForAddRow

▸ **addResponseNotificationForAddRow**(Form: *[KASForm](kasclient.kasform.md)*, notificationSpec: *[KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)*):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| formulaire | [KASForm](kasclient.kasform.md) |
| notificationSpec | [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md) |

**Renvoie:**`void`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`JSON`*): [KASForm](kasclient.kasform.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie:** [KASForm](kasclient.kasform.md)

___

