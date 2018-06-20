---
title: Configurer les connecteurs Kaizala
description: Cet Article décrit les étapes pour créer des connecteurs Kaizala et générer des jetons d’autorisation
topic: get-started-article
author: nitinjms
ms.openlocfilehash: f55d09c4619d6d17a997935ff937ae82cc560ceb
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905035"
---
# <a name="setup-for-using-the-kaizala-connectors"></a><span data-ttu-id="df4ba-103">Programme d’installation pour l’utilisation de connecteurs Kaizala</span><span class="sxs-lookup"><span data-stu-id="df4ba-103">Setup for using the Kaizala Connectors</span></span>

## <a name="personas"></a><span data-ttu-id="df4ba-104">Personnage</span><span class="sxs-lookup"><span data-stu-id="df4ba-104">Personas</span></span>

*   <span data-ttu-id="df4ba-105">**Pour les développeurs :** En interne ou 3e partie développement d’applications pour l’organisation – qui souhaitent intégrer Kaizala des processus d’entreprise de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="df4ba-105">**Developer:** In-house or 3rd party developing applications for the organization – who need to integrate Kaizala into the organization’s business processes.</span></span> <span data-ttu-id="df4ba-106">Pour les développeurs n’ont pas accès à l’utilisateur final lors du développement de l’application (diffère d’un administrateur).</span><span class="sxs-lookup"><span data-stu-id="df4ba-106">Developer does not have access to the end-user while developing the application (differs from an Admin).</span></span>
*   <span data-ttu-id="df4ba-107">**Admin :** Utilisateur qui fait partie des groupes de fin et est un administrateur.</span><span class="sxs-lookup"><span data-stu-id="df4ba-107">**Admin:** User who is part of the end-groups and is an administrator.</span></span> <span data-ttu-id="df4ba-108">Est prévu pour effectuer les tâches de gestion de groupe.</span><span class="sxs-lookup"><span data-stu-id="df4ba-108">Is expected to perform group management tasks.</span></span>
*   <span data-ttu-id="df4ba-109">**Utilisateur :** Utilisateurs finaux Kaizala</span><span class="sxs-lookup"><span data-stu-id="df4ba-109">**User:** Kaizala end users</span></span>

## <a name="pre-req-to-set-up"></a><span data-ttu-id="df4ba-110">Condition requise pour l’installation</span><span class="sxs-lookup"><span data-stu-id="df4ba-110">Pre-req to set-up</span></span>

*   <span data-ttu-id="df4ba-111">En tant qu’un **pour les développeurs :**</span><span class="sxs-lookup"><span data-stu-id="df4ba-111">As a **developer:**</span></span>
    *   <span data-ttu-id="df4ba-112">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="df4ba-112">An Office365 account</span></span>
    *   <span data-ttu-id="df4ba-113">Un Kaizala inscrit le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="df4ba-113">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="df4ba-114">Configuration pour les développeurs (n’importe quelle plate-forme) pour appeler l’API REST</span><span class="sxs-lookup"><span data-stu-id="df4ba-114">Dev set-up (any platform) to invoke REST API</span></span>
*   <span data-ttu-id="df4ba-115">En tant qu' **administrateur**</span><span class="sxs-lookup"><span data-stu-id="df4ba-115">As an **admin**</span></span>
    *   <span data-ttu-id="df4ba-116">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="df4ba-116">An Office365 account</span></span>
    *   <span data-ttu-id="df4ba-117">Un Kaizala inscrit le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="df4ba-117">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="df4ba-118">Administration d’un groupe de conversation à l’intérieur de Kaizala avec le numéro de téléphone enregistré</span><span class="sxs-lookup"><span data-stu-id="df4ba-118">Admin of a conversation group inside Kaizala with the registered phone number</span></span>
*   <span data-ttu-id="df4ba-119">En tant qu' **utilisateur**</span><span class="sxs-lookup"><span data-stu-id="df4ba-119">As a **user**</span></span>
    *   <span data-ttu-id="df4ba-120">Un Kaizala inscrit le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="df4ba-120">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="df4ba-121">Membre d’un groupe de conversation à l’intérieur de Kaizala avec le numéro de téléphone enregistré</span><span class="sxs-lookup"><span data-stu-id="df4ba-121">Member of a conversation group inside Kaizala with the registered phone number</span></span>

