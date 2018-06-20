# <a name="get-started-with-custom-kaizala-actions"></a><span data-ttu-id="925f6-101">Prendre en main des Actions personnalisées Kaizala</span><span class="sxs-lookup"><span data-stu-id="925f6-101">Get Started with custom Kaizala Actions</span></span>

## <a name="kaizala-action-development-lifecycle"></a><span data-ttu-id="925f6-102">Cycle de développement Kaizala Action</span><span class="sxs-lookup"><span data-stu-id="925f6-102">Kaizala Action Development Lifecycle</span></span>

<span data-ttu-id="925f6-103">Le cycle de vie de développement courantes d’une Action Kaizala comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="925f6-103">The typical development lifecycle of a Kaizala Action includes the following steps:</span></span>

  <span data-ttu-id="925f6-104">**Étape 1 : Déterminez l’objet de l’Action Kaizala**</span><span class="sxs-lookup"><span data-stu-id="925f6-104">**Step 1 - Decide on the purpose of the Kaizala Action**</span></span>
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
<span data-ttu-id="925f6-105">Déterminez les fonctionnalités et les scénarios les plus importants et réalisez la conception à partir de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="925f6-105">Decide the most important features and scenarios and focus your design around them.</span></span>

   <span data-ttu-id="925f6-106">**Étape 2 : identifier le modèle de données pour l’Action Kaizala**</span><span class="sxs-lookup"><span data-stu-id="925f6-106">**Step 2 - Identify the data model for the Kaizala Action**</span></span>

<span data-ttu-id="925f6-107">Toutes les Actions Kaizala actuellement formulaire basé, par exemple, le modèle de données pour la demande, collecte et regrouper des informations est un ensemble de questions et des types de réponses qui sont pris en charge par la plateforme de Services d’agrégation Kaizala (KAS).</span><span class="sxs-lookup"><span data-stu-id="925f6-107">All Kaizala Actions are currently Form based - i.e. the data model for requesting, collecting and aggregating information is a set of question and answer types that are supported by the Kaizala Aggregation Services (KAS) platform.</span></span> <span data-ttu-id="925f6-108">Considérer comment les données requises pour votre action peuvent levergage l’infrastructure de formulaire pour travailler efficacement.</span><span class="sxs-lookup"><span data-stu-id="925f6-108">Think of how the data required for your action can levergage the form infrastructure to work effectively.</span></span>

   <span data-ttu-id="925f6-109">**Étape 3 : concevoir et implémenter l’interface d’utilisateur et une expérience utilisateur pour le complément.**</span><span class="sxs-lookup"><span data-stu-id="925f6-109">**Step 3 - Design and implement the user experience and user interface for the add-in.**</span></span>

<span data-ttu-id="925f6-110">Concevoir une expérience utilisateur et la fluidité cohérente et facile à apprendre, avec les principaux scénarios qui ne nécessitent que quelques étapes à effectuer.</span><span class="sxs-lookup"><span data-stu-id="925f6-110">Design a fast and fluid user experience that is consistent, easy to learn, with primary scenarios that require only a few steps to complete.</span></span> <span data-ttu-id="925f6-111">Remeber une Action Kaizala ne peut pas faire référence à des sources externes - donc pratiques en termes de ce que vous souhaitez implémenter au sein de votre Action.</span><span class="sxs-lookup"><span data-stu-id="925f6-111">Remeber that a Kaizala Action cannot refer to external sources - so be practical in terms of what you would like to implement within your Action.</span></span>

<span data-ttu-id="925f6-112">Vous pouvez faire votre choix parmi divers outils de développement web et utiliser du code HTML et JavaScript pour implémenter l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="925f6-112">You can choose from a variety of web development tools and use HTML and JavaScript to implement the user interface.</span></span>

