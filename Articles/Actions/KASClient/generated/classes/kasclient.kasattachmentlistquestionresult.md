---
ms.openlocfilehash: 84017de85cac36d49be86fe3a7a2aca9bb9b4d34
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727918"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)

# <a name="class-kasattachmentlistquestionresult"></a>Classe : KASAttachmentListQuestionResult

Ce modèle contient des données pour chaque réponse à une question de Type de liste de pièce jointe.
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

**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType.GENERIC

attachmentListType : indique le type de la réponse de la liste des pièces jointes

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a>attachmentsResponseJSONStrings

**● attachmentsResponseJSONStrings**: * `string`[]* =]

attachmentsResponseJSONStrings : contient la liste des pièces jointes correspondant à chaque réponse sous forme de chaîne JSON directement disponible dans le questionIdToAnswerMap.

___

<a id="questionid"></a>

###  <a name="questionid"></a>questionId

**● questionId**: *`number`* = 0

Index de la question

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = « »

Titre de la question

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questionType

**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None

Type de la question

___

<a id="timestamps"></a>

###  <a name="timestamps"></a>Horodatages

**● horodatages**: * `string`[]* =]

Horodatages : contient les horodatages response pour chaque réponse.

___

<a id="userinfo"></a>

###  <a name="userinfo"></a>userInfo

**● userInfo**: *[] [KASUser](kasclient.kasuser.md)* =]

userInfo : contient des instances de KASUser avec des détails de la personne interrogée pour la réponse particulière afin que nous pouvons afficher l’image de nom et le profil de la personne interrogée.

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASQuestionResult](kasclient.kasquestionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASQuestionResult](kasclient.kasquestionresult.md)

___

