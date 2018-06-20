# <a name="instant-edit-of-actions-in-staged-environment"></a>Modifier instantané d’Actions dans l’environnement intermédiaire

Avant de commencer la modification des Actions, veuillez activer [l’état intermédiaire](test.md)

Lors de la création d’une Action, les vues HTML et les fichiers associés (css, js) sont regroupés dans le package de l’Action et est importé sur le portail de gestion Kaizala. Les autres modifications aux vues requièrent le package recréer et téléchargé sur le portail de gestion Kaizala.

Afin de simplifier la modification ultérieure des affichages HTML, Kaizala permet de modifier du code HTML, JavaScript et fichiers CSS localement et instantanément voir les mises à jour dans l’application Kaizala. Cela implique la création d’un serveur HTTP local qui va héberger les fichiers mis à jour et Kaizala application utilisera ces fichiers, au lieu des fichiers présents dans le package réel.

>  **Remarque :** Afin d’activer la modification instantanée, l’Action doit être téléchargée sur le portail de gestion Kaizala et doit être en état intermédiaire

## <a name="enable-instant-edit-in-android-devices"></a>Activer Modifier instantanés pour les appareils Android

### <a name="steps-to-create-local-http-server-in-windows"></a>Étapes pour créer un serveur HTTP local dans Windows

* **Étape 1 : Créer une copie du Package de l’Action dans votre ordinateur local**

  * Créer une copie du package de l’Action dans un emplacement de votre choix sur votre ordinateur. Le nom du dossier doit être l’ID d’Action.
    
* **Étape 2 : Exécuter python commande**

  *  Ouvrez Terminal de commande et accédez au dossier contenant le Package d’Action.
  *  Exécutez la commande suivante :`python -m SimpleHTTPServer 8000`
  
      > Installation de Python est une condition préalable pour exécuter le script ci-dessus.
  
* **Étape 3 : Vérifier le serveur local**

  * L’URL du serveur local sera maintenant`http://localhost/<ActionId>:8000`
  * Pour vérifier votre serveur d’ouvrir un navigateur et entrez ci-dessus l’url du serveur local dans la barre d’adresses et vous doit être en mesure de voir le contenu du dossier à partir de laquelle le serveur a été démarré.
  
### <a name="steps-to-setup-your-android-device"></a>Étapes pour configurer votre appareil Android

> Condition Préalable : Vous devez activer le mode de débogage, comme indiqué [ici](test.md). Versions approuvées des Actions ne prennent pas en charge cette fonctionnalité

* **Étape 1 : Se connecter à votre ordinateur à l’appareil via un câble**

    * Votre appareil doit être connecté à la votre ordinateur via usb
    
* **Étape 2 : Activer les Diagnostics sur Kaizala application** 

    * Dans Kaizala, cliquez sur profil -> Paramètres -> sur. Cliquez sur « logo Microsoft Kaziala » cinq reprises pour activer l’option de Diagnostics. ** Cliquez sur Précédent pour atteindre la page Paramètres. Cliquez sur « Dépannage » située sous l’étiquette « Diagnostics » au bas de la page Paramètres
    * Activer le commutateur 'Mini applications emplacement Override' pour activer le champ URL du serveur.
    * Accédez à <chrome://inspect/> sur votre ordinateur hôte et les activer le transfert de port. Dans paramètres de transfert de port, donnez le numéro de port en tant que « 8000 "(first tab) et l’adresse IP et port en tant que « localhost:8000 » (onglet deuxième)
    * Avec cette modification Kaizala extraira les fichiers HTML/css/JS de votre Action à partir du serveur au lieu d’utiliser les fichiers de package
    
* **Étape 3 : Apporter des modifications dans le dossier de l’Action de votre ordinateur**

    * Les modifications apportées aux fichiers peuvent être observées immédiatement par le rechargement de l’affichage dans l’application (quitter l’affichage et l’ouvrir à nouveau)
    
Une fois terminé le processus de modification les fichiers mis à jour sont disponibles pour créer le package et mettre à jour le package présent dans le portail. Désactiver le commutateur Mini application substituez l’emplacement dans la page Diagnostics pour restaurer le comportement par défaut.


## <a name="enable-instant-edit-in-ios-devices"></a>Activer Modifier instantanés pour les appareils iOS

### <a name="steps-to-create-local-http-server-in-mac"></a>Étapes pour créer un serveur HTTP local dans MAC

* **Étape 1 : Créer une copie du Package de l’Action dans votre ordinateur local**

  * Créer une copie du package de l’Action dans un emplacement de votre choix sur votre ordinateur. Le nom du dossier doit être l’ID d’Action.

* **Étape 2 : Exécutez un python script**

    * Un script python est utilisé pour créer un serveur local. Voici le script(noCacheServer.py). Copiez ce fichier de script dans le dossier contenant le dossier de package MiniApp créé ci-dessus. 
                
      > Installation de Python est une condition préalable pour exécuter le script ci-dessus.

* **Étape 3 : Démarrer le serveur local**

    * Ouvrez Terminal de commande et accédez au dossier contenant le Package de l’Action et le script de serveur. 
    * Pour démarrer le serveur Entrez la commande suivante :`python noCacheServer.py 8000`
    
    L’URL du serveur local sera maintenant`http://<IP Address of your machine>:8000`

    * Pour vérifier votre serveur d’ouvrir un navigateur et entrez ci-dessus l’url du serveur local dans la barre d’adresses et vous doit être en mesure de voir le contenu du dossier à partir de laquelle le serveur a été démarré.


### <a name="steps-to-setup-your-ios-device"></a>Étapes d’installation du périphérique iOS

> Condition Préalable : Vous devez activer le mode de débogage, comme indiqué [ici](test.md). Versions approuvées des Actions ne prennent pas en charge cette fonctionnalité
* **Étape 1 : Se connecter au même réseau sur l’appareil en tant que votre ordinateur**

    * Votre appareil doit être connecté au même réseau que votre ordinateur (ou partager le réseau de votre ordinateur et connecter depuis votre appareil)
     
* **Étape 2 : Activer les Diagnostics sur Kaizala application** 

    * Dans Kaizala, cliquez sur profil -> Paramètres. Cliquez sur le titre de paramètres cinq reprises pour activer l’option de Diagnostics. Accédez à la page Diagnostics en cliquant sur l’option de Diagnostics
    * Activer le commutateur Mini application substituez l’emplacement pour activer le champ URL du serveur. Entrez l’URL du serveur créé précédemment comme indiqué ci-dessous.`http://<IP Address>:8000`
    * Avec cette modification Kaizala extraira les fichiers HTML/css/JS de votre Action à partir du serveur au lieu d’utiliser les fichiers de package
    
* **Étape 3 : Apporter des modifications dans le dossier de l’Action de votre ordinateur**

    * Les modifications apportées aux fichiers peuvent être observées immédiatement par le rechargement de l’affichage dans l’application (quitter l’affichage et l’ouvrir à nouveau)
    
Une fois terminé le processus de modification les fichiers mis à jour sont disponibles pour créer le package et mettre à jour le package présent dans le portail. Désactiver le commutateur Mini application substituez l’emplacement dans la page Diagnostics pour restaurer le comportement par défaut.

