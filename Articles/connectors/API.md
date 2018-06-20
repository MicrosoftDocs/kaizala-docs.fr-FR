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
# <a name="kaizala-api-documentation"></a>Documentation Kaizala API

Avant de commencer, reportez-vous au [programme d’installation pour l’utilisation de connecteurs Kaizala](setup.md)

## <a name="root-domain"></a>Domaine racine

Le domaine racine pour appeler les APIs Kaizala est la suivante :

    {endpoint-url}
    
|               | Paramètre             | Type      | Facultatif ?     | Description |
| :---: | :---: | :---: | :---: | :--- |
| Url du point de terminaison  | `endpoint-url`        | Chaîne    | Non            | Authentification réussie lors de la génération jetons d’accès, une url de point de terminaison est renvoyée qui doivent être utilisées comme url de base d’api pour effectuer des appels d’API suivants    |

Veuillez noter que tout en appuyant sur n’importe quelle api Kaizala, vous pouvez obtenir l’état Http code : 308 indiquant que l’url de terminaison de l’utilisateur a changé. Emplacement de l’en-tête réponse contient dans ce cas, la nouvelle url de point de terminaison.

### <a name="api-end-points"></a>API de points de terminaison

L’API Kaizala s’exécute sur le cloud Microsoft Azure sécurisé et interagit avec la plateforme Kaizala pour effectuer des actions différentes pour les utilisateurs finaux.
L’API fonctionne avec les ressources Kaizala suivantes :

*   [/Groups](groups.md)
*   [/subGroups](subGroups.md)
*   [/Members](members.md)
*   [/messages](messages.md)
*   [/ Media](media.md)
*   [/actions](actions.md)
*   [/Subscribers](subscribers.md)

### <a name="webhooks"></a>WebHooks

L’API de Kaizala Microsoft permet également aux développeurs d’enregistrer des événements spécifiques au sein de la plateforme Kaizala via WebHooks.

*   [/webhook](webHooks.md)

### <a name="postman-collection"></a>Collection postman

Afin de tester notre API, ainsi que comprendre API Kaizala schéma, vous pouvez importer collection postman contenant des exemples et schéma pour toutes les API Microsoft Kaizala :


[![Exécuter dans Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)

Configurez les variables d’environnement dans « Kaizala-API-environment » avant d’exécuter le projet postman suivantes :
* numéro de Mobile : votre numéro de téléphone mobile qui sera utilisé pour appeler des API
* id d’application : ID associé au connecteur
* clé secrète de l’application : Secret associé au connecteur

Autres variables d’environnement sera remplie automatiquement lors de l’API de séquence abordées dans le projet Postman. 

### <a name="getting-started-with-kaizala-rest-apis"></a>Mise en route avec l’API REST de Kaizala 

[Exemple c# (partagé)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)
