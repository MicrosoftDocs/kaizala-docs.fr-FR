---
ms.openlocfilehash: 7d76c2a5eae67bd6c1063b2595561e299f9f9160
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727902"
---
<span data-ttu-id="eb49a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="eb49a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span></span>

# <a name="class-kasformprocessedsummary"></a><span data-ttu-id="eb49a-102">Classe : KASFormProcessedSummary</span><span class="sxs-lookup"><span data-stu-id="eb49a-102">Class: KASFormProcessedSummary</span></span>

## <a name="hierarchy"></a><span data-ttu-id="eb49a-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="eb49a-103">Hierarchy</span></span>

<span data-ttu-id="eb49a-104">**KASFormProcessedSummary**</span><span class="sxs-lookup"><span data-stu-id="eb49a-104">**KASFormProcessedSummary**</span></span>

## <a name="index"></a><span data-ttu-id="eb49a-105">Index</span><span class="sxs-lookup"><span data-stu-id="eb49a-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="eb49a-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb49a-106">Properties</span></span>

* [<span data-ttu-id="eb49a-107">JSON</span><span class="sxs-lookup"><span data-stu-id="eb49a-107">json</span></span>](kasclient.kasformprocessedsummary.md#json)
* [<span data-ttu-id="eb49a-108">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="eb49a-108">nonRespondersInConversation</span></span>](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [<span data-ttu-id="eb49a-109">résultats</span><span class="sxs-lookup"><span data-stu-id="eb49a-109">results</span></span>](kasclient.kasformprocessedsummary.md#results)
* [<span data-ttu-id="eb49a-110">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="eb49a-110">targetResponderCount</span></span>](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [<span data-ttu-id="eb49a-111">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="eb49a-111">totalResponseCount</span></span>](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a><span data-ttu-id="eb49a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eb49a-112">Methods</span></span>

* [<span data-ttu-id="eb49a-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="eb49a-113">fromJSON</span></span>](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="eb49a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb49a-114">Properties</span></span>

<a id="json"></a>

###  <a name="json"></a><span data-ttu-id="eb49a-115">json</span><span class="sxs-lookup"><span data-stu-id="eb49a-115">json</span></span>

<span data-ttu-id="eb49a-116">**● json**:*`JSON`*</span><span class="sxs-lookup"><span data-stu-id="eb49a-116">**● json**: *`JSON`*</span></span>

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a><span data-ttu-id="eb49a-117">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="eb49a-117">nonRespondersInConversation</span></span>

<span data-ttu-id="eb49a-118">**● nonRespondersInConversation**: \* `string`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="eb49a-118">**● nonRespondersInConversation**: *`string`[]* =  []</span></span>

<span data-ttu-id="eb49a-119">Combien de la conversation n’a pas répondu</span><span class="sxs-lookup"><span data-stu-id="eb49a-119">How many in the conversation did not respond</span></span>

___

<a id="results"></a>

###  <a name="results"></a><span data-ttu-id="eb49a-120">résultats</span><span class="sxs-lookup"><span data-stu-id="eb49a-120">results</span></span>

<span data-ttu-id="eb49a-121">**Résultats ●**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="eb49a-121">**● results**: *`object`*</span></span>

<span data-ttu-id="eb49a-122">Agrégation des résultats pour les questions aggregative Dictionary<QuestionId : nombre, le résultat : KASQuestionResult></span><span class="sxs-lookup"><span data-stu-id="eb49a-122">Aggregated result for aggregative questions Dictionary<QuestionId: number, Result: KASQuestionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="eb49a-123">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="eb49a-123">Type declaration</span></span>

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a><span data-ttu-id="eb49a-124">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="eb49a-124">targetResponderCount</span></span>

<span data-ttu-id="eb49a-125">**● targetResponderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="eb49a-125">**● targetResponderCount**: *`number`* = 0</span></span>

<span data-ttu-id="eb49a-126">Combien de la conversation ont été attribués pour répondre à ce formulaire</span><span class="sxs-lookup"><span data-stu-id="eb49a-126">How many in the conversation were assigned to respond to this form</span></span>

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a><span data-ttu-id="eb49a-127">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="eb49a-127">totalResponseCount</span></span>

<span data-ttu-id="eb49a-128">**● totalResponseCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="eb49a-128">**● totalResponseCount**: *`number`* = 0</span></span>

<span data-ttu-id="eb49a-129">Nombre total de réponses ont été reçus pour le formulaire, en tenant compte des réponses multiples d’une personne</span><span class="sxs-lookup"><span data-stu-id="eb49a-129">How many total responses were received for the form, considering multiple responses from one person</span></span>

___

## <a name="methods"></a><span data-ttu-id="eb49a-130">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eb49a-130">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="eb49a-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="eb49a-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="eb49a-132">▸ **fromJSON**(objet : *`JSON`*) : [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="eb49a-132">▸ **fromJSON**(object: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

<span data-ttu-id="eb49a-133">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="eb49a-133">**Parameters:**</span></span>

| <span data-ttu-id="eb49a-134">Nom</span><span class="sxs-lookup"><span data-stu-id="eb49a-134">Name</span></span> | <span data-ttu-id="eb49a-135">Type</span><span class="sxs-lookup"><span data-stu-id="eb49a-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="eb49a-136">objet</span><span class="sxs-lookup"><span data-stu-id="eb49a-136">object</span></span> | `JSON` |

<span data-ttu-id="eb49a-137">**Renvoie :** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="eb49a-137">**Returns:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

___

