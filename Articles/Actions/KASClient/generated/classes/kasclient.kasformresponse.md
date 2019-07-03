<span data-ttu-id="20613-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="20613-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span></span>

# <a name="class-kasformresponse"></a><span data-ttu-id="20613-102">Classe: KASFormResponse</span><span class="sxs-lookup"><span data-stu-id="20613-102">Class: KASFormResponse</span></span>

## <a name="hierarchy"></a><span data-ttu-id="20613-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="20613-103">Hierarchy</span></span>

<span data-ttu-id="20613-104">**KASFormResponse**</span><span class="sxs-lookup"><span data-stu-id="20613-104">**KASFormResponse**</span></span>

## <a name="index"></a><span data-ttu-id="20613-105">Index</span><span class="sxs-lookup"><span data-stu-id="20613-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="20613-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20613-106">Properties</span></span>

* [<span data-ttu-id="20613-107">groupId</span><span class="sxs-lookup"><span data-stu-id="20613-107">groupId</span></span>](kasclient.kasformresponse.md#groupid)
* [<span data-ttu-id="20613-108">groupName</span><span class="sxs-lookup"><span data-stu-id="20613-108">groupName</span></span>](kasclient.kasformresponse.md#groupname)
* [<span data-ttu-id="20613-109">id</span><span class="sxs-lookup"><span data-stu-id="20613-109">id</span></span>](kasclient.kasformresponse.md#id)
* [<span data-ttu-id="20613-110">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="20613-110">questionToAnswerMap</span></span>](kasclient.kasformresponse.md#questiontoanswermap)
* [<span data-ttu-id="20613-111">responderId</span><span class="sxs-lookup"><span data-stu-id="20613-111">responderId</span></span>](kasclient.kasformresponse.md#responderid)
* [<span data-ttu-id="20613-112">responderName</span><span class="sxs-lookup"><span data-stu-id="20613-112">responderName</span></span>](kasclient.kasformresponse.md#respondername)
* [<span data-ttu-id="20613-113">sendStatus</span><span class="sxs-lookup"><span data-stu-id="20613-113">sendStatus</span></span>](kasclient.kasformresponse.md#sendstatus)
* [<span data-ttu-id="20613-114">sendTime</span><span class="sxs-lookup"><span data-stu-id="20613-114">sendTime</span></span>](kasclient.kasformresponse.md#sendtime)
* [<span data-ttu-id="20613-115">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="20613-115">serverToLocalAssetUrlMap</span></span>](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a><span data-ttu-id="20613-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20613-116">Methods</span></span>

* [<span data-ttu-id="20613-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="20613-117">fromJSON</span></span>](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="20613-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20613-118">Properties</span></span>

<a id="groupid"></a>

###  <a name="groupid"></a><span data-ttu-id="20613-119">groupId</span><span class="sxs-lookup"><span data-stu-id="20613-119">groupId</span></span>

<span data-ttu-id="20613-120">**● GroupID**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="20613-120">**● groupId**: *`string`* = ""</span></span>

<span data-ttu-id="20613-121">ID de groupe</span><span class="sxs-lookup"><span data-stu-id="20613-121">Group id</span></span>

___
<a id="groupname"></a>

###  <a name="groupname"></a><span data-ttu-id="20613-122">groupName</span><span class="sxs-lookup"><span data-stu-id="20613-122">groupName</span></span>

<span data-ttu-id="20613-123">**● GroupName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="20613-123">**● groupName**: *`string`* = ""</span></span>

<span data-ttu-id="20613-124">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="20613-124">Group Name</span></span>

___
<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="20613-125">id</span><span class="sxs-lookup"><span data-stu-id="20613-125">id</span></span>

<span data-ttu-id="20613-126">**● ID**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="20613-126">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="20613-127">Un ID de réponse unique, requis en cas de mise à jour d’une réponse existante</span><span class="sxs-lookup"><span data-stu-id="20613-127">A unique response id, required in case of updating an existing response</span></span>

___
<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a><span data-ttu-id="20613-128">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="20613-128">questionToAnswerMap</span></span>

<span data-ttu-id="20613-129">**● questionToAnswerMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="20613-129">**● questionToAnswerMap**: *`object`*</span></span>

<span data-ttu-id="20613-130">Une carte de l’ID de question pour le dictionnaire<QuestionId: Number, Answer: String></span><span class="sxs-lookup"><span data-stu-id="20613-130">A map of question id to answer Dictionary<QuestionId: number, Answer: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="20613-131">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="20613-131">Type declaration</span></span>

___
<a id="responderid"></a>

###  <a name="responderid"></a><span data-ttu-id="20613-132">responderId</span><span class="sxs-lookup"><span data-stu-id="20613-132">responderId</span></span>

<span data-ttu-id="20613-133">**● responderId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="20613-133">**● responderId**: *`string`* = ""</span></span>

<span data-ttu-id="20613-134">ID du répondeur</span><span class="sxs-lookup"><span data-stu-id="20613-134">Responder id</span></span>

___
<a id="respondername"></a>

###  <a name="respondername"></a><span data-ttu-id="20613-135">responderName</span><span class="sxs-lookup"><span data-stu-id="20613-135">responderName</span></span>

<span data-ttu-id="20613-136">**● responderName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="20613-136">**● responderName**: *`string`* = ""</span></span>

<span data-ttu-id="20613-137">Nom du répondeur</span><span class="sxs-lookup"><span data-stu-id="20613-137">Responder name</span></span>

___
<a id="sendstatus"></a>

###  <a name="sendstatus"></a><span data-ttu-id="20613-138">sendStatus</span><span class="sxs-lookup"><span data-stu-id="20613-138">sendStatus</span></span>

<span data-ttu-id="20613-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus. Unknown</span><span class="sxs-lookup"><span data-stu-id="20613-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* =  KASFormMessageSendStatus.Unknown</span></span>

<span data-ttu-id="20613-140">État de l’envoi du message de réponse</span><span class="sxs-lookup"><span data-stu-id="20613-140">Response message send status</span></span>

___
<a id="sendtime"></a>

###  <a name="sendtime"></a><span data-ttu-id="20613-141">sendTime</span><span class="sxs-lookup"><span data-stu-id="20613-141">sendTime</span></span>

<span data-ttu-id="20613-142">**● sendTime**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="20613-142">**● sendTime**: *`number`* = 0</span></span>

<span data-ttu-id="20613-143">Heure d’envoi de la réponse</span><span class="sxs-lookup"><span data-stu-id="20613-143">Response send time</span></span>

___
<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a><span data-ttu-id="20613-144">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="20613-144">serverToLocalAssetUrlMap</span></span>

<span data-ttu-id="20613-145">**● serverToLocalAssetUrlMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="20613-145">**● serverToLocalAssetUrlMap**: *`object`*</span></span>

<span data-ttu-id="20613-146">Une carte pour l’localUrl de toutes les pièces jointes d’image à un dictionnaire de réponses<ServerUrl: chaîne, LocalUrl: chaîne></span><span class="sxs-lookup"><span data-stu-id="20613-146">A map for serverUrl against localUrl of all the image attachments to a response Dictionary<ServerUrl: string, LocalUrl: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="20613-147">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="20613-147">Type declaration</span></span>

___

## <a name="methods"></a><span data-ttu-id="20613-148">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20613-148">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="20613-149">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="20613-149">`<Static>` fromJSON</span></span>

<span data-ttu-id="20613-150">▸ **fromJSON**(objet: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="20613-150">▸ **fromJSON**(object: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span></span>

<span data-ttu-id="20613-151">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="20613-151">**Parameters:**</span></span>

| <span data-ttu-id="20613-152">Nom</span><span class="sxs-lookup"><span data-stu-id="20613-152">Name</span></span> | <span data-ttu-id="20613-153">Type</span><span class="sxs-lookup"><span data-stu-id="20613-153">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="20613-154">objet</span><span class="sxs-lookup"><span data-stu-id="20613-154">object</span></span> | `any` |

<span data-ttu-id="20613-155">**Renvoie:** [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="20613-155">**Returns:** [KASFormResponse](kasclient.kasformresponse.md)</span></span>

___

