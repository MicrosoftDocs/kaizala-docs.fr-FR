# <a name="anatomy-of-a-kaizala-action-package"></a><span data-ttu-id="93649-101">Anatomie d'un package d'action Kaizala</span><span class="sxs-lookup"><span data-stu-id="93649-101">Anatomy of a Kaizala Action package</span></span>

<span data-ttu-id="93649-102">Un package d'action Kaizala est un fichier ZIP standard qui n'est pas protégé par mot de passe et dont la taille maximale est de 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="93649-102">A Kaizala Action package is a regular ZIP file which is not password protected and has a maximum size of 1MB.</span></span> <span data-ttu-id="93649-103">Les ressources du package se trouvent à la racine du fichier zip et non dans une structure de répertoire.</span><span class="sxs-lookup"><span data-stu-id="93649-103">The resources in the package are at the root of the zip file and not in any directory structure.</span></span> <span data-ttu-id="93649-104">Les ressources ne peuvent pas non plus référencer de ressources externes autres que celles présentes dans le package.</span><span class="sxs-lookup"><span data-stu-id="93649-104">The resources also cannot reference any external resources other than those present in the package.</span></span>

<span data-ttu-id="93649-105">Les composants de base d'un package d'action Kaizala sont</span><span class="sxs-lookup"><span data-stu-id="93649-105">The basic components of a Kaizala Action package are</span></span> 
*   <span data-ttu-id="93649-106">Un fichier manifeste au format JSON</span><span class="sxs-lookup"><span data-stu-id="93649-106">A manifest file in JSON format</span></span>
*   <span data-ttu-id="93649-107">Un modèle d'application pour votre action Kaizala au format JSON</span><span class="sxs-lookup"><span data-stu-id="93649-107">An app model for your Kaizala Action in JSON format</span></span>
*   <span data-ttu-id="93649-108">Ressources Web qui constituent votre action Kaizala-HTML, JS, CSS et les fichiers image</span><span class="sxs-lookup"><span data-stu-id="93649-108">Web resources that constitute your Kaizala Action - HTML, JS, CSS and image files</span></span>

## <a name="package-manifest"></a><span data-ttu-id="93649-109">Manifeste de package</span><span class="sxs-lookup"><span data-stu-id="93649-109">Package Manifest</span></span>

<span data-ttu-id="93649-110">Le manifeste spécifie les paramètres de l'action Kaizala, tels que les suivants:</span><span class="sxs-lookup"><span data-stu-id="93649-110">The manifest specifies settings of the Kaizala Action, such as the following:</span></span>
*   <span data-ttu-id="93649-111">Le nom d'affichage, la description, l'ID, la version et l'icône d'action de l'action.</span><span class="sxs-lookup"><span data-stu-id="93649-111">The Action's display name, description, ID, version, and Action icon.</span></span>
*   <span data-ttu-id="93649-112">Différentes vues qui définissent votre action et les mappent à leurs points invokation respectifs</span><span class="sxs-lookup"><span data-stu-id="93649-112">Various views that define your Action and mapping them to their respective invokation points</span></span>
    * <span data-ttu-id="93649-113">Une vue de création lorsqu'une action est appelée à partir de la palette</span><span class="sxs-lookup"><span data-stu-id="93649-113">A creation view when an Action is invoked from the palette</span></span>
    * <span data-ttu-id="93649-114">Affichage de carte qui apparaît dans la zone de conversation lors de l'envoi d'une instance de l'action</span><span class="sxs-lookup"><span data-stu-id="93649-114">A card view that appears on the chat canvas when an instance of the Action is sent</span></span>
    * <span data-ttu-id="93649-115">Une vue de répondeur permettant aux utilisateurs de répondre à l'action Kaizala</span><span class="sxs-lookup"><span data-stu-id="93649-115">A responder view for users to respond to the Kaizala Action</span></span>
    * <span data-ttu-id="93649-116">Affichage de synthèse pour afficher les réponses agrégées</span><span class="sxs-lookup"><span data-stu-id="93649-116">A summary view to view aggregated responses</span></span>
*   <span data-ttu-id="93649-117">Étiquettes à utiliser dans les vues natives qui encapsulent vos affichages personnalisés</span><span class="sxs-lookup"><span data-stu-id="93649-117">Labels to be used across the native views that encapsulate your custom views</span></span>