## <a name="set-up-steps-developer--group-admin"></a><span data-ttu-id="df4ba-122">Étapes de configuration (pour les développeurs et groupe d’administration)</span><span class="sxs-lookup"><span data-stu-id="df4ba-122">Set-up steps (Developer & Group admin)</span></span>

<span data-ttu-id="df4ba-123">Il existe quatre composants d’infrastructure principaux impliqués dans l’utilisation de l’API de plateforme Kaizala :</span><span class="sxs-lookup"><span data-stu-id="df4ba-123">There are four major infrastructure components involved in working with the Kaizala Platform API:</span></span>

*   <span data-ttu-id="df4ba-124">**Connecteurs :** Tous les systèmes 3ème partie qui doivent s’intégrer avec Kaizala doivent être enregistrés avec la plate-forme Kaizala en tant que « Connecteur » et obtenir des jetons d’API correspondant au connecteur.</span><span class="sxs-lookup"><span data-stu-id="df4ba-124">**Connectors:** All 3rd party systems that need to integrate with Kaizala need to be registered with the Kaizala platform as a “Connector” and get API Tokens corresponding to the Connector.</span></span>
*   <span data-ttu-id="df4ba-125">**Portail de gestion Kaizala :** Un portail pour enregistrer la partie 3 respectif connecteurs – et leur fournir l’accès à des groupes de Conversation Kaizala.</span><span class="sxs-lookup"><span data-stu-id="df4ba-125">**Kaizala Management Portal:** A portal to register the respective 3rd party Connectors – and provide them access to Kaizala Conversation groups.</span></span>
*   <span data-ttu-id="df4ba-126">**Service d’émission de jetons :** Un point de terminaison d’URL qui doit être appelée par les applications de tiers 3e pour obtenir les jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="df4ba-126">**Token Service:** A URL end-point which needs to be called by the 3rd party apps to get Access Tokens.</span></span>
*   <span data-ttu-id="df4ba-127">**Service de la plateforme :** Un point de terminaison d’URL qui expose des ressources spécifiques pour effectuer des actions différentes à l’intérieur de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="df4ba-127">**Platform Service:** A URL end-point which exposes specific resources to perform various actions inside Kaizala.</span></span>
*   <span data-ttu-id="df4ba-128">**Étape 1 : Le développeur enregistre un connecteur**</span><span class="sxs-lookup"><span data-stu-id="df4ba-128">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="df4ba-129">Pour les développeurs accède au portail de gestion Kaizala @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="df4ba-129">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="df4ba-130">Ouvrez une session à l’aide d’un compte Office 365 existant</span><span class="sxs-lookup"><span data-stu-id="df4ba-130">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="df4ba-131">Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »</span><span class="sxs-lookup"><span data-stu-id="df4ba-131">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="df4ba-132">Entrez le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="df4ba-132">Enter Phone number</span></span>
        *   <span data-ttu-id="df4ba-133">Cliquez sur « Générer le code confidentiel »</span><span class="sxs-lookup"><span data-stu-id="df4ba-133">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="df4ba-134">Vérifier le code confidentiel reçu par SMS sur le numéro de téléphone spécifié</span><span class="sxs-lookup"><span data-stu-id="df4ba-134">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="df4ba-135">Cliquez sur « Connecteurs » dans le menu de gauche</span><span class="sxs-lookup"><span data-stu-id="df4ba-135">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="df4ba-136">Cliquez sur « Ajouter le connecteur »</span><span class="sxs-lookup"><span data-stu-id="df4ba-136">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="df4ba-137">Inscrire un connecteur pour le système 3ème partie qui utilise l’API</span><span class="sxs-lookup"><span data-stu-id="df4ba-137">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="df4ba-138">Entrez le nom du connecteur et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="df4ba-138">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="df4ba-139">Cliquez sur Continuer</span><span class="sxs-lookup"><span data-stu-id="df4ba-139">Tap on Continue</span></span>
        *   <span data-ttu-id="df4ba-140">Sélectionnez autorisations est conçu pour le connecteur d’accéder aux</span><span class="sxs-lookup"><span data-stu-id="df4ba-140">Select permissions that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="df4ba-141">Cliquez sur Créer le connecteur</span><span class="sxs-lookup"><span data-stu-id="df4ba-141">Tap on Create Connector</span></span>
    *   <span data-ttu-id="df4ba-142">Notez l’ID & Secret qui récupèrent généré et affiché sur le portail</span><span class="sxs-lookup"><span data-stu-id="df4ba-142">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="df4ba-143">**Étape 2 : Groupe Admin » permet d’accéder » le connecteur à son groupe**</span><span class="sxs-lookup"><span data-stu-id="df4ba-143">**Step 2: Group Admin “grants” the Connector access to his/her group**</span></span>

    *   <span data-ttu-id="df4ba-144">Admin accède au portail de gestion Kaizala @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="df4ba-144">Admin navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="df4ba-145">Ouvrez une session à l’aide d’un Office 365 existant compte (SKU TBD)</span><span class="sxs-lookup"><span data-stu-id="df4ba-145">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="df4ba-146">Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »</span><span class="sxs-lookup"><span data-stu-id="df4ba-146">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="df4ba-147">Entrez le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="df4ba-147">Enter Phone number</span></span>
        *   <span data-ttu-id="df4ba-148">Cliquez sur « Générer le code confidentiel »</span><span class="sxs-lookup"><span data-stu-id="df4ba-148">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="df4ba-149">Vérifier le code confidentiel reçu par SMS sur le numéro de téléphone spécifié</span><span class="sxs-lookup"><span data-stu-id="df4ba-149">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="df4ba-150">Cliquez sur « Groupes » dans le menu de gauche</span><span class="sxs-lookup"><span data-stu-id="df4ba-150">Tap on “Groups” in the left menu</span></span>
    *   <span data-ttu-id="df4ba-151">Cliquez sur le nom du groupe qui doit être accessible par le connecteur</span><span class="sxs-lookup"><span data-stu-id="df4ba-151">Tap on the group name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="df4ba-152">Cliquez sur « Connecteurs »</span><span class="sxs-lookup"><span data-stu-id="df4ba-152">Tap on “Connectors”</span></span>
    *   <span data-ttu-id="df4ba-153">Dans la liste déroulante, sélectionnez le lien que vous souhaitez accorder l’accès à</span><span class="sxs-lookup"><span data-stu-id="df4ba-153">In the drop-down, select the Connector that you want to grant access to</span></span>
    *   <span data-ttu-id="df4ba-154">Cliquez sur « Ajouter le connecteur »</span><span class="sxs-lookup"><span data-stu-id="df4ba-154">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="df4ba-155">Notez le jeton actualiser qui est généré et affiché sur le portail</span><span class="sxs-lookup"><span data-stu-id="df4ba-155">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="df4ba-156">**Étape 3 : Groupe Admin partage le jeton d’actualisation avec le développeur de l’application**</span><span class="sxs-lookup"><span data-stu-id="df4ba-156">**Step 3: Group Admin shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="df4ba-157">Admin doit partager manuellement le jeton d’actualisation reçu à l’étape 2 avec le développeur de l’application</span><span class="sxs-lookup"><span data-stu-id="df4ba-157">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="df4ba-158">**Étape 4 : Développement d’application appelle l’API de Rest de plateforme Kaizala pour générer un jeton d’accès**</span><span class="sxs-lookup"><span data-stu-id="df4ba-158">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="df4ba-159">Développeur peut utiliser maintenant le jeton d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="df4ba-159">Developer can now use the Refresh token.</span></span> <span data-ttu-id="df4ba-160">un ID de connecteur et connecteur Secret pour appeler l’API REST communiquées pour générer un jeton d’accès (plus d’informations sur ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="df4ba-160">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>


<span data-ttu-id="df4ba-161">À suivre : [jeton d’accès de générer](Tokens.md)</span><span class="sxs-lookup"><span data-stu-id="df4ba-161">Next:  [Generate Access token](Tokens.md)</span></span><br/>
<span data-ttu-id="df4ba-162">En savoir plus : [Documentation de l’API](API.md)</span><span class="sxs-lookup"><span data-stu-id="df4ba-162">More:  [API Documentation](API.md)</span></span>
