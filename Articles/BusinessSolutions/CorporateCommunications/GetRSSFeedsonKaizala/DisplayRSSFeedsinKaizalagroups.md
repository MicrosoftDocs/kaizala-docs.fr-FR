# <a name="display-rss-feeds-in-kaizala-groups"></a><span data-ttu-id="718a9-101">Afficher les flux RSS dans des groupes Kaizala</span><span class="sxs-lookup"><span data-stu-id="718a9-101">Display RSS feeds in Kaizala groups</span></span>

<span data-ttu-id="718a9-102">Organisations utilisent des flux RSS pour compléter leurs systèmes de messagerie et améliorer la façon dont elles fournissent des informations aux employés.</span><span class="sxs-lookup"><span data-stu-id="718a9-102">Organizations use RSS feeds to complement their e-mail systems and improve the way they provide information to employees.</span></span> <span data-ttu-id="718a9-103">Les organisations peuvent désormais exploiter ces flux avec la première ligne et les travailleurs mobiles en lui envoyant comme des annonces aux groupes Kaizala.</span><span class="sxs-lookup"><span data-stu-id="718a9-103">Organizations can now leverage these feeds with the first line and mobile workers by sending them as announcements to Kaizala groups.</span></span>

<span data-ttu-id="718a9-104">Quelques exemples de flux RSS d’utilisation</span><span class="sxs-lookup"><span data-stu-id="718a9-104">Few use cases of RSS feeds</span></span>

1. <span data-ttu-id="718a9-105">Actualités du secteur des sites externes</span><span class="sxs-lookup"><span data-stu-id="718a9-105">Industry News from external sites</span></span>
2. <span data-ttu-id="718a9-106">Informations sur la société à partir des sites internes</span><span class="sxs-lookup"><span data-stu-id="718a9-106">Company news from internal sites</span></span>
3. <span data-ttu-id="718a9-107">Renseignez les informations à partir des sites externes</span><span class="sxs-lookup"><span data-stu-id="718a9-107">Compete Information from external sites</span></span>
4. <span data-ttu-id="718a9-108">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="718a9-108">Product Updates</span></span>
5. <span data-ttu-id="718a9-109">Groupe de flux, Ex - Finance, conception et technique</span><span class="sxs-lookup"><span data-stu-id="718a9-109">Group specific feeds, Ex- Finance, Design and Tech</span></span> 
6. <span data-ttu-id="718a9-110">Conseils et astuces, Ex-personnalisé, Sports et photographie</span><span class="sxs-lookup"><span data-stu-id="718a9-110">Tips and Tricks, Ex- DIY, Sports and Photography</span></span>

<span data-ttu-id="718a9-111">Cet exemple aidera, un utilisateur d’administration pour ajouter un flux RSS aux groupes Kaizala.</span><span class="sxs-lookup"><span data-stu-id="718a9-111">This sample will help, an admin user to add RSS feeds to Kaizala groups.</span></span>  <span data-ttu-id="718a9-112">Cette carte a 3 champs de titre de la fiche de vue conversation carte (News Ex - Business), images, flux title (titre du flux d’informations).</span><span class="sxs-lookup"><span data-stu-id="718a9-112">This card has 3 fields in chat card view- Card title(Ex- Business News), Image, Feed title ( Title of the News Feed).</span></span> <span data-ttu-id="718a9-113">Fait d’appuyer sur la carte, vous accédez à l’affichage web au sein de Kaizala.</span><span class="sxs-lookup"><span data-stu-id="718a9-113">Tapping on the card will take you to web view within Kaizala.</span></span> 
 
 ><span data-ttu-id="718a9-114">Remarque : Uniquement l’autorisation RSS flux ouvrir l’URL dans Kaizala, dans le cas contraire, le contenu est dirigé vers un navigateur.</span><span class="sxs-lookup"><span data-stu-id="718a9-114">Note: Only whitelisted RSS feed URL's open within Kaizala, if not, the content would be directed to a browser.</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

<span data-ttu-id="718a9-115">Il s’agit d’une annonce sous la forme d’une carte et Microsoft Flow est utilisée pour envoyer cette carte d’action personnalisée au groupe Kaizala.</span><span class="sxs-lookup"><span data-stu-id="718a9-115">This is an announcement in the form of a card and Microsoft Flow is used to send this custom action card to Kaizala group.</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a><span data-ttu-id="718a9-116">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="718a9-116">Implementation steps</span></span>

1. <span data-ttu-id="718a9-117">Télécharger le [« GetRSSFeedsOnKaizala-SolutionPackage.zip »](/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*ce package contient « RSS-flux-ActionPackage.zip » et « RSS-flux-FlowPackage.zip »*)</span><span class="sxs-lookup"><span data-stu-id="718a9-117">Download the ["GetRSSFeedsOnKaizala-SolutionPackage.zip"](/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*This package contain "RSS-feed-ActionPackage.zip" and "RSS-feed-FlowPackage.zip"*)</span></span>
2. <span data-ttu-id="718a9-118">Télécharger la dernière version de Kaizala [« ActionSDK.Zip »](https://manage.kaiza.la/MiniApps/DownloadSDK)(*il contient un fichier KASClient.js*)</span><span class="sxs-lookup"><span data-stu-id="718a9-118">Download the latest version of Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK)(*This contains KASClient.js file*)</span></span>
3. <span data-ttu-id="718a9-119">Modifier le « RSS-flux-ActionPackage.zip » (*comme indiqué ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="718a9-119">Edit the "RSS-feed-ActionPackage.zip" (*as below*)</span></span>
   1. <span data-ttu-id="718a9-120">Décompressez le package action « RSS-flux-ActionPackage.zip » dans un dossier</span><span class="sxs-lookup"><span data-stu-id="718a9-120">Unzip action package "RSS-feed-ActionPackage.zip" to a folder</span></span>
   2. <span data-ttu-id="718a9-121">Modifier l’action « id » et « nom » dans package.json</span><span class="sxs-lookup"><span data-stu-id="718a9-121">Change the action "id" and "provider name" in package.json</span></span>
   3. <span data-ttu-id="718a9-122">Ajouter le fichier KASClient.js dans ce dossier</span><span class="sxs-lookup"><span data-stu-id="718a9-122">Add KASClient.js file to this folder</span></span> 
   4. <span data-ttu-id="718a9-123">Ajouter le QU'URL du flux RSS dans package.json(as below) à la liste d’autorisation URL.</span><span class="sxs-lookup"><span data-stu-id="718a9-123">Add RSS feed URL in package.json(as below) to whitelist that URL.</span></span> <span data-ttu-id="718a9-124">Dans cet exemple, les URL de tendances numérique est autorisés.</span><span class="sxs-lookup"><span data-stu-id="718a9-124">In this example, digital trends URL is whitelisted.</span></span>    
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
