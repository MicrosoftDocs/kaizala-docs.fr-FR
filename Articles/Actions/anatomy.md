# <a name="anatomy-of-a-kaizala-action-package"></a>Anatomie d'un package d'action Kaizala

Un package d'action Kaizala est un fichier ZIP standard qui n'est pas protégé par mot de passe et dont la taille maximale est de 1 Mo. Les ressources du package se trouvent à la racine du fichier zip et non dans une structure de répertoire. Les ressources ne peuvent pas non plus référencer de ressources externes autres que celles présentes dans le package.

Les composants de base d'un package d'action Kaizala sont 
*   Un fichier manifeste au format JSON
*   Un modèle d'application pour votre action Kaizala au format JSON
*   Ressources Web qui constituent votre action Kaizala-HTML, JS, CSS et les fichiers image

## <a name="package-manifest"></a>Manifeste de package

Le manifeste spécifie les paramètres de l'action Kaizala, tels que les suivants:
*   Le nom d'affichage, la description, l'ID, la version et l'icône d'action de l'action.
*   Différentes vues qui définissent votre action et les mappent à leurs points invokation respectifs
    * Une vue de création lorsqu'une action est appelée à partir de la palette
    * Affichage de carte qui apparaît dans la zone de conversation lors de l'envoi d'une instance de l'action
    * Une vue de répondeur permettant aux utilisateurs de répondre à l'action Kaizala
    * Affichage de synthèse pour afficher les réponses agrégées
*   Étiquettes à utiliser dans les vues natives qui encapsulent vos affichages personnalisés

Pour plus d'informations, consultez la rubrique [package MANIFEST Schema in JSON format](package_manifest_schema.md).

## <a name="app-model"></a>Modèle d'application

Le modèle d'application spécifie les fonctionnalités de l'action Kaizala, notamment:
*   Modèle de données de l'objet Form à utiliser pour tirer parti des services d'agrégation Kaizala
*   Propriétés de l'objet Form
*   Paramètres associés à l'objet Form

Pour plus d'informations, consultez la rubrique [schéma de modèle d'application au format JSON](appModel_schema.md).

## <a name="web-resources"></a>Ressources Web

Comme mentionné ci-dessus, le package Kaizala doit inclure toutes les ressources référencées à l'intérieur du package. Cela inclut toutes les ressources HTML, JavaScript, CSS et image.

L'action Kaizala la plus simple est constituée de trois pages HTML qui s'affichent lorsque
*   L'action Kaizal est appelée à partir de la palette d'actions dans l'affichage de création d'application cliente
*   Un utilisateur tente de répondre à une instance de carte d'action publiée sur la toile de conversation dans l'affichage application client-réponse
*   Un utilisateur tente d'afficher le résumé de toutes les réponses publiées pour une action spécifique-vue de synthèse

Pour interagir avec l'application cliente Kaizala, vous pouvez utiliser l' [API JavaScript KASClient. js](KASClient/README.md) que nous fournissons.


