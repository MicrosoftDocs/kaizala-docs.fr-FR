# <a name="employee-help-desk"></a><span data-ttu-id="680a9-101">Support technique pour les employés</span><span class="sxs-lookup"><span data-stu-id="680a9-101">Employee Help Desk</span></span>

 <span data-ttu-id="680a9-102">Dans une organisation, l'équipe du support technique examine les requêtes émises par les employés, les affecte à un agent de champ et met à jour l'état de résolution à l'employé.</span><span class="sxs-lookup"><span data-stu-id="680a9-102">In an Organization, helpdesk team looks into the queries raised by employees, assigns it to a field agent and updates back the resolution status to the employee.</span></span> <span data-ttu-id="680a9-103">Toutes les requêtes sont connectées sous forme de tickets pour faciliter le suivi et la résolution.</span><span class="sxs-lookup"><span data-stu-id="680a9-103">All the queries are logged in as tickets for easy tracking and resolution.</span></span> <span data-ttu-id="680a9-104">Un système de gestion des tickets permet aux agents du support technique de capturer, classer, résoudre et recueillir des commentaires de façon systématique.</span><span class="sxs-lookup"><span data-stu-id="680a9-104">A ticketing system enables helpdesk agents to systematically capture, categorize, resolve and collect feedback.</span></span> <span data-ttu-id="680a9-105">Cela permet à une organisation d'être efficace dans la résolution des requêtes et a un effet multiplicateur sur les scores de satisfaction des employés.</span><span class="sxs-lookup"><span data-stu-id="680a9-105">This enables an organization to be effective in query resolution and has a multiplier effect on employee satisfaction scores.</span></span>

<span data-ttu-id="680a9-106">Cette solution utilise Kaizala en tant que serveur frontal, SharePoint comme serveur principal et de flux pour interagir avec Kaizala et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="680a9-106">This solution uses Kaizala as the front-end, SharePoint as the backend and Flow as a means to interact with Kaizala and SharePoint.</span></span> <span data-ttu-id="680a9-107">Un utilisateur crée le ticket en envoyant un formulaire dans Kaizala, les détails de ticket envoyés à l'aide de cette carte sont capturés et stockés dans SharePoint à l'aide de Flow. on submission, l'utilisateur obtient une carte mise à jour, soit lorsque-</span><span class="sxs-lookup"><span data-stu-id="680a9-107">A user creates the ticket by submitting a form in Kaizala, ticket details submitted using this card is captured and stored in the SharePoint using Flow.On submission, User gets an updated card,either when-</span></span>

   1. <span data-ttu-id="680a9-108">L'agent du support technique met à jour l'état du ticket dans SharePoint (nouveau, affecté ou résolu) ou</span><span class="sxs-lookup"><span data-stu-id="680a9-108">Help desk agent updates the status of the ticket in SharePoint (New, Assigned or Resolved) or</span></span>

   2. <span data-ttu-id="680a9-109">Les agents du support technique ajoutent des commentaires sur le ticket dans SharePoint ou</span><span class="sxs-lookup"><span data-stu-id="680a9-109">Help desk agents adds comments on the ticket in SharePoint or</span></span>

   3. <span data-ttu-id="680a9-110">L'état des mises à jour de l'agent de support technique et ajoute des commentaires dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-110">Both, help desk agent updates status and adds comments in SharePoint</span></span>

<span data-ttu-id="680a9-111">Si l'utilisateur est satisfait de la résolution proposée, l'utilisateur a la possibilité de fermer le ticket et d'envoyer des commentaires.</span><span class="sxs-lookup"><span data-stu-id="680a9-111">If the user is satisfied with the proposed resolution, user has the ability to close the ticket and submit feedback.</span></span> <span data-ttu-id="680a9-112">Si l'utilisateur n'est pas satisfait de la résolution, l'utilisateur peut rouvrir le ticket.</span><span class="sxs-lookup"><span data-stu-id="680a9-112">If the user is not satisfied with the resolution, user can re-open the ticket.</span></span> <span data-ttu-id="680a9-113">Commentaires des utilisateurs-évaluation et commentaires, État: rouvert ou fermé est mis à jour dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="680a9-113">User Feedback - Rating and comments, status- Reopened or closed is updated back in SharePoint.</span></span>

