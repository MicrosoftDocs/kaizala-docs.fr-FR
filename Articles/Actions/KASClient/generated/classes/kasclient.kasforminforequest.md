<span data-ttu-id="b3f27-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)</span><span class="sxs-lookup"><span data-stu-id="b3f27-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)</span></span>

# <a name="class-kasforminforequest"></a><span data-ttu-id="b3f27-102">Classe: KASFormInfoRequest</span><span class="sxs-lookup"><span data-stu-id="b3f27-102">Class: KASFormInfoRequest</span></span>

<span data-ttu-id="b3f27-103">Cela encapsule la demande pour l’API KASClient. Form. fetchFormInfosAsync.</span><span class="sxs-lookup"><span data-stu-id="b3f27-103">This encapsulates the request for KASClient.Form.fetchFormInfosAsync api.</span></span> <span data-ttu-id="b3f27-104">Cette API permet d’extraire des informations d’instance d’action (ou formulaire) pour une action pacakge</span><span class="sxs-lookup"><span data-stu-id="b3f27-104">This api is used to fetch Action instance (or form) infos for an Action pacakge</span></span>
## <a name="hierarchy"></a><span data-ttu-id="b3f27-105">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b3f27-105">Hierarchy</span></span>

<span data-ttu-id="b3f27-106">**KASFormInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="b3f27-106">**KASFormInfoRequest**</span></span>

## <a name="index"></a><span data-ttu-id="b3f27-107">Index</span><span class="sxs-lookup"><span data-stu-id="b3f27-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="b3f27-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3f27-108">Properties</span></span>

* [<span data-ttu-id="b3f27-109">creatorId</span><span class="sxs-lookup"><span data-stu-id="b3f27-109">creatorId</span></span>](kasclient.kasforminforequest.md#creatorid)
* [<span data-ttu-id="b3f27-110">curseur</span><span class="sxs-lookup"><span data-stu-id="b3f27-110">cursor</span></span>](kasclient.kasforminforequest.md#cursor)
* [<span data-ttu-id="b3f27-111">packageId</span><span class="sxs-lookup"><span data-stu-id="b3f27-111">packageId</span></span>](kasclient.kasforminforequest.md#packageid)
* [<span data-ttu-id="b3f27-112">IDÉtendue</span><span class="sxs-lookup"><span data-stu-id="b3f27-112">scopeId</span></span>](kasclient.kasforminforequest.md#scopeid)

---

## <a name="properties"></a><span data-ttu-id="b3f27-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3f27-113">Properties</span></span>

<a id="creatorid"></a>

###  <a name="creatorid"></a><span data-ttu-id="b3f27-114">creatorId</span><span class="sxs-lookup"><span data-stu-id="b3f27-114">creatorId</span></span>

<span data-ttu-id="b3f27-115">**● creatorId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b3f27-115">**● creatorId**: *`string`* = ""</span></span>

<span data-ttu-id="b3f27-116">Instance d’action (ou formulaire) Creator ID-champ facultatif</span><span class="sxs-lookup"><span data-stu-id="b3f27-116">Action instance (or form) creator id - optional field</span></span>

___
<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="b3f27-117">curseur</span><span class="sxs-lookup"><span data-stu-id="b3f27-117">cursor</span></span>

<span data-ttu-id="b3f27-118">**● curseur**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b3f27-118">**● cursor**: *`string`* = ""</span></span>

<span data-ttu-id="b3f27-119">Curseur pour extraire les réponses dans un lot</span><span class="sxs-lookup"><span data-stu-id="b3f27-119">Cursor to fetch responses in batch</span></span>

___
<a id="packageid"></a>

###  <a name="packageid"></a><span data-ttu-id="b3f27-120">packageId</span><span class="sxs-lookup"><span data-stu-id="b3f27-120">packageId</span></span>

<span data-ttu-id="b3f27-121">**● packageId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b3f27-121">**● packageId**: *`string`* = ""</span></span>

<span data-ttu-id="b3f27-122">ID de package d’action dont les instances doivent être extraites</span><span class="sxs-lookup"><span data-stu-id="b3f27-122">Action package id whose instances need to be fetched</span></span>

___
<a id="scopeid"></a>

###  <a name="scopeid"></a><span data-ttu-id="b3f27-123">IDÉtendue</span><span class="sxs-lookup"><span data-stu-id="b3f27-123">scopeId</span></span>

<span data-ttu-id="b3f27-124">**● ScopeId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b3f27-124">**● scopeId**: *`string`* = ""</span></span>

<span data-ttu-id="b3f27-125">ID d’étendue-ID de groupe pour l’étendue unique/de groupe, ID de client pour l’étendue client, ID d’utilisateur pour l’étendue utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3f27-125">Scope id - group id for Single/Group scope, tenant id for Tenant scope, user id for User scope</span></span>

___

