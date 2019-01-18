---
ms.openlocfilehash: e2ff630472614067d27e76e75b42a4845fd08534
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727896"
---
<span data-ttu-id="e3388-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="e3388-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span></span>

# <a name="class-kasformsummaryforgroup"></a><span data-ttu-id="e3388-102">Classe : KASFormSummaryForGroup</span><span class="sxs-lookup"><span data-stu-id="e3388-102">Class: KASFormSummaryForGroup</span></span>

## <a name="hierarchy"></a><span data-ttu-id="e3388-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e3388-103">Hierarchy</span></span>

<span data-ttu-id="e3388-104">**KASFormSummaryForGroup**</span><span class="sxs-lookup"><span data-stu-id="e3388-104">**KASFormSummaryForGroup**</span></span>

## <a name="index"></a><span data-ttu-id="e3388-105">Index</span><span class="sxs-lookup"><span data-stu-id="e3388-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="e3388-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3388-106">Properties</span></span>

* [<span data-ttu-id="e3388-107">curseur</span><span class="sxs-lookup"><span data-stu-id="e3388-107">cursor</span></span>](kasclient.kasformsummaryforgroup.md#cursor)
* [<span data-ttu-id="e3388-108">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="e3388-108">directMemberResponses</span></span>](kasclient.kasformsummaryforgroup.md#directmemberresponses)
* [<span data-ttu-id="e3388-109">responderCount</span><span class="sxs-lookup"><span data-stu-id="e3388-109">responderCount</span></span>](kasclient.kasformsummaryforgroup.md#respondercount)
* [<span data-ttu-id="e3388-110">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="e3388-110">subgroupSummary</span></span>](kasclient.kasformsummaryforgroup.md#subgroupsummary)
* [<span data-ttu-id="e3388-111">targetCount</span><span class="sxs-lookup"><span data-stu-id="e3388-111">targetCount</span></span>](kasclient.kasformsummaryforgroup.md#targetcount)
### <a name="methods"></a><span data-ttu-id="e3388-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e3388-112">Methods</span></span>

* [<span data-ttu-id="e3388-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="e3388-113">fromJSON</span></span>](kasclient.kasformsummaryforgroup.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="e3388-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3388-114">Properties</span></span>

<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="e3388-115">curseur</span><span class="sxs-lookup"><span data-stu-id="e3388-115">cursor</span></span>

<span data-ttu-id="e3388-116">**Curseur ●**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="e3388-116">**● cursor**: *`string`* = ""</span></span>

___

<a id="directmemberresponses"></a>

###  <a name="directmemberresponses"></a><span data-ttu-id="e3388-117">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="e3388-117">directMemberResponses</span></span>

<span data-ttu-id="e3388-118">**● directMemberResponses**: \* `KASActionInstanceResponse`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="e3388-118">**● directMemberResponses**: *`KASActionInstanceResponse`[]* =  []</span></span>

<span data-ttu-id="e3388-119">Exemple pour le groupe {« c » : « 125955414 », « rdc » : 3, « r » : \[ {« id » : « 5a1d8f15-79b8-4cd5-a497-a5caff979b74 », « n » : « ABC », « supprimer » : « 0a228aee-c5c0-4dc5-bca0-42a634474e2b@1 », « r » : {« 0 » : « Jbbl », « 1 » : « 1540980866017 », « 2 » : « {« lt » : 0, « lg » : 0, « acc » : 0, « n » : « ty «, » » : 0} »}}, {« id » : « 41e589cf-ad48-46b9-9290-786bf64cd599 », « n » : « SRK », « supprimer » : « 13dfa760-df77-4c88-a9f6-f34a76136439@1 », « r » : {« 0 » : « Gnuk », « 1 » : « 1540981299094 », « 2 » : « {« lt » : 0, « lg » : 0, « acc » : 0, « n » : » ty «, » » : 0} »}} \], « sgs » : { » 0c6207fc-39ce-4b74-b420-db2d52f2cd08@1 « : {« n » : null, « rdc » : 1, « tc » : 6}}, « tc » : 6}</span><span class="sxs-lookup"><span data-stu-id="e3388-119">Sample summary for group { "c": "125955414", "rdc": 3, "rs": \[ { "id": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "rid": "0a228aee-c5c0-4dc5-bca0-42a634474e2b@1", "rs": { "0": "Jbbl", "1": "1540980866017", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } }, { "id": "41e589cf-ad48-46b9-9290-786bf64cd599", "n": "SRK", "rid": "13dfa760-df77-4c88-a9f6-f34a76136439@1", "rs": { "0": "Gnuk", "1": "1540981299094", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } } \], "sgs": { "0c6207fc-39ce-4b74-b420-db2d52f2cd08@1": { "n": null, "rdc": 1, "tc": 6 } }, "tc": 6 }</span></span>

___

<a id="respondercount"></a>

###  <a name="respondercount"></a><span data-ttu-id="e3388-120">responderCount</span><span class="sxs-lookup"><span data-stu-id="e3388-120">responderCount</span></span>

<span data-ttu-id="e3388-121">**● responderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="e3388-121">**● responderCount**: *`number`* = 0</span></span>

___

<a id="subgroupsummary"></a>

###  <a name="subgroupsummary"></a><span data-ttu-id="e3388-122">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="e3388-122">subgroupSummary</span></span>

<span data-ttu-id="e3388-123">**● subgroupSummary**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="e3388-123">**● subgroupSummary**: *`object`*</span></span>

#### <a name="type-declaration"></a><span data-ttu-id="e3388-124">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="e3388-124">Type declaration</span></span>

___

<a id="targetcount"></a>

###  <a name="targetcount"></a><span data-ttu-id="e3388-125">targetCount</span><span class="sxs-lookup"><span data-stu-id="e3388-125">targetCount</span></span>

<span data-ttu-id="e3388-126">**● targetCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="e3388-126">**● targetCount**: *`number`* = 0</span></span>

___

## <a name="methods"></a><span data-ttu-id="e3388-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e3388-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="e3388-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="e3388-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="e3388-129">▸ **fromJSON**(objet : *`any`*) : [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="e3388-129">▸ **fromJSON**(object: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

<span data-ttu-id="e3388-130">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="e3388-130">**Parameters:**</span></span>

| <span data-ttu-id="e3388-131">Nom</span><span class="sxs-lookup"><span data-stu-id="e3388-131">Name</span></span> | <span data-ttu-id="e3388-132">Type</span><span class="sxs-lookup"><span data-stu-id="e3388-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="e3388-133">objet</span><span class="sxs-lookup"><span data-stu-id="e3388-133">object</span></span> | `any` |

<span data-ttu-id="e3388-134">**Renvoie :** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="e3388-134">**Returns:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

___

