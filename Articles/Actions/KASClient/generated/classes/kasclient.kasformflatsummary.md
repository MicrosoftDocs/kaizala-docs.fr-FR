---
ms.openlocfilehash: 35a77307e603499ebf73881ff861b61cb7d41e76
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727947"
---
<span data-ttu-id="fe09c-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fe09c-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)</span></span>

# <a name="class-kasformflatsummary"></a><span data-ttu-id="fe09c-102">Classe : KASFormFlatSummary</span><span class="sxs-lookup"><span data-stu-id="fe09c-102">Class: KASFormFlatSummary</span></span>

## <a name="hierarchy"></a><span data-ttu-id="fe09c-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fe09c-103">Hierarchy</span></span>

<span data-ttu-id="fe09c-104">**KASFormFlatSummary**</span><span class="sxs-lookup"><span data-stu-id="fe09c-104">**KASFormFlatSummary**</span></span>

## <a name="index"></a><span data-ttu-id="fe09c-105">Index</span><span class="sxs-lookup"><span data-stu-id="fe09c-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="fe09c-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe09c-106">Properties</span></span>

* [<span data-ttu-id="fe09c-107">conversationId</span><span class="sxs-lookup"><span data-stu-id="fe09c-107">conversationId</span></span>](kasclient.kasformflatsummary.md#conversationid)
* [<span data-ttu-id="fe09c-108">formId</span><span class="sxs-lookup"><span data-stu-id="fe09c-108">formId</span></span>](kasclient.kasformflatsummary.md#formid)
* [<span data-ttu-id="fe09c-109">JSON</span><span class="sxs-lookup"><span data-stu-id="fe09c-109">json</span></span>](kasclient.kasformflatsummary.md#json)
### <a name="methods"></a><span data-ttu-id="fe09c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fe09c-110">Methods</span></span>

* [<span data-ttu-id="fe09c-111">getAllResponses</span><span class="sxs-lookup"><span data-stu-id="fe09c-111">getAllResponses</span></span>](kasclient.kasformflatsummary.md#getallresponses)
* [<span data-ttu-id="fe09c-112">getQuestionResponsesForUserId</span><span class="sxs-lookup"><span data-stu-id="fe09c-112">getQuestionResponsesForUserId</span></span>](kasclient.kasformflatsummary.md#getquestionresponsesforuserid)
* [<span data-ttu-id="fe09c-113">getRespondedUserIds</span><span class="sxs-lookup"><span data-stu-id="fe09c-113">getRespondedUserIds</span></span>](kasclient.kasformflatsummary.md#getrespondeduserids)
* [<span data-ttu-id="fe09c-114">getResponsesForUserId</span><span class="sxs-lookup"><span data-stu-id="fe09c-114">getResponsesForUserId</span></span>](kasclient.kasformflatsummary.md#getresponsesforuserid)
* [<span data-ttu-id="fe09c-115">getTotalResponseCount</span><span class="sxs-lookup"><span data-stu-id="fe09c-115">getTotalResponseCount</span></span>](kasclient.kasformflatsummary.md#gettotalresponsecount)
* [<span data-ttu-id="fe09c-116">fromJSON</span><span class="sxs-lookup"><span data-stu-id="fe09c-116">fromJSON</span></span>](kasclient.kasformflatsummary.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="fe09c-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe09c-117">Properties</span></span>

<a id="conversationid"></a>

###  <a name="conversationid"></a><span data-ttu-id="fe09c-118">conversationId</span><span class="sxs-lookup"><span data-stu-id="fe09c-118">conversationId</span></span>

<span data-ttu-id="fe09c-119">**● conversationId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="fe09c-119">**● conversationId**: *`string`* = ""</span></span>

<span data-ttu-id="fe09c-120">L’id de la conversation associée, ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="fe09c-120">The id of the associated conversation, shouldn't be changed</span></span>

___

<a id="formid"></a>

###  <a name="formid"></a><span data-ttu-id="fe09c-121">formId</span><span class="sxs-lookup"><span data-stu-id="fe09c-121">formId</span></span>

<span data-ttu-id="fe09c-122">**● formId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="fe09c-122">**● formId**: *`string`* = ""</span></span>

<span data-ttu-id="fe09c-123">L’id du formulaire associé, ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="fe09c-123">The id of the associated form, shouldn't be changed</span></span>

___

<a id="json"></a>

###  <a name="json"></a><span data-ttu-id="fe09c-124">json</span><span class="sxs-lookup"><span data-stu-id="fe09c-124">json</span></span>

<span data-ttu-id="fe09c-125">**● json**:*`JSON`*</span><span class="sxs-lookup"><span data-stu-id="fe09c-125">**● json**: *`JSON`*</span></span>

___

## <a name="methods"></a><span data-ttu-id="fe09c-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fe09c-126">Methods</span></span>

<a id="getallresponses"></a>

###  <a name="getallresponses"></a><span data-ttu-id="fe09c-127">getAllResponses</span><span class="sxs-lookup"><span data-stu-id="fe09c-127">getAllResponses</span></span>

<span data-ttu-id="fe09c-128">▸ **getAllResponses**() :`__type`</span><span class="sxs-lookup"><span data-stu-id="fe09c-128">▸ **getAllResponses**(): `__type`</span></span>

<span data-ttu-id="fe09c-129">Obtient toutes les réponses de tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="fe09c-129">Gets all the responses of all the users</span></span>

<span data-ttu-id="fe09c-130">**Renvoie :** `__type`</span><span class="sxs-lookup"><span data-stu-id="fe09c-130">**Returns:** `__type`</span></span>

___

<a id="getquestionresponsesforuserid"></a>

###  <a name="getquestionresponsesforuserid"></a><span data-ttu-id="fe09c-131">getQuestionResponsesForUserId</span><span class="sxs-lookup"><span data-stu-id="fe09c-131">getQuestionResponsesForUserId</span></span>

<span data-ttu-id="fe09c-132">▸ **getQuestionResponsesForUserId**(userId : *`string`*, questionId : *`number`*) : `string`]</span><span class="sxs-lookup"><span data-stu-id="fe09c-132">▸ **getQuestionResponsesForUserId**(userId: *`string`*, questionId: *`number`*): `string`[]</span></span>

<span data-ttu-id="fe09c-133">Obtient toutes les réponses d’un utilisateur par rapport à une question spécifique</span><span class="sxs-lookup"><span data-stu-id="fe09c-133">Gets all the responses of a user against a specific question</span></span>

<span data-ttu-id="fe09c-134">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="fe09c-134">**Parameters:**</span></span>

| <span data-ttu-id="fe09c-135">Nom</span><span class="sxs-lookup"><span data-stu-id="fe09c-135">Name</span></span> | <span data-ttu-id="fe09c-136">Type</span><span class="sxs-lookup"><span data-stu-id="fe09c-136">Type</span></span> | <span data-ttu-id="fe09c-137">Description</span><span class="sxs-lookup"><span data-stu-id="fe09c-137">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="fe09c-138">userId</span><span class="sxs-lookup"><span data-stu-id="fe09c-138">userId</span></span> | `string` |  <span data-ttu-id="fe09c-139">l’id unique de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe09c-139">the unique id of the user</span></span> |
| <span data-ttu-id="fe09c-140">questionId</span><span class="sxs-lookup"><span data-stu-id="fe09c-140">questionId</span></span> | `number` |  <span data-ttu-id="fe09c-141">l’id de la question</span><span class="sxs-lookup"><span data-stu-id="fe09c-141">the id of the question</span></span> |

<span data-ttu-id="fe09c-142">**Renvoie :** `string`[] liste de toutes les réponses indiquée par l’utilisateur pour cette question</span><span class="sxs-lookup"><span data-stu-id="fe09c-142">**Returns:** `string`[] list of all answers given by the user for that question</span></span>

___

<a id="getrespondeduserids"></a>

###  <a name="getrespondeduserids"></a><span data-ttu-id="fe09c-143">getRespondedUserIds</span><span class="sxs-lookup"><span data-stu-id="fe09c-143">getRespondedUserIds</span></span>

<span data-ttu-id="fe09c-144">▸ **getRespondedUserIds**() : `string`]</span><span class="sxs-lookup"><span data-stu-id="fe09c-144">▸ **getRespondedUserIds**(): `string`[]</span></span>

<span data-ttu-id="fe09c-145">Obtient tous les ID d’utilisateur qui a répondu à l’écran</span><span class="sxs-lookup"><span data-stu-id="fe09c-145">Gets all the user ids who responded to the form</span></span>

<span data-ttu-id="fe09c-146">**Renvoie :** `string`[] liste de tous les codes de réponse utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe09c-146">**Returns:** `string`[] list of all the responded user ids</span></span>

___

<a id="getresponsesforuserid"></a>

###  <a name="getresponsesforuserid"></a><span data-ttu-id="fe09c-147">getResponsesForUserId</span><span class="sxs-lookup"><span data-stu-id="fe09c-147">getResponsesForUserId</span></span>

<span data-ttu-id="fe09c-148">▸ **getResponsesForUserId**(userId : *`string`*) :`__type`</span><span class="sxs-lookup"><span data-stu-id="fe09c-148">▸ **getResponsesForUserId**(userId: *`string`*): `__type`</span></span>

<span data-ttu-id="fe09c-149">Obtient toutes les réponses d’un utilisateur à un formulaire</span><span class="sxs-lookup"><span data-stu-id="fe09c-149">Gets all the responses of a user to a form</span></span>

<span data-ttu-id="fe09c-150">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="fe09c-150">**Parameters:**</span></span>

| <span data-ttu-id="fe09c-151">Nom</span><span class="sxs-lookup"><span data-stu-id="fe09c-151">Name</span></span> | <span data-ttu-id="fe09c-152">Type</span><span class="sxs-lookup"><span data-stu-id="fe09c-152">Type</span></span> | <span data-ttu-id="fe09c-153">Description</span><span class="sxs-lookup"><span data-stu-id="fe09c-153">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="fe09c-154">userId</span><span class="sxs-lookup"><span data-stu-id="fe09c-154">userId</span></span> | `string` |  <span data-ttu-id="fe09c-155">l’id unique de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe09c-155">the unique id of the user</span></span> |

<span data-ttu-id="fe09c-156">**Renvoie :** `__type` id de question à la liste de réponses</span><span class="sxs-lookup"><span data-stu-id="fe09c-156">**Returns:** `__type` question id to list of answers</span></span>

___

<a id="gettotalresponsecount"></a>

###  <a name="gettotalresponsecount"></a><span data-ttu-id="fe09c-157">getTotalResponseCount</span><span class="sxs-lookup"><span data-stu-id="fe09c-157">getTotalResponseCount</span></span>

<span data-ttu-id="fe09c-158">▸ **getTotalResponseCount**() :`number`</span><span class="sxs-lookup"><span data-stu-id="fe09c-158">▸ **getTotalResponseCount**(): `number`</span></span>

<span data-ttu-id="fe09c-159">Nombre d’Obtient de toutes les réponses à tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="fe09c-159">Gets number of all responses by all users</span></span>

<span data-ttu-id="fe09c-160">**Renvoie :** `number` nombre de toutes les réponses</span><span class="sxs-lookup"><span data-stu-id="fe09c-160">**Returns:** `number` number of all responses</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="fe09c-161">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="fe09c-161">`<Static>` fromJSON</span></span>

<span data-ttu-id="fe09c-162">▸ **fromJSON**(objet : *`any`*, isResponseAppended : *`boolean`*) : [KASFormFlatSummary](kasclient.kasformflatsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fe09c-162">▸ **fromJSON**(object: *`any`*, isResponseAppended: *`boolean`*): [KASFormFlatSummary](kasclient.kasformflatsummary.md)</span></span>

<span data-ttu-id="fe09c-163">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="fe09c-163">**Parameters:**</span></span>

| <span data-ttu-id="fe09c-164">Nom</span><span class="sxs-lookup"><span data-stu-id="fe09c-164">Name</span></span> | <span data-ttu-id="fe09c-165">Type</span><span class="sxs-lookup"><span data-stu-id="fe09c-165">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="fe09c-166">objet</span><span class="sxs-lookup"><span data-stu-id="fe09c-166">object</span></span> | `any` |
| <span data-ttu-id="fe09c-167">isResponseAppended</span><span class="sxs-lookup"><span data-stu-id="fe09c-167">isResponseAppended</span></span> | `boolean` |

<span data-ttu-id="fe09c-168">**Renvoie :** [KASFormFlatSummary](kasclient.kasformflatsummary.md)</span><span class="sxs-lookup"><span data-stu-id="fe09c-168">**Returns:** [KASFormFlatSummary](kasclient.kasformflatsummary.md)</span></span>

___

