# <a name="display-sharepoint-announcements-in-kaizala-groups"></a><span data-ttu-id="5897b-101">Afficher les annonces SharePoint dans les groupes Kaizala</span><span class="sxs-lookup"><span data-stu-id="5897b-101">Display SharePoint Announcements in Kaizala groups</span></span> 
<span data-ttu-id="5897b-102">Les organisations utilisent l'application d'annonce SharePoint pour partager des actualités, des États et d'autres informations de taille réduite aux employés.</span><span class="sxs-lookup"><span data-stu-id="5897b-102">Organizations use SharePoint Announcement app to share news, status and other short bits of information to employees .</span></span> <span data-ttu-id="5897b-103">L'application d'annonce SharePoint, qui est fournie avec une liste, est un type spécial de liste qui vous permet de créer des annonces.</span><span class="sxs-lookup"><span data-stu-id="5897b-103">Sharepoint Announcement app, that comes with a list, is a special type of list that lets you create announcements.</span></span>

<span data-ttu-id="5897b-104">À l'aide de cet exemple, les organisations peuvent partager des annonces SharePoint avec la première ligne et les employés mobiles sur Kaizala.</span><span class="sxs-lookup"><span data-stu-id="5897b-104">Using this sample, organizations can share SharePoint announcements with the first line and mobile workers on Kaizala.</span></span> <span data-ttu-id="5897b-105">Cette carte comporte 3 champs en mode carte de conversation-pièces jointes (dans cet exemple, Photo Story of images), title et Announcement Body (Description).</span><span class="sxs-lookup"><span data-stu-id="5897b-105">This card has 3 fields in chat card view- Attachments( In this example, Photo story of images), Title and Announcement body (description).</span></span> <span data-ttu-id="5897b-106">Ce champ est envoyé à un groupe Kaizala en tant que carte d'annonce prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="5897b-106">This is sent to a Kaizala group as an out-of-box announcement card.</span></span>

<span data-ttu-id="5897b-107">La vue de la carte de conversation est la suivante</span><span class="sxs-lookup"><span data-stu-id="5897b-107">The chat card view is as below</span></span>

<img src="SharepointAnnouncementImages/1.png" alt="Chat card view Logo" width="340" />

<span data-ttu-id="5897b-108">En appuyant sur la carte, l'affichage immersif est comme suit.</span><span class="sxs-lookup"><span data-stu-id="5897b-108">On tapping the card, immersive view is as below</span></span>

<img src="SharepointAnnouncementImages/2.png" alt="immersive view Logo" width="180" />

<span data-ttu-id="5897b-109">Ce scénario peut être divisé en deux étapes:</span><span class="sxs-lookup"><span data-stu-id="5897b-109">This scenario can be broadly divided into 2 steps:</span></span>
1. <span data-ttu-id="5897b-110">Créer une liste d'annonces avec des colonnes-titre, pièces jointes et corps d'annonce (Description)</span><span class="sxs-lookup"><span data-stu-id="5897b-110">Create an announcement list with columns- Title, attachments and announcement body(description)</span></span> 

    > <span data-ttu-id="5897b-111">Remarque: le texte enrichi n'est pas pris en charge par la carte d'annonce prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="5897b-111">Note: Rich text is not supported by out-of-box announcement card.</span></span> <span data-ttu-id="5897b-112">Désactivez le texte enrichi pour une colonne SharePoint dont le corps d'annonce (Description) est créé lors de la création de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="5897b-112">Switch off rich text for sharepoint column that has Announcement body(description) while creating that column.</span></span>

    <img src="SharepointAnnouncementImages/3.5.png" width="200" />

2. <span data-ttu-id="5897b-113">Configurer le flux de sorte que, lorsqu'un nouvel élément est créé ou qu'un élément existant soit modifié dans la liste d'annonces, une carte d'annonce prédéfinie est envoyée à un groupe Kaizala</span><span class="sxs-lookup"><span data-stu-id="5897b-113">Configure Flow such that, when a new item is created or existing item is modified in announcement list, an out-of-box announcement card is sent to a Kaizala group</span></span>

    <img src="SharepointAnnouncementImages/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a><span data-ttu-id="5897b-114">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="5897b-114">Implementation steps</span></span>


