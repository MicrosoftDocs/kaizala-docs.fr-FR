---
ms.openlocfilehash: a2550fdcf4a5d37ac751dd188ae3cf1338962e57
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727965"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASForm](../classes/kasclient.kasform.md)

# <a name="class-kasform"></a>Classe : KASForm

## <a name="hierarchy"></a>Hierarchy

**KASForm**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [allowSendReminder](kasclient.kasform.md#allowsendreminder)
* [conversationId](kasclient.kasform.md#conversationid)
* [creatorId](kasclient.kasform.md#creatorid)
* [expiration](kasclient.kasform.md#expiry)
* [id](kasclient.kasform.md#id)
* [é anonyme](kasclient.kasform.md#isanonymous)
* [isGroupLevelAggregationRequired](kasclient.kasform.md#isgrouplevelaggregationrequired)
* [isLocationRequested](kasclient.kasform.md#islocationrequested)
* [isResponseAppended](kasclient.kasform.md#isresponseappended)
* [JSON](kasclient.kasform.md#json)
* [packageId](kasclient.kasform.md#packageid)
* [properties](kasclient.kasform.md#properties)
* [questions](kasclient.kasform.md#questions)
* [reportType](kasclient.kasform.md#reporttype)
* [title](kasclient.kasform.md#title)
* [type](kasclient.kasform.md#type)
* [version](kasclient.kasform.md#version)
* [visibilité](kasclient.kasform.md#visibility)
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

**● allowSendReminder**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility.Sender

Qui peut envoyer le rappel, la valeur par défaut est l’expéditeur

___

<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● conversationId**: *`string`* = « »

Id de conversation associée, ne doit pas être modifié.

___

<a id="creatorid"></a>

###  <a name="creatorid"></a>creatorId

**● creatorId**: *`string`* = « »

Id d’utilisateur qui a créé le formulaire, ne doivent pas être modifiés.

___

<a id="expiry"></a>

###  <a name="expiry"></a>expiration

**Expiration ●**: *`number`* = 0

Délai d’expiration du formulaire

___

<a id="id"></a>

###  <a name="id"></a>id

**Id ●**: *`string`* = « »

Id de formulaire, ne doivent pas être modifiés.

___

<a id="isanonymous"></a>

###  <a name="isanonymous"></a>é anonyme

**É anonyme ●**: *`boolean`* = false

Si le formulaire est anonyme, la valeur par défaut est false

___

<a id="isgrouplevelaggregationrequired"></a>

###  <a name="isgrouplevelaggregationrequired"></a>isGroupLevelAggregationRequired

**● isGroupLevelAggregationRequired**: *`boolean`* = false

Si le serveur doit faire l’agrégation de niveau sous-groupe de résultats pour cette instance d’action

___

<a id="islocationrequested"></a>

###  <a name="islocationrequested"></a>isLocationRequested

**● isLocationRequested**: *`boolean`* = false

Indique si l’emplacement des participants est attachée à la réponse ou non, la valeur par défaut est false

___

<a id="isresponseappended"></a>

###  <a name="isresponseappended"></a>isResponseAppended

**● isResponseAppended**: *`boolean`* = false

Indique si plusieurs réponses provenant d’un utilisateur sont autorisés ou non, la valeur par défaut est false

___

<a id="json"></a>

###  <a name="json"></a>json

**● json**:*`JSON`*

___

<a id="packageid"></a>

###  <a name="packageid"></a>packageId

**● packageId**: *`string`* = « »

Id de la MiniApp de package, ne doit pas être modifié

___

<a id="properties"></a>

###  <a name="properties"></a>properties

**Propriétés ●**: *[] [KASFormProperty](kasclient.kasformproperty.md)* =]

Une liste des métadonnées associées au formulaire

___

<a id="questions"></a>

###  <a name="questions"></a>questions

**Questions ●**: *[] [KASQuestion](kasclient.kasquestion.md)* =]

Toutes les questions associées au formulaire

___

<a id="reporttype"></a>

###  <a name="reporttype"></a>reportType

**● reportType**: *`number`* = 0

Type de rapport d’enquête, par défaut est 0, il convient de tâche de 1

___

<a id="title"></a>

###  <a name="title"></a>title

**Titre ●**: *`string`* = « »

Titre du formulaire

___

<a id="type"></a>

###  <a name="type"></a>type

**Type ●**: *`number`* = 20

Type du formulaire, par défaut est 20, ne doit pas être modifié.

___

<a id="version"></a>

###  <a name="version"></a>version

**Version ●**: *`number`* = 2

Version du formulaire, la valeur par défaut est 2, ne doit pas être modifié.

___

<a id="visibility"></a>

###  <a name="visibility"></a>visibility

**Visibilité ●**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility.All

Qui peut afficher le résumé de l’écran, valeur par défaut est All.

___

## <a name="methods"></a>Méthodes

<a id="getapicompatiblevisibilitytype"></a>

###  <a name="getapicompatiblevisibilitytype"></a>getAPICompatibleVisibilityType

▸ **getAPICompatibleVisibilityType**(visibilityType : *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)*) :`string`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| visibilityType | [KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md) |

**Renvoie :** `string`

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **toAPICompatibleJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **toClientJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**() :`JSON`

**Renvoie :** `JSON`

___

<a id="addresponsenotificationforaddrow"></a>

### <a name="static-addresponsenotificationforaddrow"></a>`<Static>`addResponseNotificationForAddRow

▸ **addResponseNotificationForAddRow**(formulaire : *[KASForm](kasclient.kasform.md)*, notificationSpec : *[KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)*) :`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| formulaire | [KASForm](kasclient.kasform.md) |
| notificationSpec | [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md) |

**Renvoie :** `void`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`JSON`*) : [KASForm](kasclient.kasform.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie :** [KASForm](kasclient.kasform.md)

___

