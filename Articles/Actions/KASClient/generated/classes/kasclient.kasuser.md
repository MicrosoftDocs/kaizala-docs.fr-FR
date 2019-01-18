---
ms.openlocfilehash: 20daed268b67eea07a8185c84086587dcf1f1aeb
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727942"
---
<span data-ttu-id="cc562-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="cc562-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)</span></span>

# <a name="class-kasuser"></a><span data-ttu-id="cc562-102">Classe : KASUser</span><span class="sxs-lookup"><span data-stu-id="cc562-102">Class: KASUser</span></span>

## <a name="hierarchy"></a><span data-ttu-id="cc562-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="cc562-103">Hierarchy</span></span>

<span data-ttu-id="cc562-104">**KASUser**</span><span class="sxs-lookup"><span data-stu-id="cc562-104">**KASUser**</span></span>

## <a name="index"></a><span data-ttu-id="cc562-105">Index</span><span class="sxs-lookup"><span data-stu-id="cc562-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="cc562-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc562-106">Properties</span></span>

* [<span data-ttu-id="cc562-107">id</span><span class="sxs-lookup"><span data-stu-id="cc562-107">id</span></span>](kasclient.kasuser.md#id)
* [<span data-ttu-id="cc562-108">name</span><span class="sxs-lookup"><span data-stu-id="cc562-108">name</span></span>](kasclient.kasuser.md#name)
* [<span data-ttu-id="cc562-109">originalName</span><span class="sxs-lookup"><span data-stu-id="cc562-109">originalName</span></span>](kasclient.kasuser.md#originalname)
* [<span data-ttu-id="cc562-110">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="cc562-110">phoneNumber</span></span>](kasclient.kasuser.md#phonenumber)
* [<span data-ttu-id="cc562-111">pictureBGColor</span><span class="sxs-lookup"><span data-stu-id="cc562-111">pictureBGColor</span></span>](kasclient.kasuser.md#picturebgcolor)
* [<span data-ttu-id="cc562-112">pictureInitials</span><span class="sxs-lookup"><span data-stu-id="cc562-112">pictureInitials</span></span>](kasclient.kasuser.md#pictureinitials)
* [<span data-ttu-id="cc562-113">URL de la photo</span><span class="sxs-lookup"><span data-stu-id="cc562-113">pictureUrl</span></span>](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a><span data-ttu-id="cc562-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cc562-114">Methods</span></span>

* [<span data-ttu-id="cc562-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="cc562-115">fromJSON</span></span>](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="cc562-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc562-116">Properties</span></span>

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="cc562-117">id</span><span class="sxs-lookup"><span data-stu-id="cc562-117">id</span></span>

<span data-ttu-id="cc562-118">**Id ●**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-118">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-119">Id d’utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="cc562-119">Unique user id</span></span>

___

<a id="name"></a>

###  <a name="name"></a><span data-ttu-id="cc562-120">name</span><span class="sxs-lookup"><span data-stu-id="cc562-120">name</span></span>

<span data-ttu-id="cc562-121">**Nom ●**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-121">**● name**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-122">Nom de l’utilisateur (« vous » pour l’utilisateur actuel)</span><span class="sxs-lookup"><span data-stu-id="cc562-122">Name of the user ("You" for the current user)</span></span>

___

<a id="originalname"></a>

###  <a name="originalname"></a><span data-ttu-id="cc562-123">originalName</span><span class="sxs-lookup"><span data-stu-id="cc562-123">originalName</span></span>

<span data-ttu-id="cc562-124">**● originalName**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-124">**● originalName**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-125">Ne pas considérer « Vous »</span><span class="sxs-lookup"><span data-stu-id="cc562-125">Not considering "You"</span></span>

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a><span data-ttu-id="cc562-126">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="cc562-126">phoneNumber</span></span>

<span data-ttu-id="cc562-127">**● phoneNumber**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-127">**● phoneNumber**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-128">Numéro de téléphone de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cc562-128">Phone number of the user</span></span>

___

<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a><span data-ttu-id="cc562-129">pictureBGColor</span><span class="sxs-lookup"><span data-stu-id="cc562-129">pictureBGColor</span></span>

<span data-ttu-id="cc562-130">**● pictureBGColor**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-130">**● pictureBGColor**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-131">En cas de l’URL de la photo n’est pas visible, nous devons utiliser les initiales en tant que le pic de profil, sous deux membres qui sont des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cc562-131">In case the PictureUrl is not there, we should use the users initials as the profile pic, below two members are for that</span></span>

___

<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a><span data-ttu-id="cc562-132">pictureInitials</span><span class="sxs-lookup"><span data-stu-id="cc562-132">pictureInitials</span></span>

<span data-ttu-id="cc562-133">**● pictureInitials**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-133">**● pictureInitials**: *`string`* = ""</span></span>

___

<a id="pictureurl"></a>

###  <a name="pictureurl"></a><span data-ttu-id="cc562-134">URL de la photo</span><span class="sxs-lookup"><span data-stu-id="cc562-134">pictureUrl</span></span>

<span data-ttu-id="cc562-135">**● pictureUrl**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="cc562-135">**● pictureUrl**: *`string`* = ""</span></span>

<span data-ttu-id="cc562-136">Url d’image de profil de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cc562-136">Profile picture url of the user</span></span>

___

## <a name="methods"></a><span data-ttu-id="cc562-137">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cc562-137">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="cc562-138">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="cc562-138">`<Static>` fromJSON</span></span>

<span data-ttu-id="cc562-139">▸ **fromJSON**(objet : *`JSON`*) : [KASUser](kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="cc562-139">▸ **fromJSON**(object: *`JSON`*): [KASUser](kasclient.kasuser.md)</span></span>

<span data-ttu-id="cc562-140">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="cc562-140">**Parameters:**</span></span>

| <span data-ttu-id="cc562-141">Nom</span><span class="sxs-lookup"><span data-stu-id="cc562-141">Name</span></span> | <span data-ttu-id="cc562-142">Type</span><span class="sxs-lookup"><span data-stu-id="cc562-142">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="cc562-143">objet</span><span class="sxs-lookup"><span data-stu-id="cc562-143">object</span></span> | `JSON` |

<span data-ttu-id="cc562-144">**Renvoie :** [KASUser](kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="cc562-144">**Returns:** [KASUser](kasclient.kasuser.md)</span></span>

___