1. <span data-ttu-id="5897b-115">[Ajouter une application d'annonce](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) à un site SharePoint (*comme ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="5897b-115">[Add Announcement app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) to SharePoint site(*as below*)</span></span>
     1. <span data-ttu-id="5897b-116">Cliquez sur l'icône Paramètres.</span><span class="sxs-lookup"><span data-stu-id="5897b-116">Click on the settings icon</span></span>
     2.  <span data-ttu-id="5897b-117">Cliquez sur Ajouter une application</span><span class="sxs-lookup"><span data-stu-id="5897b-117">Click on Add an App</span></span> 
     3.  <span data-ttu-id="5897b-118">Sélectionnez application d'annonce dans la liste des applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="5897b-118">Select Announcement App from the list of available Apps</span></span>
2. <span data-ttu-id="5897b-119">Utiliser le [composant WebPart de contenu](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) en surbrillance (le*cas échéant, pour la visualisation*)</span><span class="sxs-lookup"><span data-stu-id="5897b-119">Use the [highlighted content web part](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*if necessary , for visualization*)</span></span>
3. <span data-ttu-id="5897b-120">Télécharger le fichier [SharepointAnnouncementOnKaizala-SolutionPackage. zip](https://aka.ms/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*il s'agit d'un package de flux*)</span><span class="sxs-lookup"><span data-stu-id="5897b-120">Download the [SharepointAnnouncementOnKaizala-SolutionPackage.zip](https://aka.ms/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*This is a Flow package*)</span></span>
4. <span data-ttu-id="5897b-121">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage. zip sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="5897b-121">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip to your Microsoft Flow account</span></span>
   
   > <span data-ttu-id="5897b-122">Remarque: Si vous n'avez jamais utilisé SharePoint ou la connexion Kaizala, ajoutez d'abord les [connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="5897b-122">Note: If you have never used Sharepoint or Kaizala connection, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>
   
5. <span data-ttu-id="5897b-123">Modifier le flux (*comme ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="5897b-123">Edit the Flow (*as below*)</span></span>
    1. <span data-ttu-id="5897b-124">Dans le premier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="5897b-124">In the first block of the Flow</span></span>
    
         1. <span data-ttu-id="5897b-125">Entrez l'adresse du site</span><span class="sxs-lookup"><span data-stu-id="5897b-125">Enter the site address</span></span>
         2. <span data-ttu-id="5897b-126">Entrez le nom de la liste (*étapes à suivre pour obtenir le nom de la liste, comme indiqué ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="5897b-126">Enter the List name (*steps to get List name is as below*)</span></span>
            - <span data-ttu-id="5897b-127">Cliquez sur l'onglet contenu du site dans le coin gauche de l'écran.</span><span class="sxs-lookup"><span data-stu-id="5897b-127">Click on site contents tab on the left hand corner of the screen</span></span>
            - <span data-ttu-id="5897b-128">Sélectionnez la liste d'annonces à partir de laquelle vous souhaitez envoyer des annonces à Kaizala</span><span class="sxs-lookup"><span data-stu-id="5897b-128">Select the announcement list from which you want to send announcements to Kaizala</span></span>
            - <span data-ttu-id="5897b-129">Cliquez sur l'icône Paramètres dans le coin supérieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="5897b-129">Click on settings icon at the top right corner of the screen</span></span>
            - <span data-ttu-id="5897b-130">Accéder aux paramètres de la liste</span><span class="sxs-lookup"><span data-stu-id="5897b-130">Go to List settings</span></span>
            - <span data-ttu-id="5897b-131">Copiez l'URL de la liste à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="5897b-131">Copy the URL of the list from the browser.</span></span>
            - <span data-ttu-id="5897b-132">Décodez l'URL (vous pouvez décoder l'URL [ici](https://www.url-encode-decode.com/) )</span><span class="sxs-lookup"><span data-stu-id="5897b-132">Decode the URL (you can decode the URL [here](https://www.url-encode-decode.com/) )</span></span>
        <img src="SharepointAnnouncementImages/4.PNG" alt="" width="500" />
      
    2. <span data-ttu-id="5897b-133">Dans le deuxième bloc du flux</span><span class="sxs-lookup"><span data-stu-id="5897b-133">In the second block of the Flow</span></span>
   
        <span data-ttu-id="5897b-134">Mapper le champ «valeur» avec le titre de colonne de la liste d'annonces, avec le corps de l'annonce (Description) à partir de contenu dynamique.</span><span class="sxs-lookup"><span data-stu-id="5897b-134">Map "value" field with column title of announcement list, that has announcement body(description) from Dynamic content.</span></span> <span data-ttu-id="5897b-135">Dans l'exemple ci-dessous, le titre de la colonne est «corps de l'annonce» </span><span class="sxs-lookup"><span data-stu-id="5897b-135">In the below example, the column title is "Announcement Body"  </span></span><img src="SharepointAnnouncementImages/5.png" alt="" width="600" />
       
    3. <span data-ttu-id="5897b-136">Dans le dernier bloc du flux</span><span class="sxs-lookup"><span data-stu-id="5897b-136">In the last block of the Flow</span></span>
    
       <span data-ttu-id="5897b-137">Sélectionnez le nom du groupe dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5897b-137">Select the group name from dropdown.</span></span> <span data-ttu-id="5897b-138">Dans cet exemple, il s'agit de «tout le monde @ Fabrikam»</span><span class="sxs-lookup"><span data-stu-id="5897b-138">In this Example it is "Everyone@Fabrikam"</span></span>
       <img src="SharepointAnnouncementImages/6.png" alt="" width="450" />
6. <span data-ttu-id="5897b-139">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="5897b-139">Save the flow</span></span>

<span data-ttu-id="5897b-140">L'annonce est envoyée au groupe Kaizala sélectionné, chaque flux de temps étant déclenché.</span><span class="sxs-lookup"><span data-stu-id="5897b-140">Announcement will be sent to the selected Kaizala group, each time flow is triggered.</span></span>

> <span data-ttu-id="5897b-141">Remarque: le fichier texte n'est pas pris en charge en tant que pièce jointe</span><span class="sxs-lookup"><span data-stu-id="5897b-141">Note: Text file is not supported as attachment</span></span>
