---
ms.openlocfilehash: fb1ab90d11725ffb657738e090e9e83baee6b886
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727936"
---
<span data-ttu-id="6b36b-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="6b36b-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span></span>

# <a name="class-kaserror"></a><span data-ttu-id="6b36b-102">Classe : KASError</span><span class="sxs-lookup"><span data-stu-id="6b36b-102">Class: KASError</span></span>

## <a name="hierarchy"></a><span data-ttu-id="6b36b-103">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6b36b-103">Hierarchy</span></span>

<span data-ttu-id="6b36b-104">**KASError**</span><span class="sxs-lookup"><span data-stu-id="6b36b-104">**KASError**</span></span>

## <a name="index"></a><span data-ttu-id="6b36b-105">Index</span><span class="sxs-lookup"><span data-stu-id="6b36b-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="6b36b-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b36b-106">Properties</span></span>

* [<span data-ttu-id="6b36b-107">description</span><span class="sxs-lookup"><span data-stu-id="6b36b-107">description</span></span>](kasclient.kaserror.md#description)
* [<span data-ttu-id="6b36b-108">code d’erreur</span><span class="sxs-lookup"><span data-stu-id="6b36b-108">errorCode</span></span>](kasclient.kaserror.md#errorcode)
### <a name="methods"></a><span data-ttu-id="6b36b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b36b-109">Methods</span></span>

* [<span data-ttu-id="6b36b-110">fromString</span><span class="sxs-lookup"><span data-stu-id="6b36b-110">fromString</span></span>](kasclient.kaserror.md#fromstring)

---

## <a name="properties"></a><span data-ttu-id="6b36b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b36b-111">Properties</span></span>

<a id="description"></a>

###  <a name="description"></a><span data-ttu-id="6b36b-112">description</span><span class="sxs-lookup"><span data-stu-id="6b36b-112">description</span></span>

<span data-ttu-id="6b36b-113">**Description ●**: *`String`* = « »</span><span class="sxs-lookup"><span data-stu-id="6b36b-113">**● description**: *`String`* = ""</span></span>

___

<a id="errorcode"></a>

###  <a name="errorcode"></a><span data-ttu-id="6b36b-114">errorCode</span><span class="sxs-lookup"><span data-stu-id="6b36b-114">errorCode</span></span>

<span data-ttu-id="6b36b-115">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode.NONE</span><span class="sxs-lookup"><span data-stu-id="6b36b-115">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* =  KASErrorCode.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="6b36b-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b36b-116">Methods</span></span>

<a id="fromstring"></a>

### <a name="static-fromstring"></a><span data-ttu-id="6b36b-117">`<Static>`fromString</span><span class="sxs-lookup"><span data-stu-id="6b36b-117">`<Static>` fromString</span></span>

<span data-ttu-id="6b36b-118">▸ **fromString**(stringifyError : *`string`*) : [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="6b36b-118">▸ **fromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="6b36b-119">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="6b36b-119">**Parameters:**</span></span>

| <span data-ttu-id="6b36b-120">Nom</span><span class="sxs-lookup"><span data-stu-id="6b36b-120">Name</span></span> | <span data-ttu-id="6b36b-121">Type</span><span class="sxs-lookup"><span data-stu-id="6b36b-121">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="6b36b-122">stringifyError</span><span class="sxs-lookup"><span data-stu-id="6b36b-122">stringifyError</span></span> | `string` |

<span data-ttu-id="6b36b-123">**Renvoie :** [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="6b36b-123">**Returns:** [KASError](kasclient.kaserror.md)</span></span>

___

