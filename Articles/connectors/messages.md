---
title: /messages
description: Article de référence de l’API pour les messages de requête envoyée groupe carte réseau interne
topic: Reference
author: nitinjms
ms.openlocfilehash: 25e3a918c95bd045a374de0420eda6324d46046a
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905168"
---
# <a name="apis-to-query-messages-sent-in-a-group"></a><span data-ttu-id="099f2-103">API de requête les messages envoyés dans un groupe</span><span class="sxs-lookup"><span data-stu-id="099f2-103">APIs to query messages sent in a group</span></span>
## <a name="messages"></a><span data-ttu-id="099f2-104">/messages</span><span class="sxs-lookup"><span data-stu-id="099f2-104">/messages</span></span>
<span data-ttu-id="099f2-105">Point de terminaison API pour envoyer des messages à des groupes de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="099f2-105">API end-point to send messages to conversation groups inside Kaizala.</span></span>

### <a name="post-messages"></a><span data-ttu-id="099f2-106">/Messages POST</span><span class="sxs-lookup"><span data-stu-id="099f2-106">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

##### <a name="request-parameters"></a><span data-ttu-id="099f2-107">Paramètres de la demande</span><span class="sxs-lookup"><span data-stu-id="099f2-107">Request Parameters</span></span>

|  | <span data-ttu-id="099f2-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="099f2-108">Parameter</span></span> | <span data-ttu-id="099f2-109">Type</span><span class="sxs-lookup"><span data-stu-id="099f2-109">Type</span></span> | <span data-ttu-id="099f2-110">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="099f2-110">Optional?</span></span> | <span data-ttu-id="099f2-111">Description</span><span class="sxs-lookup"><span data-stu-id="099f2-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="099f2-112">Paramètre de chemin d’accès d’URL</span><span class="sxs-lookup"><span data-stu-id="099f2-112">URL Path Parameter</span></span> | <span data-ttu-id="099f2-113">groupId</span><span class="sxs-lookup"><span data-stu-id="099f2-113">groupId</span></span> | <span data-ttu-id="099f2-114">Chaîne</span><span class="sxs-lookup"><span data-stu-id="099f2-114">String</span></span> | <span data-ttu-id="099f2-115">Non</span><span class="sxs-lookup"><span data-stu-id="099f2-115">No</span></span> | <span data-ttu-id="099f2-116">GUID représentant le groupId de la ressource groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="099f2-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="099f2-117">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="099f2-117">HTTP Header</span></span> | <span data-ttu-id="099f2-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="099f2-118">accessToken</span></span> | <span data-ttu-id="099f2-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="099f2-119">String</span></span> | <span data-ttu-id="099f2-120">Non</span><span class="sxs-lookup"><span data-stu-id="099f2-120">No</span></span> | <span data-ttu-id="099f2-121">Reçu à partir de la fin de l’authentification par jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="099f2-121">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="099f2-122">En-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="099f2-122">HTTP Header</span></span> | <span data-ttu-id="099f2-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="099f2-123">Content-Type</span></span> | <span data-ttu-id="099f2-124">Chaîne</span><span class="sxs-lookup"><span data-stu-id="099f2-124">String</span></span> | <span data-ttu-id="099f2-125">Non</span><span class="sxs-lookup"><span data-stu-id="099f2-125">No</span></span> | <span data-ttu-id="099f2-126">valeur : application/json</span><span class="sxs-lookup"><span data-stu-id="099f2-126">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="099f2-127">Corps de la requête</span><span class="sxs-lookup"><span data-stu-id="099f2-127">Request body</span></span>

