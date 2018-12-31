# <a name="display-sharepoint-announcements-in-kaizala-groups"></a><span data-ttu-id="1926b-101">Afficher les annonces SharePoint dans les groupes de Kaizala</span><span class="sxs-lookup"><span data-stu-id="1926b-101">Display SharePoint Announcements in Kaizala groups</span></span> 
<span data-ttu-id="1926b-102">Organisations utilisent application annonce SharePoint pour partager des news, état et autres bribes d’informations aux employés.</span><span class="sxs-lookup"><span data-stu-id="1926b-102">Organizations use SharePoint Announcement app to share news, status and other short bits of information to employees .</span></span> <span data-ttu-id="1926b-103">Application annonce de SharePoint, qui est fourni avec une liste, est un type particulier de la liste qui vous permet de créer un annonces.</span><span class="sxs-lookup"><span data-stu-id="1926b-103">Sharepoint Announcement app, that comes with a list, is a special type of list that lets you create an announcements.</span></span>

<span data-ttu-id="1926b-104">À l’aide de cet exemple, les organisations peuvent partager des annonces SharePoint avec la première ligne et les travailleurs mobiles sur Kaizala.</span><span class="sxs-lookup"><span data-stu-id="1926b-104">Using this sample, organizations can share SharePoint announcements with the first line and mobile workers on Kaizala.</span></span> <span data-ttu-id="1926b-105">Cette carte a 3 champs de conversation carte afficher-les pièces jointes (dans cet exemple, article Photo d’images), titre et annonce le corps (description).</span><span class="sxs-lookup"><span data-stu-id="1926b-105">This card has 3 fields in chat card view- Attachments( In this example, Photo story of images), Title and Announcement body (description).</span></span> <span data-ttu-id="1926b-106">Il est envoyé à un groupe de Kaizala en tant qu’une carte annonce out-of-box.</span><span class="sxs-lookup"><span data-stu-id="1926b-106">This is sent to a Kaizala group as an out-of-box announcement card.</span></span>

<span data-ttu-id="1926b-107">L’affichage de carte de conversation est en dessous</span><span class="sxs-lookup"><span data-stu-id="1926b-107">The chat card view is as below</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/1.png" alt="Chat card view Logo" width="340" />

<span data-ttu-id="1926b-108">En cliquant sur la carte, mode immersif est en dessous</span><span class="sxs-lookup"><span data-stu-id="1926b-108">On tapping the card, immersive view is as below</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/2.png" alt="immersive view Logo" width="180" />

<span data-ttu-id="1926b-109">Ce scénario peut être divisé en 2 étapes :</span><span class="sxs-lookup"><span data-stu-id="1926b-109">This scenario can be broadly divided into 2 steps:</span></span>

1. <span data-ttu-id="1926b-110">Créer une liste d’annonces avec colonnes - Title, pièces jointes et annonce body(description)</span><span class="sxs-lookup"><span data-stu-id="1926b-110">Create an announcement list with columns- Title, attachments and announcement body(description)</span></span> 
    
> <span data-ttu-id="1926b-111">Remarque : RTF n’est pas pris en charge par la carte annonce out-of-box.</span><span class="sxs-lookup"><span data-stu-id="1926b-111">Note: Rich text is not supported by out-of-box announcement card.</span></span> <span data-ttu-id="1926b-112">Désactiver le texte enrichi dans la colonne sharepoint qui a body(description) annonce lors de la création de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="1926b-112">Switch off rich text for sharepoint column that has Announcement body(description) while creating that column.</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/3.5.png" width="200" />
    
2. <span data-ttu-id="1926b-113">Configurer le flux tels que lorsqu’un nouvel élément est créé ou un élément existant est modifié dans la liste d’annonces, une carte annonce out-of-box est envoyée à un groupe de Kaizala</span><span class="sxs-lookup"><span data-stu-id="1926b-113">Configure Flow such that, when a new item is created or existing item is modified in announcement list, an out-of-box announcement card is sent to a Kaizala group</span></span>

<img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a><span data-ttu-id="1926b-114">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="1926b-114">Implementation steps</span></span>


