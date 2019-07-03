---
title: API Kaizala
description: Liste des API que Kaizala expose pour permettre l’intégration à des systèmes tiers
topic: Reference
author: nitinjms
ms.openlocfilehash: 221d421feeeb2528f185fa205c7cfa81207a8478
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535683"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="de70f-103">Documentation de l’API Kaizala</span><span class="sxs-lookup"><span data-stu-id="de70f-103">Kaizala API Documentation</span></span>

<span data-ttu-id="de70f-104">Avant de commencer, reportez-vous à [la rubrique Configuration de l’utilisation des connecteurs Kaizala](setup.md)</span><span class="sxs-lookup"><span data-stu-id="de70f-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="de70f-105">Domaine racine</span><span class="sxs-lookup"><span data-stu-id="de70f-105">Root Domain</span></span>

<span data-ttu-id="de70f-106">Le domaine racine pour l’appel des API Kaizala est le suivant:</span><span class="sxs-lookup"><span data-stu-id="de70f-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="de70f-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="de70f-107">Parameter</span></span>             | <span data-ttu-id="de70f-108">Type</span><span class="sxs-lookup"><span data-stu-id="de70f-108">Type</span></span>      | <span data-ttu-id="de70f-109">Module?</span><span class="sxs-lookup"><span data-stu-id="de70f-109">Optional?</span></span>     | <span data-ttu-id="de70f-110">Description</span><span class="sxs-lookup"><span data-stu-id="de70f-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="de70f-111">URL du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="de70f-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="de70f-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="de70f-112">String</span></span>    | <span data-ttu-id="de70f-113">Non</span><span class="sxs-lookup"><span data-stu-id="de70f-113">No</span></span>            | <span data-ttu-id="de70f-114">Lors de l’authentification réussie lors de la génération de jetons d’accès, une URL de point de terminaison est renvoyée qui doit être utilisée comme URL de base de l’API pour effectuer les appels d’API suivants</span><span class="sxs-lookup"><span data-stu-id="de70f-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

<span data-ttu-id="de70f-115">Notez que lorsque vous accédez à une API Kaizala, vous pouvez obtenir le code d’État http: 308 indiquant que l’URL de point de terminaison de l’utilisateur a changé.</span><span class="sxs-lookup"><span data-stu-id="de70f-115">Please note that while hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="de70f-116">Dans ce cas, l’emplacement de l’en-tête de réponse contiendra la nouvelle URL de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="de70f-116">In that case, Response header location will contain the new endpoint-url.</span></span>

### <a name="api-end-points"></a><span data-ttu-id="de70f-117">Points de terminaison d’API</span><span class="sxs-lookup"><span data-stu-id="de70f-117">API End-points</span></span>

<span data-ttu-id="de70f-118">L’API Kaizala s’exécute sur le Cloud Microsoft Azure sécurisé et interagit avec la plateforme Kaizala pour effectuer différentes actions pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="de70f-118">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="de70f-119">L’API fonctionne avec les ressources Kaizala suivantes:</span><span class="sxs-lookup"><span data-stu-id="de70f-119">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="de70f-120">/groups</span><span class="sxs-lookup"><span data-stu-id="de70f-120">/groups</span></span>](groups.md)
*   [<span data-ttu-id="de70f-121">/subGroups</span><span class="sxs-lookup"><span data-stu-id="de70f-121">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="de70f-122">/members</span><span class="sxs-lookup"><span data-stu-id="de70f-122">/members</span></span>](members.md)
*   [<span data-ttu-id="de70f-123">/messages</span><span class="sxs-lookup"><span data-stu-id="de70f-123">/messages</span></span>](messages.md)
*   [<span data-ttu-id="de70f-124">/media</span><span class="sxs-lookup"><span data-stu-id="de70f-124">/media</span></span>](media.md)
*   [<span data-ttu-id="de70f-125">/actions</span><span class="sxs-lookup"><span data-stu-id="de70f-125">/actions</span></span>](actions.md)
*   [<span data-ttu-id="de70f-126">/subscribers</span><span class="sxs-lookup"><span data-stu-id="de70f-126">/subscribers</span></span>](subscribers.md)
*    [<span data-ttu-id="de70f-127">/reaction</span><span class="sxs-lookup"><span data-stu-id="de70f-127">/reaction</span></span>](reactions.md)

### <a name="webhooks"></a><span data-ttu-id="de70f-128">WebHooks</span><span class="sxs-lookup"><span data-stu-id="de70f-128">WebHooks</span></span>

<span data-ttu-id="de70f-129">L’API Microsoft Kaizala offre également aux développeurs la possibilité d’enregistrer des événements spécifiques dans la plateforme Kaizala via des webhooks.</span><span class="sxs-lookup"><span data-stu-id="de70f-129">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="de70f-130">/webhook</span><span class="sxs-lookup"><span data-stu-id="de70f-130">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="de70f-131">Collection postale</span><span class="sxs-lookup"><span data-stu-id="de70f-131">Postman Collection</span></span>

<span data-ttu-id="de70f-132">Pour tester nos API, ainsi que comprendre le schéma de l’API Kaizala, vous pouvez importer une collection postale contenant des exemples et du schéma pour toutes les API Kaizala Microsoft:</span><span class="sxs-lookup"><span data-stu-id="de70f-132">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="de70f-133">[![Exécuter dans le poteau](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="de70f-133">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="de70f-134">Définissez les variables d’environnement suivantes dans «Kaizala-APIs-Environment» avant d’exécuter le projet post:</span><span class="sxs-lookup"><span data-stu-id="de70f-134">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="de70f-135">Numéro de téléphone mobile: votre numéro de téléphone mobile qui sera utilisé pour l’appel des API</span><span class="sxs-lookup"><span data-stu-id="de70f-135">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="de70f-136">application-ID: ID associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="de70f-136">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="de70f-137">clé d’application: secret associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="de70f-137">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="de70f-138">D’autres variables d’environnement seront renseignées automatiquement lors de la tentative d’indication des API dans la séquence dans le projet post.</span><span class="sxs-lookup"><span data-stu-id="de70f-138">Other environment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="de70f-139">Prise en main des API REST Kaizala</span><span class="sxs-lookup"><span data-stu-id="de70f-139">Getting started with Kaizala REST APIs</span></span> 

[<span data-ttu-id="de70f-140">Exemple C# (partagé)</span><span class="sxs-lookup"><span data-stu-id="de70f-140">C# sample (shared)</span></span>](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
