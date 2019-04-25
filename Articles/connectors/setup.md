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
# <a name="setup-for-using-the-kaizala-connectors"></a><span data-ttu-id="f1694-103">Configuration de l'utilisation des connecteurs Kaizala</span><span class="sxs-lookup"><span data-stu-id="f1694-103">Setup for using the Kaizala Connectors</span></span>

## <a name="personas"></a><span data-ttu-id="f1694-104">Personnages</span><span class="sxs-lookup"><span data-stu-id="f1694-104">Personas</span></span>

*   <span data-ttu-id="f1694-105">**Développeur:** Développement d'applications internes ou tierces pour l'Organisation: qui ont besoin d'intégrer Kaizala dans les processus métiers de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="f1694-105">**Developer:** In-house or 3rd party developing applications for the organization – who need to integrate Kaizala into the organization’s business processes.</span></span> <span data-ttu-id="f1694-106">Le développeur n'a pas accès à l'utilisateur final lors du développement de l'application (diffère d'un administrateur).</span><span class="sxs-lookup"><span data-stu-id="f1694-106">Developer does not have access to the end-user while developing the application (differs from an Admin).</span></span>
*   <span data-ttu-id="f1694-107">**Administrateur:** Utilisateur qui fait partie des groupes finaux et est administrateur.</span><span class="sxs-lookup"><span data-stu-id="f1694-107">**Admin:** User who is part of the end-groups and is an administrator.</span></span> <span data-ttu-id="f1694-108">Est attendu pour effectuer des tâches de gestion de groupe.</span><span class="sxs-lookup"><span data-stu-id="f1694-108">Is expected to perform group management tasks.</span></span>
*   <span data-ttu-id="f1694-109">**Utilisateur:** Utilisateurs finaux Kaizala</span><span class="sxs-lookup"><span data-stu-id="f1694-109">**User:** Kaizala end users</span></span>

## <a name="pre-req-to-set-up"></a><span data-ttu-id="f1694-110">Pré-req to set up</span><span class="sxs-lookup"><span data-stu-id="f1694-110">Pre-req to set-up</span></span>

*   <span data-ttu-id="f1694-111">En tant que **développeur:**</span><span class="sxs-lookup"><span data-stu-id="f1694-111">As a **developer:**</span></span>
    *   <span data-ttu-id="f1694-112">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="f1694-112">An Office365 account</span></span>
    *   <span data-ttu-id="f1694-113">Numéro de téléphone enregistré Kaizala</span><span class="sxs-lookup"><span data-stu-id="f1694-113">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="f1694-114">Configuration de développement (n'importe quelle plateforme) pour appeler l'API REST</span><span class="sxs-lookup"><span data-stu-id="f1694-114">Dev set-up (any platform) to invoke REST API</span></span>
*   <span data-ttu-id="f1694-115">En tant qu' **administrateur**</span><span class="sxs-lookup"><span data-stu-id="f1694-115">As an **admin**</span></span>
    *   <span data-ttu-id="f1694-116">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="f1694-116">An Office365 account</span></span>
    *   <span data-ttu-id="f1694-117">Numéro de téléphone enregistré Kaizala</span><span class="sxs-lookup"><span data-stu-id="f1694-117">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="f1694-118">Administrateur d'un groupe de conversation dans Kaizala avec le numéro de téléphone enregistré</span><span class="sxs-lookup"><span data-stu-id="f1694-118">Admin of a conversation group inside Kaizala with the registered phone number</span></span>
*   <span data-ttu-id="f1694-119">En tant qu' **utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f1694-119">As a **user**</span></span>
    *   <span data-ttu-id="f1694-120">Numéro de téléphone enregistré Kaizala</span><span class="sxs-lookup"><span data-stu-id="f1694-120">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="f1694-121">Membre d'un groupe de conversation dans Kaizala avec le numéro de téléphone enregistré</span><span class="sxs-lookup"><span data-stu-id="f1694-121">Member of a conversation group inside Kaizala with the registered phone number</span></span>

## <a name="set-up-steps-developer--group-admin"></a><span data-ttu-id="f1694-122">Étapes de configuration (administrateur du groupe & développeur)</span><span class="sxs-lookup"><span data-stu-id="f1694-122">Set-up steps (Developer & Group admin)</span></span>

<span data-ttu-id="f1694-123">Il existe quatre principaux composants d'infrastructure impliqués dans l'utilisation de l'API de plateforme Kaizala:</span><span class="sxs-lookup"><span data-stu-id="f1694-123">There are four major infrastructure components involved in working with the Kaizala Platform API:</span></span>

*   <span data-ttu-id="f1694-124">**Connecteurs:** Tous les systèmes tiers qui doivent s'intégrer avec Kaizala doivent être enregistrés avec la plateforme Kaizala en tant que «connecteur» et obtenir des jetons d'API correspondant au connecteur.</span><span class="sxs-lookup"><span data-stu-id="f1694-124">**Connectors:** All 3rd party systems that need to integrate with Kaizala need to be registered with the Kaizala platform as a “Connector” and get API Tokens corresponding to the Connector.</span></span>
*   <span data-ttu-id="f1694-125">**Portail de gestion Kaizala:** Un portail pour enregistrer les connecteurs tiers respectifs et leur fournir l'accès aux groupes de conversation Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f1694-125">**Kaizala Management Portal:** A portal to register the respective 3rd party Connectors – and provide them access to Kaizala Conversation groups.</span></span>
*   <span data-ttu-id="f1694-126">**Service de jetons:** Point de terminaison d'URL qui doit être appelé par les applications tierces pour obtenir des jetons d'accès.</span><span class="sxs-lookup"><span data-stu-id="f1694-126">**Token Service:** A URL end-point which needs to be called by the 3rd party apps to get Access Tokens.</span></span>
*   <span data-ttu-id="f1694-127">**Service de plateforme:** Point de terminaison d'URL qui expose des ressources spécifiques pour effectuer diverses actions dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f1694-127">**Platform Service:** A URL end-point which exposes specific resources to perform various actions inside Kaizala.</span></span>
*   <span data-ttu-id="f1694-128">**Étape 1: le développeur enregistre un connecteur**</span><span class="sxs-lookup"><span data-stu-id="f1694-128">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="f1694-129">Le développeur accède au portail de gestion Kaizala @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="f1694-129">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="f1694-130">Se connecter à l'aide d'un compte Office 365 existant</span><span class="sxs-lookup"><span data-stu-id="f1694-130">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="f1694-131">Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»</span><span class="sxs-lookup"><span data-stu-id="f1694-131">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="f1694-132">Entrer le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="f1694-132">Enter Phone number</span></span>
        *   <span data-ttu-id="f1694-133">Appuyez sur «générer le code confidentiel»</span><span class="sxs-lookup"><span data-stu-id="f1694-133">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="f1694-134">Vérifier le code confidentiel reçu via un SMS sur le numéro de téléphone spécifié</span><span class="sxs-lookup"><span data-stu-id="f1694-134">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="f1694-135">Appuyez sur «connecteurs» dans le menu de gauche.</span><span class="sxs-lookup"><span data-stu-id="f1694-135">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="f1694-136">Appuyez sur «Ajouter un connecteur»</span><span class="sxs-lookup"><span data-stu-id="f1694-136">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="f1694-137">Enregistrer un connecteur pour le système tiers qui utilisera l'API</span><span class="sxs-lookup"><span data-stu-id="f1694-137">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="f1694-138">Entrez le nom du connecteur et d'autres détails.</span><span class="sxs-lookup"><span data-stu-id="f1694-138">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="f1694-139">Appuyer sur continuer</span><span class="sxs-lookup"><span data-stu-id="f1694-139">Tap on Continue</span></span>
        *   <span data-ttu-id="f1694-140">Sélectionnez les [autorisations](permission.md) qui sont prévues pour que le connecteur ait accès à</span><span class="sxs-lookup"><span data-stu-id="f1694-140">Select [permissions](permission.md) that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="f1694-141">Appuyer sur créer un connecteur</span><span class="sxs-lookup"><span data-stu-id="f1694-141">Tap on Create Connector</span></span>
    *   <span data-ttu-id="f1694-142">Notez l'ID & secret qui est généré et affiché sur le portail.</span><span class="sxs-lookup"><span data-stu-id="f1694-142">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="f1694-143">**Étape 2: l'administrateur de groupe «accorde» au connecteur l'accès à son groupe**</span><span class="sxs-lookup"><span data-stu-id="f1694-143">**Step 2: Group Admin “grants” the Connector access to his/her group**</span></span>

    *   <span data-ttu-id="f1694-144">L'administrateur navigue vers le portail de gestion Kaizala @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="f1694-144">Admin navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="f1694-145">Se connecter à l'aide d'un compte Office 365 (SKU-TBD) existant</span><span class="sxs-lookup"><span data-stu-id="f1694-145">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="f1694-146">Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»</span><span class="sxs-lookup"><span data-stu-id="f1694-146">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="f1694-147">Entrer le numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="f1694-147">Enter Phone number</span></span>
        *   <span data-ttu-id="f1694-148">Appuyez sur «générer le code confidentiel»</span><span class="sxs-lookup"><span data-stu-id="f1694-148">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="f1694-149">Vérifier le code confidentiel reçu via un SMS sur le numéro de téléphone spécifié</span><span class="sxs-lookup"><span data-stu-id="f1694-149">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="f1694-150">Appuyez sur «groupes» dans le menu de gauche.</span><span class="sxs-lookup"><span data-stu-id="f1694-150">Tap on “Groups” in the left menu</span></span>
    *   <span data-ttu-id="f1694-151">Appuyez sur le nom du groupe auquel le connecteur doit accéder.</span><span class="sxs-lookup"><span data-stu-id="f1694-151">Tap on the group name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="f1694-152">Appuyez sur «connecteurs»</span><span class="sxs-lookup"><span data-stu-id="f1694-152">Tap on “Connectors”</span></span>
    *   <span data-ttu-id="f1694-153">Dans la liste déroulante, sélectionnez le connecteur auquel vous souhaitez accorder l'accès.</span><span class="sxs-lookup"><span data-stu-id="f1694-153">In the drop-down, select the Connector that you want to grant access to</span></span>
    *   <span data-ttu-id="f1694-154">Appuyez sur «Ajouter un connecteur»</span><span class="sxs-lookup"><span data-stu-id="f1694-154">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="f1694-155">Notez le jeton d'actualisation qui est généré et affiché sur le portail.</span><span class="sxs-lookup"><span data-stu-id="f1694-155">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="f1694-156">**Étape 3: partage du jeton d'actualisation avec le développeur d'applications**</span><span class="sxs-lookup"><span data-stu-id="f1694-156">**Step 3: Group Admin shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="f1694-157">L'administrateur doit partager manuellement le jeton d'actualisation reçu à l'étape 2 avec le développeur d'applications</span><span class="sxs-lookup"><span data-stu-id="f1694-157">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="f1694-158">**Étape 4: le développeur d'applications appelle l'API REST de la plateforme Kaizala pour générer le jeton d'accès.**</span><span class="sxs-lookup"><span data-stu-id="f1694-158">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="f1694-159">Le développeur peut désormais utiliser le jeton d'actualisation.</span><span class="sxs-lookup"><span data-stu-id="f1694-159">Developer can now use the Refresh token.</span></span> <span data-ttu-id="f1694-160">un ID de connecteur et une clé secrète de connecteur pour appeler l'API REST InOrder pour générer un jeton d'accès (plus d'informations ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="f1694-160">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>


<span data-ttu-id="f1694-161">Suivant: [générer un jeton d'accès](Tokens.md)</span><span class="sxs-lookup"><span data-stu-id="f1694-161">Next:  [Generate Access token](Tokens.md)</span></span><br/>
<span data-ttu-id="f1694-162">Plus: [documentation](API.md) de l'API</span><span class="sxs-lookup"><span data-stu-id="f1694-162">More:  [API Documentation](API.md)</span></span>
