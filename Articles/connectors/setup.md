---
title: Configurer les connecteurs Kaizala
description: Cet Article décrit les étapes pour créer des connecteurs Kaizala et générer des jetons d’autorisation
topic: get-started-article
author: nitinjms
ms.openlocfilehash: e9f6551f4ae824a6da0ee4ee39f32cd2237486b6
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399362"
---
# <a name="setup-for-using-the-kaizala-connectors"></a>Programme d’installation pour l’utilisation de connecteurs Kaizala

## <a name="personas"></a>Personas

*   **Pour les développeurs :** En interne ou 3e partie développement d’applications pour l’organisation – qui souhaitent intégrer Kaizala des processus d’entreprise de l’organisation. Pour les développeurs n’ont pas accès à l’utilisateur final lors du développement de l’application (diffère d’un administrateur).
*   **Admin :** Utilisateur qui fait partie des groupes de fin et est un administrateur. Est prévu pour effectuer les tâches de gestion de groupe.
*   **Utilisateur :** Utilisateurs finaux Kaizala

## <a name="pre-req-to-set-up"></a>Condition requise pour l’installation

*   En tant qu’un **pour les développeurs :**
    *   Un compte Office 365
    *   Un Kaizala inscrit le numéro de téléphone
    *   Configuration pour les développeurs (n’importe quelle plate-forme) pour appeler l’API REST
*   En tant qu' **administrateur**
    *   Un compte Office 365
    *   Un Kaizala inscrit le numéro de téléphone
    *   Administration d’un groupe de conversation à l’intérieur de Kaizala avec le numéro de téléphone enregistré
*   En tant qu' **utilisateur**
    *   Un Kaizala inscrit le numéro de téléphone
    *   Membre d’un groupe de conversation à l’intérieur de Kaizala avec le numéro de téléphone enregistré

## <a name="set-up-steps-developer--group-admin"></a>Étapes de configuration (pour les développeurs et groupe d’administration)

Il existe quatre composants d’infrastructure principaux impliqués dans l’utilisation de l’API de plateforme Kaizala :

*   **Connecteurs :** Tous les systèmes 3ème partie qui doivent s’intégrer avec Kaizala doivent être enregistrés avec la plate-forme Kaizala en tant que « Connecteur » et obtenir des jetons d’API correspondant au connecteur.
*   **Portail de gestion Kaizala :** Un portail pour enregistrer la partie 3 respectif connecteurs – et leur fournir l’accès à des groupes de Conversation Kaizala.
*   **Service d’émission de jetons :** Un point de terminaison d’URL qui doit être appelée par les applications de tiers 3e pour obtenir les jetons d’accès.
*   **Service de la plateforme :** Un point de terminaison d’URL qui expose des ressources spécifiques pour effectuer des actions différentes à l’intérieur de Kaizala.
*   **Étape 1 : Le développeur enregistre un connecteur**

    *   Pour les développeurs accède au portail de gestion Kaizala @https://manage.kaiza.la/
    *   Ouvrez une session à l’aide d’un compte Office 365 existant
    *   Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »
        *   Entrez le numéro de téléphone
        *   Cliquez sur « Générer le code confidentiel »
        *   Vérifier le code confidentiel reçu par SMS sur le numéro de téléphone spécifié
    *   Cliquez sur « Connecteurs » dans le menu de gauche
    *   Cliquez sur « Ajouter le connecteur »
    *   Inscrire un connecteur pour le système 3ème partie qui utilise l’API
        *   Entrez le nom du connecteur et d’autres détails. Cliquez sur Continuer
        *   Sélectionnez [autorisations](permission.md) conçue pour le connecteur d’accéder aux
        *   Cliquez sur Créer le connecteur
    *   Notez l’ID & Secret qui récupèrent généré et affiché sur le portail

*   **Étape 2 : Groupe Admin » permet d’accéder » le connecteur à son groupe**

    *   Admin accède au portail de gestion Kaizala @https://manage.kaiza.la/
    *   Ouvrez une session à l’aide d’un Office 365 existant compte (SKU TBD)
    *   Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »
        *   Entrez le numéro de téléphone
        *   Cliquez sur « Générer le code confidentiel »
        *   Vérifier le code confidentiel reçu par SMS sur le numéro de téléphone spécifié
    *   Cliquez sur « Groupes » dans le menu de gauche
    *   Cliquez sur le nom du groupe qui doit être accessible par le connecteur
    *   Cliquez sur « Connecteurs »
    *   Dans la liste déroulante, sélectionnez le lien que vous souhaitez accorder l’accès à
    *   Cliquez sur « Ajouter le connecteur »
    *   Notez le jeton actualiser qui est généré et affiché sur le portail

*   **Étape 3 : Groupe Admin partage le jeton d’actualisation avec le développeur de l’application**

    *   Admin doit partager manuellement le jeton d’actualisation reçu à l’étape 2 avec le développeur de l’application

*   **Étape 4 : Développement d’application appelle l’API de Rest de plateforme Kaizala pour générer un jeton d’accès**

    *   Développeur peut utiliser maintenant le jeton d’actualisation. un ID de connecteur et connecteur Secret pour appeler l’API REST communiquées pour générer un jeton d’accès (plus d’informations sur ci-dessous)


À suivre : [jeton d’accès de générer](Tokens.md)<br/>
En savoir plus : [Documentation de l’API](API.md)
