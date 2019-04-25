# <a name="employee-help-desk"></a><span data-ttu-id="11b66-101">Support technique pour les employés</span><span class="sxs-lookup"><span data-stu-id="11b66-101">Employee Help Desk</span></span>

 <span data-ttu-id="11b66-102">Dans une organisation, l'équipe du support technique examine les requêtes émises par les employés, les affecte à un agent de champ et met à jour l'état de résolution à l'employé.</span><span class="sxs-lookup"><span data-stu-id="11b66-102">In an Organization, helpdesk team looks into the queries raised by employees, assigns it to a field agent and updates back the resolution status to the employee.</span></span> <span data-ttu-id="11b66-103">Toutes les requêtes sont connectées sous forme de tickets pour faciliter le suivi et la résolution.</span><span class="sxs-lookup"><span data-stu-id="11b66-103">All the queries are logged in as tickets for easy tracking and resolution.</span></span> <span data-ttu-id="11b66-104">Un système de gestion des tickets permet aux agents du support technique de capturer, classer, résoudre et recueillir des commentaires de façon systématique.</span><span class="sxs-lookup"><span data-stu-id="11b66-104">A ticketing system enables helpdesk agents to systematically capture, categorize, resolve and collect feedback.</span></span> <span data-ttu-id="11b66-105">Cela permet à une organisation d'être efficace dans la résolution des requêtes et a un effet multiplicateur sur les scores de satisfaction des employés.</span><span class="sxs-lookup"><span data-stu-id="11b66-105">This enables an organization to be effective in query resolution and has a multiplier effect on employee satisfaction scores.</span></span>

<span data-ttu-id="11b66-106">Cette solution utilise Kaizala en tant que serveur frontal, SharePoint comme serveur principal et de flux pour interagir avec Kaizala et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11b66-106">This solution uses Kaizala as the front-end, SharePoint as the backend and Flow as a means to interact with Kaizala and SharePoint.</span></span> <span data-ttu-id="11b66-107">Un utilisateur crée le ticket en envoyant un formulaire dans Kaizala, les détails de ticket envoyés à l'aide de cette carte sont capturés et stockés dans SharePoint à l'aide de Flow. on submission, l'utilisateur obtient une carte mise à jour, soit lorsque-</span><span class="sxs-lookup"><span data-stu-id="11b66-107">A user creates the ticket by submitting a form in Kaizala, ticket details submitted using this card is captured and stored in the SharePoint using Flow.On submission, User gets an updated card,either when-</span></span>

   1. <span data-ttu-id="11b66-108">L'agent du support technique met à jour l'état du ticket dans SharePoint (nouveau, affecté ou résolu) ou</span><span class="sxs-lookup"><span data-stu-id="11b66-108">Help desk agent updates the status of the ticket in SharePoint (New, Assigned or Resolved) or</span></span>

   2. <span data-ttu-id="11b66-109">Les agents du support technique ajoutent des commentaires sur le ticket dans SharePoint ou</span><span class="sxs-lookup"><span data-stu-id="11b66-109">Help desk agents adds comments on the ticket in SharePoint or</span></span>

   3. <span data-ttu-id="11b66-110">L'état des mises à jour de l'agent de support technique et ajoute des commentaires dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-110">Both, help desk agent updates status and adds comments in SharePoint</span></span>

<span data-ttu-id="11b66-111">Si l'utilisateur est satisfait de la résolution proposée, l'utilisateur a la possibilité de fermer le ticket et d'envoyer des commentaires.</span><span class="sxs-lookup"><span data-stu-id="11b66-111">If the user is satisfied with the proposed resolution, user has the ability to close the ticket and submit feedback.</span></span> <span data-ttu-id="11b66-112">Si l'utilisateur n'est pas satisfait de la résolution, l'utilisateur peut rouvrir le ticket.</span><span class="sxs-lookup"><span data-stu-id="11b66-112">If the user is not satisfied with the resolution, user can re-open the ticket.</span></span> <span data-ttu-id="11b66-113">Commentaires des utilisateurs-évaluation et commentaires, État: rouvert ou fermé est mis à jour dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11b66-113">User Feedback - Rating and comments, status- Reopened or closed is updated back in SharePoint.</span></span>

