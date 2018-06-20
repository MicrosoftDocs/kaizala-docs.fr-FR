# <a name="anatomy-of-a-kaizala-action-package"></a>Anatomie d’un package de l’Action Kaizala

Un package Kaizala Action est un fichier ZIP régulière qui n’est pas protégé par mot de passe et ne peut pas dépasser 1 Mo. Les ressources dans le package sont à la racine du fichier zip et non pas dans une structure de répertoire. Les ressources ne peuvent pas également faire référence à des ressources externes, autres que celles présentes dans le package.

Les composants de base d’un package Kaizala Action sont 
*   Un fichier manifeste au format JSON
*   Un modèle d’application pour votre Action Kaizala au format JSON
*   Ressources Web qui constituent votre Action Kaizala - HTML, JS, CSS et fichiers image

## <a name="package-manifest"></a>Manifeste du package

Le manifeste spécifie les paramètres de l’Action Kaizala, telles que les suivantes :
*   De l’Action nom complet, description, ID, version et icône Action.
*   Différentes vues qui définissent votre Action et les mapper à leur point invokation respectifs
    * Un affichage Création lorsqu’une Action est appelée à partir de la palette
    * Une vue de carte qui apparaît dans la zone de conversation lorsqu’une instance de l’Action est envoyée
    * Une vue répondeur pour les utilisateurs répondre à l’Action Kaizala
    * Un résumé Affichage agrégé réponses
*   Étiquettes pour être utilisés dans les affichages natives qui encapsulent les vues personnalisées

Pour plus d’informations, voir [Schéma de manifeste de Package au format JSON](package_manifest_schema.md).

## <a name="app-model"></a>Modèle d’application

Le modèle d’application spécifie les fonctionnalités de l’Action Kaizala, y compris :
*   Le modèle de données pour l’objet de formulaire à utiliser pour mettre à profit les Services d’agrégation Kaizala
*   Propriétés de l’objet de formulaire
*   Paramètres associés à l’objet de formulaire

Pour plus d’informations, voir [Schéma de modèle d’application au format JSON](appModel_schema.md).

## <a name="web-resources"></a>Ressources Web

Comme mentionné ci-dessus, le package Kaizala doit inclure toutes les ressources référencés dans le package. Cela inclut toutes les ressources HTML, JavaScript, CSS et image.

L’Action Kaizala plus élémentaire se compose de trois pages HTML qui sont affichées lorsque
*   L’Action Kaizal est appelée à partir de la Palette de l’Action dans l’application cliente - mode Création
*   Un utilisateur tente de répondre à une instance de carte Action publiée sur la zone de conversation dans l’application cliente - affichage de réponse
*   Un utilisateur essaie d’afficher le résumé de toutes les réponses validée pour une instance d’Action spécifique - affichage de synthèse

Pour interagir avec l’application de client Kaizala, vous pouvez utiliser l' [Interface API JavaScript KASClient.js](KASClient/README.md) que nous fournissons.


