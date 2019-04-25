# <a name="get-started-with-custom-kaizala-actions"></a>Prise en main des actions Kaizala personnalisées

## <a name="kaizala-action-development-lifecycle"></a>Cycle de développement d'action Kaizala

Le cycle de vie de développement classique d'une action Kaizala comprend les étapes suivantes:

  **Étape 1: déterminer l'objet de l'action Kaizala**
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
Déterminez les fonctionnalités et les scénarios les plus importants et réalisez la conception à partir de ces éléments.

   **Étape 2-identifier le modèle de données pour l'action Kaizala**

Toutes les actions Kaizala sont actuellement basées sur des formulaires, c'est-à-dire que le modèle de données pour la demande, la collecte et l'agrégation des informations est un ensemble de types de questions et de réponses pris en charge par la plateforme Kaizala (KAS). Pensez à la façon dont les données requises pour votre action peuvent levergage l'infrastructure de formulaire pour fonctionner efficacement.

   **Étape 3: concevez et implémentez l'expérience utilisateur et l'interface utilisateur pour le complément.**

Concevez une expérience utilisateur rapide et fluide qui est cohérente, facile à apprendre, avec des scénarios nécessitant uniquement quelques étapes d’exécution. N'oubliez pas qu'une action Kaizala ne peut pas faire référence à des sources externes, donc être pratique en ce qui concerne les éléments que vous souhaitez mettre en œuvre dans votre action.

Vous pouvez faire votre choix parmi divers outils de développement web et utiliser du code HTML et JavaScript pour implémenter l’interface utilisateur.

Vous pouvez utiliser le kit de développement logiciel (SDK) KAS client JS pour interagir avec les services d'agrégation Kaizala et le client Kaizala natif. 

   **Étape 4: créer un fichier manifeste pour l'action basée sur le schéma de manifeste de package**

Créez un fichier manifeste en notation JSON pour identifier l'action et ses composants, et spécifiez les noms des fichiers d'affichage.

**Étape 5: créer un fichier ZIP du package et le charger sur le portail**

Créez un fichier ZIP du package avec toutes ses ressources à la racine du package.

Téléchargez le package sur le portail de gestion Kaizala. Après le chargement, l'action est à l'état Brouillon

**Étape 6: étape de l'action de brouillon**

Sur la page de détails de la version de l'action qui est en état Brouillon, appuyez sur le bouton «étape». Une fois qu'une action est intermédiaire, vous pouvez tester & déboguer l'action 

 **Étape 7: activation de l'action intermédiaire**

Une fois qu'une action est à l'état intermédiaire et qu'elle a été testée correctement, vous pouvez activer l'action dans votre organisation. L'action passe à l'état actif. Les autres membres de votre organisation peuvent également ajouter cette action à leurs groupes respectifs.

  **Étape 8: ajouter l'action à des groupes respectifs**

Une fois que l'action est dans l'état actif, vous pouvez déployer l'action sur des groupes associés à votre organisation. 

