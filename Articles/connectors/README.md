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
# <a name="connectors"></a>Connecteurs

## <a name="overview"></a>Vue d'ensemble
Les connecteurs Kaizala permettent aux développeurs tiers d'intégrer Kaizala à leurs processus métier en leur permettant d'effectuer un ensemble d'actions organisée dans Kaizala à l'aide d'appels d'API basés sur REST. L'étendue de l'API est destinée aux systèmes externes pour appeler le point de terminaison et effectuer des actions à la demande. Autrement dit, il s'agit d'un modèle d'extraction, où les points de terminaison individuels doivent être appelés pour effectuer des actions spécifiques à l'aide des **[API](API.md)** Kaizala. Le modèle poussé dans lequel la plateforme Kaizala peut déclencher des actions peut **[](webHooks.md)** être configuré à l'aide des webhooks.

Les connecteurs Kaizala sont actuellement étendus aux groupes, c'est-à-dire que chaque connecteur Kaizala doit explicitement disposer des autorisations d'accès à un groupe de conversation, puis effectuer des actions par le biais des points de terminaison de l'API uniquement dans le contexte du groupe. Toutefois, chaque connecteur Kaizala peut être autorisé à accéder à plusieurs groupes.

* [Configuration de l'utilisation des connecteurs Kaizala](setup.md)
* [Documentation de l'API](API.md)
* [En savoir plus sur les connecteurs](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
