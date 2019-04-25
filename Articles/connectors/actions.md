---
title: /actions
description: Article de référence pour l'API permettant d'envoyer/de récupérer des instances d'action
topic: Reference
author: nitinjms
ms.openlocfilehash: da96b8dc40d10a8ff2a6ca05e493677bf236fd84
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190773"
---
# <a name="actions"></a>/actions
Point de terminaison de l'API pour l'envoi/la récupération d'instances d'actions Kaizala vers/à partir de groupes de conversation dans Kaizala. L'étendue actuelle prend en charge les types d'action suivants:

| Action | OBTENIR la prise en charge | POST pris en charge | Id |
| :---: | :---: | :---: | :---: |
| Image jointe | Oui | Oui | image |
| Pièce jointe audio | Non | Oui | audio |
| Pièce jointe de document | Non | Oui | document |
| Pièce jointe de contact | Non | Non | s/o |
| Travail | Oui | Oui | travail |
| Enquête | Oui | Oui | sondages |
| Photo avec emplacement | Oui | Non | photoWithLocation |
| Nous allons respecter | Oui | Oui | letsmeet |
| Sondage rapide | Oui | Oui | temporisateur |
| Emplacement de partage | Oui | Non | shareLocation |
| Emplacement de la demande | Non | Non | s/o |
| Emplacement en direct | Non | Non | s/o |
| Annonce | Non | Non | s/o |


*   API permettant de récupérer les [actions](actions_get.md) et les détails de l' [action](actionDetails.md)
*   [API permettant de publier de nouvelles instances d'actions](actions_post.md)
*   [API permettant de publier de nouvelles réponses d'action/modifier des réponses d'action existantes](action_responses.md)