<span data-ttu-id="93649-118">Pour plus d'informations, consultez la rubrique [package MANIFEST Schema in JSON format](package_manifest_schema.md).</span><span class="sxs-lookup"><span data-stu-id="93649-118">For more information, see [Package Manifest Schema in JSON format](package_manifest_schema.md).</span></span>

## <a name="app-model"></a><span data-ttu-id="93649-119">Modèle d'application</span><span class="sxs-lookup"><span data-stu-id="93649-119">App Model</span></span>

<span data-ttu-id="93649-120">Le modèle d'application spécifie les fonctionnalités de l'action Kaizala, notamment:</span><span class="sxs-lookup"><span data-stu-id="93649-120">The App Model specifies the capabilities of the Kaizala Action including:</span></span>
*   <span data-ttu-id="93649-121">Modèle de données de l'objet Form à utiliser pour tirer parti des services d'agrégation Kaizala</span><span class="sxs-lookup"><span data-stu-id="93649-121">The data model for the Form object to be used to leverage the Kaizala Aggregation Services</span></span>
*   <span data-ttu-id="93649-122">Propriétés de l'objet Form</span><span class="sxs-lookup"><span data-stu-id="93649-122">Properties for the form object</span></span>
*   <span data-ttu-id="93649-123">Paramètres associés à l'objet Form</span><span class="sxs-lookup"><span data-stu-id="93649-123">Settings associated with the Form object</span></span>

<span data-ttu-id="93649-124">Pour plus d'informations, consultez la rubrique [schéma de modèle d'application au format JSON](appModel_schema.md).</span><span class="sxs-lookup"><span data-stu-id="93649-124">For more information, see [App Model Schema in JSON format](appModel_schema.md).</span></span>

## <a name="web-resources"></a><span data-ttu-id="93649-125">Ressources Web</span><span class="sxs-lookup"><span data-stu-id="93649-125">Web Resources</span></span>

<span data-ttu-id="93649-126">Comme mentionné ci-dessus, le package Kaizala doit inclure toutes les ressources référencées à l'intérieur du package.</span><span class="sxs-lookup"><span data-stu-id="93649-126">As mentioned above, the Kaizala package must include all the resources being referenced inside the package.</span></span> <span data-ttu-id="93649-127">Cela inclut toutes les ressources HTML, JavaScript, CSS et image.</span><span class="sxs-lookup"><span data-stu-id="93649-127">This includes all the HTML, JavaScript, CSS and image resources.</span></span>

<span data-ttu-id="93649-128">L'action Kaizala la plus simple est constituée de trois pages HTML qui s'affichent lorsque</span><span class="sxs-lookup"><span data-stu-id="93649-128">The most basic Kaizala Action consists of three HTML pages that are displayed when</span></span>
*   <span data-ttu-id="93649-129">L'action Kaizal est appelée à partir de la palette d'actions dans l'affichage de création d'application cliente</span><span class="sxs-lookup"><span data-stu-id="93649-129">The Kaizal Action is invoked from the Action Palette in the client app - Creation view</span></span>
*   <span data-ttu-id="93649-130">Un utilisateur tente de répondre à une instance de carte d'action publiée sur la toile de conversation dans l'affichage application client-réponse</span><span class="sxs-lookup"><span data-stu-id="93649-130">A user tries to respond to a Action card instance posted on the Chat Canvas in the client app - Response view</span></span>
*   <span data-ttu-id="93649-131">Un utilisateur tente d'afficher le résumé de toutes les réponses publiées pour une action spécifique-vue de synthèse</span><span class="sxs-lookup"><span data-stu-id="93649-131">A user tries to view the summary of all responses posted for a specific Action instace - Summary view</span></span>

<span data-ttu-id="93649-132">Pour interagir avec l'application cliente Kaizala, vous pouvez utiliser l' [API JavaScript KASClient. js](KASClient/README.md) que nous fournissons.</span><span class="sxs-lookup"><span data-stu-id="93649-132">To interact with the Kaizala client app, you can use the [KASClient.js JavaScript API](KASClient/README.md) that we provide.</span></span>


