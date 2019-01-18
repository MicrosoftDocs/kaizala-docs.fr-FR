---
ms.openlocfilehash: 84e9530593e8850a0cf354ae2e07c77e0b68db75
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727909"
---
<span data-ttu-id="01e9f-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="01e9f-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span></span>

# <a name="class-kasformresponse"></a><span data-ttu-id="01e9f-102">Classe : KASFormResponse</span><span class="sxs-lookup"><span data-stu-id="01e9f-102">Class: KASFormResponse</span></span>

## <a name="hierarchy"></a><span data-ttu-id="01e9f-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="01e9f-103">Hierarchy</span></span>

<span data-ttu-id="01e9f-104">**KASFormResponse**</span><span class="sxs-lookup"><span data-stu-id="01e9f-104">**KASFormResponse**</span></span>

## <a name="index"></a><span data-ttu-id="01e9f-105">Index</span><span class="sxs-lookup"><span data-stu-id="01e9f-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="01e9f-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01e9f-106">Properties</span></span>

* [<span data-ttu-id="01e9f-107">groupId</span><span class="sxs-lookup"><span data-stu-id="01e9f-107">groupId</span></span>](kasclient.kasformresponse.md#groupid)
* [<span data-ttu-id="01e9f-108">groupName</span><span class="sxs-lookup"><span data-stu-id="01e9f-108">groupName</span></span>](kasclient.kasformresponse.md#groupname)
* [<span data-ttu-id="01e9f-109">id</span><span class="sxs-lookup"><span data-stu-id="01e9f-109">id</span></span>](kasclient.kasformresponse.md#id)
* [<span data-ttu-id="01e9f-110">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="01e9f-110">questionToAnswerMap</span></span>](kasclient.kasformresponse.md#questiontoanswermap)
* [<span data-ttu-id="01e9f-111">responderId</span><span class="sxs-lookup"><span data-stu-id="01e9f-111">responderId</span></span>](kasclient.kasformresponse.md#responderid)
* [<span data-ttu-id="01e9f-112">responderName</span><span class="sxs-lookup"><span data-stu-id="01e9f-112">responderName</span></span>](kasclient.kasformresponse.md#respondername)
* [<span data-ttu-id="01e9f-113">sendStatus</span><span class="sxs-lookup"><span data-stu-id="01e9f-113">sendStatus</span></span>](kasclient.kasformresponse.md#sendstatus)
* [<span data-ttu-id="01e9f-114">sendTime</span><span class="sxs-lookup"><span data-stu-id="01e9f-114">sendTime</span></span>](kasclient.kasformresponse.md#sendtime)
* [<span data-ttu-id="01e9f-115">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="01e9f-115">serverToLocalAssetUrlMap</span></span>](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a><span data-ttu-id="01e9f-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01e9f-116">Methods</span></span>

* [<span data-ttu-id="01e9f-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="01e9f-117">fromJSON</span></span>](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="01e9f-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01e9f-118">Properties</span></span>

<a id="groupid"></a>

###  <a name="groupid"></a><span data-ttu-id="01e9f-119">groupId</span><span class="sxs-lookup"><span data-stu-id="01e9f-119">groupId</span></span>

<span data-ttu-id="01e9f-120">**● groupId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="01e9f-120">**● groupId**: *`string`* = ""</span></span>

<span data-ttu-id="01e9f-121">Id de groupe</span><span class="sxs-lookup"><span data-stu-id="01e9f-121">Group id</span></span>

___

<a id="groupname"></a>

###  <a name="groupname"></a><span data-ttu-id="01e9f-122">groupName</span><span class="sxs-lookup"><span data-stu-id="01e9f-122">groupName</span></span>

<span data-ttu-id="01e9f-123">**● groupName**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="01e9f-123">**● groupName**: *`string`* = ""</span></span>

<span data-ttu-id="01e9f-124">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="01e9f-124">Group Name</span></span>

___

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="01e9f-125">id</span><span class="sxs-lookup"><span data-stu-id="01e9f-125">id</span></span>

<span data-ttu-id="01e9f-126">**Id ●**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="01e9f-126">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="01e9f-127">Un id réponse unique, requis en cas de mise à jour d’une réponse existante</span><span class="sxs-lookup"><span data-stu-id="01e9f-127">A unique response id, required in case of updating an existing response</span></span>

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a><span data-ttu-id="01e9f-128">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="01e9f-128">questionToAnswerMap</span></span>

<span data-ttu-id="01e9f-129">**● questionToAnswerMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="01e9f-129">**● questionToAnswerMap**: *`object`*</span></span>

<span data-ttu-id="01e9f-130">Un mappage d’id de question pour répondre aux Dictionary<QuestionId : nombre, réponse : string></span><span class="sxs-lookup"><span data-stu-id="01e9f-130">A map of question id to answer Dictionary<QuestionId: number, Answer: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="01e9f-131">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="01e9f-131">Type declaration</span></span>

___

<a id="responderid"></a>

###  <a name="responderid"></a><span data-ttu-id="01e9f-132">responderId</span><span class="sxs-lookup"><span data-stu-id="01e9f-132">responderId</span></span>

<span data-ttu-id="01e9f-133">**● responderId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="01e9f-133">**● responderId**: *`string`* = ""</span></span>

<span data-ttu-id="01e9f-134">Identificateur de réponse</span><span class="sxs-lookup"><span data-stu-id="01e9f-134">Responder id</span></span>

___

<a id="respondername"></a>

###  <a name="respondername"></a><span data-ttu-id="01e9f-135">responderName</span><span class="sxs-lookup"><span data-stu-id="01e9f-135">responderName</span></span>

<span data-ttu-id="01e9f-136">**● responderName**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="01e9f-136">**● responderName**: *`string`* = ""</span></span>

<span data-ttu-id="01e9f-137">Nom du répondeur</span><span class="sxs-lookup"><span data-stu-id="01e9f-137">Responder name</span></span>

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a><span data-ttu-id="01e9f-138">sendStatus</span><span class="sxs-lookup"><span data-stu-id="01e9f-138">sendStatus</span></span>

<span data-ttu-id="01e9f-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus.Unknown</span><span class="sxs-lookup"><span data-stu-id="01e9f-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* =  KASFormMessageSendStatus.Unknown</span></span>

<span data-ttu-id="01e9f-140">État d’envoyer de message de réponse</span><span class="sxs-lookup"><span data-stu-id="01e9f-140">Response message send status</span></span>

___

<a id="sendtime"></a>

###  <a name="sendtime"></a><span data-ttu-id="01e9f-141">sendTime</span><span class="sxs-lookup"><span data-stu-id="01e9f-141">sendTime</span></span>

<span data-ttu-id="01e9f-142">**● sendTime**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="01e9f-142">**● sendTime**: *`number`* = 0</span></span>

<span data-ttu-id="01e9f-143">Envoyer le temps de réponse</span><span class="sxs-lookup"><span data-stu-id="01e9f-143">Response send time</span></span>

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a><span data-ttu-id="01e9f-144">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="01e9f-144">serverToLocalAssetUrlMap</span></span>

<span data-ttu-id="01e9f-145">**● serverToLocalAssetUrlMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="01e9f-145">**● serverToLocalAssetUrlMap**: *`object`*</span></span>

<span data-ttu-id="01e9f-146">Un mappage pour la propriété serverUrl par rapport à localUrl de toutes les pièces jointes image pour une réponse Dictionary<ServerUrl : chaîne, LocalUrl : string></span><span class="sxs-lookup"><span data-stu-id="01e9f-146">A map for serverUrl against localUrl of all the image attachments to a response Dictionary<ServerUrl: string, LocalUrl: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="01e9f-147">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="01e9f-147">Type declaration</span></span>

___

## <a name="methods"></a><span data-ttu-id="01e9f-148">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01e9f-148">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="01e9f-149">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="01e9f-149">`<Static>` fromJSON</span></span>

<span data-ttu-id="01e9f-150">▸ **fromJSON**(objet : *`any`*) : [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="01e9f-150">▸ **fromJSON**(object: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span></span>

<span data-ttu-id="01e9f-151">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="01e9f-151">**Parameters:**</span></span>

| <span data-ttu-id="01e9f-152">Nom</span><span class="sxs-lookup"><span data-stu-id="01e9f-152">Name</span></span> | <span data-ttu-id="01e9f-153">Type</span><span class="sxs-lookup"><span data-stu-id="01e9f-153">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="01e9f-154">objet</span><span class="sxs-lookup"><span data-stu-id="01e9f-154">object</span></span> | `any` |

<span data-ttu-id="01e9f-155">**Renvoie :** [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="01e9f-155">**Returns:** [KASFormResponse](kasclient.kasformresponse.md)</span></span>

___

