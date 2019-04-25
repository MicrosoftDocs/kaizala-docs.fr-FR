---
title: /messages
description: Article de référence pour l'API permettant de demander des messages envoyés à l'adresse interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190711"
---
# <a name="messages"></a><span data-ttu-id="149bd-103">/messages</span><span class="sxs-lookup"><span data-stu-id="149bd-103">/messages</span></span>

<span data-ttu-id="149bd-104">Point de terminaison de l'API pour envoyer des messages à des groupes de conversation dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="149bd-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="149bd-105">POST/messages</span><span class="sxs-lookup"><span data-stu-id="149bd-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="149bd-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="149bd-106">Request Parameters</span></span>

|  | <span data-ttu-id="149bd-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="149bd-107">Parameter</span></span> | <span data-ttu-id="149bd-108">Type</span><span class="sxs-lookup"><span data-stu-id="149bd-108">Type</span></span> | <span data-ttu-id="149bd-109">Module?</span><span class="sxs-lookup"><span data-stu-id="149bd-109">Optional?</span></span> | <span data-ttu-id="149bd-110">Description</span><span class="sxs-lookup"><span data-stu-id="149bd-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="149bd-111">Paramètre de chemin d'URL</span><span class="sxs-lookup"><span data-stu-id="149bd-111">URL Path Parameter</span></span> | <span data-ttu-id="149bd-112">groupId</span><span class="sxs-lookup"><span data-stu-id="149bd-112">groupId</span></span> | <span data-ttu-id="149bd-113">String</span><span class="sxs-lookup"><span data-stu-id="149bd-113">String</span></span> | <span data-ttu-id="149bd-114">Non</span><span class="sxs-lookup"><span data-stu-id="149bd-114">No</span></span> | <span data-ttu-id="149bd-115">GUID représentant l'ID de ressource de la ressource de groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="149bd-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="149bd-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="149bd-116">HTTP Header</span></span> | <span data-ttu-id="149bd-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="149bd-117">accessToken</span></span> | <span data-ttu-id="149bd-118">String</span><span class="sxs-lookup"><span data-stu-id="149bd-118">String</span></span> | <span data-ttu-id="149bd-119">Non</span><span class="sxs-lookup"><span data-stu-id="149bd-119">No</span></span> | <span data-ttu-id="149bd-120">Jeton d'accès reçu depuis le point de terminaison auth</span><span class="sxs-lookup"><span data-stu-id="149bd-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="149bd-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="149bd-121">HTTP Header</span></span> | <span data-ttu-id="149bd-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="149bd-122">Content-Type</span></span> | <span data-ttu-id="149bd-123">String</span><span class="sxs-lookup"><span data-stu-id="149bd-123">String</span></span> | <span data-ttu-id="149bd-124">Non</span><span class="sxs-lookup"><span data-stu-id="149bd-124">No</span></span> | <span data-ttu-id="149bd-125">valeur: application/JSON</span><span class="sxs-lookup"><span data-stu-id="149bd-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="149bd-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="149bd-126">Request body</span></span>

| <span data-ttu-id="149bd-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="149bd-127">Parameter</span></span> | <span data-ttu-id="149bd-128">Type</span><span class="sxs-lookup"><span data-stu-id="149bd-128">Type</span></span> | <span data-ttu-id="149bd-129">Module?</span><span class="sxs-lookup"><span data-stu-id="149bd-129">Optional?</span></span> | <span data-ttu-id="149bd-130">Description</span><span class="sxs-lookup"><span data-stu-id="149bd-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="149bd-131">message</span><span class="sxs-lookup"><span data-stu-id="149bd-131">message</span></span> | <span data-ttu-id="149bd-132">String</span><span class="sxs-lookup"><span data-stu-id="149bd-132">String</span></span> | <span data-ttu-id="149bd-133">Non</span><span class="sxs-lookup"><span data-stu-id="149bd-133">No</span></span> | <span data-ttu-id="149bd-134">Message texte à envoyer (limite maximale de 1000 caractères)</span><span class="sxs-lookup"><span data-stu-id="149bd-134">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="149bd-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="149bd-135">sendToAllSubscribers</span></span> | <span data-ttu-id="149bd-136">Bool</span><span class="sxs-lookup"><span data-stu-id="149bd-136">Bool</span></span> | <span data-ttu-id="149bd-137">Oui</span><span class="sxs-lookup"><span data-stu-id="149bd-137">Yes</span></span> | <span data-ttu-id="149bd-138">Valeur par défaut: false.</span><span class="sxs-lookup"><span data-stu-id="149bd-138">Default: false.</span></span> <span data-ttu-id="149bd-139">Valide uniquement si le groupId appartient à un groupe public.</span><span class="sxs-lookup"><span data-stu-id="149bd-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="149bd-140">True pour envoyer le message texte à tous les abonnés qui nécessitent l'administrateur du jeton pour être administrateur du groupe public</span><span class="sxs-lookup"><span data-stu-id="149bd-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="149bd-141">leurs</span><span class="sxs-lookup"><span data-stu-id="149bd-141">subscribers</span></span> | <span data-ttu-id="149bd-142">Chaîne []</span><span class="sxs-lookup"><span data-stu-id="149bd-142">String[]</span></span> | <span data-ttu-id="149bd-143">Oui</span><span class="sxs-lookup"><span data-stu-id="149bd-143">Yes</span></span> | <span data-ttu-id="149bd-144">Chaque élément correspond à un numéro de téléphone mobile (avec le code pays.</span><span class="sxs-lookup"><span data-stu-id="149bd-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="149bd-145">Nnn.</span><span class="sxs-lookup"><span data-stu-id="149bd-145">Eg.</span></span> <span data-ttu-id="149bd-146">+ 911999999999).</span><span class="sxs-lookup"><span data-stu-id="149bd-146">+911999999999).</span></span> <span data-ttu-id="149bd-147">Le message texte n'est envoyé qu'aux abonnés sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="149bd-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="149bd-148">À utiliser pour la communication sélective aux abonnés dans le contexte d'un groupe public</span><span class="sxs-lookup"><span data-stu-id="149bd-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="149bd-149">Exemple de requête JSON</span><span class="sxs-lookup"><span data-stu-id="149bd-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="149bd-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="149bd-150">Response body</span></span>

| <span data-ttu-id="149bd-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="149bd-151">Parameter</span></span> | <span data-ttu-id="149bd-152">Type</span><span class="sxs-lookup"><span data-stu-id="149bd-152">Type</span></span> | <span data-ttu-id="149bd-153">Description</span><span class="sxs-lookup"><span data-stu-id="149bd-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="149bd-154">ID</span><span class="sxs-lookup"><span data-stu-id="149bd-154">referenceId</span></span> | <span data-ttu-id="149bd-155">Chaîne</span><span class="sxs-lookup"><span data-stu-id="149bd-155">String</span></span> | <span data-ttu-id="149bd-156">GUID représentant la fin de la demande</span><span class="sxs-lookup"><span data-stu-id="149bd-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="149bd-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="149bd-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
