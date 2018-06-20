---
title: /actions
description: Article de référence de l’API à envoyer/extraire des instances de l’Action
topic: Reference
author: nitinjms
ms.openlocfilehash: 6f58e45b9eb5d4a4987c3aeb36ff8fe1862fe7bc
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905126"
---
# <a name="api-to-sendretrieve-action-instances"></a><span data-ttu-id="84a78-103">API à envoyer/extraire des instances de l’Action</span><span class="sxs-lookup"><span data-stu-id="84a78-103">API to send/retrieve Action instances</span></span>
## <a name="actions"></a><span data-ttu-id="84a78-104">/actions</span><span class="sxs-lookup"><span data-stu-id="84a78-104">/actions</span></span>
<span data-ttu-id="84a78-105">Point de terminaison API à envoyer/extraire des instances de Kaizala Actions dans les groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="84a78-105">API end-point to send/retrieve instances of Kaizala Actions to/from conversation groups inside Kaizala.</span></span> <span data-ttu-id="84a78-106">Portée actuelle est à prendre en charge la suite de types d’actions :</span><span class="sxs-lookup"><span data-stu-id="84a78-106">Current scope is to support following action types:</span></span>

| <span data-ttu-id="84a78-107">Action</span><span class="sxs-lookup"><span data-stu-id="84a78-107">Action</span></span> | <span data-ttu-id="84a78-108">OBTENIR la prise en charge</span><span class="sxs-lookup"><span data-stu-id="84a78-108">GET Supported</span></span> | <span data-ttu-id="84a78-109">Prise en charge de la publication</span><span class="sxs-lookup"><span data-stu-id="84a78-109">POST Supported</span></span> | <span data-ttu-id="84a78-110">ID</span><span class="sxs-lookup"><span data-stu-id="84a78-110">Id</span></span> |
| :---: | :---: | :---: | :---: |
| <span data-ttu-id="84a78-111">Image des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="84a78-111">Picture Attachment</span></span> | <span data-ttu-id="84a78-112">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-112">Yes</span></span> | <span data-ttu-id="84a78-113">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-113">Yes</span></span> | <span data-ttu-id="84a78-114">image</span><span class="sxs-lookup"><span data-stu-id="84a78-114">image</span></span> |
| <span data-ttu-id="84a78-115">Pièce jointe audio</span><span class="sxs-lookup"><span data-stu-id="84a78-115">Audio Attachment</span></span> | <span data-ttu-id="84a78-116">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-116">No</span></span> | <span data-ttu-id="84a78-117">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-117">Yes</span></span> | <span data-ttu-id="84a78-118">audio</span><span class="sxs-lookup"><span data-stu-id="84a78-118">audio</span></span> |
| <span data-ttu-id="84a78-119">Pièce jointe</span><span class="sxs-lookup"><span data-stu-id="84a78-119">Document Attachment</span></span> | <span data-ttu-id="84a78-120">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-120">No</span></span> | <span data-ttu-id="84a78-121">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-121">Yes</span></span> | <span data-ttu-id="84a78-122">document</span><span class="sxs-lookup"><span data-stu-id="84a78-122">document</span></span> |
| <span data-ttu-id="84a78-123">Pièce jointe de contact</span><span class="sxs-lookup"><span data-stu-id="84a78-123">Contact Attachment</span></span> | <span data-ttu-id="84a78-124">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-124">No</span></span> | <span data-ttu-id="84a78-125">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-125">No</span></span> | <span data-ttu-id="84a78-126">s/o</span><span class="sxs-lookup"><span data-stu-id="84a78-126">n/a</span></span> |
| <span data-ttu-id="84a78-127">Travail</span><span class="sxs-lookup"><span data-stu-id="84a78-127">Job</span></span> | <span data-ttu-id="84a78-128">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-128">Yes</span></span> | <span data-ttu-id="84a78-129">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-129">Yes</span></span> | <span data-ttu-id="84a78-130">travail</span><span class="sxs-lookup"><span data-stu-id="84a78-130">job</span></span> |
| <span data-ttu-id="84a78-131">Enquête</span><span class="sxs-lookup"><span data-stu-id="84a78-131">Survey</span></span> | <span data-ttu-id="84a78-132">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-132">Yes</span></span> | <span data-ttu-id="84a78-133">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-133">Yes</span></span> | <span data-ttu-id="84a78-134">enquête</span><span class="sxs-lookup"><span data-stu-id="84a78-134">survey</span></span> |
| <span data-ttu-id="84a78-135">Photo avec l’emplacement</span><span class="sxs-lookup"><span data-stu-id="84a78-135">Photo with Location</span></span> | <span data-ttu-id="84a78-136">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-136">Yes</span></span> | <span data-ttu-id="84a78-137">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-137">No</span></span> | <span data-ttu-id="84a78-138">photoWithLocation</span><span class="sxs-lookup"><span data-stu-id="84a78-138">photoWithLocation</span></span> |
| <span data-ttu-id="84a78-139">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="84a78-139">Let's Meet</span></span> | <span data-ttu-id="84a78-140">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-140">Yes</span></span> | <span data-ttu-id="84a78-141">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-141">Yes</span></span> | <span data-ttu-id="84a78-142">letsmeet</span><span class="sxs-lookup"><span data-stu-id="84a78-142">letsmeet</span></span> |
| <span data-ttu-id="84a78-143">Interrogation rapide</span><span class="sxs-lookup"><span data-stu-id="84a78-143">Quick Poll</span></span> | <span data-ttu-id="84a78-144">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-144">Yes</span></span> | <span data-ttu-id="84a78-145">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-145">Yes</span></span> | <span data-ttu-id="84a78-146">sondage</span><span class="sxs-lookup"><span data-stu-id="84a78-146">poll</span></span> |
| <span data-ttu-id="84a78-147">Emplacement de partage</span><span class="sxs-lookup"><span data-stu-id="84a78-147">Share Location</span></span> | <span data-ttu-id="84a78-148">Oui</span><span class="sxs-lookup"><span data-stu-id="84a78-148">Yes</span></span> | <span data-ttu-id="84a78-149">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-149">No</span></span> | <span data-ttu-id="84a78-150">shareLocation</span><span class="sxs-lookup"><span data-stu-id="84a78-150">shareLocation</span></span> |
| <span data-ttu-id="84a78-151">Emplacement de la demande</span><span class="sxs-lookup"><span data-stu-id="84a78-151">Request Location</span></span> | <span data-ttu-id="84a78-152">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-152">No</span></span> | <span data-ttu-id="84a78-153">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-153">No</span></span> | <span data-ttu-id="84a78-154">s/o</span><span class="sxs-lookup"><span data-stu-id="84a78-154">n/a</span></span> |
| <span data-ttu-id="84a78-155">Emplacement Live</span><span class="sxs-lookup"><span data-stu-id="84a78-155">Live Location</span></span> | <span data-ttu-id="84a78-156">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-156">No</span></span> | <span data-ttu-id="84a78-157">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-157">No</span></span> | <span data-ttu-id="84a78-158">s/o</span><span class="sxs-lookup"><span data-stu-id="84a78-158">n/a</span></span> |
| <span data-ttu-id="84a78-159">Annonce</span><span class="sxs-lookup"><span data-stu-id="84a78-159">Announcement</span></span> | <span data-ttu-id="84a78-160">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-160">No</span></span> | <span data-ttu-id="84a78-161">Non</span><span class="sxs-lookup"><span data-stu-id="84a78-161">No</span></span> | <span data-ttu-id="84a78-162">s/o</span><span class="sxs-lookup"><span data-stu-id="84a78-162">n/a</span></span> |


*   <span data-ttu-id="84a78-163">API pour récupérer les [Actions](actions_get.md) et les [Détails de l’Action](actionDetails.md)</span><span class="sxs-lookup"><span data-stu-id="84a78-163">API to retreive [Actions](actions_get.md) and [Action details](actionDetails.md)</span></span>
*   [<span data-ttu-id="84a78-164">API de publier des nouvelles instances d’Actions</span><span class="sxs-lookup"><span data-stu-id="84a78-164">API to post new instances of Actions</span></span>](actions_post.md)
*   [<span data-ttu-id="84a78-165">API à publier des réponses de l’action de nouvelle action réponses/modifier existant</span><span class="sxs-lookup"><span data-stu-id="84a78-165">API to post new action responses/edit existing action responses</span></span>](action_responses.md)