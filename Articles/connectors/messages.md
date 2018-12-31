---
title: /messages
description: Article de référence de l’API pour les messages de requête envoyée groupe carte réseau interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 58839035fca768f92eda40974029208eb31dda7f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/31/2018
ms.locfileid: "27465700"
---
# <a name="messages"></a><span data-ttu-id="8777a-103">/messages</span><span class="sxs-lookup"><span data-stu-id="8777a-103">/messages</span></span>

<span data-ttu-id="8777a-104">Point de terminaison API pour envoyer des messages à des groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="8777a-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="8777a-105">/Messages POST</span><span class="sxs-lookup"><span data-stu-id="8777a-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="8777a-106">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="8777a-106">Request Parameters</span></span>

|  | <span data-ttu-id="8777a-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8777a-107">Parameter</span></span> | <span data-ttu-id="8777a-108">Type</span><span class="sxs-lookup"><span data-stu-id="8777a-108">Type</span></span> | <span data-ttu-id="8777a-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="8777a-109">Optional?</span></span> | <span data-ttu-id="8777a-110">Description</span><span class="sxs-lookup"><span data-stu-id="8777a-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="8777a-111">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="8777a-111">URL Path Parameter</span></span> | <span data-ttu-id="8777a-112">groupId</span><span class="sxs-lookup"><span data-stu-id="8777a-112">groupId</span></span> | <span data-ttu-id="8777a-113">String</span><span class="sxs-lookup"><span data-stu-id="8777a-113">String</span></span> | <span data-ttu-id="8777a-114">Non</span><span class="sxs-lookup"><span data-stu-id="8777a-114">No</span></span> | <span data-ttu-id="8777a-115">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="8777a-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="8777a-116">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="8777a-116">HTTP Header</span></span> | <span data-ttu-id="8777a-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="8777a-117">accessToken</span></span> | <span data-ttu-id="8777a-118">String</span><span class="sxs-lookup"><span data-stu-id="8777a-118">String</span></span> | <span data-ttu-id="8777a-119">Non</span><span class="sxs-lookup"><span data-stu-id="8777a-119">No</span></span> | <span data-ttu-id="8777a-120">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="8777a-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="8777a-121">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="8777a-121">HTTP Header</span></span> | <span data-ttu-id="8777a-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8777a-122">Content-Type</span></span> | <span data-ttu-id="8777a-123">String</span><span class="sxs-lookup"><span data-stu-id="8777a-123">String</span></span> | <span data-ttu-id="8777a-124">Non</span><span class="sxs-lookup"><span data-stu-id="8777a-124">No</span></span> | <span data-ttu-id="8777a-125">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="8777a-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="8777a-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8777a-126">Request body</span></span>

| <span data-ttu-id="8777a-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8777a-127">Parameter</span></span> | <span data-ttu-id="8777a-128">Type</span><span class="sxs-lookup"><span data-stu-id="8777a-128">Type</span></span> | <span data-ttu-id="8777a-129">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="8777a-129">Optional?</span></span> | <span data-ttu-id="8777a-130">Description</span><span class="sxs-lookup"><span data-stu-id="8777a-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="8777a-131">message</span><span class="sxs-lookup"><span data-stu-id="8777a-131">message</span></span> | <span data-ttu-id="8777a-132">String</span><span class="sxs-lookup"><span data-stu-id="8777a-132">String</span></span> | <span data-ttu-id="8777a-133">Non</span><span class="sxs-lookup"><span data-stu-id="8777a-133">No</span></span> | <span data-ttu-id="8777a-134">Message texte envoyé (limite maximale de 1 000 caractères)</span><span class="sxs-lookup"><span data-stu-id="8777a-134">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="8777a-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="8777a-135">sendToAllSubscribers</span></span> | <span data-ttu-id="8777a-136">Bool</span><span class="sxs-lookup"><span data-stu-id="8777a-136">Bool</span></span> | <span data-ttu-id="8777a-137">Oui</span><span class="sxs-lookup"><span data-stu-id="8777a-137">Yes</span></span> | <span data-ttu-id="8777a-138">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="8777a-138">Default: false.</span></span> <span data-ttu-id="8777a-139">Valide uniquement dans les cas groupId appartient à un groupe Public.</span><span class="sxs-lookup"><span data-stu-id="8777a-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="8777a-140">True pour envoyer le message à tous les abonnés qui requiert l’utilisateur du jeton admin du groupe Public</span><span class="sxs-lookup"><span data-stu-id="8777a-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="8777a-141">abonnés</span><span class="sxs-lookup"><span data-stu-id="8777a-141">subscribers</span></span> | <span data-ttu-id="8777a-142">String]</span><span class="sxs-lookup"><span data-stu-id="8777a-142">String[]</span></span> | <span data-ttu-id="8777a-143">Oui</span><span class="sxs-lookup"><span data-stu-id="8777a-143">Yes</span></span> | <span data-ttu-id="8777a-144">Chaque élément correspond à un numéro de téléphone mobile (avec le code du pays.</span><span class="sxs-lookup"><span data-stu-id="8777a-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="8777a-145">Par exemple.</span><span class="sxs-lookup"><span data-stu-id="8777a-145">Eg.</span></span> <span data-ttu-id="8777a-146">+911999999999).</span><span class="sxs-lookup"><span data-stu-id="8777a-146">+911999999999).</span></span> <span data-ttu-id="8777a-147">Message texte sera envoyé uniquement pour les abonnés sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="8777a-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="8777a-148">À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe Public</span><span class="sxs-lookup"><span data-stu-id="8777a-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="8777a-149">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="8777a-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="8777a-150">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="8777a-150">Response body</span></span>

| <span data-ttu-id="8777a-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8777a-151">Parameter</span></span> | <span data-ttu-id="8777a-152">Type</span><span class="sxs-lookup"><span data-stu-id="8777a-152">Type</span></span> | <span data-ttu-id="8777a-153">Description</span><span class="sxs-lookup"><span data-stu-id="8777a-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8777a-154">referenceId</span><span class="sxs-lookup"><span data-stu-id="8777a-154">referenceId</span></span> | <span data-ttu-id="8777a-155">String</span><span class="sxs-lookup"><span data-stu-id="8777a-155">String</span></span> | <span data-ttu-id="8777a-156">GUID représentant l’exécution réussie de la demande</span><span class="sxs-lookup"><span data-stu-id="8777a-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="8777a-157">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="8777a-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
