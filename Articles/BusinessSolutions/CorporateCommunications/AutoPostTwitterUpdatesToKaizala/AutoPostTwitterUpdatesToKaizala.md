# <a name="auto-post-twitter-updates-to-kaizala"></a><span data-ttu-id="68c88-101">Mises à jour Kaizala auto-Post Twitter</span><span class="sxs-lookup"><span data-stu-id="68c88-101">Auto-Post Twitter updates to Kaizala</span></span>

<span data-ttu-id="68c88-102">Validation pour Twitter pages employé fait partie des activités quotidiennes, mais que vous ayez à valider les mêmes informations plusieurs fois est très difficile.</span><span class="sxs-lookup"><span data-stu-id="68c88-102">Posting to Twitter employee pages is part of daily business, but having to post the same information multiple times is quite difficult.</span></span> <span data-ttu-id="68c88-103">Encourager les employés peuvent partager des mises à jour des médias sociaux, lorsque vous avez terminé correctement peut étendre considérablement suivant de la société.</span><span class="sxs-lookup"><span data-stu-id="68c88-103">Encouraging employees to share social media updates, when done properly can dramatically expand company's following.</span></span> 

<span data-ttu-id="68c88-104">Cet exemple de solution gagne du temps par automatique-validation les mises à jour de l’état de votre compte twitter officiel aux groupes Kaizala.</span><span class="sxs-lookup"><span data-stu-id="68c88-104">This sample solution saves your time by auto-posting the status updates from your official twitter account to Kaizala groups.</span></span> <span data-ttu-id="68c88-105">Une carte de l’annonce est envoyée au groupe lorsqu’un ou tous les sous déclencheurs se produisent</span><span class="sxs-lookup"><span data-stu-id="68c88-105">An announcement card is sent to the group when one or all the below triggers occur</span></span>

1. <span data-ttu-id="68c88-106">Un nouveau tweet est publié sur un handle spécifique twitter E.g.,"@InsideFabrikam »</span><span class="sxs-lookup"><span data-stu-id="68c88-106">A new tweet is posted on a specific twitter handle E.g.,"@InsideFabrikam"</span></span>

2. <span data-ttu-id="68c88-107">Une publication est nouveau tweetée dans ce handle twitter</span><span class="sxs-lookup"><span data-stu-id="68c88-107">A post is re-tweeted in that twitter handle</span></span> 
    
3. <span data-ttu-id="68c88-108">Une publication est simplement un hashtag spécifique E.g.,"#EmployeeEngagement »</span><span class="sxs-lookup"><span data-stu-id="68c88-108">A post has a specific hashtag E.g.,"#EmployeeEngagement"</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/6.png" alt="Tweet" width="400" />

<span data-ttu-id="68c88-109">Cette carte possède trois champs carte titre, corps (description) et des pièces jointes (images, des vidéos ou GIF).</span><span class="sxs-lookup"><span data-stu-id="68c88-109">This card has three fields- card title, attachments(images, videos or GIF) and body (description).</span></span> <span data-ttu-id="68c88-110">Le corps de l’annonce est l’URL twitter et sur appuyant sur cette URL, les utilisateurs seraient redirigés vers la page d’état sur twitter.</span><span class="sxs-lookup"><span data-stu-id="68c88-110">The announcement body has the twitter URL and on tapping this URL, users would be directed to status page on twitter.</span></span>

> <span data-ttu-id="68c88-111">Remarque : En cas de vidéo ou GIF, vignette s’affiche dans la vue de carte de conversation</span><span class="sxs-lookup"><span data-stu-id="68c88-111">Note: In case of Video or GIF, thumbnail is shown in chat card view</span></span>

<span data-ttu-id="68c88-112">Afficher la carte conversation :</span><span class="sxs-lookup"><span data-stu-id="68c88-112">Chat card View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

<span data-ttu-id="68c88-113">Mode immersif :</span><span class="sxs-lookup"><span data-stu-id="68c88-113">Immersive View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/2.png" alt="Immersive view Logo" width="190" />

