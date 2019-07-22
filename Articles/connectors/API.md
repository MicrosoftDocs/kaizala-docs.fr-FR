---
title: API Kaizala
description: Liste des API que Kaizala expose pour permettre l’intégration à des systèmes tiers
topic: Reference
author: nitinjms
ms.openlocfilehash: c46e15ec9bd88ebbaf1d0d1a1241f1bfd892c00a
ms.sourcegitcommit: 19e8481e67d9178efb7ea6ca19831ee7a9fa4a8b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2019
ms.locfileid: "35811959"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="a0348-103">Documentation de l’API Kaizala</span><span class="sxs-lookup"><span data-stu-id="a0348-103">Kaizala API Documentation</span></span>

<span data-ttu-id="a0348-104">Avant de commencer, reportez-vous à [la rubrique Configuration de l’utilisation des connecteurs Kaizala](setup.md)</span><span class="sxs-lookup"><span data-stu-id="a0348-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="a0348-105">Domaine racine</span><span class="sxs-lookup"><span data-stu-id="a0348-105">Root Domain</span></span>

<span data-ttu-id="a0348-106">Le domaine racine pour l’appel des API Kaizala est le suivant:</span><span class="sxs-lookup"><span data-stu-id="a0348-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="a0348-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0348-107">Parameter</span></span>             | <span data-ttu-id="a0348-108">Type</span><span class="sxs-lookup"><span data-stu-id="a0348-108">Type</span></span>      | <span data-ttu-id="a0348-109">Module?</span><span class="sxs-lookup"><span data-stu-id="a0348-109">Optional?</span></span>     | <span data-ttu-id="a0348-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0348-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="a0348-111">URL du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a0348-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="a0348-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="a0348-112">String</span></span>    | <span data-ttu-id="a0348-113">Non</span><span class="sxs-lookup"><span data-stu-id="a0348-113">No</span></span>            | <span data-ttu-id="a0348-114">Lors de l’authentification réussie lors de la génération de jetons d’accès, une URL de point de terminaison est renvoyée qui doit être utilisée comme URL de base de l’API pour effectuer les appels d’API suivants</span><span class="sxs-lookup"><span data-stu-id="a0348-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

> <span data-ttu-id="a0348-115">Tout en accédant à une API Kaizala, vous pouvez obtenir le code d’État http: 308 indiquant que l’URL de point de terminaison de l’utilisateur a changé.</span><span class="sxs-lookup"><span data-stu-id="a0348-115">While hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="a0348-116">Dans ce cas, l’emplacement de l’en-tête de réponse contiendra la nouvelle URL de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a0348-116">In that case, Response header location will contain the new endpoint-url.</span></span>

> <span data-ttu-id="a0348-117">**Suggestion:** Les clients peuvent configurer le délai d’expiration pour recevoir une réponse des API Kaizala à 1 min</span><span class="sxs-lookup"><span data-stu-id="a0348-117">**Suggestion:** Clients can configure timeout to receive response from Kaizala APIs at 1 min</span></span>

### <a name="api-end-points"></a><span data-ttu-id="a0348-118">Points de terminaison d’API</span><span class="sxs-lookup"><span data-stu-id="a0348-118">API End-points</span></span>

<span data-ttu-id="a0348-119">L’API Kaizala s’exécute sur le Cloud Microsoft Azure sécurisé et interagit avec la plateforme Kaizala pour effectuer différentes actions pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="a0348-119">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="a0348-120">L’API fonctionne avec les ressources Kaizala suivantes:</span><span class="sxs-lookup"><span data-stu-id="a0348-120">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="a0348-121">/groups</span><span class="sxs-lookup"><span data-stu-id="a0348-121">/groups</span></span>](groups.md)
*   [<span data-ttu-id="a0348-122">/subGroups</span><span class="sxs-lookup"><span data-stu-id="a0348-122">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="a0348-123">/members</span><span class="sxs-lookup"><span data-stu-id="a0348-123">/members</span></span>](members.md)
*   [<span data-ttu-id="a0348-124">/messages</span><span class="sxs-lookup"><span data-stu-id="a0348-124">/messages</span></span>](messages.md)
*   [<span data-ttu-id="a0348-125">/media</span><span class="sxs-lookup"><span data-stu-id="a0348-125">/media</span></span>](media.md)
*   [<span data-ttu-id="a0348-126">/actions</span><span class="sxs-lookup"><span data-stu-id="a0348-126">/actions</span></span>](actions.md)
*   [<span data-ttu-id="a0348-127">/subscribers</span><span class="sxs-lookup"><span data-stu-id="a0348-127">/subscribers</span></span>](subscribers.md)
*    [<span data-ttu-id="a0348-128">/reaction</span><span class="sxs-lookup"><span data-stu-id="a0348-128">/reaction</span></span>](reactions.md)

### <a name="webhooks"></a><span data-ttu-id="a0348-129">WebHooks</span><span class="sxs-lookup"><span data-stu-id="a0348-129">WebHooks</span></span>

<span data-ttu-id="a0348-130">L’API Microsoft Kaizala offre également aux développeurs la possibilité d’enregistrer des événements spécifiques dans la plateforme Kaizala via des webhooks.</span><span class="sxs-lookup"><span data-stu-id="a0348-130">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="a0348-131">/webhook</span><span class="sxs-lookup"><span data-stu-id="a0348-131">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="a0348-132">Collection postale</span><span class="sxs-lookup"><span data-stu-id="a0348-132">Postman Collection</span></span>

<span data-ttu-id="a0348-133">Pour tester nos API, ainsi que comprendre le schéma de l’API Kaizala, vous pouvez importer une collection postale contenant des exemples et du schéma pour toutes les API Kaizala Microsoft:</span><span class="sxs-lookup"><span data-stu-id="a0348-133">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="a0348-134">[![Exécuter dans le poteau](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="a0348-134">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="a0348-135">Définissez les variables d’environnement suivantes dans «Kaizala-APIs-Environment» avant d’exécuter le projet post:</span><span class="sxs-lookup"><span data-stu-id="a0348-135">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="a0348-136">Numéro de téléphone mobile: votre numéro de téléphone mobile qui sera utilisé pour l’appel des API</span><span class="sxs-lookup"><span data-stu-id="a0348-136">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="a0348-137">application-ID: ID associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="a0348-137">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="a0348-138">clé d’application: secret associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="a0348-138">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="a0348-139">D’autres variables d’environnement seront renseignées automatiquement lors de la tentative d’indication des API dans la séquence dans le projet post.</span><span class="sxs-lookup"><span data-stu-id="a0348-139">Other environment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="a0348-140">Prise en main des API REST Kaizala</span><span class="sxs-lookup"><span data-stu-id="a0348-140">Getting started with Kaizala REST APIs</span></span> 

[<span data-ttu-id="a0348-141">Exemple C# (partagé)</span><span class="sxs-lookup"><span data-stu-id="a0348-141">C# sample (shared)</span></span>](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
