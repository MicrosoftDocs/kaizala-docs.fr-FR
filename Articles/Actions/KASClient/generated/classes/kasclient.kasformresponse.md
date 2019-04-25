<span data-ttu-id="3fc53-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="3fc53-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span></span>

# <a name="class-kasformresponse"></a><span data-ttu-id="3fc53-102">Classe: KASFormResponse</span><span class="sxs-lookup"><span data-stu-id="3fc53-102">Class: KASFormResponse</span></span>

## <a name="hierarchy"></a><span data-ttu-id="3fc53-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="3fc53-103">Hierarchy</span></span>

<span data-ttu-id="3fc53-104">**KASFormResponse**</span><span class="sxs-lookup"><span data-stu-id="3fc53-104">**KASFormResponse**</span></span>

## <a name="index"></a><span data-ttu-id="3fc53-105">Index</span><span class="sxs-lookup"><span data-stu-id="3fc53-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3fc53-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3fc53-106">Properties</span></span>

* [<span data-ttu-id="3fc53-107">groupId</span><span class="sxs-lookup"><span data-stu-id="3fc53-107">groupId</span></span>](kasclient.kasformresponse.md#groupid)
* [<span data-ttu-id="3fc53-108">groupName</span><span class="sxs-lookup"><span data-stu-id="3fc53-108">groupName</span></span>](kasclient.kasformresponse.md#groupname)
* [<span data-ttu-id="3fc53-109">id</span><span class="sxs-lookup"><span data-stu-id="3fc53-109">id</span></span>](kasclient.kasformresponse.md#id)
* [<span data-ttu-id="3fc53-110">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="3fc53-110">questionToAnswerMap</span></span>](kasclient.kasformresponse.md#questiontoanswermap)
* [<span data-ttu-id="3fc53-111">responderId</span><span class="sxs-lookup"><span data-stu-id="3fc53-111">responderId</span></span>](kasclient.kasformresponse.md#responderid)
* [<span data-ttu-id="3fc53-112">responderName</span><span class="sxs-lookup"><span data-stu-id="3fc53-112">responderName</span></span>](kasclient.kasformresponse.md#respondername)
* [<span data-ttu-id="3fc53-113">sendStatus</span><span class="sxs-lookup"><span data-stu-id="3fc53-113">sendStatus</span></span>](kasclient.kasformresponse.md#sendstatus)
* [<span data-ttu-id="3fc53-114">sendTime</span><span class="sxs-lookup"><span data-stu-id="3fc53-114">sendTime</span></span>](kasclient.kasformresponse.md#sendtime)
* [<span data-ttu-id="3fc53-115">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="3fc53-115">serverToLocalAssetUrlMap</span></span>](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a><span data-ttu-id="3fc53-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3fc53-116">Methods</span></span>

* [<span data-ttu-id="3fc53-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="3fc53-117">fromJSON</span></span>](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="3fc53-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3fc53-118">Properties</span></span>

<a id="groupid"></a>

###  <a name="groupid"></a><span data-ttu-id="3fc53-119">groupId</span><span class="sxs-lookup"><span data-stu-id="3fc53-119">groupId</span></span>

<span data-ttu-id="3fc53-120">**● GroupID**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="3fc53-120">**● groupId**: *`string`* = ""</span></span>

<span data-ttu-id="3fc53-121">ID de groupe</span><span class="sxs-lookup"><span data-stu-id="3fc53-121">Group id</span></span>

___

<a id="groupname"></a>

###  <a name="groupname"></a><span data-ttu-id="3fc53-122">groupName</span><span class="sxs-lookup"><span data-stu-id="3fc53-122">groupName</span></span>

<span data-ttu-id="3fc53-123">**● GroupName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="3fc53-123">**● groupName**: *`string`* = ""</span></span>

<span data-ttu-id="3fc53-124">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="3fc53-124">Group Name</span></span>

___

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="3fc53-125">id</span><span class="sxs-lookup"><span data-stu-id="3fc53-125">id</span></span>

<span data-ttu-id="3fc53-126">**● ID**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="3fc53-126">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="3fc53-127">Un ID de réponse unique, requis en cas de mise à jour d'une réponse existante</span><span class="sxs-lookup"><span data-stu-id="3fc53-127">A unique response id, required in case of updating an existing response</span></span>

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a><span data-ttu-id="3fc53-128">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="3fc53-128">questionToAnswerMap</span></span>

<span data-ttu-id="3fc53-129">**● questionToAnswerMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="3fc53-129">**● questionToAnswerMap**: *`object`*</span></span>

<span data-ttu-id="3fc53-130">Une carte de l'ID de question pour répondre à Dictionary<QuestionId: Number, Answer: string></span><span class="sxs-lookup"><span data-stu-id="3fc53-130">A map of question id to answer Dictionary<QuestionId: number, Answer: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="3fc53-131">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="3fc53-131">Type declaration</span></span>

___

<a id="responderid"></a>

###  <a name="responderid"></a><span data-ttu-id="3fc53-132">responderId</span><span class="sxs-lookup"><span data-stu-id="3fc53-132">responderId</span></span>

<span data-ttu-id="3fc53-133">**● responderId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="3fc53-133">**● responderId**: *`string`* = ""</span></span>

<span data-ttu-id="3fc53-134">ID du répondeur</span><span class="sxs-lookup"><span data-stu-id="3fc53-134">Responder id</span></span>

___

<a id="respondername"></a>

###  <a name="respondername"></a><span data-ttu-id="3fc53-135">responderName</span><span class="sxs-lookup"><span data-stu-id="3fc53-135">responderName</span></span>

<span data-ttu-id="3fc53-136">**● responderName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="3fc53-136">**● responderName**: *`string`* = ""</span></span>

<span data-ttu-id="3fc53-137">Nom du répondeur</span><span class="sxs-lookup"><span data-stu-id="3fc53-137">Responder name</span></span>

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a><span data-ttu-id="3fc53-138">sendStatus</span><span class="sxs-lookup"><span data-stu-id="3fc53-138">sendStatus</span></span>

<span data-ttu-id="3fc53-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus. Unknown</span><span class="sxs-lookup"><span data-stu-id="3fc53-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* =  KASFormMessageSendStatus.Unknown</span></span>

<span data-ttu-id="3fc53-140">État de l'envoi du message de réponse</span><span class="sxs-lookup"><span data-stu-id="3fc53-140">Response message send status</span></span>

___

<a id="sendtime"></a>

###  <a name="sendtime"></a><span data-ttu-id="3fc53-141">sendTime</span><span class="sxs-lookup"><span data-stu-id="3fc53-141">sendTime</span></span>

<span data-ttu-id="3fc53-142">**● sendTime**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="3fc53-142">**● sendTime**: *`number`* = 0</span></span>

<span data-ttu-id="3fc53-143">Heure d'envoi de la réponse</span><span class="sxs-lookup"><span data-stu-id="3fc53-143">Response send time</span></span>

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a><span data-ttu-id="3fc53-144">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="3fc53-144">serverToLocalAssetUrlMap</span></span>

<span data-ttu-id="3fc53-145">**● serverToLocalAssetUrlMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="3fc53-145">**● serverToLocalAssetUrlMap**: *`object`*</span></span>

<span data-ttu-id="3fc53-146">Une carte pour l'localUrl de toutes les pièces jointes d'image à une réponse Dictionary<ServerUrl: chaîne, LocalUrl: string></span><span class="sxs-lookup"><span data-stu-id="3fc53-146">A map for serverUrl against localUrl of all the image attachments to a response Dictionary<ServerUrl: string, LocalUrl: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="3fc53-147">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="3fc53-147">Type declaration</span></span>

___

## <a name="methods"></a><span data-ttu-id="3fc53-148">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3fc53-148">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="3fc53-149">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="3fc53-149">`<Static>` fromJSON</span></span>

<span data-ttu-id="3fc53-150">▸ **fromJSON**(objet: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="3fc53-150">▸ **fromJSON**(object: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span></span>

<span data-ttu-id="3fc53-151">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="3fc53-151">**Parameters:**</span></span>

| <span data-ttu-id="3fc53-152">Nom</span><span class="sxs-lookup"><span data-stu-id="3fc53-152">Name</span></span> | <span data-ttu-id="3fc53-153">Type</span><span class="sxs-lookup"><span data-stu-id="3fc53-153">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="3fc53-154">objet</span><span class="sxs-lookup"><span data-stu-id="3fc53-154">object</span></span> | `any` |

<span data-ttu-id="3fc53-155">**Renvoie:** [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="3fc53-155">**Returns:** [KASFormResponse](kasclient.kasformresponse.md)</span></span>

___

