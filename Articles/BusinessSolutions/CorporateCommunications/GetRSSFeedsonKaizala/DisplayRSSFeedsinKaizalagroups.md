# <a name="display-rss-feeds-in-kaizala-groups"></a>Afficher les flux RSS dans des groupes Kaizala

Organisations utilisent des flux RSS pour compléter leurs systèmes de messagerie et améliorer la façon dont elles fournissent des informations aux employés. Les organisations peuvent désormais exploiter ces flux avec la première ligne et les travailleurs mobiles en lui envoyant comme des annonces aux groupes Kaizala.

Quelques exemples de flux RSS d’utilisation :

1. Actualités du secteur des sites externes
2. Informations sur la société à partir des sites internes
3. Renseignez les informations à partir des sites externes
4. Mises à jour de produit
5. Groupe de flux, par exemple, Finance, conception et Tech 
6. Conseils et astuces, par exemple, outil, Sports et photographie

Cet exemple aidera, un utilisateur d’administration pour ajouter un flux RSS aux groupes Kaizala. Cette carte est 3 dotée de champs dans le titre de l’entrée de l’affichage carte conversation (par exemple, des informations sur les), une Image et le titre du flux. Fait d’appuyer sur la carte prendrait l’utilisateur de l’affichage web au sein de Kaizala. 
 
 >Remarque : Uniquement l’autorisation RSS flux ouvrir l’URL dans Kaizala, dans le cas contraire, le contenu est dirigé vers un navigateur.

<img src="GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

Il s’agit d’une annonce sous la forme d’une carte et flux est utilisé pour envoyer cette carte d’action personnalisée au groupe Kaizala.

<img src="GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a>Étapes d’implémentation

1. Télécharger le [« GetRSSFeedsOnKaizala-SolutionPackage.zip »](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*ce package contient « RSS-flux-ActionPackage.zip » et « RSS-flux-FlowPackage.zip »*)
2. Télécharger la dernière version de Kaizala [« ActionSDK.Zip »](https://manage.kaiza.la/MiniApps/DownloadSDK)(*il contient un fichier KASClient.js*)
3. Modifier le « RSS-flux-ActionPackage.zip » (*comme indiqué ci-dessous*)
   1. Décompressez le package action « RSS-flux-ActionPackage.zip » dans un dossier
   2. Modifier l’action « id » et « nom » dans package.json
   3. Ajouter le fichier KASClient.js dans ce dossier 
   4. Ajouter le QU'URL du flux RSS dans package.json(as below) à la liste d’autorisation URL. Dans cet exemple, les URL de tendances numérique est autorisés.    
         ```
      "externalUrls": [
      { "url": "https://www.digitaltrends.com" }
      ]  
      ```
   5. Le code postal tout le contenu de ce dossier (*ce dossier est votre package Action modifié qui doit être importé dans le portail de gestion kaizala*)
   
 > Remarque : Sélectionnez tous les fichiers dans votre répertoire de travail et créer un nouveau fichier zip pour votre package. Assurez-vous que tous les fichiers sont présents dans le répertoire racine du package. Cette valeur doit inclure KASClient.js, package.json avec nouveau « id », « nom du fournisseur » et autorisation URL
 
4. [Importation](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) du package action modifiées au portail de gestion kaizala (*cette carte est envoyé par un appel d’API, et il n’est pas nécessaire d’ajouter la carte à un groupe*)
5. [Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le « RSS-flux-Flowpackage.zip » à votre compte Microsoft Flow

    > Remarque : Si vous n’avez jamais utilisé connexions RSS ou Kaizala, première [Ajouter des connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)    

6. Modifier les détails dans importés flux (*voir les étapes ci-dessous*) 
   1. Dans le premier bloc, entrez l’URL du flux RSS <img src= "GetRSSFeedsOnKaizalaImages/3.1.PNG" width="600" />
   2. Dans le deuxième bloc, entrez le titre de l’entrée dans le champ « valeur ». Le titre de la carte seront visible pour les utilisateurs dans l’affichage de carte de conversation. Par exemple, des informations sur « »
   
      <img src= "GetRSSFeedsOnKaizalaImages/3.2.PNG" width="600" />
   3. Dans le troisième bloc, entrez l’Action « id » dans le champ « valeur », ce qui vous avez attribué dans package.json
      <img src="GetRSSFeedsOnKaizalaImages/4.png" width="600" />
   4. Dans le dernier bloc du flux
        1. Sélectionnez le nom du groupe ou entrez l’id de groupe dans lequel vous souhaitez envoyer la carte
        2. Pour obtenir l’id de groupe, accédez à votre groupe sur https://manage.kaiza.la et sélectionnez l’identificateur à la fin de l’URL.
        
            <img src="GetRSSFeedsOnKaizalaImages/6.PNG" width="600" />
            
        3. Cliquez sur action, sélectionnez le type d’action en tant que « valeur personnalisée » dans la liste déroulante
        4. Mapper les corps à « ActionBodyJson »
       
       <img src="GetRSSFeedsOnKaizalaImages/5.png" width="600" />
7.  Enregistrer le flux

 Flux RSS sont envoyées au groupe Kaizala sélectionné, chaque flux de temps est déclenché. 

> Remarque : Vous ne pouvez définir un flux RSS URL dans le flux. Pour indiquer plusieurs flux au même groupe, différents flux doivent être créées pour chaque flux

> Problème connu : sur iOS, les annonces prennent l’utilisateur en dehors de l’affichage Web dans la mesure où ils ne sont pas autorisés

### <a name="useful-links"></a>Liens utiles
1. [Comment créer des groupes Kaizala](https://docs.microsoft.com/en-us/office365/kaizala/groups)
2. [Configurer le flux RSS pour un site SharePoint](https://support.office.com/en-us/article/create-or-subscribe-to-an-rss-feed-fb35047d-8dbd-412a-a5f3-f1712af14dcb)
