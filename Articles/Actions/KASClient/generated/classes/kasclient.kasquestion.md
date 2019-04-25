[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)

# <a name="class-kasquestion"></a>Classe: KASQuestion

## <a name="hierarchy"></a>Hierarchy

**KASQuestion**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [configurer](kasclient.kasquestion.md#config)
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

###  <a name="config"></a>configurer

**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = null

Configuration/comportement d'une question

___

<a id="displaytype"></a>

###  <a name="displaytype"></a>displayType

**● DisplayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType. None

Type d'affichage des options de la question

___

<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`number`* = 0

Index de la question commençant par 0

___

<a id="iseditable"></a>

###  <a name="iseditable"></a>isEditable

**● IsEditable**: *`boolean`* = true

Indique si la question peut être modifiée par le répondeur, la valeur par défaut est true.

___

<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a>isExcludedFromReporting

**● isExcludedFromReporting**: *`boolean`* = false

Indique si la question sera ignorée de toutes sortes de rapports

___

<a id="isinvisible"></a>

###  <a name="isinvisible"></a>isInvisible

**● isInvisible**: *`boolean`* = false

Indique si la question doit être invisible pour le répondeur, la valeur par défaut est false.

___

<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a>isResponseOptional

**● isResponseOptional**: *`boolean`* = false

Indique s'il est obligatoire de répondre à cette question.

___

<a id="options"></a>

###  <a name="options"></a>options

**● options**: * [KASQuestionOption](kasclient.kasquestionoption.md)[]* = []

Liste des options pour la question

___

<a id="title"></a>

###  <a name="title"></a>title

**● titre**: *`string`* = ""

Titre de la question

___

<a id="type"></a>

###  <a name="type"></a>type

**● type**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Type de la question

___

<a id="valif"></a>

###  <a name="valif"></a>valif

**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = null

Règles de validation d'une question-JSON de règle (s), chaîne d'erreur et chaîne d'aide

___

<a id="visif"></a>

###  <a name="visif"></a>visif

**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = null

Règles de visibilité d'une chaîne de règle de question

___

## <a name="methods"></a>Méthodes

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a>getAPICompatibleQuestionType

▸ **getAPICompatibleQuestionType**(type: *`string`*):`string`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| type | `string` |

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

<a id="validateresponse"></a>

###  <a name="validateresponse"></a>validateResponse

▸ **validateResponse**(Response: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| réponse | `string` |

**Renvoie:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`any`*): [KASQuestion](kasclient.kasquestion.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie:** [KASQuestion](kasclient.kasquestion.md)

___

