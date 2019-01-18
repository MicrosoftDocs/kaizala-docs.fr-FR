---
ms.openlocfilehash: 1e51f3aa34eb9a0a229cae1d4fd25be002447a1e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727940"
---
<span data-ttu-id="35d47-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span></span>

# <a name="class-kasquestionresult"></a><span data-ttu-id="35d47-102">Classe : KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="35d47-102">Class: KASQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="35d47-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="35d47-103">Hierarchy</span></span>

<span data-ttu-id="35d47-104">**KASQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="35d47-104">**KASQuestionResult**</span></span>

<span data-ttu-id="35d47-105">↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-105">↳  [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span></span>

<span data-ttu-id="35d47-106">↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-106">↳  [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="35d47-107">↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-107">↳  [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

## <a name="index"></a><span data-ttu-id="35d47-108">Index</span><span class="sxs-lookup"><span data-stu-id="35d47-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="35d47-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35d47-109">Properties</span></span>

* [<span data-ttu-id="35d47-110">questionId</span><span class="sxs-lookup"><span data-stu-id="35d47-110">questionId</span></span>](kasclient.kasquestionresult.md#questionid)
* [<span data-ttu-id="35d47-111">questionTitle</span><span class="sxs-lookup"><span data-stu-id="35d47-111">questionTitle</span></span>](kasclient.kasquestionresult.md#questiontitle)
* [<span data-ttu-id="35d47-112">questionType</span><span class="sxs-lookup"><span data-stu-id="35d47-112">questionType</span></span>](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="35d47-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35d47-113">Methods</span></span>

* [<span data-ttu-id="35d47-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="35d47-114">fromJSON</span></span>](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="35d47-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35d47-115">Properties</span></span>

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="35d47-116">questionId</span><span class="sxs-lookup"><span data-stu-id="35d47-116">questionId</span></span>

<span data-ttu-id="35d47-117">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="35d47-117">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="35d47-118">Index de la question</span><span class="sxs-lookup"><span data-stu-id="35d47-118">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="35d47-119">questionTitle</span><span class="sxs-lookup"><span data-stu-id="35d47-119">questionTitle</span></span>

<span data-ttu-id="35d47-120">**● questionTitle**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="35d47-120">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="35d47-121">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="35d47-121">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="35d47-122">questionType</span><span class="sxs-lookup"><span data-stu-id="35d47-122">questionType</span></span>

<span data-ttu-id="35d47-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="35d47-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="35d47-124">Type de la question</span><span class="sxs-lookup"><span data-stu-id="35d47-124">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="35d47-125">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35d47-125">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="35d47-126">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="35d47-126">`<Static>` fromJSON</span></span>

<span data-ttu-id="35d47-127">▸ **fromJSON**(objet : *`any`*) : [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-127">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="35d47-128">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="35d47-128">**Parameters:**</span></span>

| <span data-ttu-id="35d47-129">Nom</span><span class="sxs-lookup"><span data-stu-id="35d47-129">Name</span></span> | <span data-ttu-id="35d47-130">Type</span><span class="sxs-lookup"><span data-stu-id="35d47-130">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="35d47-131">objet</span><span class="sxs-lookup"><span data-stu-id="35d47-131">object</span></span> | `any` |

<span data-ttu-id="35d47-132">**Renvoie :** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="35d47-132">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