1. <span data-ttu-id="1926b-115">[Application annonce ajouter](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) au site SharePoint (*comme indiqué ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="1926b-115">[Add Announcement app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) to SharePoint site(*as below*)</span></span>
     1. <span data-ttu-id="1926b-116">Cliquez sur l’icône Paramètres</span><span class="sxs-lookup"><span data-stu-id="1926b-116">Click on the settings icon</span></span>
     2.  <span data-ttu-id="1926b-117">Cliquez sur Ajouter une application</span><span class="sxs-lookup"><span data-stu-id="1926b-117">Click on Add an App</span></span> 
     3.  <span data-ttu-id="1926b-118">Sélectionnez application annonce dans la liste des applications disponibles</span><span class="sxs-lookup"><span data-stu-id="1926b-118">Select Announcement App from the list of available Apps</span></span>
2. <span data-ttu-id="1926b-119">Utiliser le [composant WebPart contenu mis en surbrillance](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*le cas échéant, pour la visualisation*)</span><span class="sxs-lookup"><span data-stu-id="1926b-119">Use the [highlighted content web part](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*if necessary , for visualization*)</span></span>
3. <span data-ttu-id="1926b-120">Téléchargez le [SharepointAnnouncementOnKaizala-SolutionPackage.zip](/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*il s’agit d’un package de flux*)</span><span class="sxs-lookup"><span data-stu-id="1926b-120">Download the [SharepointAnnouncementOnKaizala-SolutionPackage.zip](/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*This is a Flow package*)</span></span>
4. <span data-ttu-id="1926b-121">[Importation](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip à votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="1926b-121">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip to your Microsoft Flow account</span></span>

> <span data-ttu-id="1926b-122">Remarque : Si vous n’avez jamais utilisé Sharepoint ou Kaizala connexion, première [Ajouter des connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="1926b-122">Note: If you have never used Sharepoint or Kaizala connection, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>

5. <span data-ttu-id="1926b-123">Modifier le flux (*comme indiqué ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="1926b-123">Edit the Flow (*as below*)</span></span>

    1. <span data-ttu-id="1926b-124">Dans le premier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="1926b-124">In the first block of the Flow</span></span>
         1. <span data-ttu-id="1926b-125">Entrez l’adresse du site</span><span class="sxs-lookup"><span data-stu-id="1926b-125">Enter the site address</span></span>
         2. <span data-ttu-id="1926b-126">Entrez le nom de la liste (*comme suit pour obtenir la liste nom est comme suit*)</span><span class="sxs-lookup"><span data-stu-id="1926b-126">Enter the List name (*steps to get List name is as below*)</span></span>
            - <span data-ttu-id="1926b-127">Cliquez sur l’onglet de contenu de site dans le coin gauche de l’écran</span><span class="sxs-lookup"><span data-stu-id="1926b-127">Click on site contents tab on the left hand corner of the screen</span></span>
            - <span data-ttu-id="1926b-128">Sélectionnez la liste d’annonces à partir de laquelle vous voulez envoyer des annonces à Kaizala</span><span class="sxs-lookup"><span data-stu-id="1926b-128">Select the announcement list from which you want to send announcements to Kaizala</span></span>
            - <span data-ttu-id="1926b-129">Cliquez sur l’icône Paramètres dans le coin supérieur droit de l’écran</span><span class="sxs-lookup"><span data-stu-id="1926b-129">Click on settings icon at the top right corner of the screen</span></span>
            - <span data-ttu-id="1926b-130">Accéder aux paramètres de liste</span><span class="sxs-lookup"><span data-stu-id="1926b-130">Go to List settings</span></span>
            - <span data-ttu-id="1926b-131">Copiez l’URL de la liste à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="1926b-131">Copy the URL of the list from the browser.</span></span>
            - <span data-ttu-id="1926b-132">L’URL de décodage (vous pouvez décoder le URL [ici](https://www.url-encode-decode.com/) )</span><span class="sxs-lookup"><span data-stu-id="1926b-132">Decode the URL (you can decode the URL [here](https://www.url-encode-decode.com/) )</span></span>
          <img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/4.PNG" alt="" width="500" />

   2. <span data-ttu-id="1926b-133">Dans le deuxième bloc du flux</span><span class="sxs-lookup"><span data-stu-id="1926b-133">In the second block of the Flow</span></span>
      
      <span data-ttu-id="1926b-134">Mapper le champ « valeur » avec le titre de la colonne de liste d’annonces, qui a body(description) annonce du contenu dynamique.</span><span class="sxs-lookup"><span data-stu-id="1926b-134">Map "value" field with column title of announcement list, that has announcement body(description) from Dynamic content.</span></span> <span data-ttu-id="1926b-135">Dans le sous exemple, le titre de colonne est « Annonce corps »</span><span class="sxs-lookup"><span data-stu-id="1926b-135">In the below example, the column title is "Announcement Body"</span></span>
        
       <img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/5.png" alt="" width="600" />

    3. <span data-ttu-id="1926b-136">Dans le dernier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="1926b-136">In the last block of the Flow</span></span>
       
       <span data-ttu-id="1926b-137">Sélectionnez le nom du groupe dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1926b-137">Select the group name from dropdown.</span></span> <span data-ttu-id="1926b-138">Dans cet exemple, il est « Everyone@Fabrikam »</span><span class="sxs-lookup"><span data-stu-id="1926b-138">In this Example it is "Everyone@Fabrikam"</span></span>
       
       <img src="/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/Sharepoint%20announcement%20Images/6.png" alt="" width="450" />

6. <span data-ttu-id="1926b-139">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="1926b-139">Save the flow</span></span>

<span data-ttu-id="1926b-140">Annonce seront envoyés au groupe Kaizala sélectionné, chaque flux de temps est déclenché.</span><span class="sxs-lookup"><span data-stu-id="1926b-140">Announcement will be sent to the selected Kaizala group, each time flow is triggered.</span></span>

> <span data-ttu-id="1926b-141">Remarque : Fichier texte n’est pas pris en charge en tant que pièce jointe</span><span class="sxs-lookup"><span data-stu-id="1926b-141">Note: Text file is not supported as attachment</span></span>
