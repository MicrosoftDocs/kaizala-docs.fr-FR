---
title: /actions
description: Article de référence de l’API à envoyer/extraire des instances de l’Action
topic: Reference
author: nitinjms
ms.openlocfilehash: da96b8dc40d10a8ff2a6ca05e493677bf236fd84
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399368"
---
# <a name="actions"></a>/actions
Point de terminaison API à envoyer/extraire des instances de Kaizala Actions dans les groupes de conversation dans Kaizala. Portée actuelle est à prendre en charge la suite de types d’actions :

| Action | OBTENIR la prise en charge | Prise en charge de la publication | ID |
| :---: | :---: | :---: | :---: |
| Image des pièces jointes | Oui | Oui | image |
| Pièce jointe audio | Non | Oui | audio |
| Pièce jointe | Non | Oui | document |
| Pièce jointe de contact | Non | Non | s/o |
| Travail | Oui | Oui | travail |
| Enquête | Oui | Oui | enquête |
| Photo avec l’emplacement | Oui | Non | photoWithLocation |
| Rendez-vous | Oui | Oui | letsmeet |
| Interrogation rapide | Oui | Oui | sondage |
| Emplacement de partage | Oui | Non | shareLocation |
| Emplacement de la demande | Non | Non | s/o |
| Emplacement Live | Non | Non | s/o |
| Annonce | Non | Non | s/o |


*   API pour récupérer les [Actions](actions_get.md) et les [Détails de l’Action](actionDetails.md)
*   [API de publier des nouvelles instances d’Actions](actions_post.md)
*   [API à publier des réponses de l’action de nouvelle action réponses/modifier existant](action_responses.md)
