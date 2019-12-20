---
title: /messages
description: Article de référence pour l’API permettant de demander des messages envoyés à l’adresse interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 64d694e067336a7da0c08ea116498086ee5650ce
ms.sourcegitcommit: 9e57984827280ed977019d33dd78b1ce5e3097fc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809430"
---
# <a name="messages"></a><span data-ttu-id="440df-103">/messages</span><span class="sxs-lookup"><span data-stu-id="440df-103">/messages</span></span>

<span data-ttu-id="440df-104">Point de terminaison de l’API pour envoyer des messages à des groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="440df-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="440df-105">POST/messages</span><span class="sxs-lookup"><span data-stu-id="440df-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="440df-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="440df-106">Request Parameters</span></span>

|  | <span data-ttu-id="440df-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="440df-107">Parameter</span></span> | <span data-ttu-id="440df-108">Type</span><span class="sxs-lookup"><span data-stu-id="440df-108">Type</span></span> | <span data-ttu-id="440df-109">Module?</span><span class="sxs-lookup"><span data-stu-id="440df-109">Optional?</span></span> | <span data-ttu-id="440df-110">Description</span><span class="sxs-lookup"><span data-stu-id="440df-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="440df-111">Paramètre de chemin d’URL</span><span class="sxs-lookup"><span data-stu-id="440df-111">URL Path Parameter</span></span> | <span data-ttu-id="440df-112">groupId</span><span class="sxs-lookup"><span data-stu-id="440df-112">groupId</span></span> | <span data-ttu-id="440df-113">String</span><span class="sxs-lookup"><span data-stu-id="440df-113">String</span></span> | <span data-ttu-id="440df-114">Non</span><span class="sxs-lookup"><span data-stu-id="440df-114">No</span></span> | <span data-ttu-id="440df-115">GUID représentant l’ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="440df-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="440df-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="440df-116">HTTP Header</span></span> | <span data-ttu-id="440df-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="440df-117">accessToken</span></span> | <span data-ttu-id="440df-118">String</span><span class="sxs-lookup"><span data-stu-id="440df-118">String</span></span> | <span data-ttu-id="440df-119">Non</span><span class="sxs-lookup"><span data-stu-id="440df-119">No</span></span> | <span data-ttu-id="440df-120">Jeton d’accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="440df-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="440df-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="440df-121">HTTP Header</span></span> | <span data-ttu-id="440df-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="440df-122">Content-Type</span></span> | <span data-ttu-id="440df-123">String</span><span class="sxs-lookup"><span data-stu-id="440df-123">String</span></span> | <span data-ttu-id="440df-124">Non</span><span class="sxs-lookup"><span data-stu-id="440df-124">No</span></span> | <span data-ttu-id="440df-125">valeur : application/JSON</span><span class="sxs-lookup"><span data-stu-id="440df-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="440df-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="440df-126">Request body</span></span>

| <span data-ttu-id="440df-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="440df-127">Parameter</span></span> | <span data-ttu-id="440df-128">Type</span><span class="sxs-lookup"><span data-stu-id="440df-128">Type</span></span> | <span data-ttu-id="440df-129">Module?</span><span class="sxs-lookup"><span data-stu-id="440df-129">Optional?</span></span> | <span data-ttu-id="440df-130">Description</span><span class="sxs-lookup"><span data-stu-id="440df-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="440df-131">message</span><span class="sxs-lookup"><span data-stu-id="440df-131">message</span></span> | <span data-ttu-id="440df-132">String</span><span class="sxs-lookup"><span data-stu-id="440df-132">String</span></span> | <span data-ttu-id="440df-133">Non</span><span class="sxs-lookup"><span data-stu-id="440df-133">No</span></span> | <span data-ttu-id="440df-134">Message texte à envoyer (limite maximale de 4000 caractères)</span><span class="sxs-lookup"><span data-stu-id="440df-134">Text message to be sent (Max limit of 4000 Characters)</span></span> |
| <span data-ttu-id="440df-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="440df-135">sendToAllSubscribers</span></span> | <span data-ttu-id="440df-136">Bool</span><span class="sxs-lookup"><span data-stu-id="440df-136">Bool</span></span> | <span data-ttu-id="440df-137">Oui</span><span class="sxs-lookup"><span data-stu-id="440df-137">Yes</span></span> | <span data-ttu-id="440df-138">Valeur par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="440df-138">Default: false.</span></span> <span data-ttu-id="440df-139">Valide uniquement si le groupId appartient à un groupe public.</span><span class="sxs-lookup"><span data-stu-id="440df-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="440df-140">True pour envoyer le message texte à tous les abonnés qui nécessitent l’administrateur du jeton pour être administrateur du groupe public</span><span class="sxs-lookup"><span data-stu-id="440df-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="440df-141">leurs</span><span class="sxs-lookup"><span data-stu-id="440df-141">subscribers</span></span> | <span data-ttu-id="440df-142">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="440df-142">String[]</span></span> | <span data-ttu-id="440df-143">Oui</span><span class="sxs-lookup"><span data-stu-id="440df-143">Yes</span></span> | <span data-ttu-id="440df-144">Chaque élément correspond à un numéro de téléphone mobile (avec le code pays.</span><span class="sxs-lookup"><span data-stu-id="440df-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="440df-145">Nnn.</span><span class="sxs-lookup"><span data-stu-id="440df-145">Eg.</span></span> <span data-ttu-id="440df-146">+ 911999999999).</span><span class="sxs-lookup"><span data-stu-id="440df-146">+911999999999).</span></span> <span data-ttu-id="440df-147">Le message texte n’est envoyé qu’aux abonnés sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="440df-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="440df-148">À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe public</span><span class="sxs-lookup"><span data-stu-id="440df-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="440df-149">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="440df-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="440df-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="440df-150">Response body</span></span>

| <span data-ttu-id="440df-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="440df-151">Parameter</span></span> | <span data-ttu-id="440df-152">Type</span><span class="sxs-lookup"><span data-stu-id="440df-152">Type</span></span> | <span data-ttu-id="440df-153">Description</span><span class="sxs-lookup"><span data-stu-id="440df-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="440df-154">ID</span><span class="sxs-lookup"><span data-stu-id="440df-154">referenceId</span></span> | <span data-ttu-id="440df-155">String</span><span class="sxs-lookup"><span data-stu-id="440df-155">String</span></span> | <span data-ttu-id="440df-156">GUID représentant la fin de la demande</span><span class="sxs-lookup"><span data-stu-id="440df-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="440df-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="440df-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
