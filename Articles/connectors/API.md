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
# <a name="kaizala-api-documentation"></a>Documentation de l’API Kaizala

Avant de commencer, reportez-vous à [la rubrique Configuration de l’utilisation des connecteurs Kaizala](setup.md)

## <a name="root-domain"></a>Domaine racine

Le domaine racine pour l’appel des API Kaizala est le suivant:

    {endpoint-url}
    
|               | Paramètre             | Type      | Module?     | Description |
| :---: | :---: | :---: | :---: | :--- |
| URL du point de terminaison  | `endpoint-url`        | Chaîne    | Non            | Lors de l’authentification réussie lors de la génération de jetons d’accès, une URL de point de terminaison est renvoyée qui doit être utilisée comme URL de base de l’API pour effectuer les appels d’API suivants    |

> Tout en accédant à une API Kaizala, vous pouvez obtenir le code d’État http: 308 indiquant que l’URL de point de terminaison de l’utilisateur a changé. Dans ce cas, l’emplacement de l’en-tête de réponse contiendra la nouvelle URL de point de terminaison.

> **Suggestion:** Les clients peuvent configurer le délai d’expiration pour recevoir une réponse des API Kaizala à 1 min

### <a name="api-end-points"></a>Points de terminaison d’API

L’API Kaizala s’exécute sur le Cloud Microsoft Azure sécurisé et interagit avec la plateforme Kaizala pour effectuer différentes actions pour les utilisateurs finaux.
L’API fonctionne avec les ressources Kaizala suivantes:

*   [/groups](groups.md)
*   [/subGroups](subGroups.md)
*   [/members](members.md)
*   [/messages](messages.md)
*   [/media](media.md)
*   [/actions](actions.md)
*   [/subscribers](subscribers.md)
*    [/reaction](reactions.md)

### <a name="webhooks"></a>WebHooks

L’API Microsoft Kaizala offre également aux développeurs la possibilité d’enregistrer des événements spécifiques dans la plateforme Kaizala via des webhooks.

*   [/webhook](webHooks.md)

### <a name="postman-collection"></a>Collection postale

Pour tester nos API, ainsi que comprendre le schéma de l’API Kaizala, vous pouvez importer une collection postale contenant des exemples et du schéma pour toutes les API Kaizala Microsoft:


[![Exécuter dans le poteau](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)

Définissez les variables d’environnement suivantes dans «Kaizala-APIs-Environment» avant d’exécuter le projet post:
* Numéro de téléphone mobile: votre numéro de téléphone mobile qui sera utilisé pour l’appel des API
* application-ID: ID associé au connecteur
* clé d’application: secret associé au connecteur

D’autres variables d’environnement seront renseignées automatiquement lors de la tentative d’indication des API dans la séquence dans le projet post. 

### <a name="getting-started-with-kaizala-rest-apis"></a>Prise en main des API REST Kaizala 

[Exemple C# (partagé)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
