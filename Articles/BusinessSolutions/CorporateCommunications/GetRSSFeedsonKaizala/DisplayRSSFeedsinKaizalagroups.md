# <a name="display-rss-feeds-in-kaizala-groups"></a>Afficher les flux RSS dans des groupes Kaizala

Organisations utilisent des flux RSS pour compléter leurs systèmes de messagerie et améliorer la façon dont elles fournissent des informations aux employés. Les organisations peuvent désormais exploiter ces flux avec la première ligne et les travailleurs mobiles en lui envoyant comme des annonces aux groupes Kaizala.

Quelques exemples de flux RSS d’utilisation

1. Actualités du secteur des sites externes
2. Informations sur la société à partir des sites internes
3. Renseignez les informations à partir des sites externes
4. Mises à jour de produit
5. Groupe de flux, Ex - Finance, conception et technique 
6. Conseils et astuces, Ex-personnalisé, Sports et photographie

Cet exemple aidera, un utilisateur d’administration pour ajouter un flux RSS aux groupes Kaizala.  Cette carte a 3 champs de titre de la fiche de vue conversation carte (News Ex - Business), images, flux title (titre du flux d’informations). Fait d’appuyer sur la carte, vous accédez à l’affichage web au sein de Kaizala. 
 
 >Remarque : Uniquement l’autorisation RSS flux ouvrir l’URL dans Kaizala, dans le cas contraire, le contenu est dirigé vers un navigateur.

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

Il s’agit d’une annonce sous la forme d’une carte et Microsoft Flow est utilisée pour envoyer cette carte d’action personnalisée au groupe Kaizala.

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a>Étapes d’implémentation

1. Télécharger le [« GetRSSFeedsOnKaizala-SolutionPackage.zip »](/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*ce package contient « RSS-flux-ActionPackage.zip » et « RSS-flux-FlowPackage.zip »*)
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
           
   5. Zip all the contents in this folder (*This folder is your modified Action package which should be imported to kaizala management portal*)
   
 > Note: Select all the files in your working directory and create a new zip file for your package. Ensure that all files are present in the root directory of the package. This should include KASClient.js, package.json with new "id", "provider name" and whitelisted URL
    
4. [Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to kaizala management portal (*This card is sent by calling API, so there is no need to add the card to a group*)

5. [Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "RSS-feed-Flowpackage.zip" to your Microsoft Flow account

> Note- If you have never used RSS or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)
    
6. Edit details in Imported Flow (*See steps below*) 
   1. In the First block , enter the RSS feed URL
  
       <img src= "/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/3.1.PNG" width="600" />
   
   2. In the second block, enter the card title in "value" field. The card title will be visible to users in chat card view. Ex- "Business News"

      <img src= "/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/3.2.PNG" width="600" />

   3. In the third block, enter the Action "id" in "value" field, that you have given in package.json
   
      <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/4.png" width="600" />
   
   4. In the Last block of the Flow
        1. Select the group name or enter the group id where you want to send the card
        2. To get the group id, go to your group on https://manage.kaiza.la and select the identifier at the end of the URL.

      <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/6.PNG" width="600" />
   
       3. Click on action, to select action type as "custom value" from the dropdown
       4. Map action body to "ActionBodyJson"
       
       <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/5.png" width="600" />

7.  Save the Flow

RSS feeds will be sent to the selected Kaizala group, each time flow is triggered. 



> Note: You can only set one RSS feed URL in the Flow. To direct multiple feeds to same group, different Flows have to be created for each feed

> Known issue: On iOS, the ads take the user out of the webview since they are not whitelisted

### Useful links

1. [How to create Kaizala Groups](https://docs.microsoft.com/en-us/office365/kaizala/groups)
2. [Configure RSS Feed to SharePoint site](https://support.office.com/en-us/article/create-or-subscribe-to-an-rss-feed-fb35047d-8dbd-412a-a5f3-f1712af14dcb)
