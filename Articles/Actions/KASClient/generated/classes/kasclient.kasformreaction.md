---
ms.openlocfilehash: 3b1a2cbce6762e7efcb4371db75d71596d651887
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727906"
---
<span data-ttu-id="441c3-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormReaction](../classes/kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="441c3-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormReaction](../classes/kasclient.kasformreaction.md)</span></span>

# <a name="class-kasformreaction"></a><span data-ttu-id="441c3-102">Classe : KASFormReaction</span><span class="sxs-lookup"><span data-stu-id="441c3-102">Class: KASFormReaction</span></span>

## <a name="hierarchy"></a><span data-ttu-id="441c3-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="441c3-103">Hierarchy</span></span>

<span data-ttu-id="441c3-104">**KASFormReaction**</span><span class="sxs-lookup"><span data-stu-id="441c3-104">**KASFormReaction**</span></span>

## <a name="index"></a><span data-ttu-id="441c3-105">Index</span><span class="sxs-lookup"><span data-stu-id="441c3-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="441c3-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="441c3-106">Properties</span></span>

* [<span data-ttu-id="441c3-107">commentsCount</span><span class="sxs-lookup"><span data-stu-id="441c3-107">commentsCount</span></span>](kasclient.kasformreaction.md#commentscount)
* [<span data-ttu-id="441c3-108">didIComment</span><span class="sxs-lookup"><span data-stu-id="441c3-108">didIComment</span></span>](kasclient.kasformreaction.md#didicomment)
* [<span data-ttu-id="441c3-109">didILike</span><span class="sxs-lookup"><span data-stu-id="441c3-109">didILike</span></span>](kasclient.kasformreaction.md#didilike)
* [<span data-ttu-id="441c3-110">hideComments</span><span class="sxs-lookup"><span data-stu-id="441c3-110">hideComments</span></span>](kasclient.kasformreaction.md#hidecomments)
* [<span data-ttu-id="441c3-111">hideLikes</span><span class="sxs-lookup"><span data-stu-id="441c3-111">hideLikes</span></span>](kasclient.kasformreaction.md#hidelikes)
* [<span data-ttu-id="441c3-112">hideLikesDetails</span><span class="sxs-lookup"><span data-stu-id="441c3-112">hideLikesDetails</span></span>](kasclient.kasformreaction.md#hidelikesdetails)
* [<span data-ttu-id="441c3-113">likesCount</span><span class="sxs-lookup"><span data-stu-id="441c3-113">likesCount</span></span>](kasclient.kasformreaction.md#likescount)
### <a name="methods"></a><span data-ttu-id="441c3-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="441c3-114">Methods</span></span>

* [<span data-ttu-id="441c3-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="441c3-115">fromJSON</span></span>](kasclient.kasformreaction.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="441c3-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="441c3-116">Properties</span></span>

<a id="commentscount"></a>

###  <a name="commentscount"></a><span data-ttu-id="441c3-117">commentsCount</span><span class="sxs-lookup"><span data-stu-id="441c3-117">commentsCount</span></span>

<span data-ttu-id="441c3-118">**● commentsCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="441c3-118">**● commentsCount**: *`number`* = 0</span></span>

<span data-ttu-id="441c3-119">Nombre de commentaires reçus pour le formulaire</span><span class="sxs-lookup"><span data-stu-id="441c3-119">Number of comments received for the form</span></span>

___

<a id="didicomment"></a>

###  <a name="didicomment"></a><span data-ttu-id="441c3-120">didIComment</span><span class="sxs-lookup"><span data-stu-id="441c3-120">didIComment</span></span>

<span data-ttu-id="441c3-121">**● didIComment**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="441c3-121">**● didIComment**: *`boolean`* = false</span></span>

<span data-ttu-id="441c3-122">Indique si l’utilisateur actuel a aimé déjà ou non</span><span class="sxs-lookup"><span data-stu-id="441c3-122">Denotes whether the current user has already liked or not</span></span>

___

<a id="didilike"></a>

###  <a name="didilike"></a><span data-ttu-id="441c3-123">didILike</span><span class="sxs-lookup"><span data-stu-id="441c3-123">didILike</span></span>

<span data-ttu-id="441c3-124">**● didILike**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="441c3-124">**● didILike**: *`boolean`* = false</span></span>

<span data-ttu-id="441c3-125">Indique si l’utilisateur actuel a aimé déjà ou non</span><span class="sxs-lookup"><span data-stu-id="441c3-125">Denotes whether the current user has already liked or not</span></span>

___

<a id="hidecomments"></a>

###  <a name="hidecomments"></a><span data-ttu-id="441c3-126">hideComments</span><span class="sxs-lookup"><span data-stu-id="441c3-126">hideComments</span></span>

<span data-ttu-id="441c3-127">**● hideComments**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="441c3-127">**● hideComments**: *`boolean`* = false</span></span>

<span data-ttu-id="441c3-128">Indique s’il faut afficher ou non les commentaires</span><span class="sxs-lookup"><span data-stu-id="441c3-128">Denotes whether to show comments or not</span></span>

___

<a id="hidelikes"></a>

###  <a name="hidelikes"></a><span data-ttu-id="441c3-129">hideLikes</span><span class="sxs-lookup"><span data-stu-id="441c3-129">hideLikes</span></span>

<span data-ttu-id="441c3-130">**● hideLikes**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="441c3-130">**● hideLikes**: *`boolean`* = false</span></span>

<span data-ttu-id="441c3-131">Indique si Afficher j’aime ou non</span><span class="sxs-lookup"><span data-stu-id="441c3-131">Denotes whether to show likes or not</span></span>

___

<a id="hidelikesdetails"></a>

###  <a name="hidelikesdetails"></a><span data-ttu-id="441c3-132">hideLikesDetails</span><span class="sxs-lookup"><span data-stu-id="441c3-132">hideLikesDetails</span></span>

<span data-ttu-id="441c3-133">**● hideLikesDetails**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="441c3-133">**● hideLikesDetails**: *`boolean`* = false</span></span>

<span data-ttu-id="441c3-134">Indique si Afficher j’aime imeersive affichage ou non</span><span class="sxs-lookup"><span data-stu-id="441c3-134">Denotes whether to show likes imeersive view or not</span></span>

___

<a id="likescount"></a>

###  <a name="likescount"></a><span data-ttu-id="441c3-135">likesCount</span><span class="sxs-lookup"><span data-stu-id="441c3-135">likesCount</span></span>

<span data-ttu-id="441c3-136">**● likesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="441c3-136">**● likesCount**: *`number`* = 0</span></span>

<span data-ttu-id="441c3-137">Nombre de J’aime reçu pour le formulaire</span><span class="sxs-lookup"><span data-stu-id="441c3-137">Number of likes received for the form</span></span>

___

## <a name="methods"></a><span data-ttu-id="441c3-138">Méthodes</span><span class="sxs-lookup"><span data-stu-id="441c3-138">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="441c3-139">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="441c3-139">`<Static>` fromJSON</span></span>

<span data-ttu-id="441c3-140">▸ **fromJSON**(objet : *`JSON`*) : [KASFormReaction](kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="441c3-140">▸ **fromJSON**(object: *`JSON`*): [KASFormReaction](kasclient.kasformreaction.md)</span></span>

<span data-ttu-id="441c3-141">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="441c3-141">**Parameters:**</span></span>

| <span data-ttu-id="441c3-142">Nom</span><span class="sxs-lookup"><span data-stu-id="441c3-142">Name</span></span> | <span data-ttu-id="441c3-143">Type</span><span class="sxs-lookup"><span data-stu-id="441c3-143">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="441c3-144">objet</span><span class="sxs-lookup"><span data-stu-id="441c3-144">object</span></span> | `JSON` |

<span data-ttu-id="441c3-145">**Renvoie :** [KASFormReaction](kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="441c3-145">**Returns:** [KASFormReaction](kasclient.kasformreaction.md)</span></span>

___

