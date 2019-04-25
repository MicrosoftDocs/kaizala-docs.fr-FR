---
title: Vue d’ensemble
description: Vue d'ensemble de la plateforme de développement Microsoft Kaizala
topic: overview
author: nitinjms
ms.openlocfilehash: 74d0cb957b81354c6f9d7c359eccf554910d283d
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190699"
---
# <a name="microsoft-kaizala-developer-documentation"></a><span data-ttu-id="0022e-103">Documentation du développeur Microsoft Kaizala</span><span class="sxs-lookup"><span data-stu-id="0022e-103">Microsoft Kaizala Developer Documentation</span></span>

<span data-ttu-id="0022e-104">Kaizala est une application de productivité et de messagerie qui permet à vos utilisateurs mobiles d'obtenir plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="0022e-104">Kaizala is a messaging and productivity app that enable your mobile users to achieve more.</span></span> <span data-ttu-id="0022e-105">Avec Kaizala, vous pouvez avoir 1:1 chat avec des individus, discuter avec vos équipes et même ajouter des groupes à vos groupes existants pour communiquer dans les grandes organisations ou les communautés.</span><span class="sxs-lookup"><span data-stu-id="0022e-105">With Kaizala, you can have 1:1 chat with individuals, group chat with your teams, and even add groups to your existing groups to communicate within large organizations or communities.</span></span>

> <span data-ttu-id="0022e-106">**Vous n'avez pas Kaizala? Téléchargez l'application maintenant pour Windows Phone, Android & iOS. [Voici comment procéder](install.md).**</span><span class="sxs-lookup"><span data-stu-id="0022e-106">**Don't have Kaizala? Download the app now for Windows Phone, Android & iOS. [Here's how](install.md).**</span></span>

## <a name="microsoft-kaizala-developer-platform"></a><span data-ttu-id="0022e-107">Plateforme de développement Microsoft Kaizala</span><span class="sxs-lookup"><span data-stu-id="0022e-107">Microsoft Kaizala Developer Platform</span></span> 
<span data-ttu-id="0022e-108">La plateforme de développeur Kaizala offre plusieurs façons d'intégrer et d'étendre Kaizala afin de répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0022e-108">The Kaizala Developer Platform offers multiple ways to integrate and extend Kaizala to suit your organizational needs.</span></span> <span data-ttu-id="0022e-109">Avec l'aperçu du développeur, vous pouvez utiliser des connecteurs pour intégrer Kaizala à vos processus métiers et concevoir des actions personnalisées via le portail de gestion Kaizala.</span><span class="sxs-lookup"><span data-stu-id="0022e-109">With the developer preview, you can use Connectors to integrate Kaizala with your business processes and design custom Actions through the Kaizala Management Portal.</span></span>

## <a name="connectors"></a><span data-ttu-id="0022e-110">Connecteurs</span><span class="sxs-lookup"><span data-stu-id="0022e-110">Connectors</span></span>

<span data-ttu-id="0022e-111">Les connecteurs Kaizala permettent aux développeurs tiers d'intégrer Kaizala à leurs processus métier en leur permettant d'effectuer un ensemble d'actions organisée dans Kaizala à l'aide d'appels d'API basés sur REST.</span><span class="sxs-lookup"><span data-stu-id="0022e-111">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="0022e-112">L'étendue de l'API est destinée aux systèmes externes pour appeler le point de terminaison et effectuer des actions à la demande.</span><span class="sxs-lookup"><span data-stu-id="0022e-112">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="0022e-113">Autrement dit, il s'agit d'un modèle d'extraction, où les points de terminaison individuels doivent être appelés pour effectuer des actions spécifiques à l'aide des **[API](connectors/API.md)** Kaizala.</span><span class="sxs-lookup"><span data-stu-id="0022e-113">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](connectors/API.md)**.</span></span> <span data-ttu-id="0022e-114">Le modèle poussé dans lequel la plateforme Kaizala peut déclencher des actions peut **[](connectors/webHooks.md)** être configuré à l'aide des webhooks.</span><span class="sxs-lookup"><span data-stu-id="0022e-114">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](connectors/webHooks.md)**.</span></span>

[<span data-ttu-id="0022e-115">Prise en main des connecteurs</span><span class="sxs-lookup"><span data-stu-id="0022e-115">Get started with Connectors</span></span>](connectors/README.md)

## <a name="kaizala-actions"></a><span data-ttu-id="0022e-116">Actions Kaizala</span><span class="sxs-lookup"><span data-stu-id="0022e-116">Kaizala Actions</span></span>

<span data-ttu-id="0022e-117">Les actions Kaizala sont des «unités de travail» qui aident les utilisateurs à effectuer des tâches dans un contexte de conversation à l'intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="0022e-117">Kaizala Actions are basic 'units of work' that help users get work done within a conversation context inside Kaizala.</span></span> <span data-ttu-id="0022e-118">Certaines de ces actions, telles que Job, Survey, Poll, etc., sont fournies en tout ou partie.</span><span class="sxs-lookup"><span data-stu-id="0022e-118">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box and provide scoped functionality.</span></span> <span data-ttu-id="0022e-119">Ces actions peuvent être découvertes dans l'application Kaizala et peuvent être appelées dans un contexte de conversation à partir de la palette d'actions.</span><span class="sxs-lookup"><span data-stu-id="0022e-119">These Actions can be discovered within the Kaizala app and can be invoked in a conversation context from the Action Palette.</span></span>

[<span data-ttu-id="0022e-120">Prise en main des actions Kaizala</span><span class="sxs-lookup"><span data-stu-id="0022e-120">Get started with Kaizala Actions</span></span>](Actions/README.md)

## <a name="submit-your-questions-bugs-feature-requests-and-contributions"></a><span data-ttu-id="0022e-121">Envoyer vos questions, bogues, demandes de fonctionnalité et contributions</span><span class="sxs-lookup"><span data-stu-id="0022e-121">Submit your questions, bugs, feature requests, and contributions</span></span>

<span data-ttu-id="0022e-122">Nous écoutons la communauté des développeurs sur [plusieurs canaux](feedback.md).</span><span class="sxs-lookup"><span data-stu-id="0022e-122">We listen to the developer community across [several channels](feedback.md).</span></span>
