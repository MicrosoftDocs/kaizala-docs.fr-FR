# <a name="test-and-debug"></a>Tester et déboguer

Une fois le développement d’une Action personnalisée est terminé, vous souhaiterez peut-être tester pour voir si son fonctionne correctement mettre fin à fin et corriger les éventuels problèmes que vous détectez dans le test. Ainsi que dans certains cas, vous souhaitez déboguer les affichages html pour les problèmes possibles.

Le portail de gestion Kaizala offre un moyen pratique pour tester et déboguer vos nouvelles Actions Kaizala. 
>   Vous aurez besoin d’un actif Kaizala Pro ou un abonnement à Office 365 d’organisation pour accéder au portail de gestion.

## <a name="steps-to-test-a-action"></a>Procédure de test d’une Action

Une fois que vous avez satisfait les conditions préalables, vous pouvez tester votre action en suivant étapes ci-dessous

*   Accédez au portail de gestion de Kaizala @https://manage.kaiza.la/
*    Ouvrez une session à l’aide d’un compte Office 365 existant
*    Inscrire un numéro de téléphone sur le portail en tapant sur « Ajouter un numéro de téléphone »
*    Cliquez sur « Actions » dans le menu de gauche
*    Sélectionnez « Mes Actions » dans la liste déroulante
*    Recherchez et cliquez sur l’Action que vous souhaitez tester 
*    Ouvrir la version de l’Action qui se trouve dans l’état de brouillon
*    Dans cette page, cliquez sur 'Étape'
*    Une fois que l’Action est mis en place, vous pouvez ajouter l’Action pour les groupes dont vous êtes un administrateur de

> Le groupe doit posséder une palette gérée pour le rôle d’utilisateur qui est test de l’Action

Pour pouvoir accéder à la palette 'managed', procédez comme suit :
*    Accédez à « Groupes » dans le menu de gauche
*    Recherchez le groupe que vous souhaitez gérer la palette Action et cliquez sur le groupe sélectionné
*    Accédez à l’onglet « Actions » pour le groupe sélectionné
*    Cliquez sur le lien Gestion Action Palette pour différents rôles
     *    Dans la boîte de dialogue Sélectionnez les utilisateurs pour lesquels vous souhaitez gérer la palette
     *    Cliquez sur « Enregistrer »
*    Vous pouvez trouver l’action dans la palette des groupes sélectionnés et l’utiliser en conséquence.

## <a name="steps-to-debug-a-action"></a>Étapes pour déboguer une action

Une fois que vous avez téléchargé un Action de test, vous pouvez déboguer les affichages html pour le test d’Action

*   Activer les options de développement en appuyant sur le numéro de version 7 fois. [Savoir plus](https://www.androidcentral.com/how-enable-developer-settings-android-42).
*   Activer USB @ paramètres de débogage -> Options pour les développeurs -> débogage USB
*   Attacher téléphone à ordinateur à l’aide du câble USB et installer les pilotes de périphériques si nécessaire. [Informations supplémentaires](https://developer.android.com/studio/run/oem-usb.html)
*   Ouvrez l’application Kaizala, puis l’activité qui comporte un contenu en mode Web.
*   Entrez du navigateur Chrome dans l’ordinateur et tapez **chrome://inspect** dans la barre d’adresses et de l’accès. 
*   Utilisateur verra son appareil mentionnée ici, ainsi qu’une page HTML qui est ouvert dans l’affichage Web de son application Kaizala.


**Plus :** [Instantanée modifier des Actions de migration](EditAction.md)</br>
**Suivant :** [Publier sur un groupe](publish.md)
