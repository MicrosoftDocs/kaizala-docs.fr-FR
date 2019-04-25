---
title: Configurer les connecteurs Kaizala
description: Cet article décrit les étapes à suivre pour créer des connecteurs Kaizala et générer des jetons d'autorisation
topic: get-started-article
author: nitinjms
ms.openlocfilehash: e9f6551f4ae824a6da0ee4ee39f32cd2237486b6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190797"
---
# <a name="setup-for-using-the-kaizala-connectors"></a>Configuration de l'utilisation des connecteurs Kaizala

## <a name="personas"></a>Personnages

*   **Développeur:** Développement d'applications internes ou tierces pour l'Organisation: qui ont besoin d'intégrer Kaizala dans les processus métiers de l'organisation. Le développeur n'a pas accès à l'utilisateur final lors du développement de l'application (diffère d'un administrateur).
*   **Administrateur:** Utilisateur qui fait partie des groupes finaux et est administrateur. Est attendu pour effectuer des tâches de gestion de groupe.
*   **Utilisateur:** Utilisateurs finaux Kaizala

## <a name="pre-req-to-set-up"></a>Pré-req to set up

*   En tant que **développeur:**
    *   Un compte Office 365
    *   Numéro de téléphone enregistré Kaizala
    *   Configuration de développement (n'importe quelle plateforme) pour appeler l'API REST
*   En tant qu' **administrateur**
    *   Un compte Office 365
    *   Numéro de téléphone enregistré Kaizala
    *   Administrateur d'un groupe de conversation dans Kaizala avec le numéro de téléphone enregistré
*   En tant qu' **utilisateur**
    *   Numéro de téléphone enregistré Kaizala
    *   Membre d'un groupe de conversation dans Kaizala avec le numéro de téléphone enregistré

## <a name="set-up-steps-developer--group-admin"></a>Étapes de configuration (administrateur du groupe & développeur)

Il existe quatre principaux composants d'infrastructure impliqués dans l'utilisation de l'API de plateforme Kaizala:

*   **Connecteurs:** Tous les systèmes tiers qui doivent s'intégrer avec Kaizala doivent être enregistrés avec la plateforme Kaizala en tant que «connecteur» et obtenir des jetons d'API correspondant au connecteur.
*   **Portail de gestion Kaizala:** Un portail pour enregistrer les connecteurs tiers respectifs et leur fournir l'accès aux groupes de conversation Kaizala.
*   **Service de jetons:** Point de terminaison d'URL qui doit être appelé par les applications tierces pour obtenir des jetons d'accès.
*   **Service de plateforme:** Point de terminaison d'URL qui expose des ressources spécifiques pour effectuer diverses actions dans Kaizala.
*   **Étape 1: le développeur enregistre un connecteur**

    *   Le développeur accède au portail de gestion Kaizala @https://manage.kaiza.la/
    *   Se connecter à l'aide d'un compte Office 365 existant
    *   Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»
        *   Entrer le numéro de téléphone
        *   Appuyez sur «générer le code confidentiel»
        *   Vérifier le code confidentiel reçu via un SMS sur le numéro de téléphone spécifié
    *   Appuyez sur «connecteurs» dans le menu de gauche.
    *   Appuyez sur «Ajouter un connecteur»
    *   Enregistrer un connecteur pour le système tiers qui utilisera l'API
        *   Entrez le nom du connecteur et d'autres détails. Appuyer sur continuer
        *   Sélectionnez les [autorisations](permission.md) qui sont prévues pour que le connecteur ait accès à
        *   Appuyer sur créer un connecteur
    *   Notez l'ID & secret qui est généré et affiché sur le portail.

*   **Étape 2: l'administrateur de groupe «accorde» au connecteur l'accès à son groupe**

    *   L'administrateur navigue vers le portail de gestion Kaizala @https://manage.kaiza.la/
    *   Se connecter à l'aide d'un compte Office 365 (SKU-TBD) existant
    *   Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»
        *   Entrer le numéro de téléphone
        *   Appuyez sur «générer le code confidentiel»
        *   Vérifier le code confidentiel reçu via un SMS sur le numéro de téléphone spécifié
    *   Appuyez sur «groupes» dans le menu de gauche.
    *   Appuyez sur le nom du groupe auquel le connecteur doit accéder.
    *   Appuyez sur «connecteurs»
    *   Dans la liste déroulante, sélectionnez le connecteur auquel vous souhaitez accorder l'accès.
    *   Appuyez sur «Ajouter un connecteur»
    *   Notez le jeton d'actualisation qui est généré et affiché sur le portail.

*   **Étape 3: partage du jeton d'actualisation avec le développeur d'applications**

    *   L'administrateur doit partager manuellement le jeton d'actualisation reçu à l'étape 2 avec le développeur d'applications

*   **Étape 4: le développeur d'applications appelle l'API REST de la plateforme Kaizala pour générer le jeton d'accès.**

    *   Le développeur peut désormais utiliser le jeton d'actualisation. un ID de connecteur et une clé secrète de connecteur pour appeler l'API REST InOrder pour générer un jeton d'accès (plus d'informations ci-dessous)


Suivant: [générer un jeton d'accès](Tokens.md)<br/>
Plus: [documentation](API.md) de l'API
