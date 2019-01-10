# <a name="share-inspirational-quotes"></a>Partager des guillemets inspiration

Chaque organisateur aime inspirer des ressources et parfois l’inspiration est requise pour guider une équipe provient de simples mots de prudence. Quelques mots de prudence avec les équipes peuvent avoir un impact dynamique sur morale employé et les performances. 

Organisations permet cette carte partager inspiration devis régulièrement et pas seulement limiter à séminaires, salles et au courrier électronique de la réunion. Les utilisateurs peuvent choisir parmi cinq arrière-plans colorés ou partage image guillemets dans un groupe. Les utilisateurs peuvent également choisir rédiger un message, ainsi que la proposition. 

> Remarque : Cette carte est optimisée pour les images portrait 

Il s’agit d’une carte avec des vues de création, affichage de carte graphique et immersif simple.

Mode création :

<img src="InspirationalQuotes@WorkplaceImages/1.png" alt="Chat card view Logo" width="200" />

Afficher la carte conversation :

<img src="InspirationalQuotes@WorkplaceImages/2.png" alt="Chat card view Logo" width="200" />

Mode immersif :

<img src="InspirationalQuotes@WorkplaceImages/3.png" alt="Chat card view Logo" width="200" />

## <a name="implementation-steps"></a>Étapes d’implémentation :
1. Télécharger le [« ShareQuotesOnKaizala-SolutionPackage.zip »](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/InspirationalQuotes%40Workplace/ShareQuotesOnKaizala-SolutionPackage.zip) (*cette action contient*)
2. Télécharger la dernière version de Kaizala [« ActionSDK.Zip »](https://manage.kaiza.la/MiniApps/DownloadSDK) (*contient KASClient.js*)
3. Modifier le « ShareQuotesOnKaizala-SolutionPackage.Zip » (*comme indiqué ci-dessous*)
   1. Décompressez « ShareQuotesOnKaizala-SolutionPackage.Zip » dans un dossier
   2. Modifier l’action « id » et « nom » dans package.json
   3. Ajouter KASClient.js à ce dossier 
   4. Ajouter des html2canvas.min.js de https://html2canvas.hertzen.com/ dans ce dossier.
   5. Le code postal tout le contenu de ce dossier (*ce dossier est votre package modifié action qui doit être importé dans le portail de gestion kaizala*) 
       
      > Remarque : sélectionnez tous les fichiers dans votre répertoire de travail et créer un nouveau fichier zip pour votre package. Assurez-vous que tous les fichiers sont présents dans le répertoire racine du package. Cela doit inclure client KAS, package. JSON avec une nouvelle action « id » et « nom du fournisseur ». En outre, **Veuillez reportez-vous au guide de licence de html2canvas.min.js et être conforme aux termes et conditions avant d’ajouter des html2canvas.min.js à votre package d’action et télécharger vers votre client**
       
4. [Importation](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) du package action modifiées au [portail de gestion kaizala](https://manage.kaiza.la/)
5. [Publier](https://docs.microsoft.com/en-us/kaizala/actions/publish) l’action et ajouter l’action à un groupe dans lequel vous souhaitez ajouter la carte
6. Sélectionnez les rôles d’utilisateur en tant qu’administrateur et membre pour envoyer la carte dans plat et les groupes publics gérées

> Remarque : Dans un groupe plat, tous les membres du groupe et administrateurs peuvent créer et envoyer cette carte. Dans groupe Public gérée, seuls les utilisateurs rôle admin et membre peuvent envoyer cette carte, tandis que les abonnés reçoit la carte.

Voici quelques devis connues personnalités qui vous aidera à démarrer :

 1. Nous sommes ce que nous faisons à plusieurs reprises. Excellence, n’est pas un acte, mais une habitude. – Aristote
 2. Il n’existe aucune secrets de la réussite. Il est le résultat de la préparation d’un travail et apprentissage à partir de l’échec. – Colin Powell
 3. L’esprit est tout. Ce que vous pensez devenir. – Buddha
 4. Exemple n’est pas l’essentiel dans influant sur d’autres personnes. Il est la seule chose-Albert Schweitzer
 5. Toujours l’esprit que votre propre solution aboutisse est plus importante que n’importe quel autre - Abraham Lincoln

## <a name="useful-links"></a>Liens utiles

[Groupes de Kaizala](https://docs.microsoft.com/en-us/kaizala/partnerdocs/groupsinkaizala)
