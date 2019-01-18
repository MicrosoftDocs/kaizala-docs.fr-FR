---
ms.openlocfilehash: cd7a7880b45a68ea4ac977487756c754a2291dd4
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727924"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)

# <a name="class-kasquestion"></a>Classe : KASQuestion

## <a name="hierarchy"></a>Hierarchy

**KASQuestion**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [Options de configuration](kasclient.kasquestion.md#config)
* [displayType](kasclient.kasquestion.md#displaytype)
* [id](kasclient.kasquestion.md#id)
* [isEditable](kasclient.kasquestion.md#iseditable)
* [isExcludedFromReporting](kasclient.kasquestion.md#isexcludedfromreporting)
* [isInvisible](kasclient.kasquestion.md#isinvisible)
* [isResponseOptional](kasclient.kasquestion.md#isresponseoptional)
* [options](kasclient.kasquestion.md#options)
* [title](kasclient.kasquestion.md#title)
* [type](kasclient.kasquestion.md#type)
* [valif](kasclient.kasquestion.md#valif)
* [visif](kasclient.kasquestion.md#visif)
### <a name="methods"></a>Méthodes

* [getAPICompatibleQuestionType](kasclient.kasquestion.md#getapicompatiblequestiontype)
* [toAPICompatibleJSON](kasclient.kasquestion.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasquestion.md#toclientjson)
* [toJSON](kasclient.kasquestion.md#tojson)
* [validateResponse](kasclient.kasquestion.md#validateresponse)
* [fromJSON](kasclient.kasquestion.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="config"></a>

###  <a name="config"></a>Options de configuration

**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = null

Configuration/comportement d’une question

___

<a id="displaytype"></a>

###  <a name="displaytype"></a>displayType

**● displayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType.None

Afficher le type des options de la question

___

<a id="id"></a>

###  <a name="id"></a>id

**Id ●**: *`number`* = 0

Index de la question, commence par 0

___

<a id="iseditable"></a>

###  <a name="iseditable"></a>isEditable

**● isEditable**: *`boolean`* = true

Indique si la question peut être modifiée par le répondeur, la valeur par défaut est true

___

<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a>isExcludedFromReporting

**● isExcludedFromReporting**: *`boolean`* = false

Indique si la question est ignorée dans tous les types de rapports

___

<a id="isinvisible"></a>

###  <a name="isinvisible"></a>isInvisible

**● isInvisible**: *`boolean`* = false

Indique si la question doit être invisible pour le répondeur, la valeur par défaut est false

___

<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a>isResponseOptional

**● isResponseOptional**: *`boolean`* = false

Indique si elle est obligatoire pour répondre à cette question

___

<a id="options"></a>

###  <a name="options"></a>options

**Options ●**: *[] [KASQuestionOption](kasclient.kasquestionoption.md)* =]

Liste d’options pour la question

___

<a id="title"></a>

###  <a name="title"></a>title

**Titre ●**: *`string`* = « »

Titre de la question

___

<a id="type"></a>

###  <a name="type"></a>type

**Type ●**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None

Type de la question

___

<a id="valif"></a>

###  <a name="valif"></a>valif

**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = null

Règles de validation d’une question - JSON de règles, de chaîne d’erreur et de chaîne d’aide

___

<a id="visif"></a>

###  <a name="visif"></a>visif

**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = null

Règles de visibilité d’une question - chaîne de règle

___

## <a name="methods"></a>Méthodes

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a>getAPICompatibleQuestionType

▸ **getAPICompatibleQuestionType**(type : *`string`*) :`string`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| type | `string` |

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

<a id="validateresponse"></a>

###  <a name="validateresponse"></a>validateResponse

▸ **validateResponse**(réponse : *`string`*) : [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| réponse | `string` |

**Renvoie :** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASQuestion](kasclient.kasquestion.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASQuestion](kasclient.kasquestion.md)

___

