---
title: API Kaizala
description: Liste des API que Kaizala expose pour permettre l’intégration avec des systèmes tiers 3
topic: Reference
author: nitinjms
ms.openlocfilehash: 06cb4b8d4883d0d9a50479cf9c9da048cc42e3a7
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905103"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="95b93-103">Documentation Kaizala API</span><span class="sxs-lookup"><span data-stu-id="95b93-103">Kaizala API Documentation</span></span>

<span data-ttu-id="95b93-104">Avant de commencer, reportez-vous au [programme d’installation pour l’utilisation de connecteurs Kaizala](setup.md)</span><span class="sxs-lookup"><span data-stu-id="95b93-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="95b93-105">Domaine racine</span><span class="sxs-lookup"><span data-stu-id="95b93-105">Root Domain</span></span>

<span data-ttu-id="95b93-106">Le domaine racine pour appeler les APIs Kaizala est la suivante :</span><span class="sxs-lookup"><span data-stu-id="95b93-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="95b93-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="95b93-107">Parameter</span></span>             | <span data-ttu-id="95b93-108">Type</span><span class="sxs-lookup"><span data-stu-id="95b93-108">Type</span></span>      | <span data-ttu-id="95b93-109">Facultatif ?</span><span class="sxs-lookup"><span data-stu-id="95b93-109">Optional?</span></span>     | <span data-ttu-id="95b93-110">Description</span><span class="sxs-lookup"><span data-stu-id="95b93-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="95b93-111">Url du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="95b93-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="95b93-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="95b93-112">String</span></span>    | <span data-ttu-id="95b93-113">Non</span><span class="sxs-lookup"><span data-stu-id="95b93-113">No</span></span>            | <span data-ttu-id="95b93-114">Authentification réussie lors de la génération jetons d’accès, une url de point de terminaison est renvoyée qui doivent être utilisées comme url de base d’api pour effectuer des appels d’API suivants</span><span class="sxs-lookup"><span data-stu-id="95b93-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

<span data-ttu-id="95b93-115">Veuillez noter que tout en appuyant sur n’importe quelle api Kaizala, vous pouvez obtenir l’état Http code : 308 indiquant que l’url de terminaison de l’utilisateur a changé.</span><span class="sxs-lookup"><span data-stu-id="95b93-115">Please note that while hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="95b93-116">Emplacement de l’en-tête réponse contient dans ce cas, la nouvelle url de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="95b93-116">In that case, Response header location will contain the new endpoint-url.</span></span>

### <a name="api-end-points"></a><span data-ttu-id="95b93-117">API de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="95b93-117">API End-points</span></span>

<span data-ttu-id="95b93-118">L’API Kaizala s’exécute sur le cloud Microsoft Azure sécurisé et interagit avec la plateforme Kaizala pour effectuer des actions différentes pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="95b93-118">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="95b93-119">L’API fonctionne avec les ressources Kaizala suivantes :</span><span class="sxs-lookup"><span data-stu-id="95b93-119">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="95b93-120">/Groups</span><span class="sxs-lookup"><span data-stu-id="95b93-120">/groups</span></span>](groups.md)
*   [<span data-ttu-id="95b93-121">/subGroups</span><span class="sxs-lookup"><span data-stu-id="95b93-121">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="95b93-122">/Members</span><span class="sxs-lookup"><span data-stu-id="95b93-122">/members</span></span>](members.md)
*   [<span data-ttu-id="95b93-123">/messages</span><span class="sxs-lookup"><span data-stu-id="95b93-123">/messages</span></span>](messages.md)
*   [<span data-ttu-id="95b93-124">/ Media</span><span class="sxs-lookup"><span data-stu-id="95b93-124">/media</span></span>](media.md)
*   [<span data-ttu-id="95b93-125">/actions</span><span class="sxs-lookup"><span data-stu-id="95b93-125">/actions</span></span>](actions.md)
*   [<span data-ttu-id="95b93-126">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="95b93-126">/subscribers</span></span>](subscribers.md)

### <a name="webhooks"></a><span data-ttu-id="95b93-127">WebHooks</span><span class="sxs-lookup"><span data-stu-id="95b93-127">WebHooks</span></span>

<span data-ttu-id="95b93-128">L’API de Kaizala Microsoft permet également aux développeurs d’enregistrer des événements spécifiques au sein de la plateforme Kaizala via WebHooks.</span><span class="sxs-lookup"><span data-stu-id="95b93-128">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="95b93-129">/webhook</span><span class="sxs-lookup"><span data-stu-id="95b93-129">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="95b93-130">Collection postman</span><span class="sxs-lookup"><span data-stu-id="95b93-130">Postman Collection</span></span>

<span data-ttu-id="95b93-131">Afin de tester notre API, ainsi que comprendre API Kaizala schéma, vous pouvez importer collection postman contenant des exemples et schéma pour toutes les API Microsoft Kaizala :</span><span class="sxs-lookup"><span data-stu-id="95b93-131">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="95b93-132">[![Exécuter dans Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="95b93-132">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="95b93-133">Configurez les variables d’environnement dans « Kaizala-API-environment » avant d’exécuter le projet postman suivantes :</span><span class="sxs-lookup"><span data-stu-id="95b93-133">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="95b93-134">numéro de Mobile : votre numéro de téléphone mobile qui sera utilisé pour appeler des API</span><span class="sxs-lookup"><span data-stu-id="95b93-134">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="95b93-135">id d’application : ID associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="95b93-135">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="95b93-136">clé secrète de l’application : Secret associé au connecteur</span><span class="sxs-lookup"><span data-stu-id="95b93-136">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="95b93-137">Autres variables d’environnement sera remplie automatiquement lors de l’API de séquence abordées dans le projet Postman.</span><span class="sxs-lookup"><span data-stu-id="95b93-137">Other enviroment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="95b93-138">Mise en route avec l’API REST de Kaizala</span><span class="sxs-lookup"><span data-stu-id="95b93-138">Getting started with Kaizala REST APIs</span></span> 

<span data-ttu-id="95b93-139">[Exemple c# (partagé)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)</span><span class="sxs-lookup"><span data-stu-id="95b93-139">[C# sample (shared)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)</span></span>
