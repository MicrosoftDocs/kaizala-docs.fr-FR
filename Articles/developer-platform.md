---
title: Vue d’ensemble
description: Vue d’ensemble de la plateforme de développement de Microsoft Kaizala
topic: overview
author: nitinjms
ms.openlocfilehash: 74d0cb957b81354c6f9d7c359eccf554910d283d
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905138"
---
# <a name="microsoft-kaizala-developer-documentation"></a><span data-ttu-id="509d7-103">Documentation pour les développeurs Microsoft Kaizala</span><span class="sxs-lookup"><span data-stu-id="509d7-103">Microsoft Kaizala Developer Documentation</span></span>

<span data-ttu-id="509d7-104">Kaizala est une application de messagerie et de la productivité qui permettent de vos utilisateurs mobiles obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="509d7-104">Kaizala is a messaging and productivity app that enable your mobile users to achieve more.</span></span> <span data-ttu-id="509d7-105">Avec Kaizala, vous pouvez avoir 1:1 conversation avec des personnes, la conversation de groupe avec vos équipes et même ajouter des groupes à vos groupes existants pour communiquer dans les grandes organisations ou des Communautés.</span><span class="sxs-lookup"><span data-stu-id="509d7-105">With Kaizala, you can have 1:1 chat with individuals, group chat with your teams, and even add groups to your existing groups to communicate within large organizations or communities.</span></span>

> <span data-ttu-id="509d7-106">**Vous n’avez Kaizala ? Télécharger l’application maintenant pour Windows Phone, Android & iOS. [Voici comment](install.md).**</span><span class="sxs-lookup"><span data-stu-id="509d7-106">**Don't have Kaizala? Download the app now for Windows Phone, Android & iOS. [Here's how](install.md).**</span></span>

## <a name="microsoft-kaizala-developer-platform"></a><span data-ttu-id="509d7-107">Plateforme de développement de Microsoft Kaizala</span><span class="sxs-lookup"><span data-stu-id="509d7-107">Microsoft Kaizala Developer Platform</span></span> 
<span data-ttu-id="509d7-108">La plateforme de développement Kaizala offre plusieurs façons d’intégrer et étendre Kaizala en fonction des besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="509d7-108">The Kaizala Developer Platform offers multiple ways to integrate and extend Kaizala to suit your organizational needs.</span></span> <span data-ttu-id="509d7-109">Avec l’aperçu pour les développeurs, vous pouvez utiliser des connecteurs pour intégrer Kaizala à vos processus d’entreprise et concevoir les Actions personnalisées par le biais du portail de gestion Kaizala.</span><span class="sxs-lookup"><span data-stu-id="509d7-109">With the developer preview, you can use Connectors to integrate Kaizala with your business processes and design custom Actions through the Kaizala Management Portal.</span></span>

## <a name="connectors"></a><span data-ttu-id="509d7-110">Connecteurs</span><span class="sxs-lookup"><span data-stu-id="509d7-110">Connectors</span></span>

<span data-ttu-id="509d7-111">Connecteurs Kaizala activer 3e développeurs tiers d’intégrer Kaizala leurs processus d’entreprise en fournissant des appels d’API en fonction de la capacité à exécuter un ensemble d’actions curated dans Kaizala à l’aide de REST.</span><span class="sxs-lookup"><span data-stu-id="509d7-111">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="509d7-112">L’étendue de l’API est pour les systèmes externes pour le point de terminaison d’appel et effectuer des actions sur la demande.</span><span class="sxs-lookup"><span data-stu-id="509d7-112">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="509d7-113">Autrement dit, il s’agit d’un modèle de collecte – où les points de terminaison individuels doivent être appelée pour effectuer des actions spécifiques à l’aide Kaizala **[API](connectors/API.md)**.</span><span class="sxs-lookup"><span data-stu-id="509d7-113">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](connectors/API.md)**.</span></span> <span data-ttu-id="509d7-114">Le modèle PUSH où plateforme Kaizala peut déclencher des actions permettre être configuré à l’aide de **[webhooks](connectors/webHooks.md)**.</span><span class="sxs-lookup"><span data-stu-id="509d7-114">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](connectors/webHooks.md)**.</span></span>

[<span data-ttu-id="509d7-115">Prendre en main les connecteurs</span><span class="sxs-lookup"><span data-stu-id="509d7-115">Get started with Connectors</span></span>](connectors/README.md)

## <a name="kaizala-actions"></a><span data-ttu-id="509d7-116">Actions Kaizala</span><span class="sxs-lookup"><span data-stu-id="509d7-116">Kaizala Actions</span></span>

<span data-ttu-id="509d7-117">Actions Kaizala sont base « unités de travail » qui permettent aux utilisateurs de travailler dans un contexte de conversation à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="509d7-117">Kaizala Actions are basic 'units of work' that help users get work done within a conversation context inside Kaizala.</span></span> <span data-ttu-id="509d7-118">Certaines de ces Actions comme tâche, enquête, sondage, etc. sont expédié out-de-the-box et fournissent des fonctionnalités étendues.</span><span class="sxs-lookup"><span data-stu-id="509d7-118">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box and provide scoped functionality.</span></span> <span data-ttu-id="509d7-119">Ces Actions peuvent être découverts au sein de l’application Kaizala et peuvent être appelées dans un contexte de conversation dans la Palette de l’Action.</span><span class="sxs-lookup"><span data-stu-id="509d7-119">These Actions can be discovered within the Kaizala app and can be invoked in a conversation context from the Action Palette.</span></span>

[<span data-ttu-id="509d7-120">Prendre en main Kaizala Actions</span><span class="sxs-lookup"><span data-stu-id="509d7-120">Get started with Kaizala Actions</span></span>](Actions/README.md)

## <a name="submit-your-questions-bugs-feature-requests-and-contributions"></a><span data-ttu-id="509d7-121">Soumettre vos questions, bogues, demandes de fonctionnalités et collaboration</span><span class="sxs-lookup"><span data-stu-id="509d7-121">Submit your questions, bugs, feature requests, and contributions</span></span>

<span data-ttu-id="509d7-122">Nous écouter la Communauté des développeurs sur [plusieurs canaux](feedback.md).</span><span class="sxs-lookup"><span data-stu-id="509d7-122">We listen to the developer community across [several channels](feedback.md).</span></span>
