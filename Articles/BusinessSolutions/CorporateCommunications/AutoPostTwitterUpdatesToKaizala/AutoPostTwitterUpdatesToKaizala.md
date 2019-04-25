# <a name="auto-post-twitter-updates-to-kaizala"></a><span data-ttu-id="7c3db-101">Publication automatique des mises à jour Twitter sur Kaizala</span><span class="sxs-lookup"><span data-stu-id="7c3db-101">Auto-Post Twitter updates to Kaizala</span></span>

<span data-ttu-id="7c3db-102">La publication des pages d'employés Twitter fait partie de l'activité quotidienne, mais il est assez difficile de publier les mêmes informations plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="7c3db-102">Posting to Twitter employee pages is part of daily business, but having to post the same information multiple times is quite difficult.</span></span> <span data-ttu-id="7c3db-103">Encourager les employés à partager les mises à jour des réseaux sociaux, lorsqu'ils sont effectués correctement, peuvent considérablement élargir les points suivants.</span><span class="sxs-lookup"><span data-stu-id="7c3db-103">Encouraging employees to share social media updates, when done properly can dramatically expand company's following.</span></span> 

<span data-ttu-id="7c3db-104">Cet exemple de solution vous permet de gagner du temps en publiant automatiquement des tweets à partir de votre compte Twitter officiel vers les groupes Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7c3db-104">This sample solution saves your time by auto-posting Tweets from your official Twitter account to Kaizala groups.</span></span> <span data-ttu-id="7c3db-105">Une carte d'annonce est envoyée au groupe lorsqu'un ou tous les déclencheurs suivants se produisent</span><span class="sxs-lookup"><span data-stu-id="7c3db-105">An announcement card is sent to the group when one or all the below triggers occur</span></span>

1. <span data-ttu-id="7c3db-106">Un nouveau Tweet est publié sur une poignée Twitter spécifique, par exemple, «@InsideFabrikam»</span><span class="sxs-lookup"><span data-stu-id="7c3db-106">A new tweet is posted on a specific Twitter handle E.g.,"@InsideFabrikam"</span></span>

2. <span data-ttu-id="7c3db-107">Un billet est ré-tweeté dans ce handle Twitter</span><span class="sxs-lookup"><span data-stu-id="7c3db-107">A post is re-tweeted in that Twitter handle</span></span> 
    
3. <span data-ttu-id="7c3db-108">Un billet a un mot-dièse spécifique, par exemple «#EmployeeEngagement»</span><span class="sxs-lookup"><span data-stu-id="7c3db-108">A post has a specific hashtag E.g.,"#EmployeeEngagement"</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/6.png" alt="Tweet" width="400" />

<span data-ttu-id="7c3db-109">Cette carte comporte trois champs, le titre de la carte, les pièces jointes (images, vidéos ou GIF) et le corps (Description).</span><span class="sxs-lookup"><span data-stu-id="7c3db-109">This card has three fields- card title, attachments(images, videos or GIF) and body (description).</span></span> <span data-ttu-id="7c3db-110">Le corps de l'annonce est doté de l'URL Twitter et en appuyant sur cette URL, les utilisateurs sont dirigés vers la page d'État sur Twitter.</span><span class="sxs-lookup"><span data-stu-id="7c3db-110">The announcement body has the Twitter URL and on tapping this URL, users would be directed to status page on Twitter.</span></span>

> <span data-ttu-id="7c3db-111">Remarque: en cas de vidéo ou GIF, la miniature apparaît en mode carte de conversation.</span><span class="sxs-lookup"><span data-stu-id="7c3db-111">Note: In case of Video or GIF, thumbnail is shown in chat card view</span></span>

<span data-ttu-id="7c3db-112">Affichage de la carte de conversation:</span><span class="sxs-lookup"><span data-stu-id="7c3db-112">Chat card View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

<span data-ttu-id="7c3db-113">Vue immersive:</span><span class="sxs-lookup"><span data-stu-id="7c3db-113">Immersive View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/2.png" alt="Immersive view Logo" width="190" />

