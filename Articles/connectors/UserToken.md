# <a name="generate-tenant-level-user-token"></a>Générer le jeton de l’utilisateur au niveau du client

Jeton d’actualisation de l’utilisateur au niveau du client peut servir à accorder l’accès à tous les groupes de l’utilisateur dont l’utilisateur est un administrateur. Pour un utilisateur client, ce jeton permet d’accéder à tous les groupes d’une organisation.

## <a name="steps-to-generate-tenant-level-user-token"></a>Étapes pour générer le jeton de l’utilisateur au niveau du client
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
        *   Sélectionnez autorisations est conçu pour le connecteur d’accéder aux
        *   Cliquez sur Créer le connecteur
    *   Notez l’ID & Secret qui récupèrent généré et affiché sur le portail

*   **Étape 2 : Client utilisateur » permet d’accéder » le connecteur à tous les groupes auxquels il est administrateur**

    *   L’utilisateur navigue vers un portail de gestion Kaizala @https://manage.kaiza.la/
    *   Ouvrez une session à l’aide d’un Office 365 existant compte (SKU TBD)
    *   Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »
        *   Entrez le numéro de téléphone
        *   Cliquez sur « Générer le code confidentiel »
        *   Vérifier le code confidentiel reçu par SMS sur le numéro de téléphone spécifié
    *   Cliquez sur « Connecteurs » dans le menu de gauche
    *   Cliquez sur le nom du connecteur qui doit être accessible par le connecteur
    *   Cliquez sur « Jeton utilisateur de générer »
    *   Notez le jeton actualiser qui est généré et affiché sur le portail

*   **Étape 3 : Utilisateur partage le jeton d’actualisation avec le développeur de l’application**

    *   Admin doit partager manuellement le jeton d’actualisation reçu à l’étape 2 avec le développeur de l’application

*   **Étape 4 : Développement d’application appelle l’API de Rest de plateforme Kaizala pour générer un jeton d’accès**

    *   Développeur peut utiliser maintenant le jeton d’actualisation. un ID de connecteur et connecteur Secret pour appeler l’API REST communiquées pour générer un jeton d’accès (plus d’informations sur ci-dessous)

