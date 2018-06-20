# <a name="get-started-with-custom-kaizala-actions"></a>Prendre en main des Actions personnalisées Kaizala

## <a name="kaizala-action-development-lifecycle"></a>Cycle de développement Kaizala Action

Le cycle de vie de développement courantes d’une Action Kaizala comprend les étapes suivantes :

  **Étape 1 : Déterminez l’objet de l’Action Kaizala**
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
Déterminez les fonctionnalités et les scénarios les plus importants et réalisez la conception à partir de ces éléments.

   **Étape 2 : identifier le modèle de données pour l’Action Kaizala**

Toutes les Actions Kaizala actuellement formulaire basé, par exemple, le modèle de données pour la demande, collecte et regrouper des informations est un ensemble de questions et des types de réponses qui sont pris en charge par la plateforme de Services d’agrégation Kaizala (KAS). Considérer comment les données requises pour votre action peuvent levergage l’infrastructure de formulaire pour travailler efficacement.

   **Étape 3 : concevoir et implémenter l’interface d’utilisateur et une expérience utilisateur pour le complément.**

Concevoir une expérience utilisateur et la fluidité cohérente et facile à apprendre, avec les principaux scénarios qui ne nécessitent que quelques étapes à effectuer. Remeber une Action Kaizala ne peut pas faire référence à des sources externes - donc pratiques en termes de ce que vous souhaitez implémenter au sein de votre Action.

Vous pouvez faire votre choix parmi divers outils de développement web et utiliser du code HTML et JavaScript pour implémenter l’interface utilisateur.

Vous pouvez utiliser le Kit de développement logiciel JS KAS Client pour interagir avec les Services d’agrégation Kaizala Kaizala Client natif. 

   **Étape 4 : créer un fichier manifeste pour l’Action basé sur le schéma de manifeste de Package**

Créez un fichier manifest dans la notation JSON pour identifier l’Action et ses composants et spécifiez les noms des fichiers de vue.

**Étape 5 : créer un fichier ZIP du package et le télécharger sur le portail**

Créez un fichier ZIP du package avec toutes ses ressources à la racine du package.

Télécharger le package sur le portail de gestion Kaizala. Après le téléchargement, l’Action consiste en mode brouillon

**Étape 6 - étape de l’Action de brouillon**

Dans la page Détails de la version de l’Action qui est en mode brouillon, cliquez sur le bouton 'Étape'. Une fois qu’une Action est mis en place, vous pouvez tester et déboguer l’Action 

 **Étape 7 – activer l’Action intermédiaire**

Une fois qu’une Action est en état intermédiaire et a été testée avec succès, vous pouvez activer l’Action dans votre organisation. Action déplace dans un état actif. Les autres membres de votre organisation peuvent également ajouter cette Action à leurs groupes respectifs.

  **Étape 8 : ajouter l’Action à différents groupes**

Une fois que l’Action est Active, vous pouvez déployer l’Action aux groupes associés à votre organisation. 

