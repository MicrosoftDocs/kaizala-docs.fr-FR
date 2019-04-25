# <a name="test-and-debug"></a>Test et déBogage

Une fois que le développement d'une action personnalisée est terminé, vous pouvez le tester pour voir s'il a fini de se terminer et résoudre les bogues que vous avez découverts lors des tests. De même, dans certains cas, vous souhaitez déboguer les vues html pour tout problème éventuel.

Le portail de gestion Kaizala offre un moyen pratique de tester & de déboguer vos nouvelles actions Kaizala. 
>   Vous aurez besoin d'un abonnement d'organisation actif Kaizala Pro ou Office 365 pour accéder au portail de gestion.

## <a name="steps-to-test-a-action"></a>Étapes de test d'une action

Une fois que vous avez satisfait les conditions préalables, vous pouvez tester votre action en suivant les étapes ci-dessous.

*   Accédez au portail de gestion Kaizala @https://manage.kaiza.la/
*    Se connecter à l'aide d'un compte Office 365 existant
*    Enregistrer un numéro de téléphone sur le portail en tapant «ajouter un numéro de téléphone»
*    Appuyez sur «actions» dans le menu de gauche.
*    Sélectionnez «mes actions» dans la liste déroulante.
*    Recherchez et cliquez sur l'action que vous souhaitez tester. 
*    Ouvrir la version de l'action qui est en état Brouillon
*    Sur cette page, appuyez sur «stage»
*    Une fois que l'action est intermédiaire, vous pouvez ajouter l'action aux groupes dont vous êtes administrateur.

> Le groupe doit disposer d'une palette gérée pour le rôle d'utilisateur qui teste l'action.

Pour faire de la palette «gérée», suivez les étapes ci-dessous:
*    Accéder à «groupes» dans le menu de gauche
*    Recherchez le groupe pour lequel vous souhaitez gérer la palette d'action, puis cliquez sur le groupe sélectionné.
*    Accéder à l'onglet actions pour le groupe sélectionné
*    Cliquez sur le lien pour gérer la palette d'action pour différents rôles.
     *    Dans la boîte de dialogue, sélectionnez les utilisateurs pour lesquels vous souhaitez gérer la palette.
     *    Cliquez sur «Enregistrer».
*    Vous pouvez rechercher l'action dans la palette des groupes sélectionnés et l'utiliser en conséquence.

## <a name="steps-to-debug-a-action"></a>Étapes de débogage d'une action

Une fois que vous avez téléchargé une action de test, vous pouvez déboguer les vues HTML de l'action de test.

*   Activez les options de développeur en appuyant sur le numéro de build 7 fois. En [savoir plus](https://www.androidcentral.com/how-enable-developer-settings-android-42).
*   Activer le débogage USB @ Settings-options pour les développeurs >-> USB Debugging
*   Reliez le téléphone à l'ordinateur à l'aide du câble USB et installez les pilotes de périphérique requis, le cas échéant. [En savoir plus](https://developer.android.com/studio/run/oem-usb.html)
*   Ouvrez l'application Kaizala, puis ouvrez l'activité qui comporte du contenu WebView.
*   Ouvrez le navigateur Chrome dans ordinateur et tapez **chrome://Inspect** dans la barre d'adresses, puis appuyez sur entrée. 
*   L'utilisateur verra son appareil mentionné ici, ainsi qu'une page HTML, qui est ouverte dans le WebView de son application Kaizala.


En **savoir plus:** [Modification instantanée des actions intermédiaires](EditAction.md)</br>
**Suivant:** [Publier dans un groupe](publish.md)
