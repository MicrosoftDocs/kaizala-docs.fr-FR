# <a name="generate-tenant-level-user-token"></a>Générer un jeton d'utilisateur au niveau du client

Le jeton d'actualisation de l'utilisateur au niveau du client peut être utilisé pour accorder l'accès à tous les groupes de l'utilisateur dans lequel l'utilisateur est un administrateur. Pour un utilisateur client, ce jeton accorde l'accès à tous les groupes d'une organisation.

## <a name="steps-to-generate-tenant-level-user-token"></a>Étapes à suivre pour générer un jeton d'utilisateur au niveau du client
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
        *   Sélectionnez les autorisations qui sont prévues pour que le connecteur ait accès à
        *   Appuyer sur créer un connecteur
    *   Notez l'ID & secret qui est généré et affiché sur le portail.

*   **Étape 2: l'utilisateur client «accorde» au connecteur l'accès à tous les groupes dont il est l'administrateur**

    *   L'utilisateur navigue vers le portail de gestion Kaizala @https://manage.kaiza.la/
    *   Se connecter à l'aide d'un compte Office 365 (SKU-TBD) existant
    *   Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»
        *   Entrer le numéro de téléphone
        *   Appuyez sur «générer le code confidentiel»
        *   Vérifier le code confidentiel reçu via un SMS sur le numéro de téléphone spécifié
    *   Appuyez sur «connecteurs» dans le menu de gauche.
    *   Appuyez sur le nom du connecteur auquel le connecteur doit accéder.
    *   Appuyez sur «générer un jeton utilisateur»
    *   Notez le jeton d'actualisation qui est généré et affiché sur le portail.

*   **Étape 3: l'utilisateur partage le jeton d'actualisation avec le développeur d'applications**

    *   L'administrateur doit partager manuellement le jeton d'actualisation reçu à l'étape 2 avec le développeur d'applications

*   **Étape 4: le développeur d'applications appelle l'API REST de la plateforme Kaizala pour générer le jeton d'accès.**

    *   Le développeur peut désormais utiliser le jeton d'actualisation. un ID de connecteur et une clé secrète de connecteur pour appeler l'API REST InOrder pour générer un jeton d'accès (plus d'informations ci-dessous)