> <span data-ttu-id="11b66-114">Remarque: cette carte fonctionne uniquement dans les groupes Hub et spoke</span><span class="sxs-lookup"><span data-stu-id="11b66-114">Note: This card works only in Hub and spoke groups</span></span>

  <span data-ttu-id="11b66-115">Affichage par l'utilisateur de la création et de l'envoi d'un ticket:</span><span class="sxs-lookup"><span data-stu-id="11b66-115">User view of ticket creation and submission:</span></span>

  <img src="EmployeeHelpdesk-Images/1.jpg" width="350">

   <span data-ttu-id="11b66-116">Affichage de la mise à jour de l'État vers «affecté» dans SharePoint et de la carte correspondante envoyée à l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="11b66-116">View on updating the status to "Assigned" in sharepoint and the corresponding card that is sent to user</span></span>

   <img src="EmployeeHelpdesk-Images/2.jpg" width="600">

   <span data-ttu-id="11b66-117">Affichage de l'État mis à jour sur «résolu» dans SharePoint et la carte correspondante envoyée à l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="11b66-117">View of status being updated to "Resolved" in sharepoint and the corresponding card that is sent to user</span></span>
   
   <img src="EmployeeHelpdesk-Images/3.jpg" width="600">

   <span data-ttu-id="11b66-118">Affichage des commentaires de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="11b66-118">User Feedback view</span></span>

   <img src="EmployeeHelpdesk-Images/4.jpg" width="350">


## <a name="implementation-steps"></a><span data-ttu-id="11b66-119">Étapes d'implémentation:</span><span class="sxs-lookup"><span data-stu-id="11b66-119">Implementation Steps:</span></span>
<span data-ttu-id="11b66-120">Cette opération est généralement divisée en trois étapes:</span><span class="sxs-lookup"><span data-stu-id="11b66-120">This is broadly divided into 3 steps:</span></span>

