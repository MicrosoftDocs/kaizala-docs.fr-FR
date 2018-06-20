# <a name="developing-a-new-kaizala-action"></a>Développement d’une nouvelle Action Kaizala

Un package de l’Action Kaizala est un fichier zip qui contient tous les fichiers de manifeste et des ressources requises à la racine.

Pour commencer, créez un nouveau dossier sur votre ordinateur afin de rendre votre dorectory de travail.

Vous aurez besoin d’un éditeur de code pour travailler avec différents types de ressources web et les fichiers manifeste.

>   Nous vous recommandons de l’éditeur de Code Visual Studio. Vous pouvez le télécharger à partir [d’ici](https://code.visualstudio.com/)

## <a name="defining-the-app-model"></a>Définition du modèle d’application

Les Actions Kaizala prend en charge les modèles de données de formulaire en fonction de qui peuvent être utilisés pour la création, collecte et consolidation des données en utilisant les Services d’agrégation Kaizala.

Par conséquent, vous devez d’abord définir les questions que vous devez inclure pour créer un objet form.

Reportez-vous à l' [application schéma JSON de modèle](appModel_schema.md) pour créer le modèle d’application de votre Action.

## <a name="define-the-creation-view"></a>Définir le mode de création

Lorsqu’une nouvelle instance de l’Action Kaizala est appelée à partir de Action Palette l’application, la ressource HTML marqué comme la CreationView s’affiche. L’objectif de cet affichage Création consiste à créer une nouvelle instance de l’objet de formulaire tel que défini dans le modèle d’application. 

Pour interagir avec les Services d’agrégation Kaizala et la création de la nouvelle instance de formulaire, vous pouvez faire référence aux API dans le [Kit de développement logiciel KASClient JS](KASClient/README.md). Vous devez télécharger le [Fichier de KASClient JS](https://manage.kaiza.la/MiniApps/DownloadSDK) et l’inclure dans votre package.

Créer un nouveau fichier HTML qui représente ce mode Création. Dans le fichier javascript correspondant, appeler le Kit de développement KASClient JS et créez un objet form.

## <a name="create-the-package-manifest-file"></a>Créer le fichier de manifeste de Package

Maintenant que vous disposez d’un semblance de ce que vous souhaitez atteindre et avez créé un affichage – vous pouvez commencer à créer votre fichier manifeste de package.

Le fichier manifeste de Kaizala Package fournit des informations essentielles pour la plate-forme Kaizala pour qu’il reconnaisse et exécuter l’action Kaizala personnalisée.

Reportez-vous à la [JSON schéma de manifeste de package](package_manifest_schema.md) pour créer le manifeste du package de votre Action.

À ce stade, vous devez également inclure un fichier d’icône pour votre Action personnalisée dans le package.

Fichier HTML d’affichage Création dans le manifeste du package et mappez-le sur l’objet de paramètre pertinent.

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a>Configurer la carte qui apparaît dans la zone de conversation

Lorsqu’une nouvelle instance d’une Action Kaizala est créée et publiée dans une conversation, une carte d’Action s’affiche dans la zone de dessin pour d’autres utilisateurs de la conversation afficher et soumettre leurs réponses.

Afin de personnaliser l’affichage de carte de conversation, reportez-vous à [Personnalisation de ChatCardView](ChatCanvasCardView.md) 
## <a name="define-the-response--summary-views"></a>Définir la réponse et les affichages de synthèse

Lorsque les utilisateurs tentent d’afficher plus d’informations et de répondre à une instance de l’Action Kaizala publié dans une conversation, ils peuvent voir les deux types d’affichages.
*   Affichage de réponse lorsqu’ils cliquez sur le bouton d’appel à l’action principal et want publier une réponse
*   Affichage de synthèse lorsqu’ils cliquez sur l’en-tête de la carte et pour afficher la vue agrégée de toutes les reesponses publiés

Créez un ou plusieurs fichiers HTML nécessaire pour définir votre Action et mettez-les en correspondance avec les paramètres appropriées dans le fichier manifeste de package.

Pour interagir avec les Services d’agrégation Kaizala et le client natif Kaizala pour récupérer des informations, envoyer une réponse ou obtenir des réponses agrégées, vous pouvez faire référence aux API dans le [Kit de développement logiciel KASClient JS](KASClient/README.md).


## <a name="create-the-zip-file"></a>Créer le fichier ZIP

Sélectionnez tous les fichiers dans votre répertoire de travail et créer un nouveau fichier zip pour votre package. Assurez-vous que tous les fichiers sont présents dans le répertoire racine du package.

*   À suivre : [Publier](publish.md)
