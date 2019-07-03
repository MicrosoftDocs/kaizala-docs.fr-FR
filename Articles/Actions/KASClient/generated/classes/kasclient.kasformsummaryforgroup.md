<span data-ttu-id="a1adb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a1adb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span></span>

# <a name="class-kasformsummaryforgroup"></a><span data-ttu-id="a1adb-102">Classe: KASFormSummaryForGroup</span><span class="sxs-lookup"><span data-stu-id="a1adb-102">Class: KASFormSummaryForGroup</span></span>

## <a name="hierarchy"></a><span data-ttu-id="a1adb-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a1adb-103">Hierarchy</span></span>

<span data-ttu-id="a1adb-104">**KASFormSummaryForGroup**</span><span class="sxs-lookup"><span data-stu-id="a1adb-104">**KASFormSummaryForGroup**</span></span>

## <a name="index"></a><span data-ttu-id="a1adb-105">Index</span><span class="sxs-lookup"><span data-stu-id="a1adb-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="a1adb-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1adb-106">Properties</span></span>

* [<span data-ttu-id="a1adb-107">curseur</span><span class="sxs-lookup"><span data-stu-id="a1adb-107">cursor</span></span>](kasclient.kasformsummaryforgroup.md#cursor)
* [<span data-ttu-id="a1adb-108">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="a1adb-108">directMemberResponses</span></span>](kasclient.kasformsummaryforgroup.md#directmemberresponses)
* [<span data-ttu-id="a1adb-109">responderCount</span><span class="sxs-lookup"><span data-stu-id="a1adb-109">responderCount</span></span>](kasclient.kasformsummaryforgroup.md#respondercount)
* [<span data-ttu-id="a1adb-110">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="a1adb-110">subgroupSummary</span></span>](kasclient.kasformsummaryforgroup.md#subgroupsummary)
* [<span data-ttu-id="a1adb-111">targetCount</span><span class="sxs-lookup"><span data-stu-id="a1adb-111">targetCount</span></span>](kasclient.kasformsummaryforgroup.md#targetcount)
### <a name="methods"></a><span data-ttu-id="a1adb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a1adb-112">Methods</span></span>

* [<span data-ttu-id="a1adb-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="a1adb-113">fromJSON</span></span>](kasclient.kasformsummaryforgroup.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="a1adb-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1adb-114">Properties</span></span>

<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="a1adb-115">curseur</span><span class="sxs-lookup"><span data-stu-id="a1adb-115">cursor</span></span>

<span data-ttu-id="a1adb-116">**● curseur**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="a1adb-116">**● cursor**: *`string`* = ""</span></span>

___
<a id="directmemberresponses"></a>

###  <a name="directmemberresponses"></a><span data-ttu-id="a1adb-117">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="a1adb-117">directMemberResponses</span></span>

<span data-ttu-id="a1adb-118">**● directMemberResponses**: \* `KASActionInstanceResponse`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="a1adb-118">**● directMemberResponses**: *`KASActionInstanceResponse`[]* =  []</span></span>

<span data-ttu-id="a1adb-119">Exemple de résumé pour le groupe {"c": "125955414", "RDC": 3, «RS \[ »: {"ID": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "RID": "0a228aee-c5c0-4dc5-bca0-42a634474e2b @ 1", "RS": {"0": "Jbbl", "1": "1540980866017", "2": "{" lt ": 0," LG ": 0," ACC " : 0, "n": "", "Ty": 0} "}}, {" ID ":" 41e589cf-Ad48-46b9-9290-786bf64cd599 "," n ":" SRK "," RID ":" 13dfa760-df77-4c88-a9f6-f34a76136439 @ 1 "," RS ": {" 0 ":" Gnuk "," 1 ":" 1540981299094 "," 2 ":" {"lt": 0, "LG": 0, "ACC": "...": "" = "," = 0} "}} \]," SG ": {" 0c6207fc-39CE-4b74-B420-db2d52f2cd08 @ 1 ": {" n ": null," RDC ": 1," TC ": 6}}," TC ": 6}</span><span class="sxs-lookup"><span data-stu-id="a1adb-119">Sample summary for group { "c": "125955414", "rdc": 3, "rs": \[ { "id": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "rid": "0a228aee-c5c0-4dc5-bca0-42a634474e2b@1", "rs": { "0": "Jbbl", "1": "1540980866017", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } }, { "id": "41e589cf-ad48-46b9-9290-786bf64cd599", "n": "SRK", "rid": "13dfa760-df77-4c88-a9f6-f34a76136439@1", "rs": { "0": "Gnuk", "1": "1540981299094", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } } \], "sgs": { "0c6207fc-39ce-4b74-b420-db2d52f2cd08@1": { "n": null, "rdc": 1, "tc": 6 } }, "tc": 6 }</span></span>

___
<a id="respondercount"></a>

###  <a name="respondercount"></a><span data-ttu-id="a1adb-120">responderCount</span><span class="sxs-lookup"><span data-stu-id="a1adb-120">responderCount</span></span>

<span data-ttu-id="a1adb-121">**● responderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a1adb-121">**● responderCount**: *`number`* = 0</span></span>

___
<a id="subgroupsummary"></a>

###  <a name="subgroupsummary"></a><span data-ttu-id="a1adb-122">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="a1adb-122">subgroupSummary</span></span>

<span data-ttu-id="a1adb-123">**● subgroupSummary**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="a1adb-123">**● subgroupSummary**: *`object`*</span></span>

#### <a name="type-declaration"></a><span data-ttu-id="a1adb-124">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="a1adb-124">Type declaration</span></span>

___
<a id="targetcount"></a>

###  <a name="targetcount"></a><span data-ttu-id="a1adb-125">targetCount</span><span class="sxs-lookup"><span data-stu-id="a1adb-125">targetCount</span></span>

<span data-ttu-id="a1adb-126">**● targetCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a1adb-126">**● targetCount**: *`number`* = 0</span></span>

___

## <a name="methods"></a><span data-ttu-id="a1adb-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a1adb-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="a1adb-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="a1adb-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="a1adb-129">▸ **fromJSON**(objet: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a1adb-129">▸ **fromJSON**(object: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

<span data-ttu-id="a1adb-130">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="a1adb-130">**Parameters:**</span></span>

| <span data-ttu-id="a1adb-131">Nom</span><span class="sxs-lookup"><span data-stu-id="a1adb-131">Name</span></span> | <span data-ttu-id="a1adb-132">Type</span><span class="sxs-lookup"><span data-stu-id="a1adb-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="a1adb-133">objet</span><span class="sxs-lookup"><span data-stu-id="a1adb-133">object</span></span> | `any` |

<span data-ttu-id="a1adb-134">**Renvoie:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a1adb-134">**Returns:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

___

