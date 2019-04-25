# <a name="get-started-with-custom-kaizala-actions"></a><span data-ttu-id="4ea84-101">Prise en main des actions Kaizala personnalisées</span><span class="sxs-lookup"><span data-stu-id="4ea84-101">Get Started with custom Kaizala Actions</span></span>

## <a name="kaizala-action-development-lifecycle"></a><span data-ttu-id="4ea84-102">Cycle de développement d'action Kaizala</span><span class="sxs-lookup"><span data-stu-id="4ea84-102">Kaizala Action Development Lifecycle</span></span>

<span data-ttu-id="4ea84-103">Le cycle de vie de développement classique d'une action Kaizala comprend les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="4ea84-103">The typical development lifecycle of a Kaizala Action includes the following steps:</span></span>

  <span data-ttu-id="4ea84-104">**Étape 1: déterminer l'objet de l'action Kaizala**</span><span class="sxs-lookup"><span data-stu-id="4ea84-104">**Step 1 - Decide on the purpose of the Kaizala Action**</span></span>
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
<span data-ttu-id="4ea84-105">Déterminez les fonctionnalités et les scénarios les plus importants et réalisez la conception à partir de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="4ea84-105">Decide the most important features and scenarios and focus your design around them.</span></span>

   <span data-ttu-id="4ea84-106">**Étape 2-identifier le modèle de données pour l'action Kaizala**</span><span class="sxs-lookup"><span data-stu-id="4ea84-106">**Step 2 - Identify the data model for the Kaizala Action**</span></span>

<span data-ttu-id="4ea84-107">Toutes les actions Kaizala sont actuellement basées sur des formulaires, c'est-à-dire que le modèle de données pour la demande, la collecte et l'agrégation des informations est un ensemble de types de questions et de réponses pris en charge par la plateforme Kaizala (KAS).</span><span class="sxs-lookup"><span data-stu-id="4ea84-107">All Kaizala Actions are currently Form based - i.e. the data model for requesting, collecting and aggregating information is a set of question and answer types that are supported by the Kaizala Aggregation Services (KAS) platform.</span></span> <span data-ttu-id="4ea84-108">Pensez à la façon dont les données requises pour votre action peuvent levergage l'infrastructure de formulaire pour fonctionner efficacement.</span><span class="sxs-lookup"><span data-stu-id="4ea84-108">Think of how the data required for your action can levergage the form infrastructure to work effectively.</span></span>

   <span data-ttu-id="4ea84-109">**Étape 3: concevez et implémentez l'expérience utilisateur et l'interface utilisateur pour le complément.**</span><span class="sxs-lookup"><span data-stu-id="4ea84-109">**Step 3 - Design and implement the user experience and user interface for the add-in.**</span></span>

<span data-ttu-id="4ea84-110">Concevez une expérience utilisateur rapide et fluide qui est cohérente, facile à apprendre, avec des scénarios nécessitant uniquement quelques étapes d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4ea84-110">Design a fast and fluid user experience that is consistent, easy to learn, with primary scenarios that require only a few steps to complete.</span></span> <span data-ttu-id="4ea84-111">N'oubliez pas qu'une action Kaizala ne peut pas faire référence à des sources externes, donc être pratique en ce qui concerne les éléments que vous souhaitez mettre en œuvre dans votre action.</span><span class="sxs-lookup"><span data-stu-id="4ea84-111">Remember that a Kaizala Action cannot refer to external sources - so be practical in terms of what you would like to implement within your Action.</span></span>

<span data-ttu-id="4ea84-112">Vous pouvez faire votre choix parmi divers outils de développement web et utiliser du code HTML et JavaScript pour implémenter l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ea84-112">You can choose from a variety of web development tools and use HTML and JavaScript to implement the user interface.</span></span>

