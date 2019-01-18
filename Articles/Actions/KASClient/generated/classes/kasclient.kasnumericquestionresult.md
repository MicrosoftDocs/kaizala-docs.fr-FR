---
ms.openlocfilehash: 9384cc245b6c5c3d8889e6c9025eae7f31802469
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727943"
---
<span data-ttu-id="57b62-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="57b62-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)</span></span>

# <a name="class-kasnumericquestionresult"></a><span data-ttu-id="57b62-102">Classe : KASNumericQuestionResult</span><span class="sxs-lookup"><span data-stu-id="57b62-102">Class: KASNumericQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="57b62-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="57b62-103">Hierarchy</span></span>

 [<span data-ttu-id="57b62-104">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="57b62-104">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="57b62-105">**↳ KASNumericQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="57b62-105">**↳ KASNumericQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="57b62-106">Index</span><span class="sxs-lookup"><span data-stu-id="57b62-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="57b62-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="57b62-107">Properties</span></span>

* [<span data-ttu-id="57b62-108">moyenne</span><span class="sxs-lookup"><span data-stu-id="57b62-108">average</span></span>](kasclient.kasnumericquestionresult.md#average)
* [<span data-ttu-id="57b62-109">questionId</span><span class="sxs-lookup"><span data-stu-id="57b62-109">questionId</span></span>](kasclient.kasnumericquestionresult.md#questionid)
* [<span data-ttu-id="57b62-110">questionTitle</span><span class="sxs-lookup"><span data-stu-id="57b62-110">questionTitle</span></span>](kasclient.kasnumericquestionresult.md#questiontitle)
* [<span data-ttu-id="57b62-111">questionType</span><span class="sxs-lookup"><span data-stu-id="57b62-111">questionType</span></span>](kasclient.kasnumericquestionresult.md#questiontype)
* [<span data-ttu-id="57b62-112">somme</span><span class="sxs-lookup"><span data-stu-id="57b62-112">sum</span></span>](kasclient.kasnumericquestionresult.md#sum)
### <a name="methods"></a><span data-ttu-id="57b62-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="57b62-113">Methods</span></span>

* [<span data-ttu-id="57b62-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="57b62-114">fromJSON</span></span>](kasclient.kasnumericquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="57b62-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="57b62-115">Properties</span></span>

<a id="average"></a>

###  <a name="average"></a><span data-ttu-id="57b62-116">average</span><span class="sxs-lookup"><span data-stu-id="57b62-116">average</span></span>

<span data-ttu-id="57b62-117">**Moyenne ●**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="57b62-117">**● average**: *`number`* = 0</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="57b62-118">questionId</span><span class="sxs-lookup"><span data-stu-id="57b62-118">questionId</span></span>

<span data-ttu-id="57b62-119">**● questionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="57b62-119">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="57b62-120">Index de la question</span><span class="sxs-lookup"><span data-stu-id="57b62-120">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="57b62-121">questionTitle</span><span class="sxs-lookup"><span data-stu-id="57b62-121">questionTitle</span></span>

<span data-ttu-id="57b62-122">**● questionTitle**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="57b62-122">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="57b62-123">Titre de la question</span><span class="sxs-lookup"><span data-stu-id="57b62-123">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="57b62-124">questionType</span><span class="sxs-lookup"><span data-stu-id="57b62-124">questionType</span></span>

<span data-ttu-id="57b62-125">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="57b62-125">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="57b62-126">Type de la question</span><span class="sxs-lookup"><span data-stu-id="57b62-126">Type of the question</span></span>

___

<a id="sum"></a>

###  <a name="sum"></a><span data-ttu-id="57b62-127">sum</span><span class="sxs-lookup"><span data-stu-id="57b62-127">sum</span></span>

<span data-ttu-id="57b62-128">**Somme ●**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="57b62-128">**● sum**: *`number`* = 0</span></span>

<span data-ttu-id="57b62-129">Pour des questions numériques sera le résultat agrégé somme et moyenne de toutes les réponses</span><span class="sxs-lookup"><span data-stu-id="57b62-129">For Numeric questions the aggregated result will be sum, and average of all the responses</span></span>

___

## <a name="methods"></a><span data-ttu-id="57b62-130">Méthodes</span><span class="sxs-lookup"><span data-stu-id="57b62-130">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="57b62-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="57b62-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="57b62-132">▸ **fromJSON**(objet : *`any`*) : [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="57b62-132">▸ **fromJSON**(object: *`any`*): [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="57b62-133">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="57b62-133">**Parameters:**</span></span>

| <span data-ttu-id="57b62-134">Nom</span><span class="sxs-lookup"><span data-stu-id="57b62-134">Name</span></span> | <span data-ttu-id="57b62-135">Type</span><span class="sxs-lookup"><span data-stu-id="57b62-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="57b62-136">objet</span><span class="sxs-lookup"><span data-stu-id="57b62-136">object</span></span> | `any` |

<span data-ttu-id="57b62-137">**Renvoie :** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="57b62-137">**Returns:** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

___

