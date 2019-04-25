[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)

# <a name="class-kasattachmentlistquestionresult"></a>Classe: KASAttachmentListQuestionResult

Ce modèle contient des données pour chaque réponse à une question de type de liste de pièces jointes.
## <a name="hierarchy"></a>Hierarchy

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASAttachmentListQuestionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [attachmentListType](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [attachmentsResponseJSONStrings](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [questionId](kasclient.kasattachmentlistquestionresult.md#questionid)
* [questionTitle](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [questionType](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [Horodatages](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [userInfo](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a>attachmentListType

**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic

attachmentListType: contient le type de la réponse de liste de pièces jointes

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a>attachmentsResponseJSONStrings

**● attachmentsResponseJSONStrings**: * `string`[]* = []

attachmentsResponseJSONStrings: contient la liste des pièces jointes correspondant à chaque réponse sous la forme d'une chaîne JSON qui est directement disponible dans le questionIdToAnswerMap.

___

<a id="questionid"></a>

###  <a name="questionid"></a>questionId

**● questionId**: *`number`* = 0

Index de la question

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = ""

Titre de la question

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questionType

**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Type de la question

___

<a id="timestamps"></a>

###  <a name="timestamps"></a>Horodatages

**● horodatages**: * `string`[]* = []

timeStamps: contient les horodatages de réponse pour chaque réponse.

___

<a id="userinfo"></a>

###  <a name="userinfo"></a>userInfo

**● UserInfo**: * [KASUser](kasclient.kasuser.md)[]* = []

userInfo: contient des instances de KASUser avec les détails de la personne interrogée pour la réponse particulière, afin que nous puissions afficher le nom et l'image de profil de la personne interrogée.

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASQuestionResult](kasclient.kasquestionresult.md)

___