<span data-ttu-id="7c3db-114">Dans ce scénario, le flux est utilisé pour envoyer la carte à un groupe sélectionné dans Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7c3db-114">In this scenario, Flow is used to send the card to a selected group in Kaizala.</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/3.png" alt="Flow+Twitter>Kaizala" width="500" />

## <a name="implementation-steps"></a><span data-ttu-id="7c3db-115">Étapes d'implémentation:</span><span class="sxs-lookup"><span data-stu-id="7c3db-115">Implementation steps:</span></span>

1. <span data-ttu-id="7c3db-116">Télécharger le [AutoPostTwitterUpdatesToKaizala-SolutionPackage. zip](https://aka.ms/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*contient un package de flux*)</span><span class="sxs-lookup"><span data-stu-id="7c3db-116">Download the [AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip](https://aka.ms/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*This contains Flow Package*)</span></span>

2. <span data-ttu-id="7c3db-117">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «AutoPostTwitterUpdatesToKaizala-SolutionPackage. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="7c3db-117">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip" to your Microsoft Flow account</span></span>

     > <span data-ttu-id="7c3db-118">Remarque: Si vous n'avez jamais utilisé de connexions Twitter ou Kaizala, ajoutez d'abord les [connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="7c3db-118">Note- If you have never used Twitter or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>

3. <span data-ttu-id="7c3db-119">Modifier le flux (*comme ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="7c3db-119">Edit the Flow (*as Below*)</span></span>

    1.  <span data-ttu-id="7c3db-120">Dans le premier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="7c3db-120">In the first block of the Flow</span></span>
    
        <span data-ttu-id="7c3db-121">Entrer le descripteur Twitter ou entrer le mot-dièse, ou les deux</span><span class="sxs-lookup"><span data-stu-id="7c3db-121">Enter the Twitter handle or enter the hashtag, or both</span></span>
        
        <img src="AutoPostTwitterUpdatesToKaizalaImages/4.PNG" alt="Firstblock>Kaizala" width="400" />
    
    2.  <span data-ttu-id="7c3db-122">Dans le dernier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="7c3db-122">In the last block of the Flow</span></span>
      
        1. <span data-ttu-id="7c3db-123">Sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="7c3db-123">Select the group name</span></span> 
    
        2. <span data-ttu-id="7c3db-124">Entrez le titre.</span><span class="sxs-lookup"><span data-stu-id="7c3db-124">Enter the title.</span></span> <span data-ttu-id="7c3db-125">Le titre sera visible par les utilisateurs en mode carte de conversation.</span><span class="sxs-lookup"><span data-stu-id="7c3db-125">The title will be visible to users in chat card view.</span></span> <span data-ttu-id="7c3db-126">Par exemple, «InsideFabrikam»</span><span class="sxs-lookup"><span data-stu-id="7c3db-126">E.g., "InsideFabrikam"</span></span>
     
        <img src="AutoPostTwitterUpdatesToKaizalaImages/5.PNG" alt="Flow+Twitter>Kaizala" width="400" />
     
4. <span data-ttu-id="7c3db-127">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="7c3db-127">Save the flow</span></span>

<span data-ttu-id="7c3db-128">L'annonce est envoyée au groupe Kaizala sélectionné, chaque flux de temps étant déclenché.</span><span class="sxs-lookup"><span data-stu-id="7c3db-128">Announcement will be sent to the selected Kaizala group, each time Flow is triggered.</span></span>

> <span data-ttu-id="7c3db-129">Remarque: en cas de tweets avec sondages/emplacement, seul le texte de question/tweet de sondage s'affichera dans la carte, pas les options de sondage ou l'emplacement tweet.</span><span class="sxs-lookup"><span data-stu-id="7c3db-129">Note:In case of tweets with polls/location only the poll question/tweet text will show up in the card, not the poll options or the tweet location</span></span>

> <span data-ttu-id="7c3db-130">Remarque: consultez votre administrateur informatique en cas de [stratégie DLP](https://docs.microsoft.com/en-us/flow/prevent-data-loss) définie par votre organisation pour Twitter</span><span class="sxs-lookup"><span data-stu-id="7c3db-130">Note: Please check with your IT admin in case of any [DLP policy](https://docs.microsoft.com/en-us/flow/prevent-data-loss) set by your organization for Twitter</span></span>
