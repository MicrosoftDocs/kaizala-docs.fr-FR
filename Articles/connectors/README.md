---
title: Connecteurs
description: Article permettant de fournir une vue d'ensemble des connecteurs Kaizala
topic: Overview
author: nitinjms
ms.openlocfilehash: 94c6844cfa8f5a85da26c3ab27dc38a366fbc97e
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190795"
---
# <a name="connectors"></a><span data-ttu-id="2906b-103">Connecteurs</span><span class="sxs-lookup"><span data-stu-id="2906b-103">Connectors</span></span>

## <a name="overview"></a><span data-ttu-id="2906b-104">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="2906b-104">Overview</span></span>
<span data-ttu-id="2906b-105">Les connecteurs Kaizala permettent aux développeurs tiers d'intégrer Kaizala à leurs processus métier en leur permettant d'effectuer un ensemble d'actions organisée dans Kaizala à l'aide d'appels d'API basés sur REST.</span><span class="sxs-lookup"><span data-stu-id="2906b-105">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="2906b-106">L'étendue de l'API est destinée aux systèmes externes pour appeler le point de terminaison et effectuer des actions à la demande.</span><span class="sxs-lookup"><span data-stu-id="2906b-106">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="2906b-107">Autrement dit, il s'agit d'un modèle d'extraction, où les points de terminaison individuels doivent être appelés pour effectuer des actions spécifiques à l'aide des **[API](API.md)** Kaizala.</span><span class="sxs-lookup"><span data-stu-id="2906b-107">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](API.md)**.</span></span> <span data-ttu-id="2906b-108">Le modèle poussé dans lequel la plateforme Kaizala peut déclencher des actions peut **[](webHooks.md)** être configuré à l'aide des webhooks.</span><span class="sxs-lookup"><span data-stu-id="2906b-108">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](webHooks.md)**.</span></span>

<span data-ttu-id="2906b-109">Les connecteurs Kaizala sont actuellement étendus aux groupes, c'est-à-dire que chaque connecteur Kaizala doit explicitement disposer des autorisations d'accès à un groupe de conversation, puis effectuer des actions par le biais des points de terminaison de l'API uniquement dans le contexte du groupe.</span><span class="sxs-lookup"><span data-stu-id="2906b-109">Kaizala Connectors are currently group-scoped - i.e. each Kaizala Connector needs to explicitly be granted permissions to a Conversation group - and then can perform actions through the API end-points only within the context of the group.</span></span> <span data-ttu-id="2906b-110">Toutefois, chaque connecteur Kaizala peut être autorisé à accéder à plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="2906b-110">However, each Kaizala Connector can be granted access to multiple groups.</span></span>

* [<span data-ttu-id="2906b-111">Configuration de l'utilisation des connecteurs Kaizala</span><span class="sxs-lookup"><span data-stu-id="2906b-111">Setup for using the Kaizala Connectors</span></span>](setup.md)
* [<span data-ttu-id="2906b-112">Documentation de l'API</span><span class="sxs-lookup"><span data-stu-id="2906b-112">API Documentation</span></span>](API.md)
* [<span data-ttu-id="2906b-113">En savoir plus sur les connecteurs</span><span class="sxs-lookup"><span data-stu-id="2906b-113">Read more about Connectors</span></span>](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