<span data-ttu-id="4ea84-113">Vous pouvez utiliser le kit de développement logiciel (SDK) KAS client JS pour interagir avec les services d'agrégation Kaizala et le client Kaizala natif.</span><span class="sxs-lookup"><span data-stu-id="4ea84-113">You can use the KAS Client JS SDK to interact with the Kaizala Aggregation Services and the native Kaizala Client.</span></span> 

   <span data-ttu-id="4ea84-114">**Étape 4: créer un fichier manifeste pour l'action basée sur le schéma de manifeste de package**</span><span class="sxs-lookup"><span data-stu-id="4ea84-114">**Step 4 -Create a manifest file for the Action based on the Package Manifest Schema**</span></span>

<span data-ttu-id="4ea84-115">Créez un fichier manifeste en notation JSON pour identifier l'action et ses composants, et spécifiez les noms des fichiers d'affichage.</span><span class="sxs-lookup"><span data-stu-id="4ea84-115">Create a manifest file in JSON notation to identify the Action and its components and specify the names of the view files.</span></span>

<span data-ttu-id="4ea84-116">**Étape 5: créer un fichier ZIP du package et le charger sur le portail**</span><span class="sxs-lookup"><span data-stu-id="4ea84-116">**Step 5 - Create a ZIP file of the package and upload it on the portal**</span></span>

<span data-ttu-id="4ea84-117">Créez un fichier ZIP du package avec toutes ses ressources à la racine du package.</span><span class="sxs-lookup"><span data-stu-id="4ea84-117">Create a ZIP file of the package with all of it's resources at the root of the package.</span></span>

<span data-ttu-id="4ea84-118">Téléchargez le package sur le portail de gestion Kaizala.</span><span class="sxs-lookup"><span data-stu-id="4ea84-118">Upload the package on the Kaizala Management Portal.</span></span> <span data-ttu-id="4ea84-119">Après le chargement, l'action est à l'état Brouillon</span><span class="sxs-lookup"><span data-stu-id="4ea84-119">After upload, Action is in Draft state</span></span>

<span data-ttu-id="4ea84-120">**Étape 6: étape de l'action de brouillon**</span><span class="sxs-lookup"><span data-stu-id="4ea84-120">**Step 6 - Stage the Draft Action**</span></span>

<span data-ttu-id="4ea84-121">Sur la page de détails de la version de l'action qui est en état Brouillon, appuyez sur le bouton «étape».</span><span class="sxs-lookup"><span data-stu-id="4ea84-121">On the detail page of the Action version which is in draft state, Tap on 'Stage' button.</span></span> <span data-ttu-id="4ea84-122">Une fois qu'une action est intermédiaire, vous pouvez tester & déboguer l'action</span><span class="sxs-lookup"><span data-stu-id="4ea84-122">Once an Action is staged, you can test & debug the Action</span></span> 

 <span data-ttu-id="4ea84-123">**Étape 7: activation de l'action intermédiaire**</span><span class="sxs-lookup"><span data-stu-id="4ea84-123">**Step 7 - Activate the Staged Action**</span></span>

<span data-ttu-id="4ea84-124">Une fois qu'une action est à l'état intermédiaire et qu'elle a été testée correctement, vous pouvez activer l'action dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4ea84-124">Once an Action is in staged state, and has been tested successfully, you can activate the Action in your organization.</span></span> <span data-ttu-id="4ea84-125">L'action passe à l'état actif.</span><span class="sxs-lookup"><span data-stu-id="4ea84-125">Action moves to Active state.</span></span> <span data-ttu-id="4ea84-126">Les autres membres de votre organisation peuvent également ajouter cette action à leurs groupes respectifs.</span><span class="sxs-lookup"><span data-stu-id="4ea84-126">Other members in your organization can also add this Action to their respective groups.</span></span>

  <span data-ttu-id="4ea84-127">**Étape 8: ajouter l'action à des groupes respectifs**</span><span class="sxs-lookup"><span data-stu-id="4ea84-127">**Step 8 - Add the Action to respective groups**</span></span>

<span data-ttu-id="4ea84-128">Une fois que l'action est dans l'état actif, vous pouvez déployer l'action sur des groupes associés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4ea84-128">Once Action is in Active state, you can deploy the Action to groups associated with your organization.</span></span> 