<span data-ttu-id="68c88-114">Dans ce scénario, le flux est utilisé pour envoyer la carte à un groupe sélectionné dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="68c88-114">In this scenario, Flow is used to send the card to a selected group in Kaizala.</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/3.png" alt="Flow+Twitter>Kaizala" width="500" />

## <a name="implementation-steps"></a><span data-ttu-id="68c88-115">Étapes d’implémentation :</span><span class="sxs-lookup"><span data-stu-id="68c88-115">Implementation steps:</span></span>

1. <span data-ttu-id="68c88-116">Téléchargez le [AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/AutoPostTwitterUpdatesToKaizala/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*il contient le Package de flux*)</span><span class="sxs-lookup"><span data-stu-id="68c88-116">Download the [AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/AutoPostTwitterUpdatesToKaizala/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*This contains Flow Package*)</span></span>

2. <span data-ttu-id="68c88-117">[Importation](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) « AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip » à votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="68c88-117">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip" to your Microsoft Flow account</span></span>

     > <span data-ttu-id="68c88-118">Remarque : Si vous n’avez jamais utilisé connexions Twitter ou Kaizala, première [Ajouter des connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="68c88-118">Note- If you have never used Twitter or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>

3. <span data-ttu-id="68c88-119">Modifier le flux (*comme indiqué ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="68c88-119">Edit the Flow (*as Below*)</span></span>

    1.  <span data-ttu-id="68c88-120">Dans le premier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="68c88-120">In the first block of the Flow</span></span>
    
        <span data-ttu-id="68c88-121">Entrez la poignée twitter ou le hashtag, ou les deux</span><span class="sxs-lookup"><span data-stu-id="68c88-121">Enter the twitter handle or enter the hashtag, or both</span></span>
        
        <img src="AutoPostTwitterUpdatesToKaizalaImages/4.PNG" alt="Firstblock>Kaizala" width="400" />
    
    2.  <span data-ttu-id="68c88-122">Dans le dernier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="68c88-122">In the last block of the Flow</span></span>
      
        1. <span data-ttu-id="68c88-123">Sélectionnez le nom du groupe</span><span class="sxs-lookup"><span data-stu-id="68c88-123">Select the group name</span></span> 
    
        2. <span data-ttu-id="68c88-124">Entrez le titre.</span><span class="sxs-lookup"><span data-stu-id="68c88-124">Enter the title.</span></span> <span data-ttu-id="68c88-125">Le titre sera visible pour les utilisateurs dans l’affichage de carte de conversation.</span><span class="sxs-lookup"><span data-stu-id="68c88-125">The title will be visible to users in chat card view.</span></span> <span data-ttu-id="68c88-126">Par exemple, « InsideFabrikam »</span><span class="sxs-lookup"><span data-stu-id="68c88-126">E.g., "InsideFabrikam"</span></span>
     
        <img src="AutoPostTwitterUpdatesToKaizalaImages/5.PNG" alt="Flow+Twitter>Kaizala" width="400" />
     
4. <span data-ttu-id="68c88-127">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="68c88-127">Save the flow</span></span>

<span data-ttu-id="68c88-128">Annonce est envoyé au groupe Kaizala sélectionné, chaque fois que flux est déclenché.</span><span class="sxs-lookup"><span data-stu-id="68c88-128">Announcement will be sent to the selected Kaizala group, each time Flow is triggered.</span></span>

> <span data-ttu-id="68c88-129">Remarque : en cas de tweet sondages/emplacement uniquement le texte de la question/tweet sondage s’affichera dans la fiche, pas les options de sondage ou l’emplacement tweet</span><span class="sxs-lookup"><span data-stu-id="68c88-129">Note:In case of tweets with polls/location only the poll question/tweet text will show up in the card, not the poll options or the tweet location</span></span>

> <span data-ttu-id="68c88-130">Remarque : Vérifiez avec votre administrateur informatique en cas de toute [stratégie DLP](https://docs.microsoft.com/en-us/flow/prevent-data-loss) défini par votre organisation pour Twitter</span><span class="sxs-lookup"><span data-stu-id="68c88-130">Note: Please check with your IT admin in case of any [DLP policy](https://docs.microsoft.com/en-us/flow/prevent-data-loss) set by your organization for Twitter</span></span>
