<span data-ttu-id="cc118-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="cc118-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)</span></span>

# <a name="class-kasquestion"></a><span data-ttu-id="cc118-102">Classe: KASQuestion</span><span class="sxs-lookup"><span data-stu-id="cc118-102">Class: KASQuestion</span></span>

## <a name="hierarchy"></a><span data-ttu-id="cc118-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="cc118-103">Hierarchy</span></span>

<span data-ttu-id="cc118-104">**KASQuestion**</span><span class="sxs-lookup"><span data-stu-id="cc118-104">**KASQuestion**</span></span>

## <a name="index"></a><span data-ttu-id="cc118-105">Index</span><span class="sxs-lookup"><span data-stu-id="cc118-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="cc118-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc118-106">Properties</span></span>

* [<span data-ttu-id="cc118-107">attachmentsList</span><span class="sxs-lookup"><span data-stu-id="cc118-107">attachmentsList</span></span>](kasclient.kasquestion.md#attachmentslist)
* [<span data-ttu-id="cc118-108">configurer</span><span class="sxs-lookup"><span data-stu-id="cc118-108">config</span></span>](kasclient.kasquestion.md#config)
* [<span data-ttu-id="cc118-109">displayType</span><span class="sxs-lookup"><span data-stu-id="cc118-109">displayType</span></span>](kasclient.kasquestion.md#displaytype)
* [<span data-ttu-id="cc118-110">id</span><span class="sxs-lookup"><span data-stu-id="cc118-110">id</span></span>](kasclient.kasquestion.md#id)
* [<span data-ttu-id="cc118-111">isEditable</span><span class="sxs-lookup"><span data-stu-id="cc118-111">isEditable</span></span>](kasclient.kasquestion.md#iseditable)
* [<span data-ttu-id="cc118-112">isExcludedFromReporting</span><span class="sxs-lookup"><span data-stu-id="cc118-112">isExcludedFromReporting</span></span>](kasclient.kasquestion.md#isexcludedfromreporting)
* [<span data-ttu-id="cc118-113">isInvisible</span><span class="sxs-lookup"><span data-stu-id="cc118-113">isInvisible</span></span>](kasclient.kasquestion.md#isinvisible)
* [<span data-ttu-id="cc118-114">isResponseOptional</span><span class="sxs-lookup"><span data-stu-id="cc118-114">isResponseOptional</span></span>](kasclient.kasquestion.md#isresponseoptional)
* [<span data-ttu-id="cc118-115">options</span><span class="sxs-lookup"><span data-stu-id="cc118-115">options</span></span>](kasclient.kasquestion.md#options)
* [<span data-ttu-id="cc118-116">questionMetadata</span><span class="sxs-lookup"><span data-stu-id="cc118-116">questionMetadata</span></span>](kasclient.kasquestion.md#questionmetadata)
* [<span data-ttu-id="cc118-117">title</span><span class="sxs-lookup"><span data-stu-id="cc118-117">title</span></span>](kasclient.kasquestion.md#title)
* [<span data-ttu-id="cc118-118">type</span><span class="sxs-lookup"><span data-stu-id="cc118-118">type</span></span>](kasclient.kasquestion.md#type)
* [<span data-ttu-id="cc118-119">valif</span><span class="sxs-lookup"><span data-stu-id="cc118-119">valif</span></span>](kasclient.kasquestion.md#valif)
* [<span data-ttu-id="cc118-120">visif</span><span class="sxs-lookup"><span data-stu-id="cc118-120">visif</span></span>](kasclient.kasquestion.md#visif)
### <a name="methods"></a><span data-ttu-id="cc118-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cc118-121">Methods</span></span>

* [<span data-ttu-id="cc118-122">getAPICompatibleQuestionType</span><span class="sxs-lookup"><span data-stu-id="cc118-122">getAPICompatibleQuestionType</span></span>](kasclient.kasquestion.md#getapicompatiblequestiontype)
* [<span data-ttu-id="cc118-123">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-123">toAPICompatibleJSON</span></span>](kasclient.kasquestion.md#toapicompatiblejson)
* [<span data-ttu-id="cc118-124">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-124">toClientJSON</span></span>](kasclient.kasquestion.md#toclientjson)
* [<span data-ttu-id="cc118-125">toJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-125">toJSON</span></span>](kasclient.kasquestion.md#tojson)
* [<span data-ttu-id="cc118-126">validateResponse</span><span class="sxs-lookup"><span data-stu-id="cc118-126">validateResponse</span></span>](kasclient.kasquestion.md#validateresponse)
* [<span data-ttu-id="cc118-127">fromJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-127">fromJSON</span></span>](kasclient.kasquestion.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="cc118-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc118-128">Properties</span></span>

<a id="attachmentslist"></a>

###  <a name="attachmentslist"></a><span data-ttu-id="cc118-129">attachmentsList</span><span class="sxs-lookup"><span data-stu-id="cc118-129">attachmentsList</span></span>

<span data-ttu-id="cc118-130">**● attachmentsList**: \* [KASAttachment](kasclient.kasattachment.md)[]\* = []</span><span class="sxs-lookup"><span data-stu-id="cc118-130">**● attachmentsList**: *[KASAttachment](kasclient.kasattachment.md)[]* =  []</span></span>

<span data-ttu-id="cc118-131">Attchments d’une question-tableau de KASAttachment</span><span class="sxs-lookup"><span data-stu-id="cc118-131">Attchments of a question - Array of KASAttachment</span></span>

___
<a id="config"></a>

###  <a name="config"></a><span data-ttu-id="cc118-132">configurer</span><span class="sxs-lookup"><span data-stu-id="cc118-132">config</span></span>

<span data-ttu-id="cc118-133">**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = null</span><span class="sxs-lookup"><span data-stu-id="cc118-133">**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* =  null</span></span>

<span data-ttu-id="cc118-134">Configuration/comportement d’une question</span><span class="sxs-lookup"><span data-stu-id="cc118-134">Configuration/behaviour of a question</span></span>

___
<a id="displaytype"></a>

###  <a name="displaytype"></a><span data-ttu-id="cc118-135">displayType</span><span class="sxs-lookup"><span data-stu-id="cc118-135">displayType</span></span>

<span data-ttu-id="cc118-136">**● DisplayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType. None</span><span class="sxs-lookup"><span data-stu-id="cc118-136">**● displayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* =  KASQuestionDisplayType.None</span></span>

<span data-ttu-id="cc118-137">Type d’affichage des options de la question</span><span class="sxs-lookup"><span data-stu-id="cc118-137">Display type of the question's options</span></span>

___
<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="cc118-138">id</span><span class="sxs-lookup"><span data-stu-id="cc118-138">id</span></span>

<span data-ttu-id="cc118-139">**● ID**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="cc118-139">**● id**: *`number`* = 0</span></span>

<span data-ttu-id="cc118-140">Index de la question commençant par 0</span><span class="sxs-lookup"><span data-stu-id="cc118-140">Index of the question, starts with 0</span></span>

___
<a id="iseditable"></a>

###  <a name="iseditable"></a><span data-ttu-id="cc118-141">isEditable</span><span class="sxs-lookup"><span data-stu-id="cc118-141">isEditable</span></span>

<span data-ttu-id="cc118-142">**● IsEditable**: *`boolean`* = true</span><span class="sxs-lookup"><span data-stu-id="cc118-142">**● isEditable**: *`boolean`* = true</span></span>

<span data-ttu-id="cc118-143">Indique si la question peut être modifiée par le répondeur, la valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="cc118-143">Denotes if the question can be edited by the responder, default is true</span></span>

___
<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a><span data-ttu-id="cc118-144">isExcludedFromReporting</span><span class="sxs-lookup"><span data-stu-id="cc118-144">isExcludedFromReporting</span></span>

<span data-ttu-id="cc118-145">**● isExcludedFromReporting**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="cc118-145">**● isExcludedFromReporting**: *`boolean`* = false</span></span>

<span data-ttu-id="cc118-146">Indique si la question sera ignorée de toutes sortes de rapports</span><span class="sxs-lookup"><span data-stu-id="cc118-146">Denotes if the question will be skipped from all sorts of reporting</span></span>

___
<a id="isinvisible"></a>

###  <a name="isinvisible"></a><span data-ttu-id="cc118-147">isInvisible</span><span class="sxs-lookup"><span data-stu-id="cc118-147">isInvisible</span></span>

<span data-ttu-id="cc118-148">**● isInvisible**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="cc118-148">**● isInvisible**: *`boolean`* = false</span></span>

<span data-ttu-id="cc118-149">Indique si la question doit être invisible pour le répondeur, la valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="cc118-149">Denotes if the question should be invisible to the responder, default is false</span></span>

___
<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a><span data-ttu-id="cc118-150">isResponseOptional</span><span class="sxs-lookup"><span data-stu-id="cc118-150">isResponseOptional</span></span>

<span data-ttu-id="cc118-151">**● isResponseOptional**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="cc118-151">**● isResponseOptional**: *`boolean`* = false</span></span>

<span data-ttu-id="cc118-152">Indique s’il est obligatoire de répondre à cette question.</span><span class="sxs-lookup"><span data-stu-id="cc118-152">Denotes if it's mandatory to respond to this question</span></span>

___
<a id="options"></a>

###  <a name="options"></a><span data-ttu-id="cc118-153">options</span><span class="sxs-lookup"><span data-stu-id="cc118-153">options</span></span>

<span data-ttu-id="cc118-154">**● options**: \* [KASQuestionOption](kasclient.kasquestionoption.md)[]\* = []</span><span class="sxs-lookup"><span data-stu-id="cc118-154">**● options**: *[KASQuestionOption](kasclient.kasquestionoption.md)[]* =  []</span></span>

<span data-ttu-id="cc118-155">Liste des options pour la question</span><span class="sxs-lookup"><span data-stu-id="cc118-155">List of options for the question</span></span>

___
<a id="questionmetadata"></a>

###  <a name="questionmetadata"></a><span data-ttu-id="cc118-156">questionMetadata</span><span class="sxs-lookup"><span data-stu-id="cc118-156">questionMetadata</span></span>

<span data-ttu-id="cc118-157">**● questionMetadata**:*`string`*</span><span class="sxs-lookup"><span data-stu-id="cc118-157">**● questionMetadata**: *`string`*</span></span>

___
<a id="title"></a>

###  <a name="title"></a><span data-ttu-id="cc118-158">title</span><span class="sxs-lookup"><span data-stu-id="cc118-158">title</span></span>

<span data-ttu-id="cc118-159">**● titre**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="cc118-159">**● title**: *`string`* = ""</span></span>

<span data-ttu-id="cc118-160">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="cc118-160">Title of the question</span></span>

___
<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="cc118-161">type</span><span class="sxs-lookup"><span data-stu-id="cc118-161">type</span></span>

<span data-ttu-id="cc118-162">**● type**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="cc118-162">**● type**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="cc118-163">Type de la question</span><span class="sxs-lookup"><span data-stu-id="cc118-163">Type of the question</span></span>

___
<a id="valif"></a>

###  <a name="valif"></a><span data-ttu-id="cc118-164">valif</span><span class="sxs-lookup"><span data-stu-id="cc118-164">valif</span></span>

<span data-ttu-id="cc118-165">**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = null</span><span class="sxs-lookup"><span data-stu-id="cc118-165">**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* =  null</span></span>

<span data-ttu-id="cc118-166">Règles de validation d’une question-JSON de règle (s), chaîne d’erreur et chaîne d’aide</span><span class="sxs-lookup"><span data-stu-id="cc118-166">Validation rules of a question - JSON of rule(s), error string and help string</span></span>

___
<a id="visif"></a>

###  <a name="visif"></a><span data-ttu-id="cc118-167">visif</span><span class="sxs-lookup"><span data-stu-id="cc118-167">visif</span></span>

<span data-ttu-id="cc118-168">**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = null</span><span class="sxs-lookup"><span data-stu-id="cc118-168">**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* =  null</span></span>

<span data-ttu-id="cc118-169">Règles de visibilité d’une chaîne de règle de question</span><span class="sxs-lookup"><span data-stu-id="cc118-169">Visibility rules of a question - rule string</span></span>

___

## <a name="methods"></a><span data-ttu-id="cc118-170">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cc118-170">Methods</span></span>

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a><span data-ttu-id="cc118-171">getAPICompatibleQuestionType</span><span class="sxs-lookup"><span data-stu-id="cc118-171">getAPICompatibleQuestionType</span></span>

<span data-ttu-id="cc118-172">▸ **getAPICompatibleQuestionType**(type: *`string`*):`string`</span><span class="sxs-lookup"><span data-stu-id="cc118-172">▸ **getAPICompatibleQuestionType**(type: *`string`*): `string`</span></span>

<span data-ttu-id="cc118-173">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="cc118-173">**Parameters:**</span></span>

| <span data-ttu-id="cc118-174">Nom</span><span class="sxs-lookup"><span data-stu-id="cc118-174">Name</span></span> | <span data-ttu-id="cc118-175">Type</span><span class="sxs-lookup"><span data-stu-id="cc118-175">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="cc118-176">type</span><span class="sxs-lookup"><span data-stu-id="cc118-176">type</span></span> | `string` |

<span data-ttu-id="cc118-177">**Renvoie:**`string`</span><span class="sxs-lookup"><span data-stu-id="cc118-177">**Returns:** `string`</span></span>

___
<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a><span data-ttu-id="cc118-178">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-178">toAPICompatibleJSON</span></span>

<span data-ttu-id="cc118-179">▸ **toAPICompatibleJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-179">▸ **toAPICompatibleJSON**(): `JSON`</span></span>

<span data-ttu-id="cc118-180">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-180">**Returns:** `JSON`</span></span>

___
<a id="toclientjson"></a>

###  <a name="toclientjson"></a><span data-ttu-id="cc118-181">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-181">toClientJSON</span></span>

<span data-ttu-id="cc118-182">▸ **toClientJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-182">▸ **toClientJSON**(): `JSON`</span></span>

<span data-ttu-id="cc118-183">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-183">**Returns:** `JSON`</span></span>

___
<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="cc118-184">toJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-184">toJSON</span></span>

<span data-ttu-id="cc118-185">▸ **toJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-185">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="cc118-186">**Renvoie:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="cc118-186">**Returns:** `JSON`</span></span>

___
<a id="validateresponse"></a>

###  <a name="validateresponse"></a><span data-ttu-id="cc118-187">validateResponse</span><span class="sxs-lookup"><span data-stu-id="cc118-187">validateResponse</span></span>

<span data-ttu-id="cc118-188">▸ **validateResponse**(Response: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span><span class="sxs-lookup"><span data-stu-id="cc118-188">▸ **validateResponse**(response: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span></span>

<span data-ttu-id="cc118-189">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="cc118-189">**Parameters:**</span></span>

| <span data-ttu-id="cc118-190">Nom</span><span class="sxs-lookup"><span data-stu-id="cc118-190">Name</span></span> | <span data-ttu-id="cc118-191">Type</span><span class="sxs-lookup"><span data-stu-id="cc118-191">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="cc118-192">réponse</span><span class="sxs-lookup"><span data-stu-id="cc118-192">response</span></span> | `string` |

<span data-ttu-id="cc118-193">**Renvoie:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span><span class="sxs-lookup"><span data-stu-id="cc118-193">**Returns:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="cc118-194">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="cc118-194">`<Static>` fromJSON</span></span>

<span data-ttu-id="cc118-195">▸ **fromJSON**(objet: *`any`*): [KASQuestion](kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="cc118-195">▸ **fromJSON**(object: *`any`*): [KASQuestion](kasclient.kasquestion.md)</span></span>

<span data-ttu-id="cc118-196">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="cc118-196">**Parameters:**</span></span>

| <span data-ttu-id="cc118-197">Nom</span><span class="sxs-lookup"><span data-stu-id="cc118-197">Name</span></span> | <span data-ttu-id="cc118-198">Type</span><span class="sxs-lookup"><span data-stu-id="cc118-198">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="cc118-199">objet</span><span class="sxs-lookup"><span data-stu-id="cc118-199">object</span></span> | `any` |

<span data-ttu-id="cc118-200">**Renvoie:** [KASQuestion](kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="cc118-200">**Returns:** [KASQuestion](kasclient.kasquestion.md)</span></span>

___

