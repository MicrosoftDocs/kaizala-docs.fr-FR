<span data-ttu-id="6f8a5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6f8a5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span></span>

# <a name="class-kasattachmentlistquestionresult"></a><span data-ttu-id="6f8a5-102">Classe: KASAttachmentListQuestionResult</span><span class="sxs-lookup"><span data-stu-id="6f8a5-102">Class: KASAttachmentListQuestionResult</span></span>

<span data-ttu-id="6f8a5-103">Ce modèle contient des données pour chaque réponse à une question de type de liste de pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-103">This model contains data for every response to an Attachment List Type question.</span></span>
## <a name="hierarchy"></a><span data-ttu-id="6f8a5-104">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6f8a5-104">Hierarchy</span></span>

 [<span data-ttu-id="6f8a5-105">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="6f8a5-105">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="6f8a5-106">**↳ KASAttachmentListQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="6f8a5-106">**↳ KASAttachmentListQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="6f8a5-107">Index</span><span class="sxs-lookup"><span data-stu-id="6f8a5-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="6f8a5-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f8a5-108">Properties</span></span>

* [<span data-ttu-id="6f8a5-109">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="6f8a5-109">attachmentListType</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [<span data-ttu-id="6f8a5-110">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="6f8a5-110">attachmentsResponseJSONStrings</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [<span data-ttu-id="6f8a5-111">questionId</span><span class="sxs-lookup"><span data-stu-id="6f8a5-111">questionId</span></span>](kasclient.kasattachmentlistquestionresult.md#questionid)
* [<span data-ttu-id="6f8a5-112">questionTitle</span><span class="sxs-lookup"><span data-stu-id="6f8a5-112">questionTitle</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [<span data-ttu-id="6f8a5-113">questionType</span><span class="sxs-lookup"><span data-stu-id="6f8a5-113">questionType</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [<span data-ttu-id="6f8a5-114">Horodatages</span><span class="sxs-lookup"><span data-stu-id="6f8a5-114">timeStamps</span></span>](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [<span data-ttu-id="6f8a5-115">userInfo</span><span class="sxs-lookup"><span data-stu-id="6f8a5-115">userInfo</span></span>](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a><span data-ttu-id="6f8a5-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f8a5-116">Methods</span></span>

* [<span data-ttu-id="6f8a5-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="6f8a5-117">fromJSON</span></span>](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="6f8a5-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f8a5-118">Properties</span></span>

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a><span data-ttu-id="6f8a5-119">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="6f8a5-119">attachmentListType</span></span>

<span data-ttu-id="6f8a5-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic</span><span class="sxs-lookup"><span data-stu-id="6f8a5-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* =  AttachmentListResponseType.GENERIC</span></span>

<span data-ttu-id="6f8a5-121">attachmentListType: contient le type de la réponse de liste de pièces jointes</span><span class="sxs-lookup"><span data-stu-id="6f8a5-121">attachmentListType: contains the type of the attachment list response</span></span>

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a><span data-ttu-id="6f8a5-122">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="6f8a5-122">attachmentsResponseJSONStrings</span></span>

<span data-ttu-id="6f8a5-123">**● attachmentsResponseJSONStrings**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="6f8a5-123">**● attachmentsResponseJSONStrings**: *`string`[]* =  []</span></span>

<span data-ttu-id="6f8a5-124">attachmentsResponseJSONStrings: contient la liste des pièces jointes correspondant à chaque réponse sous la forme d'une chaîne JSON qui est directement disponible dans le questionIdToAnswerMap.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-124">attachmentsResponseJSONStrings: contains the list of attachments corresponding to every response as a JSON string which is directly available in the questionIdToAnswerMap.</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="6f8a5-125">questionId</span><span class="sxs-lookup"><span data-stu-id="6f8a5-125">questionId</span></span>

<span data-ttu-id="6f8a5-126">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="6f8a5-126">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="6f8a5-127">Index de la question</span><span class="sxs-lookup"><span data-stu-id="6f8a5-127">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="6f8a5-128">questionTitle</span><span class="sxs-lookup"><span data-stu-id="6f8a5-128">questionTitle</span></span>

<span data-ttu-id="6f8a5-129">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="6f8a5-129">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="6f8a5-130">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="6f8a5-130">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="6f8a5-131">questionType</span><span class="sxs-lookup"><span data-stu-id="6f8a5-131">questionType</span></span>

<span data-ttu-id="6f8a5-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="6f8a5-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="6f8a5-133">Type de la question</span><span class="sxs-lookup"><span data-stu-id="6f8a5-133">Type of the question</span></span>

___

<a id="timestamps"></a>

###  <a name="timestamps"></a><span data-ttu-id="6f8a5-134">Horodatages</span><span class="sxs-lookup"><span data-stu-id="6f8a5-134">timeStamps</span></span>

<span data-ttu-id="6f8a5-135">**● horodatages**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="6f8a5-135">**● timeStamps**: *`string`[]* =  []</span></span>

<span data-ttu-id="6f8a5-136">timeStamps: contient les horodatages de réponse pour chaque réponse.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-136">timeStamps: contains the response timestamps for every response.</span></span>

___

<a id="userinfo"></a>

###  <a name="userinfo"></a><span data-ttu-id="6f8a5-137">userInfo</span><span class="sxs-lookup"><span data-stu-id="6f8a5-137">userInfo</span></span>

<span data-ttu-id="6f8a5-138">**● UserInfo**: \* [KASUser](kasclient.kasuser.md)[]\* = []</span><span class="sxs-lookup"><span data-stu-id="6f8a5-138">**● userInfo**: *[KASUser](kasclient.kasuser.md)[]* =  []</span></span>

<span data-ttu-id="6f8a5-139">userInfo: contient des instances de KASUser avec les détails de la personne interrogée pour la réponse particulière, afin que nous puissions afficher le nom et l'image de profil de la personne interrogée.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-139">userInfo: contains instances of KASUser with details for the respondent for the particular response so that we can show the name and profile picture of the respondent.</span></span>

___

## <a name="methods"></a><span data-ttu-id="6f8a5-140">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f8a5-140">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="6f8a5-141">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="6f8a5-141">`<Static>` fromJSON</span></span>

<span data-ttu-id="6f8a5-142">▸ **fromJSON**(objet: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6f8a5-142">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="6f8a5-143">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="6f8a5-143">**Parameters:**</span></span>

| <span data-ttu-id="6f8a5-144">Nom</span><span class="sxs-lookup"><span data-stu-id="6f8a5-144">Name</span></span> | <span data-ttu-id="6f8a5-145">Type</span><span class="sxs-lookup"><span data-stu-id="6f8a5-145">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="6f8a5-146">objet</span><span class="sxs-lookup"><span data-stu-id="6f8a5-146">object</span></span> | `any` |

<span data-ttu-id="6f8a5-147">**Renvoie:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6f8a5-147">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

