# <a name="instant-edit-of-actions-in-staged-environment"></a>Modification instantanée des actions dans un environnement intermédiaire

Avant de commencer à modifier les actions, activez l' [état intermédiaire](test.md) .

Lors de la création d'une action, les vues HTML et ses fichiers associés (CSS, js) sont regroupés dans le package d'action et sont importés sur le portail de gestion Kaizala. Toute modification supplémentaire apportée aux affichages nécessite que le package soit recréé et téléchargé sur le portail de gestion Kaizala.

Afin de simplifier la modification ultérieure des affichages HTML, Kaizala permet de modifier les fichiers HTML, JavaScript et CSS localement et de voir immédiatement les mises à jour dans l'application Kaizala. Cela implique la création d'un serveur HTTP local qui hébergera les fichiers mis à jour et l'application Kaizala utilisera ces fichiers au lieu des fichiers présents dans le package.

>  **Remarque:** Pour activer la modification instantanée, l'action doit être téléchargée sur le portail de gestion Kaizala et doit être à l'état intermédiaire.

## <a name="enable-instant-edit-in-android-devices"></a>Activer la modification instantanée dans les appareils Android

### <a name="steps-to-create-local-http-server-in-windows"></a>Étapes à suivre pour créer un serveur HTTP local dans Windows

* **Étape 1: créer une copie du package d'actions sur votre ordinateur local**

  * Créez une copie du package d'actions à l'emplacement de votre choix sur votre ordinateur. Le nom du dossier doit être l'ID d'action.
    
* **Étape 2: exécuter la commande python**

  *  Ouvrez le terminal de commandes et accédez au dossier contenant le package d'action.
  *  Exécutez la commande suivante:`python -m SimpleHTTPServer 8000`
  
      > L'installation de Python est une condition préalable à l'exécution du script ci-dessus.
  
* **Étape 3: vérifier le serveur local**

  * L'URL de votre serveur local sera désormais`http://localhost/<ActionId>:8000`
  * Pour vérifier que votre serveur ouvre un navigateur et entrez au-dessus de l'URL du serveur local dans la barre d'adresses, vous devez être en mesure d'afficher le contenu du dossier à partir duquel le serveur a été démarré.
  
### <a name="steps-to-setup-your-android-device"></a>Étapes de configuration de votre appareil Android

> Conditions préalables: vous devez activer le mode débogage, comme indiqué [ici](test.md). Les versions approuvées des actions ne prennent pas en charge cette fonctionnalité.

* **Étape 1: connecter votre ordinateur à l'appareil via un USB**

    * Votre appareil doit être connecté à votre ordinateur via USB
    
* **Étape 2: activer les diagnostics sur l'application Kaizala** 

    * Dans Kaizala, accédez à Profile-> paramètres-> à propos de. Appuyez sur «logo Microsoft Kaziala» cinq fois pour activer l'option Diagnostics. * * Appuyez sur retour pour accéder à la page Paramètres. Cliquez sur l'option dépannage sous l'étiquette «Diagnostics» en bas de la page Paramètres.
    * Activez le commutateur «mini-applications à l'emplacement prioritaire» pour activer le champ URL du serveur.
    * Accédez à <chrome://inspect/> sur votre ordinateur hôte et activez le transfert de port. Dans paramètres de transfert de port, donnez au numéro de Port la valeur «8000» (premier onglet) et l'adresse IP et le port «localhost: 8000» (deuxième onglet)
    * Avec cette modification Kaizala extrait les fichiers HTML/CSS/JS de votre action à partir du serveur au lieu d'utiliser les fichiers empaquetés.
    
* **Étape 3: effectuer des modifications dans le dossier action de votre ordinateur**

    * Toutes les modifications apportées aux fichiers peuvent être observées immédiatement en rechargeant l'affichage dans l'application (quittez et redémarrez l'affichage)
    
Une fois le processus d'édition terminé, les fichiers mis à jour peuvent être regroupés pour créer le package et mettre à jour le package présent dans le portail. Désactivez le commutateur mini-emplacement d'une mini-application dans la page Diagnostics pour restaurer le comportement par défaut.

