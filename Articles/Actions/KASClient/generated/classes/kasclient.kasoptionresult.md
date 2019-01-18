---
ms.openlocfilehash: c52e672a7e3356171388692054fcd1dc3cee5365
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727908"
---
<span data-ttu-id="98fea-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="98fea-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span></span>

# <a name="class-kasoptionresult"></a><span data-ttu-id="98fea-102">Classe : KASOptionResult</span><span class="sxs-lookup"><span data-stu-id="98fea-102">Class: KASOptionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="98fea-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="98fea-103">Hierarchy</span></span>

<span data-ttu-id="98fea-104">**KASOptionResult**</span><span class="sxs-lookup"><span data-stu-id="98fea-104">**KASOptionResult**</span></span>

## <a name="index"></a><span data-ttu-id="98fea-105">Index</span><span class="sxs-lookup"><span data-stu-id="98fea-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="98fea-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98fea-106">Properties</span></span>

* [<span data-ttu-id="98fea-107">Id_option</span><span class="sxs-lookup"><span data-stu-id="98fea-107">optionId</span></span>](kasclient.kasoptionresult.md#optionid)
* [<span data-ttu-id="98fea-108">optionTitle</span><span class="sxs-lookup"><span data-stu-id="98fea-108">optionTitle</span></span>](kasclient.kasoptionresult.md#optiontitle)
* [<span data-ttu-id="98fea-109">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="98fea-109">responderToResponseCount</span></span>](kasclient.kasoptionresult.md#respondertoresponsecount)
* [<span data-ttu-id="98fea-110">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="98fea-110">totalResponsesCount</span></span>](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a><span data-ttu-id="98fea-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98fea-111">Methods</span></span>

* [<span data-ttu-id="98fea-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="98fea-112">fromJSON</span></span>](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="98fea-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98fea-113">Properties</span></span>

<a id="optionid"></a>

###  <a name="optionid"></a><span data-ttu-id="98fea-114">Id_option</span><span class="sxs-lookup"><span data-stu-id="98fea-114">optionId</span></span>

<span data-ttu-id="98fea-115">**● Id_option**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="98fea-115">**● optionId**: *`number`* = 0</span></span>

<span data-ttu-id="98fea-116">Index de l’option</span><span class="sxs-lookup"><span data-stu-id="98fea-116">Index of the option</span></span>

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a><span data-ttu-id="98fea-117">optionTitle</span><span class="sxs-lookup"><span data-stu-id="98fea-117">optionTitle</span></span>

<span data-ttu-id="98fea-118">**● optionTitle**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="98fea-118">**● optionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="98fea-119">Titre de l’option</span><span class="sxs-lookup"><span data-stu-id="98fea-119">Title of the option</span></span>

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a><span data-ttu-id="98fea-120">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="98fea-120">responderToResponseCount</span></span>

<span data-ttu-id="98fea-121">**● responderToResponseCount**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="98fea-121">**● responderToResponseCount**: *`object`*</span></span>

<span data-ttu-id="98fea-122">Un mappage de l’ID d’utilisateur par rapport à leur nombre de réponse Dictionary<UserId : chaîne, ResponseCount : number></span><span class="sxs-lookup"><span data-stu-id="98fea-122">A map of user ids against their response count Dictionary<UserId: string, ResponseCount: number></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="98fea-123">Déclaration de type</span><span class="sxs-lookup"><span data-stu-id="98fea-123">Type declaration</span></span>

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a><span data-ttu-id="98fea-124">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="98fea-124">totalResponsesCount</span></span>

<span data-ttu-id="98fea-125">**● totalResponsesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="98fea-125">**● totalResponsesCount**: *`number`* = 0</span></span>

<span data-ttu-id="98fea-126">Combien choisi cette option</span><span class="sxs-lookup"><span data-stu-id="98fea-126">How many have chosen this option</span></span>

___

## <a name="methods"></a><span data-ttu-id="98fea-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98fea-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="98fea-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="98fea-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="98fea-129">▸ **fromJSON**(objet : *`any`*) : [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="98fea-129">▸ **fromJSON**(object: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

<span data-ttu-id="98fea-130">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="98fea-130">**Parameters:**</span></span>

| <span data-ttu-id="98fea-131">Nom</span><span class="sxs-lookup"><span data-stu-id="98fea-131">Name</span></span> | <span data-ttu-id="98fea-132">Type</span><span class="sxs-lookup"><span data-stu-id="98fea-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="98fea-133">objet</span><span class="sxs-lookup"><span data-stu-id="98fea-133">object</span></span> | `any` |

<span data-ttu-id="98fea-134">**Renvoie :** [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="98fea-134">**Returns:** [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

___

