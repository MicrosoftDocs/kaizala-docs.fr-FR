---
ms.openlocfilehash: bb410570ca61dd12bc05c9b5b2d9f0b154b2e7da
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727901"
---
<span data-ttu-id="6119e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="6119e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span></span>

# <a name="class-kasparticipantdata"></a><span data-ttu-id="6119e-102">Classe : KASParticipantData</span><span class="sxs-lookup"><span data-stu-id="6119e-102">Class: KASParticipantData</span></span>

<span data-ttu-id="6119e-103">Définit les propriétés d’un participant de conversation</span><span class="sxs-lookup"><span data-stu-id="6119e-103">Defines properties of a conversation participant</span></span>
## <a name="hierarchy"></a><span data-ttu-id="6119e-104">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6119e-104">Hierarchy</span></span>

<span data-ttu-id="6119e-105">**KASParticipantData**</span><span class="sxs-lookup"><span data-stu-id="6119e-105">**KASParticipantData**</span></span>

## <a name="index"></a><span data-ttu-id="6119e-106">Index</span><span class="sxs-lookup"><span data-stu-id="6119e-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="6119e-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6119e-107">Properties</span></span>

* [<span data-ttu-id="6119e-108">participantId</span><span class="sxs-lookup"><span data-stu-id="6119e-108">participantId</span></span>](kasclient.kasparticipantdata.md#participantid)
* [<span data-ttu-id="6119e-109">participantRole</span><span class="sxs-lookup"><span data-stu-id="6119e-109">participantRole</span></span>](kasclient.kasparticipantdata.md#participantrole)
* [<span data-ttu-id="6119e-110">participantType</span><span class="sxs-lookup"><span data-stu-id="6119e-110">participantType</span></span>](kasclient.kasparticipantdata.md#participanttype)
### <a name="methods"></a><span data-ttu-id="6119e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6119e-111">Methods</span></span>

* [<span data-ttu-id="6119e-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="6119e-112">fromJSON</span></span>](kasclient.kasparticipantdata.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="6119e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6119e-113">Properties</span></span>

<a id="participantid"></a>

###  <a name="participantid"></a><span data-ttu-id="6119e-114">participantId</span><span class="sxs-lookup"><span data-stu-id="6119e-114">participantId</span></span>

<span data-ttu-id="6119e-115">**● participantId**: *`string`* = « »</span><span class="sxs-lookup"><span data-stu-id="6119e-115">**● participantId**: *`string`* = ""</span></span>

___

<a id="participantrole"></a>

###  <a name="participantrole"></a><span data-ttu-id="6119e-116">participantRole</span><span class="sxs-lookup"><span data-stu-id="6119e-116">participantRole</span></span>

<span data-ttu-id="6119e-117">**● participantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole.NONE</span><span class="sxs-lookup"><span data-stu-id="6119e-117">**● participantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* =  KASParticipantRole.NONE</span></span>

___

<a id="participanttype"></a>

###  <a name="participanttype"></a><span data-ttu-id="6119e-118">participantType</span><span class="sxs-lookup"><span data-stu-id="6119e-118">participantType</span></span>

<span data-ttu-id="6119e-119">**● participantType**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* = KASParticipantType.NONE</span><span class="sxs-lookup"><span data-stu-id="6119e-119">**● participantType**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* =  KASParticipantType.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="6119e-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6119e-120">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="6119e-121">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="6119e-121">`<Static>` fromJSON</span></span>

<span data-ttu-id="6119e-122">▸ **fromJSON**(objet : *`any`*) : [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="6119e-122">▸ **fromJSON**(object: *`any`*): [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

<span data-ttu-id="6119e-123">**Paramètres :**</span><span class="sxs-lookup"><span data-stu-id="6119e-123">**Parameters:**</span></span>

| <span data-ttu-id="6119e-124">Nom</span><span class="sxs-lookup"><span data-stu-id="6119e-124">Name</span></span> | <span data-ttu-id="6119e-125">Type</span><span class="sxs-lookup"><span data-stu-id="6119e-125">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="6119e-126">objet</span><span class="sxs-lookup"><span data-stu-id="6119e-126">object</span></span> | `any` |

<span data-ttu-id="6119e-127">**Renvoie :** [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="6119e-127">**Returns:** [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

___

