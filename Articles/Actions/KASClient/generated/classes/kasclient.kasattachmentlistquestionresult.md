---
ms.openlocfilehash: 84017de85cac36d49be86fe3a7a2aca9bb9b4d34
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727918"
---
<span data-ttu-id="97e5e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="97e5e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span></span>

# <a name="class-kasattachmentlistquestionresult"></a><span data-ttu-id="97e5e-102">Classe : KASAttachmentListQuestionResult</span><span class="sxs-lookup"><span data-stu-id="97e5e-102">Class: KASAttachmentListQuestionResult</span></span>

<span data-ttu-id="97e5e-103">Ce modèle contient des données pour chaque réponse à une question de Type de liste de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="97e5e-103">This model contains data for every response to an Attachment List Type question.</span></span>
## <a name="hierarchy"></a><span data-ttu-id="97e5e-104">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="97e5e-104">Hierarchy</span></span>

 [<span data-ttu-id="97e5e-105">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="97e5e-105">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="97e5e-106">**↳ KASAttachmentListQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="97e5e-106">**↳ KASAttachmentListQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="97e5e-107">Index</span><span class="sxs-lookup"><span data-stu-id="97e5e-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="97e5e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97e5e-108">Properties</span></span>

* [<span data-ttu-id="97e5e-109">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="97e5e-109">attachmentListType</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [<span data-ttu-id="97e5e-110">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="97e5e-110">attachmentsResponseJSONStrings</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [<span data-ttu-id="97e5e-111">questionId</span><span class="sxs-lookup"><span data-stu-id="97e5e-111">questionId</span></span>](kasclient.kasattachmentlistquestionresult.md#questionid)
* [<span data-ttu-id="97e5e-112">questionTitle</span><span class="sxs-lookup"><span data-stu-id="97e5e-112">questionTitle</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [<span data-ttu-id="97e5e-113">questionType</span><span class="sxs-lookup"><span data-stu-id="97e5e-113">questionType</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [<span data-ttu-id="97e5e-114">Horodatages</span><span class="sxs-lookup"><span data-stu-id="97e5e-114">timeStamps</span></span>](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [<span data-ttu-id="97e5e-115">userInfo</span><span class="sxs-lookup"><span data-stu-id="97e5e-115">userInfo</span></span>](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a><span data-ttu-id="97e5e-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97e5e-116">Methods</span></span>

* [<span data-ttu-id="97e5e-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="97e5e-117">fromJSON</span></span>](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="97e5e-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97e5e-118">Properties</span></span>

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a><span data-ttu-id="97e5e-119">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="97e5e-119">attachmentListType</span></span>

<span data-ttu-id="97e5e-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType.GENERIC</span><span class="sxs-lookup"><span data-stu-id="97e5e-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* =  AttachmentListResponseType.GENERIC</span></span>

<span data-ttu-id="97e5e-121">attachmentListType : indique le type de la réponse de la liste des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="97e5e-121">attachmentListType: contains the type of the attachment list response</span></span>

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a><span data-ttu-id="97e5e-122">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="97e5e-122">attachmentsResponseJSONStrings</span></span>

<span data-ttu-id="97e5e-123">**● attachmentsResponseJSONStrings**: \* `string`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="97e5e-123">**● attachmentsResponseJSONStrings**: *`string`[]* =  []</span></span>

<span data-ttu-id="97e5e-124">attachmentsResponseJSONStrings : contient la liste des pièces jointes correspondant à chaque réponse sous forme de chaîne JSON directement disponible dans le questionIdToAnswerMap.</span><span class="sxs-lookup"><span data-stu-id="97e5e-124">attachmentsResponseJSONStrings: contains the list of attachments corresponding to every response as a JSON string which is directly available in the questionIdToAnswerMap.</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="97e5e-125">questionId</span><span class="sxs-lookup"><span data-stu-id="97e5e-125">questionId</span></span>

<span data-ttu-id="97e5e-126">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="97e5e-126">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="97e5e-127">Index de la question</span><span class="sxs-lookup"><span data-stu-id="97e5e-127">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="97e5e-128">questionTitle</span><span class="sxs-lookup"><span data-stu-id="97e5e-128">questionTitle</span></span>

<span data-ttu-id="97e5e-129">**● questionTitle**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="97e5e-129">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="97e5e-130">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="97e5e-130">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="97e5e-131">questionType</span><span class="sxs-lookup"><span data-stu-id="97e5e-131">questionType</span></span>

<span data-ttu-id="97e5e-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="97e5e-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="97e5e-133">Type de la question</span><span class="sxs-lookup"><span data-stu-id="97e5e-133">Type of the question</span></span>

___

<a id="timestamps"></a>

###  <a name="timestamps"></a><span data-ttu-id="97e5e-134">Horodatages</span><span class="sxs-lookup"><span data-stu-id="97e5e-134">timeStamps</span></span>

<span data-ttu-id="97e5e-135">**● horodatages**: \* `string`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="97e5e-135">**● timeStamps**: *`string`[]* =  []</span></span>

<span data-ttu-id="97e5e-136">Horodatages : contient les horodatages response pour chaque réponse.</span><span class="sxs-lookup"><span data-stu-id="97e5e-136">timeStamps: contains the response timestamps for every response.</span></span>

___

<a id="userinfo"></a>

###  <a name="userinfo"></a><span data-ttu-id="97e5e-137">userInfo</span><span class="sxs-lookup"><span data-stu-id="97e5e-137">userInfo</span></span>

<span data-ttu-id="97e5e-138">**● userInfo**: *[] [KASUser](kasclient.kasuser.md)* =]</span><span class="sxs-lookup"><span data-stu-id="97e5e-138">**● userInfo**: *[KASUser](kasclient.kasuser.md)[]* =  []</span></span>

<span data-ttu-id="97e5e-139">userInfo : contient des instances de KASUser avec des détails de la personne interrogée pour la réponse particulière afin que nous pouvons afficher l’image de nom et le profil de la personne interrogée.</span><span class="sxs-lookup"><span data-stu-id="97e5e-139">userInfo: contains instances of KASUser with details for the respondent for the particular response so that we can show the name and profile picture of the respondent.</span></span>

___

## <a name="methods"></a><span data-ttu-id="97e5e-140">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97e5e-140">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="97e5e-141">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="97e5e-141">`<Static>` fromJSON</span></span>

<span data-ttu-id="97e5e-142">▸ **fromJSON**(objet : *`any`*) : [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="97e5e-142">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="97e5e-143">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="97e5e-143">**Parameters:**</span></span>

| <span data-ttu-id="97e5e-144">Nom</span><span class="sxs-lookup"><span data-stu-id="97e5e-144">Name</span></span> | <span data-ttu-id="97e5e-145">Type</span><span class="sxs-lookup"><span data-stu-id="97e5e-145">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="97e5e-146">objet</span><span class="sxs-lookup"><span data-stu-id="97e5e-146">object</span></span> | `any` |

<span data-ttu-id="97e5e-147">**Renvoie :** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="97e5e-147">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