> <span data-ttu-id="680a9-114">Remarque: cette carte fonctionne uniquement dans les groupes Hub et spoke</span><span class="sxs-lookup"><span data-stu-id="680a9-114">Note: This card works only in Hub and spoke groups</span></span>

  <span data-ttu-id="680a9-115">Affichage par l'utilisateur de la création et de l'envoi d'un ticket:</span><span class="sxs-lookup"><span data-stu-id="680a9-115">User view of ticket creation and submission:</span></span>

  <img src="EmployeeHelpdesk-Images/1.jpg" width="350">

   <span data-ttu-id="680a9-116">Affichage de l'État mis à jour sur «affecté» dans SharePoint et la carte correspondante envoyée à l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="680a9-116">View of status being updated to "Assigned" in sharepoint and the corresponding card that is sent to user</span></span>

   <img src="EmployeeHelpdesk-Images/2.jpg" width="600">

   <span data-ttu-id="680a9-117">Affichage de l'État mis à jour sur «résolu» dans SharePoint et la carte correspondante envoyée à l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="680a9-117">View of status being updated to "Resolved" in sharepoint and the corresponding card that is sent to user</span></span>
   
   <img src="EmployeeHelpdesk-Images/3.jpg" width="600">

   <span data-ttu-id="680a9-118">Affichage des commentaires de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="680a9-118">User Feedback view</span></span>

   <img src="EmployeeHelpdesk-Images/4.jpg" width="350">


## <a name="implementation-steps"></a><span data-ttu-id="680a9-119">Étapes d'implémentation:</span><span class="sxs-lookup"><span data-stu-id="680a9-119">Implementation Steps:</span></span>
<span data-ttu-id="680a9-120">Cette opération est généralement divisée en trois étapes:</span><span class="sxs-lookup"><span data-stu-id="680a9-120">This is broadly divided into 3 steps:</span></span>