| <span data-ttu-id="099f2-128">Paramètre</span><span class="sxs-lookup"><span data-stu-id="099f2-128">Parameter</span></span> | <span data-ttu-id="099f2-129">Type</span><span class="sxs-lookup"><span data-stu-id="099f2-129">Type</span></span> | <span data-ttu-id="099f2-130">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="099f2-130">Optional?</span></span> | <span data-ttu-id="099f2-131">Description</span><span class="sxs-lookup"><span data-stu-id="099f2-131">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="099f2-132">message</span><span class="sxs-lookup"><span data-stu-id="099f2-132">message</span></span> | <span data-ttu-id="099f2-133">Chaîne</span><span class="sxs-lookup"><span data-stu-id="099f2-133">String</span></span> | <span data-ttu-id="099f2-134">Non</span><span class="sxs-lookup"><span data-stu-id="099f2-134">No</span></span> | <span data-ttu-id="099f2-135">Message texte envoyé (limite maximale de 1 000 caractères)</span><span class="sxs-lookup"><span data-stu-id="099f2-135">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="099f2-136">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="099f2-136">sendToAllSubscribers</span></span> | <span data-ttu-id="099f2-137">Bool</span><span class="sxs-lookup"><span data-stu-id="099f2-137">Bool</span></span> | <span data-ttu-id="099f2-138">Oui</span><span class="sxs-lookup"><span data-stu-id="099f2-138">Yes</span></span> | <span data-ttu-id="099f2-139">Par défaut : false.</span><span class="sxs-lookup"><span data-stu-id="099f2-139">Default: false.</span></span> <span data-ttu-id="099f2-140">Valide uniquement dans les cas groupId appartient à un groupe Public.</span><span class="sxs-lookup"><span data-stu-id="099f2-140">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="099f2-141">True pour envoyer le message à tous les abonnés qui requiert l’utilisateur du jeton admin du groupe Public</span><span class="sxs-lookup"><span data-stu-id="099f2-141">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="099f2-142">abonnés</span><span class="sxs-lookup"><span data-stu-id="099f2-142">subscribers</span></span> | <span data-ttu-id="099f2-143">String]</span><span class="sxs-lookup"><span data-stu-id="099f2-143">String[]</span></span> | <span data-ttu-id="099f2-144">Oui</span><span class="sxs-lookup"><span data-stu-id="099f2-144">Yes</span></span> | <span data-ttu-id="099f2-145">Chaque élément correspond à un numéro de téléphone mobile (avec le code du pays.</span><span class="sxs-lookup"><span data-stu-id="099f2-145">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="099f2-146">Par exemple.</span><span class="sxs-lookup"><span data-stu-id="099f2-146">Eg.</span></span> <span data-ttu-id="099f2-147">+911999999999).</span><span class="sxs-lookup"><span data-stu-id="099f2-147">+911999999999).</span></span> <span data-ttu-id="099f2-148">Message texte sera envoyé uniquement pour les abonnés sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="099f2-148">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="099f2-149">À utiliser pour la communication sélective aux abonnés dans le contexte d’un groupe Public</span><span class="sxs-lookup"><span data-stu-id="099f2-149">To be used for selective communication to subscribers in context of a Public Group</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="099f2-150">Exemple de demande JSON</span><span class="sxs-lookup"><span data-stu-id="099f2-150">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

##### <a name="response-body"></a><span data-ttu-id="099f2-151">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="099f2-151">Response body</span></span>

| <span data-ttu-id="099f2-152">Paramètre</span><span class="sxs-lookup"><span data-stu-id="099f2-152">Parameter</span></span> | <span data-ttu-id="099f2-153">Type</span><span class="sxs-lookup"><span data-stu-id="099f2-153">Type</span></span> | <span data-ttu-id="099f2-154">Description</span><span class="sxs-lookup"><span data-stu-id="099f2-154">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="099f2-155">referenceId</span><span class="sxs-lookup"><span data-stu-id="099f2-155">referenceId</span></span> | <span data-ttu-id="099f2-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="099f2-156">String</span></span> | <span data-ttu-id="099f2-157">GUID représentant l’achèvement succesful de la demande</span><span class="sxs-lookup"><span data-stu-id="099f2-157">GUID representing the succesful completion of the request</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="099f2-158">Exemple de réponse JSON</span><span class="sxs-lookup"><span data-stu-id="099f2-158">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