1. <span data-ttu-id="11b66-121">Télécharger des packages d'actions qui permettent à un utilisateur de (*2 packages d'actions*)</span><span class="sxs-lookup"><span data-stu-id="11b66-121">Upload action packages that enable a user to (*2 Action Packages*)</span></span>

   1. <span data-ttu-id="11b66-122">Création et envoi d'un ticket pour le service d'assistance (*CreateTicket-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="11b66-122">Create and submit a ticket to help desk (*CreateTicket-ActionPackage.Zip*)</span></span>

   2. <span data-ttu-id="11b66-123">Recevoir des mises à jour d'État & des commentaires du support technique (*StatusUpdateFromHelpdesk-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="11b66-123">Receive status updates & comments from help desk (*StatusUpdateFromHelpdesk-ActionPackage.Zip*)</span></span>

2. <span data-ttu-id="11b66-124">Configurer une liste SharePoint qui permet aux agents du support technique de</span><span class="sxs-lookup"><span data-stu-id="11b66-124">Set up a SharePoint list that enables helpdesk agents to</span></span>

    1. <span data-ttu-id="11b66-125">Stocker les détails du ticket</span><span class="sxs-lookup"><span data-stu-id="11b66-125">Store the ticket details</span></span>

    2. <span data-ttu-id="11b66-126">Affecter, commenter et modifier l'état du ticket</span><span class="sxs-lookup"><span data-stu-id="11b66-126">Assign, comment and change the ticket status</span></span>

3. <span data-ttu-id="11b66-127">Configurer Microsoft Flow pour interagir avec SharePoint et Kaizala (*3 flux*)</span><span class="sxs-lookup"><span data-stu-id="11b66-127">Configure Microsoft Flow to interact with SharePoint and Kaizala (*3 Flows*)</span></span>

    1. <span data-ttu-id="11b66-128">Pour collecter les détails des tickets à partir de la carte et les stocker dans SharePoint (*TicketCreationFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="11b66-128">To collect ticket details from the card and store it in SharePoint(*TicketCreationFlow.Zip*)</span></span>
    
    2. <span data-ttu-id="11b66-129">Pour envoyer une carte mise à jour à l'utilisateur lorsque l'agent du support technique met à jour l'État, les commentaires ou les deux dans le SharePoint (*TicketStatusUpdatesFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="11b66-129">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint(*TicketStatusUpdatesFlow.Zip*)</span></span>

    3. <span data-ttu-id="11b66-130">Pour mettre à jour la liste SharePoint lorsque l'utilisateur choisit de fermer, de rouvrir ou d'ajouter des commentaires de commentaires à partir de la carte (*TicketReopenFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="11b66-130">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card(*TicketReopenFlow.Zip*)</span></span>

### <a name="upload-action-packages"></a><span data-ttu-id="11b66-131">Télécharger des packages d'actions</span><span class="sxs-lookup"><span data-stu-id="11b66-131">Upload Action Packages</span></span>
1. <span data-ttu-id="11b66-132">Télécharger le fichier [«EmployeeHelpDesk-SolutionPackage. zip»](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/EmployeeHelpdesk-SolutionPackage.zip) (*il contient 2 packages d'action et 3 flux*)</span><span class="sxs-lookup"><span data-stu-id="11b66-132">Download the ["EmployeeHelpDesk-SolutionPackage.zip"](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/EmployeeHelpdesk-SolutionPackage.zip) (*This contains 2 Action Packages and 3 Flows*)</span></span>

2. <span data-ttu-id="11b66-133">Téléchargez la dernière version de Kaizala [«ActionSDK. zip»](https://manage.kaiza.la/MiniApps/DownloadSDK) (*elle contient KASClient. js*)</span><span class="sxs-lookup"><span data-stu-id="11b66-133">Download the latest version of Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*This contains KASClient.js*)</span></span>

3. <span data-ttu-id="11b66-134">Configurer le «CreateTicket-ActionPackage. zip»</span><span class="sxs-lookup"><span data-stu-id="11b66-134">Set up the "CreateTicket-ActionPackage.Zip"</span></span>

   1. <span data-ttu-id="11b66-135">DéCompresser «CreateTicket-ActionPackage. zip» dans un dossier</span><span class="sxs-lookup"><span data-stu-id="11b66-135">Unzip "CreateTicket-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="11b66-136">Modifier les actions «ID» et «nom du fournisseur» dans package. JSON</span><span class="sxs-lookup"><span data-stu-id="11b66-136">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="11b66-137">Ajouter KASClient. js à ce dossier</span><span class="sxs-lookup"><span data-stu-id="11b66-137">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="11b66-138">Zip tout le contenu de ce dossier (*ce dossier est votre package d'action modifié qui doit être importé dans le portail de gestion Kaizala*)</span><span class="sxs-lookup"><span data-stu-id="11b66-138">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="11b66-139">[Importer](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) le package d'actions modifié dans le [portail de gestion Kaizala](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="11b66-139">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="11b66-140">[Publiez](https://docs.microsoft.com/en-us/kaizala/actions/publish) l'action et ajoutez l'action à un groupe auquel vous voulez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="11b66-140">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="11b66-141">Sélectionner les rôles d'utilisateur en tant qu'administrateur et membre</span><span class="sxs-lookup"><span data-stu-id="11b66-141">Select user roles as admin and member</span></span>

4. <span data-ttu-id="11b66-142">Configurer «StatusUpdateFromHelpDesk-ActionPackage. zip»</span><span class="sxs-lookup"><span data-stu-id="11b66-142">Set up "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

   1.  <span data-ttu-id="11b66-143">DéCompresser «StatusUpdateFromHelpDesk-ActionPackage. zip» dans un dossier</span><span class="sxs-lookup"><span data-stu-id="11b66-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="11b66-144">Modifier les actions «ID» et «nom du fournisseur» dans package. JSON</span><span class="sxs-lookup"><span data-stu-id="11b66-144">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="11b66-145">Ajouter KASClient. js à ce dossier</span><span class="sxs-lookup"><span data-stu-id="11b66-145">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="11b66-146">Zip tout le contenu de ce dossier (*ce dossier est votre package d'action modifié qui doit être importé dans le portail de gestion Kaizala*)</span><span class="sxs-lookup"><span data-stu-id="11b66-146">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="11b66-147">[Importer](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) le package d'actions modifié dans le [portail de gestion Kaizala](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="11b66-147">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="11b66-148">[Publiez](https://docs.microsoft.com/en-us/kaizala/actions/publish) l'action et ajoutez l'action à un groupe auquel vous voulez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="11b66-148">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="11b66-149">Sélectionner un rôle d'utilisateur en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="11b66-149">Select user role as admin</span></span>

       > <span data-ttu-id="11b66-150">Remarque: «CreateTicket-ActionPackage. zip» est la carte utilisée pour déclencher un ticket et doit être mise à la disposition de l'administrateur et des abonnés.» StatusUpdateFromHelpDesk-ActionPackage. zip "afficher les commentaires et les mises à jour de l'état du support technique.</span><span class="sxs-lookup"><span data-stu-id="11b66-150">Note: "CreateTicket-ActionPackage.Zip" is the card that is used to raise a ticket and should be made available to admin and Subscribers."StatusUpdateFromHelpDesk-ActionPackage.Zip" show helpdesk comments and status updates.</span></span> <span data-ttu-id="11b66-151">Les abonnés n'ont pas besoin d'afficher cette carte dans la palette d'action, donc elle n'est visible que par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="11b66-151">Subscribers do not have to see this card in action palette, hence this is only made visible to admin.</span></span>

### <a name="set-up-a-sharepoint-list"></a><span data-ttu-id="11b66-152">Configurer une liste SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-152">Set up a SharePoint List</span></span>

1. <span data-ttu-id="11b66-153">[Créer](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) une liste dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-153">[Create](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) a new list in SharePoint</span></span>

2. <span data-ttu-id="11b66-154">[Ajouter](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) des colonnes et [modifier](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*comme indiqué ci-dessous dans les mêmes paramètres de colonne ordre et format*) pour cette liste</span><span class="sxs-lookup"><span data-stu-id="11b66-154">[Add](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) columns and [Edit](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*as below in the same order and format*) column settings for this list</span></span>


    <span data-ttu-id="11b66-155">Paramètres de colonne recommandés--------| service---| Une seule ligne de l'emplacement de texte | Une seule ligne de texte catégorie | Une seule ligne de texte Description | Plusieurs lignes de photos de texte | Plusieurs lignes de texte CreatorName | Une seule ligne de texte CreatorContact | Une seule ligne de texte ReportedAt | Une seule ligne de texte AffectéÀ | Une seule ligne de texte AssignedBy | État d'une seule ligne de texte | Choix avec des options comme nouveau, affecté, résolu, fermé et rouvert (*ces étapes de ticket sont obligatoires*) HelpdeskComments | Plusieurs lignes de texte UserFeedback | Plusieurs lignes de texte ReasonsToReopen | Plusieurs lignes de texte CreatorKaizalaName | Une seule ligne de texte CreatorKaizalaContact | Une seule ligne de texte UserRating | Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="11b66-155">Column  Recommended settings  -------- |---   Department|Single line of text   Location|Single line of text   Category|Single line of text   Description |Multiple lines of text   Photos|Multiple lines of text   CreatorName|Single line of text   CreatorContact|Single line of text   ReportedAt|Single line of text   AssignedTo|Single line of text   AssignedBy|Single line of text   Status|Choice with options as New, Assigned, Resolved, Closed and Reopened (*These ticket stages are mandatory*)   HelpdeskComments|Multiple lines of text   UserFeedback|Multiple lines of text   ReasonsToReopen|Multiple lines of text   CreatorKaizalaName|Single line of text   CreatorKaizalaContact|Single line of text   UserRating|Single line of text</span></span>
 

4. <span data-ttu-id="11b66-156">[Modifier l'affichage de liste](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) sur l'ID de poste à la première place. Il s'agit de l'ID de ticket unique qui s'affichera dans la carte, une fois le ticket attribué.</span><span class="sxs-lookup"><span data-stu-id="11b66-156">[Edit list view](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) to position ID in first place.This is the unique ticket ID that will be displayed in the card, once the ticket is assigned.</span></span>

     ><span data-ttu-id="11b66-157">Remarque: [Télécharger](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) le modèle Excel pour les en-têtes de colonne</span><span class="sxs-lookup"><span data-stu-id="11b66-157">Note: [Download](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) excel template for column headers</span></span>

### <a name="import-and-set-up-flows"></a><span data-ttu-id="11b66-158">Importer et configurer des flux</span><span class="sxs-lookup"><span data-stu-id="11b66-158">Import and Set up Flows</span></span>

<span data-ttu-id="11b66-159">Cette solution comporte 3 flux,</span><span class="sxs-lookup"><span data-stu-id="11b66-159">This solution has 3 Flows,</span></span>

1. <span data-ttu-id="11b66-160">Pour collecter les détails des tickets à partir de la carte et les stocker dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-160">To collect ticket details from the card and store it in SharePoint</span></span>

    1. <span data-ttu-id="11b66-161">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketCreationFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="11b66-161">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketCreationFlow.Zip" to your Microsoft Flow account</span></span>

          > <span data-ttu-id="11b66-162">Remarque: Si vous n'avez jamais utilisé les connexions SharePoint ou Kaizala, ajoutez d'abord les [connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="11b66-162">Note- If you have never used Sharepoint or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>    

    2. <span data-ttu-id="11b66-163">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="11b66-163">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="11b66-164">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-164">In the First block</span></span> 

               1. <span data-ttu-id="11b66-165">Entrez l'ID de groupe ou sélectionnez le nom du groupe auquel vous souhaitez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="11b66-165">Enter the Group ID or Select the Group name where you want to add the card</span></span>

               2. <span data-ttu-id="11b66-166">Cliquez sur le champ package d'action pour entrer le code d'action que vous avez indiqué pour «CreateTicket-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="11b66-166">Click on Action Package field to enter action id that you have given for "CreateTicket-ActionPackage.zip"</span></span>

               3. <span data-ttu-id="11b66-167">Mapper l'action sur «tout»</span><span class="sxs-lookup"><span data-stu-id="11b66-167">Map action to "All"</span></span>

                  <img src="EmployeeHelpdesk-Images/5.JPG" width="600">

          2. <span data-ttu-id="11b66-168">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-168">In the Last block</span></span>

               1. <span data-ttu-id="11b66-169">Entrer l'adresse du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-169">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="11b66-170">Entrer le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="11b66-170">Enter List Name</span></span>
                  
                  <img src="EmployeeHelpdesk-Images/6.JPG" width="600">

                   > <span data-ttu-id="11b66-171">Remarque: toutes les colonnes de la liste SharePoint seront affichées dans le flux de la saisie de l'adresse du site SharePoint & nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="11b66-171">Note: All the columns in the SharePoint list will be displayed in Flow on entering Sharepoint Site address & List Name.</span></span> <span data-ttu-id="11b66-172">Vérifiez le mappage des champs de liste SharePoint dans le flux.</span><span class="sxs-lookup"><span data-stu-id="11b66-172">Verify the mapping of SharePoint list fields in Flow.</span></span> 

          3.  <span data-ttu-id="11b66-173">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="11b66-173">Save the Flow</span></span>
           

2. <span data-ttu-id="11b66-174">Pour envoyer une carte mise à jour à l'utilisateur lorsque l'agent du support technique met à jour l'État, les commentaires ou les deux dans le SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-174">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint</span></span>

    1. <span data-ttu-id="11b66-175">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketStatusUpdatesFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="11b66-175">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketStatusUpdatesFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="11b66-176">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="11b66-176">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="11b66-177">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-177">In the first block</span></span>

               1.  <span data-ttu-id="11b66-178">Entrer l'adresse du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="11b66-178">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="11b66-179">Entrer le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="11b66-179">Enter List Name</span></span>

                  <img src="EmployeeHelpdesk-Images/6.5.jpg" width="600">

          2. <span data-ttu-id="11b66-180">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-180">In the last block</span></span>

               1. <span data-ttu-id="11b66-181">Entrez l'ID de groupe ou sélectionnez un nom de groupe à l'endroit où vous souhaitez envoyer les mises à jour d'État.</span><span class="sxs-lookup"><span data-stu-id="11b66-181">Enter the group ID or select group name to where you want to send the status updates</span></span>

               2. <span data-ttu-id="11b66-182">Cliquez sur action pour sélectionner «package d'actions».</span><span class="sxs-lookup"><span data-stu-id="11b66-182">Click on Action to select "Action Package"</span></span> 

               3. <span data-ttu-id="11b66-183">Cliquez sur package d'action pour entrer l'ID d'action que vous avez indiqué pour «StatusUpdateFromHelpDesk-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="11b66-183">Click on Action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

               4. <span data-ttu-id="11b66-184">Mapper le corps sur «ActionBody»</span><span class="sxs-lookup"><span data-stu-id="11b66-184">Map body to "ActionBody"</span></span>

                  <img src="EmployeeHelpdesk-Images/7.JPG" width="600">

        3.  <span data-ttu-id="11b66-185">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="11b66-185">Save the Flow</span></span>
    
3. <span data-ttu-id="11b66-186">Pour mettre à jour la liste SharePoint lorsque l'utilisateur choisit de fermer, de rouvrir ou d'ajouter des commentaires de commentaires à partir de la carte</span><span class="sxs-lookup"><span data-stu-id="11b66-186">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card</span></span>
 
    1. <span data-ttu-id="11b66-187">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketReopenFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="11b66-187">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketReopenFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="11b66-188">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="11b66-188">Edit details in Imported Flow (*See steps below*)</span></span> 

        1. <span data-ttu-id="11b66-189">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-189">In the First block</span></span> 

             1. <span data-ttu-id="11b66-190">Sélectionnez un nom de groupe ou entrez l'ID de groupe.</span><span class="sxs-lookup"><span data-stu-id="11b66-190">Select group name or enter the group ID</span></span>

             2. <span data-ttu-id="11b66-191">Cliquez sur package d'action pour entrer l'ID d'action que vous avez indiqué pour «StatusUpdateFromHelpDesk-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="11b66-191">Click on action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

             3. <span data-ttu-id="11b66-192">Mapper l'action sur «tout»</span><span class="sxs-lookup"><span data-stu-id="11b66-192">Map action to "All"</span></span>

                <img src="EmployeeHelpdesk-Images/8.JPG" width="600">

        2. <span data-ttu-id="11b66-193">Dans le deuxième bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-193">In the second block</span></span>

             1. <span data-ttu-id="11b66-194">Entrez l'adresse du site</span><span class="sxs-lookup"><span data-stu-id="11b66-194">Enter the site address</span></span>

             2. <span data-ttu-id="11b66-195">Entrez le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="11b66-195">Enter the list name</span></span> 

                <img src="EmployeeHelpdesk-Images/9.JPG" width="600">

        3. <span data-ttu-id="11b66-196">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="11b66-196">In the Last block</span></span>

             1. <span data-ttu-id="11b66-197">Entrez l'adresse du site</span><span class="sxs-lookup"><span data-stu-id="11b66-197">Enter the site address</span></span>

             2. <span data-ttu-id="11b66-198">Entrez le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="11b66-198">Enter the list name</span></span>

                <img src="EmployeeHelpdesk-Images/10.JPG" width="600">

        4.  <span data-ttu-id="11b66-199">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="11b66-199">Save the Flow</span></span>