<span data-ttu-id="925f6-113">Vous pouvez utiliser le Kit de développement logiciel JS KAS Client pour interagir avec les Services d’agrégation Kaizala Kaizala Client natif.</span><span class="sxs-lookup"><span data-stu-id="925f6-113">You can use the KAS Client JS SDK to interact with the Kaizala Aggregation Services and the native Kaizala Client.</span></span> 

   <span data-ttu-id="925f6-114">**Étape 4 : créer un fichier manifeste pour l’Action basé sur le schéma de manifeste de Package**</span><span class="sxs-lookup"><span data-stu-id="925f6-114">**Step 4 -Create a manifest file for the Action based on the Package Manifest Schema**</span></span>

<span data-ttu-id="925f6-115">Créez un fichier manifest dans la notation JSON pour identifier l’Action et ses composants et spécifiez les noms des fichiers de vue.</span><span class="sxs-lookup"><span data-stu-id="925f6-115">Create a manifest file in JSON notation to identify the Action and its components and specify the names of the view files.</span></span>

<span data-ttu-id="925f6-116">**Étape 5 : créer un fichier ZIP du package et le télécharger sur le portail**</span><span class="sxs-lookup"><span data-stu-id="925f6-116">**Step 5 - Create a ZIP file of the package and upload it on the portal**</span></span>

<span data-ttu-id="925f6-117">Créez un fichier ZIP du package avec toutes ses ressources à la racine du package.</span><span class="sxs-lookup"><span data-stu-id="925f6-117">Create a ZIP file of the package with all of it's resources at the root of the package.</span></span>

<span data-ttu-id="925f6-118">Télécharger le package sur le portail de gestion Kaizala.</span><span class="sxs-lookup"><span data-stu-id="925f6-118">Upload the package on the Kaizala Management Portal.</span></span> <span data-ttu-id="925f6-119">Après le téléchargement, l’Action consiste en mode brouillon</span><span class="sxs-lookup"><span data-stu-id="925f6-119">After upload, Action is in Draft state</span></span>

<span data-ttu-id="925f6-120">**Étape 6 - étape de l’Action de brouillon**</span><span class="sxs-lookup"><span data-stu-id="925f6-120">**Step 6 - Stage the Draft Action**</span></span>

<span data-ttu-id="925f6-121">Dans la page Détails de la version de l’Action qui est en mode brouillon, cliquez sur le bouton 'Étape'.</span><span class="sxs-lookup"><span data-stu-id="925f6-121">On the detail page of the Action version which is in draft state, Tap on 'Stage' button.</span></span> <span data-ttu-id="925f6-122">Une fois qu’une Action est mis en place, vous pouvez tester et déboguer l’Action</span><span class="sxs-lookup"><span data-stu-id="925f6-122">Once an Action is staged, you can test & debug the Action</span></span> 

 <span data-ttu-id="925f6-123">**Étape 7 – activer l’Action intermédiaire**</span><span class="sxs-lookup"><span data-stu-id="925f6-123">**Step 7 - Activate the Staged Action**</span></span>

<span data-ttu-id="925f6-124">Une fois qu’une Action est en état intermédiaire et a été testée avec succès, vous pouvez activer l’Action dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="925f6-124">Once an Action is in staged state, and has been tested successfully, you can activate the Action in your organization.</span></span> <span data-ttu-id="925f6-125">Action déplace dans un état actif.</span><span class="sxs-lookup"><span data-stu-id="925f6-125">Action moves to Active state.</span></span> <span data-ttu-id="925f6-126">Les autres membres de votre organisation peuvent également ajouter cette Action à leurs groupes respectifs.</span><span class="sxs-lookup"><span data-stu-id="925f6-126">Other members in your organization can also add this Action to their respective groups.</span></span>

  <span data-ttu-id="925f6-127">**Étape 8 : ajouter l’Action à différents groupes**</span><span class="sxs-lookup"><span data-stu-id="925f6-127">**Step 8 - Add the Action to respective groups**</span></span>

<span data-ttu-id="925f6-128">Une fois que l’Action est Active, vous pouvez déployer l’Action aux groupes associés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="925f6-128">Once Action is in Active state, you can deploy the Action to groups associated with your organization.</span></span> 

