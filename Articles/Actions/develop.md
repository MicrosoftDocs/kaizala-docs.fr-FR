# <a name="developing-a-new-kaizala-action"></a>Développement d'une nouvelle action Kaizala

Un package d'action Kaizala est un fichier zip qui contient tous les fichiers de manifeste et de ressource requis à la racine.

Pour commencer, créez un dossier sur votre PC pour en faire votre répertoire de travail.

Vous aurez besoin d'un éditeur de code pour utiliser différents types de ressources Web & fichiers manifeste.

>   Nous recommandons l'éditeur de code Visual Studio. Vous pouvez le télécharger à partir de [cet emplacement](https://code.visualstudio.com/) .

## <a name="defining-the-app-model"></a>Définition du modèle d'application

Les actions Kaizala prennent actuellement en charge les modèles de données basés sur des formulaires qui peuvent être utilisés pour la création, la collecte et l'agrégation de données à l'aide des services d'agrégation Kaizala.

Par conséquent, vous devez d'abord définir les «questions» que vous devez inclure pour créer un objet de formulaire.

RePortez-vous au [schéma JSON du modèle d'application](appModel_schema.md) pour créer le modèle d'application de votre action.

## <a name="define-the-creation-view"></a>Définir la vue de création

Lorsqu'une nouvelle instance de l'action Kaizala est appelée à partir de la palette d'action de l'application, la ressource HTML marquée comme CreationView est rendue. L'objectif de cette vue de création est de créer une nouvelle instance de l'objet Form tel qu'il est défini dans le modèle d'application. 

Pour interagir avec les services d'agrégation Kaizala et en créant la nouvelle instance de formulaire, vous pouvez consulter les API dans le [Kit de développement logiciel (SDK) KASCLIENT js](KASClient/README.md). Vous devrez télécharger le [fichier KASCLIENT js](https://manage.kaiza.la/MiniApps/DownloadSDK) et l'inclure dans votre package.

Créez un fichier HTML qui représente cette vue de création. Dans le fichier JavaScript correspondant, appelez le kit de développement logiciel (SDK) KASClient JS et créez un objet Form.

## <a name="create-the-package-manifest-file"></a>Créer le fichier manifeste de package

Maintenant que vous avez un semblance de ce que vous souhaitez obtenir et que vous avez créé une vue, vous pouvez commencer à créer votre fichier manifeste de package.

Le fichier manifeste du package Kaizala fournit des informations essentielles sur la plateforme Kaizala pour qu'il reconnaisse et exécute votre action Kaizala personnalisée.

RePortez-vous au [schéma JSON du manifeste de package](package_manifest_schema.md) pour créer le manifeste de package de votre action.

À ce stade, vous devez également inclure un fichier d'icône pour votre action personnalisée dans le package.

RePortez-vous à votre fichier HTML d'affichage de création dans le manifeste du package et mappez-le à l'objet Parameter approprié.

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a>Configurer la carte qui apparaît dans la zone de conversation de conversation

Lorsqu'une nouvelle instance d'une action Kaizala est créée et publiée dans une conversation, une carte d'action s'affiche dans la zone de dessin pour que d'autres utilisateurs de la conversation puissent afficher et envoyer leurs réponses.

Pour personnaliser la vue de la carte de conversation, reportez-vous à la rubrique [customizIng ChatCardView](ChatCanvasCardView.md) 
## <a name="define-the-response--summary-views"></a>Définir les vues récapitulatives de la réponse &

Lorsque les utilisateurs essaient d'afficher des détails et de répondre à une instance de l'action Kaizala publiée dans une conversation, ils peuvent voir deux types d'affichage.
*   Affichage des réponses lorsqu'ils cliquent sur le bouton d'appel à l'action principal et que vous souhaitez valider une réponse
*   Affichage de synthèse lorsqu'ils cliquent sur l'en-tête de la carte et que vous souhaitez afficher la vue agrégée de tous les reesponses publiés

Créez un ou plusieurs fichiers HTML selon vos besoins pour définir votre action et mappez-les aux paramètres pertinentes dans le fichier manifeste du package.

Pour interagir avec les services d'agrégation Kaizala et le client natif Kaizala pour récupérer des informations, soumettre une réponse ou obtenir des réponses regroupées, vous pouvez consulter les API dans le [Kit de développement logiciel (SDK) de KASCLIENT js](KASClient/README.md).


## <a name="create-the-zip-file"></a>Créer le fichier ZIP

Sélectionnez tous les fichiers dans votre répertoire de travail et créez un fichier zip pour votre package. Assurez-vous que tous les fichiers sont présents dans le répertoire racine du package.

*   À suivre: [publier](publish.md)