1. <span data-ttu-id="680a9-121">Télécharger des packages d'actions qui permettent à un utilisateur de (*2 packages d'actions*)</span><span class="sxs-lookup"><span data-stu-id="680a9-121">Upload action packages that enable a user to (*2 Action Packages*)</span></span>

   1. <span data-ttu-id="680a9-122">Création et envoi d'un ticket pour le service d'assistance (*CreateTicket-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="680a9-122">Create and submit a ticket to help desk (*CreateTicket-ActionPackage.Zip*)</span></span>

   2. <span data-ttu-id="680a9-123">Recevoir des mises à jour d'État & des commentaires du support technique (*StatusUpdateFromHelpdesk-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="680a9-123">Receive status updates & comments from help desk (*StatusUpdateFromHelpdesk-ActionPackage.Zip*)</span></span>

2. <span data-ttu-id="680a9-124">Configurer une liste SharePoint qui permet aux agents du support technique de</span><span class="sxs-lookup"><span data-stu-id="680a9-124">Set up a SharePoint list that enables helpdesk agents to</span></span>

    1. <span data-ttu-id="680a9-125">Stocker les détails du ticket</span><span class="sxs-lookup"><span data-stu-id="680a9-125">Store the ticket details</span></span>

    2. <span data-ttu-id="680a9-126">Affecter, commenter et modifier l'état du ticket</span><span class="sxs-lookup"><span data-stu-id="680a9-126">Assign, comment and change the ticket status</span></span>

3. <span data-ttu-id="680a9-127">Configurer Microsoft Flow pour interagir avec SharePoint et Kaizala (*3 flux*)</span><span class="sxs-lookup"><span data-stu-id="680a9-127">Configure Microsoft Flow to interact with SharePoint and Kaizala (*3 Flows*)</span></span>

    1. <span data-ttu-id="680a9-128">Pour collecter les détails des tickets à partir de la carte et les stocker dans SharePoint (*TicketCreationFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="680a9-128">To collect ticket details from the card and store it in SharePoint(*TicketCreationFlow.Zip*)</span></span>
    
    2. <span data-ttu-id="680a9-129">Pour envoyer une carte mise à jour à l'utilisateur lorsque l'agent du support technique met à jour l'État, les commentaires ou les deux dans le SharePoint (*TicketStatusUpdatesFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="680a9-129">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint(*TicketStatusUpdatesFlow.Zip*)</span></span>

    3. <span data-ttu-id="680a9-130">Pour mettre à jour la liste SharePoint lorsque l'utilisateur choisit de fermer, de rouvrir ou d'ajouter des commentaires de commentaires à partir de la carte (*TicketReopenFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="680a9-130">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card(*TicketReopenFlow.Zip*)</span></span>

### <a name="upload-action-packages"></a><span data-ttu-id="680a9-131">Télécharger des packages d'actions</span><span class="sxs-lookup"><span data-stu-id="680a9-131">Upload Action Packages</span></span>
1. <span data-ttu-id="680a9-132">Télécharger le fichier [«EmployeeHelpDesk-SolutionPackage. zip»](https://aka.ms/EmployeeHelpdesk-SolutionPackage.zip)(*il contient 2 packages d'action et 3 flux*)</span><span class="sxs-lookup"><span data-stu-id="680a9-132">Download the ["EmployeeHelpDesk-SolutionPackage.zip"](https://aka.ms/EmployeeHelpdesk-SolutionPackage.zip)(*This contains 2 Action Packages and 3 Flows*)</span></span>

2. <span data-ttu-id="680a9-133">Téléchargez la dernière version de Kaizala [«ActionSDK. zip»](https://manage.kaiza.la/MiniApps/DownloadSDK) (*elle contient KASClient. js*)</span><span class="sxs-lookup"><span data-stu-id="680a9-133">Download the latest version of Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*This contains KASClient.js*)</span></span>

3. <span data-ttu-id="680a9-134">Configurer le «CreateTicket-ActionPackage. zip»</span><span class="sxs-lookup"><span data-stu-id="680a9-134">Set up the "CreateTicket-ActionPackage.Zip"</span></span>

   1. <span data-ttu-id="680a9-135">DéCompresser «CreateTicket-ActionPackage. zip» dans un dossier</span><span class="sxs-lookup"><span data-stu-id="680a9-135">Unzip "CreateTicket-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="680a9-136">Modifier les actions «ID» et «nom du fournisseur» dans package. JSON</span><span class="sxs-lookup"><span data-stu-id="680a9-136">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="680a9-137">Ajouter KASClient. js à ce dossier</span><span class="sxs-lookup"><span data-stu-id="680a9-137">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="680a9-138">Zip tout le contenu de ce dossier (*ce dossier est votre package d'action modifié qui doit être importé dans le portail de gestion Kaizala*)</span><span class="sxs-lookup"><span data-stu-id="680a9-138">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="680a9-139">[Importer](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) le package d'actions modifié dans le [portail de gestion Kaizala](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="680a9-139">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="680a9-140">[Publiez](https://docs.microsoft.com/en-us/kaizala/actions/publish) l'action et ajoutez l'action à un groupe auquel vous voulez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="680a9-140">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="680a9-141">Sélectionner les rôles d'utilisateur en tant qu'administrateur et membre</span><span class="sxs-lookup"><span data-stu-id="680a9-141">Select user roles as admin and member</span></span>

4. <span data-ttu-id="680a9-142">Configurer «StatusUpdateFromHelpDesk-ActionPackage. zip»</span><span class="sxs-lookup"><span data-stu-id="680a9-142">Set up "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

   1.  <span data-ttu-id="680a9-143">DéCompresser «StatusUpdateFromHelpDesk-ActionPackage. zip» dans un dossier</span><span class="sxs-lookup"><span data-stu-id="680a9-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="680a9-144">Modifier les actions «ID» et «nom du fournisseur» dans package. JSON</span><span class="sxs-lookup"><span data-stu-id="680a9-144">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="680a9-145">Ajouter KASClient. js à ce dossier</span><span class="sxs-lookup"><span data-stu-id="680a9-145">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="680a9-146">Zip tout le contenu de ce dossier (*ce dossier est votre package d'action modifié qui doit être importé dans le portail de gestion Kaizala*)</span><span class="sxs-lookup"><span data-stu-id="680a9-146">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="680a9-147">[Importer](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) le package d'actions modifié dans le [portail de gestion Kaizala](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="680a9-147">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="680a9-148">[Publiez](https://docs.microsoft.com/en-us/kaizala/actions/publish) l'action et ajoutez l'action à un groupe auquel vous voulez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="680a9-148">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="680a9-149">Sélectionner un rôle d'utilisateur en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="680a9-149">Select user role as admin</span></span>

       > <span data-ttu-id="680a9-150">Remarque: «CreateTicket-ActionPackage. zip» est la carte utilisée pour déclencher un ticket et doit être mise à la disposition de l'administrateur et des abonnés.» StatusUpdateFromHelpDesk-ActionPackage. zip "afficher les commentaires et les mises à jour de l'état du support technique.</span><span class="sxs-lookup"><span data-stu-id="680a9-150">Note: "CreateTicket-ActionPackage.Zip" is the card that is used to raise a ticket and should be made available to admin and Subscribers."StatusUpdateFromHelpDesk-ActionPackage.Zip" show helpdesk comments and status updates.</span></span> <span data-ttu-id="680a9-151">Les abonnés n'ont pas besoin d'afficher cette carte dans la palette d'action, donc elle n'est visible que par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="680a9-151">Subscribers do not have to see this card in action palette, hence this is only made visible to admin.</span></span>

### <a name="set-up-a-sharepoint-list"></a><span data-ttu-id="680a9-152">Configurer une liste SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-152">Set up a SharePoint List</span></span>

1. <span data-ttu-id="680a9-153">[Créer](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) une liste dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-153">[Create](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) a new list in SharePoint</span></span>

2. <span data-ttu-id="680a9-154">[Ajouter](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) des colonnes et [modifier](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*comme indiqué ci-dessous dans les mêmes paramètres de colonne ordre et format*) pour cette liste</span><span class="sxs-lookup"><span data-stu-id="680a9-154">[Add](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) columns and [Edit](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*as below in the same order and format*) column settings for this list</span></span>


    |<span data-ttu-id="680a9-155">Column</span><span class="sxs-lookup"><span data-stu-id="680a9-155">Column</span></span>|<span data-ttu-id="680a9-156">Paramètres recommandés</span><span class="sxs-lookup"><span data-stu-id="680a9-156">Recommended settings</span></span>|
    |-------- |---|
    |<span data-ttu-id="680a9-157">Service</span><span class="sxs-lookup"><span data-stu-id="680a9-157">Department</span></span>|<span data-ttu-id="680a9-158">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-158">Single line of text</span></span>|
    |<span data-ttu-id="680a9-159">Emplacement</span><span class="sxs-lookup"><span data-stu-id="680a9-159">Location</span></span>|<span data-ttu-id="680a9-160">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-160">Single line of text</span></span>|
    |<span data-ttu-id="680a9-161">Catégorie</span><span class="sxs-lookup"><span data-stu-id="680a9-161">Category</span></span>|<span data-ttu-id="680a9-162">Ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-162">Single line of text</span></span>|
    |<span data-ttu-id="680a9-163">Description</span><span class="sxs-lookup"><span data-stu-id="680a9-163">Description</span></span> |<span data-ttu-id="680a9-164">Plusieurs lignes de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-164">Multiple lines of text</span></span>|
    |<span data-ttu-id="680a9-165">Photos</span><span class="sxs-lookup"><span data-stu-id="680a9-165">Photos</span></span>|<span data-ttu-id="680a9-166">Plusieurs lignes de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-166">Multiple lines of text</span></span>|
    |<span data-ttu-id="680a9-167">CreatorName</span><span class="sxs-lookup"><span data-stu-id="680a9-167">CreatorName</span></span>|<span data-ttu-id="680a9-168">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-168">Single line of text</span></span>|
    |<span data-ttu-id="680a9-169">CreatorContact</span><span class="sxs-lookup"><span data-stu-id="680a9-169">CreatorContact</span></span>|<span data-ttu-id="680a9-170">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-170">Single line of text</span></span>|
    |<span data-ttu-id="680a9-171">ReportedAt</span><span class="sxs-lookup"><span data-stu-id="680a9-171">ReportedAt</span></span>|<span data-ttu-id="680a9-172">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-172">Single line of text</span></span>|
    |<span data-ttu-id="680a9-173">AssignedTo</span><span class="sxs-lookup"><span data-stu-id="680a9-173">AssignedTo</span></span>|<span data-ttu-id="680a9-174">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-174">Single line of text</span></span>|
    |<span data-ttu-id="680a9-175">AssignedBy</span><span class="sxs-lookup"><span data-stu-id="680a9-175">AssignedBy</span></span>|<span data-ttu-id="680a9-176">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-176">Single line of text</span></span>|
    |<span data-ttu-id="680a9-177">Statut</span><span class="sxs-lookup"><span data-stu-id="680a9-177">Status</span></span>|<span data-ttu-id="680a9-178">Choix avec des options comme nouveau, affecté, résolu, fermé et rouvert (*ces étapes de ticket sont obligatoires*)</span><span class="sxs-lookup"><span data-stu-id="680a9-178">Choice with options as New, Assigned, Resolved, Closed and Reopened (*These ticket stages are mandatory*)</span></span>|
    |<span data-ttu-id="680a9-179">HelpdeskComments</span><span class="sxs-lookup"><span data-stu-id="680a9-179">HelpdeskComments</span></span>|<span data-ttu-id="680a9-180">Plusieurs lignes de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-180">Multiple lines of text</span></span>|
    |<span data-ttu-id="680a9-181">UserFeedback</span><span class="sxs-lookup"><span data-stu-id="680a9-181">UserFeedback</span></span>|<span data-ttu-id="680a9-182">Plusieurs lignes de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-182">Multiple lines of text</span></span>|
    |<span data-ttu-id="680a9-183">ReasonsToReopen</span><span class="sxs-lookup"><span data-stu-id="680a9-183">ReasonsToReopen</span></span>|<span data-ttu-id="680a9-184">Plusieurs lignes de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-184">Multiple lines of text</span></span>|
    |<span data-ttu-id="680a9-185">CreatorKaizalaName</span><span class="sxs-lookup"><span data-stu-id="680a9-185">CreatorKaizalaName</span></span>|<span data-ttu-id="680a9-186">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-186">Single line of text</span></span>|
    |<span data-ttu-id="680a9-187">CreatorKaizalaContact</span><span class="sxs-lookup"><span data-stu-id="680a9-187">CreatorKaizalaContact</span></span>|<span data-ttu-id="680a9-188">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-188">Single line of text</span></span>|
    |<span data-ttu-id="680a9-189">UserRating</span><span class="sxs-lookup"><span data-stu-id="680a9-189">UserRating</span></span>|<span data-ttu-id="680a9-190">Une seule ligne de texte</span><span class="sxs-lookup"><span data-stu-id="680a9-190">Single line of text</span></span>|
 

4. <span data-ttu-id="680a9-191">[Modifier l'affichage de liste](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) sur l'ID de poste à la première place. Il s'agit de l'ID de ticket unique qui s'affichera dans la carte, une fois le ticket attribué.</span><span class="sxs-lookup"><span data-stu-id="680a9-191">[Edit list view](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) to position ID in first place.This is the unique ticket ID that will be displayed in the card, once the ticket is assigned.</span></span>

     ><span data-ttu-id="680a9-192">Remarque: [Télécharger](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) le modèle Excel pour les en-têtes de colonne</span><span class="sxs-lookup"><span data-stu-id="680a9-192">Note: [Download](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) excel template for column headers</span></span>

### <a name="import-and-set-up-flows"></a><span data-ttu-id="680a9-193">Importer et configurer des flux</span><span class="sxs-lookup"><span data-stu-id="680a9-193">Import and Set up Flows</span></span>

<span data-ttu-id="680a9-194">Cette solution comporte 3 flux,</span><span class="sxs-lookup"><span data-stu-id="680a9-194">This solution has 3 Flows,</span></span>

1. <span data-ttu-id="680a9-195">Pour collecter les détails des tickets à partir de la carte et les stocker dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-195">To collect ticket details from the card and store it in SharePoint</span></span>

    1. <span data-ttu-id="680a9-196">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketCreationFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="680a9-196">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketCreationFlow.Zip" to your Microsoft Flow account</span></span>

          > <span data-ttu-id="680a9-197">Remarque: Si vous n'avez jamais utilisé les connexions SharePoint ou Kaizala, ajoutez d'abord les [connexions](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="680a9-197">Note- If you have never used Sharepoint or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>    

    2. <span data-ttu-id="680a9-198">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="680a9-198">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="680a9-199">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-199">In the First block</span></span> 

               1. <span data-ttu-id="680a9-200">Entrez l'ID de groupe ou sélectionnez le nom du groupe auquel vous souhaitez ajouter la carte.</span><span class="sxs-lookup"><span data-stu-id="680a9-200">Enter the Group ID or Select the Group name where you want to add the card</span></span>

               2. <span data-ttu-id="680a9-201">Cliquez sur le champ package d'action pour entrer le code d'action que vous avez indiqué pour «CreateTicket-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="680a9-201">Click on Action Package field to enter action id that you have given for "CreateTicket-ActionPackage.zip"</span></span>

               3. <span data-ttu-id="680a9-202">Mapper l'action sur «tout»</span><span class="sxs-lookup"><span data-stu-id="680a9-202">Map action to "All"</span></span>

                  <img src="EmployeeHelpdesk-Images/5.JPG" width="600">

          2. <span data-ttu-id="680a9-203">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-203">In the Last block</span></span>

               1. <span data-ttu-id="680a9-204">Entrer l'adresse du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-204">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="680a9-205">Entrer le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="680a9-205">Enter List Name</span></span>
                  
                  <img src="EmployeeHelpdesk-Images/6.JPG" width="600">

                   > <span data-ttu-id="680a9-206">Remarque: toutes les colonnes de la liste SharePoint seront affichées dans le flux de la saisie de l'adresse du site SharePoint & nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="680a9-206">Note: All the columns in the SharePoint list will be displayed in Flow on entering Sharepoint Site address & List Name.</span></span> <span data-ttu-id="680a9-207">Vérifiez le mappage des champs de liste SharePoint dans le flux.</span><span class="sxs-lookup"><span data-stu-id="680a9-207">Verify the mapping of SharePoint list fields in Flow.</span></span> 

          3.  <span data-ttu-id="680a9-208">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="680a9-208">Save the Flow</span></span>
           

2. <span data-ttu-id="680a9-209">Pour envoyer une carte mise à jour à l'utilisateur lorsque l'agent du support technique met à jour l'État, les commentaires ou les deux dans le SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-209">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint</span></span>

    1. <span data-ttu-id="680a9-210">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketStatusUpdatesFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="680a9-210">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketStatusUpdatesFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="680a9-211">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="680a9-211">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="680a9-212">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-212">In the first block</span></span>

               1.  <span data-ttu-id="680a9-213">Entrer l'adresse du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="680a9-213">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="680a9-214">Entrer le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="680a9-214">Enter List Name</span></span>

                  <img src="EmployeeHelpdesk-Images/6.5.jpg" width="600">

          2. <span data-ttu-id="680a9-215">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-215">In the last block</span></span>

               1. <span data-ttu-id="680a9-216">Entrez l'ID de groupe ou sélectionnez un nom de groupe à l'endroit où vous souhaitez envoyer les mises à jour d'État.</span><span class="sxs-lookup"><span data-stu-id="680a9-216">Enter the group ID or select group name to where you want to send the status updates</span></span>

               2. <span data-ttu-id="680a9-217">Cliquez sur action pour sélectionner «package d'actions».</span><span class="sxs-lookup"><span data-stu-id="680a9-217">Click on Action to select "Action Package"</span></span> 

               3. <span data-ttu-id="680a9-218">Cliquez sur package d'action pour entrer l'ID d'action que vous avez indiqué pour «StatusUpdateFromHelpDesk-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="680a9-218">Click on Action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

               4. <span data-ttu-id="680a9-219">Mapper le corps sur «ActionBody»</span><span class="sxs-lookup"><span data-stu-id="680a9-219">Map body to "ActionBody"</span></span>

                  <img src="EmployeeHelpdesk-Images/7.JPG" width="600">

        3.  <span data-ttu-id="680a9-220">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="680a9-220">Save the Flow</span></span>
    
3. <span data-ttu-id="680a9-221">Pour mettre à jour la liste SharePoint lorsque l'utilisateur choisit de fermer, de rouvrir ou d'ajouter des commentaires de commentaires à partir de la carte</span><span class="sxs-lookup"><span data-stu-id="680a9-221">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card</span></span>
 
    1. <span data-ttu-id="680a9-222">[Importer](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) le fichier «TicketReopenFlow. zip» sur votre compte Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="680a9-222">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketReopenFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="680a9-223">Modifier les détails dans le flux importé (*voir les étapes ci-dessous*)</span><span class="sxs-lookup"><span data-stu-id="680a9-223">Edit details in Imported Flow (*See steps below*)</span></span> 

        1. <span data-ttu-id="680a9-224">Dans le premier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-224">In the First block</span></span> 

             1. <span data-ttu-id="680a9-225">Sélectionnez un nom de groupe ou entrez l'ID de groupe.</span><span class="sxs-lookup"><span data-stu-id="680a9-225">Select group name or enter the group ID</span></span>

             2. <span data-ttu-id="680a9-226">Cliquez sur package d'action pour entrer l'ID d'action que vous avez indiqué pour «StatusUpdateFromHelpDesk-ActionPackage. zip».</span><span class="sxs-lookup"><span data-stu-id="680a9-226">Click on action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

             3. <span data-ttu-id="680a9-227">Mapper l'action sur «tout»</span><span class="sxs-lookup"><span data-stu-id="680a9-227">Map action to "All"</span></span>

                <img src="EmployeeHelpdesk-Images/8.JPG" width="600">

        2. <span data-ttu-id="680a9-228">Dans le deuxième bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-228">In the second block</span></span>

             1. <span data-ttu-id="680a9-229">Entrez l'adresse du site</span><span class="sxs-lookup"><span data-stu-id="680a9-229">Enter the site address</span></span>

             2. <span data-ttu-id="680a9-230">Entrez le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="680a9-230">Enter the list name</span></span> 

                <img src="EmployeeHelpdesk-Images/9.JPG" width="600">

        3. <span data-ttu-id="680a9-231">Dans le dernier bloc</span><span class="sxs-lookup"><span data-stu-id="680a9-231">In the Last block</span></span>

             1. <span data-ttu-id="680a9-232">Entrez l'adresse du site</span><span class="sxs-lookup"><span data-stu-id="680a9-232">Enter the site address</span></span>

             2. <span data-ttu-id="680a9-233">Entrez le nom de la liste</span><span class="sxs-lookup"><span data-stu-id="680a9-233">Enter the list name</span></span>

                <img src="EmployeeHelpdesk-Images/10.JPG" width="600">

        4.  <span data-ttu-id="680a9-234">Enregistrer le flux</span><span class="sxs-lookup"><span data-stu-id="680a9-234">Save the Flow</span></span>
