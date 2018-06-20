# <a name="anatomy-of-a-kaizala-action-package"></a><span data-ttu-id="236fd-101">Anatomie d’un package de l’Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="236fd-101">Anatomy of a Kaizala Action package</span></span>

<span data-ttu-id="236fd-102">Un package Kaizala Action est un fichier ZIP régulière qui n’est pas protégé par mot de passe et ne peut pas dépasser 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="236fd-102">A Kaizala Action package is a regular ZIP file which is not password protected and has a maximum size of 1MB.</span></span> <span data-ttu-id="236fd-103">Les ressources dans le package sont à la racine du fichier zip et non pas dans une structure de répertoire.</span><span class="sxs-lookup"><span data-stu-id="236fd-103">The resources in the package are at the root of the zip file and not in any directory structure.</span></span> <span data-ttu-id="236fd-104">Les ressources ne peuvent pas également faire référence à des ressources externes, autres que celles présentes dans le package.</span><span class="sxs-lookup"><span data-stu-id="236fd-104">The resources also cannot reference any external resources other than those present in the package.</span></span>

<span data-ttu-id="236fd-105">Les composants de base d’un package Kaizala Action sont</span><span class="sxs-lookup"><span data-stu-id="236fd-105">The basic components of a Kaizala Action package are</span></span> 
*   <span data-ttu-id="236fd-106">Un fichier manifeste au format JSON</span><span class="sxs-lookup"><span data-stu-id="236fd-106">A manifest file in JSON format</span></span>
*   <span data-ttu-id="236fd-107">Un modèle d’application pour votre Action Kaizala au format JSON</span><span class="sxs-lookup"><span data-stu-id="236fd-107">An app model for your Kaizala Action in JSON format</span></span>
*   <span data-ttu-id="236fd-108">Ressources Web qui constituent votre Action Kaizala - HTML, JS, CSS et fichiers image</span><span class="sxs-lookup"><span data-stu-id="236fd-108">Web resources that constitute your Kaizala Action - HTML, JS, CSS and image files</span></span>

## <a name="package-manifest"></a><span data-ttu-id="236fd-109">Manifeste du package</span><span class="sxs-lookup"><span data-stu-id="236fd-109">Package Manifest</span></span>

<span data-ttu-id="236fd-110">Le manifeste spécifie les paramètres de l’Action Kaizala, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="236fd-110">The manifest specifies settings of the Kaizala Action, such as the following:</span></span>
*   <span data-ttu-id="236fd-111">De l’Action nom complet, description, ID, version et icône Action.</span><span class="sxs-lookup"><span data-stu-id="236fd-111">The Action's display name, description, ID, version, and Action icon.</span></span>
*   <span data-ttu-id="236fd-112">Différentes vues qui définissent votre Action et les mapper à leur point invokation respectifs</span><span class="sxs-lookup"><span data-stu-id="236fd-112">Various views that define your Action and mapping them to their respective invokation points</span></span>
    * <span data-ttu-id="236fd-113">Un affichage Création lorsqu’une Action est appelée à partir de la palette</span><span class="sxs-lookup"><span data-stu-id="236fd-113">A creation view when an Action is invoked from the palette</span></span>
    * <span data-ttu-id="236fd-114">Une vue de carte qui apparaît dans la zone de conversation lorsqu’une instance de l’Action est envoyée</span><span class="sxs-lookup"><span data-stu-id="236fd-114">A card view that appears on the chat canvas when an instance of the Action is sent</span></span>
    * <span data-ttu-id="236fd-115">Une vue répondeur pour les utilisateurs répondre à l’Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="236fd-115">A responder view for users to respond to the Kaizala Action</span></span>
    * <span data-ttu-id="236fd-116">Un résumé Affichage agrégé réponses</span><span class="sxs-lookup"><span data-stu-id="236fd-116">A summary view to view aggregated responses</span></span>
*   <span data-ttu-id="236fd-117">Étiquettes pour être utilisés dans les affichages natives qui encapsulent les vues personnalisées</span><span class="sxs-lookup"><span data-stu-id="236fd-117">Labels to be used across the native views that encapsulate your custom views</span></span>

<span data-ttu-id="236fd-118">Pour plus d’informations, voir [Schéma de manifeste de Package au format JSON](package_manifest_schema.md).</span><span class="sxs-lookup"><span data-stu-id="236fd-118">For more information, see [Package Manifest Schema in JSON format](package_manifest_schema.md).</span></span>

## <a name="app-model"></a><span data-ttu-id="236fd-119">Modèle d’application</span><span class="sxs-lookup"><span data-stu-id="236fd-119">App Model</span></span>

<span data-ttu-id="236fd-120">Le modèle d’application spécifie les fonctionnalités de l’Action Kaizala, y compris :</span><span class="sxs-lookup"><span data-stu-id="236fd-120">The App Model specifies the capabilities of the Kaizala Action including:</span></span>
*   <span data-ttu-id="236fd-121">Le modèle de données pour l’objet de formulaire à utiliser pour mettre à profit les Services d’agrégation Kaizala</span><span class="sxs-lookup"><span data-stu-id="236fd-121">The data model for the Form object to be used to leverage the Kaizala Aggregation Services</span></span>
*   <span data-ttu-id="236fd-122">Propriétés de l’objet de formulaire</span><span class="sxs-lookup"><span data-stu-id="236fd-122">Properties for the form object</span></span>
*   <span data-ttu-id="236fd-123">Paramètres associés à l’objet de formulaire</span><span class="sxs-lookup"><span data-stu-id="236fd-123">Settings associated with the Form object</span></span>

<span data-ttu-id="236fd-124">Pour plus d’informations, voir [Schéma de modèle d’application au format JSON](appModel_schema.md).</span><span class="sxs-lookup"><span data-stu-id="236fd-124">For more information, see [App Model Schema in JSON format](appModel_schema.md).</span></span>

## <a name="web-resources"></a><span data-ttu-id="236fd-125">Ressources Web</span><span class="sxs-lookup"><span data-stu-id="236fd-125">Web Resources</span></span>

<span data-ttu-id="236fd-126">Comme mentionné ci-dessus, le package Kaizala doit inclure toutes les ressources référencés dans le package.</span><span class="sxs-lookup"><span data-stu-id="236fd-126">As mentioned above, the Kaizala package must include all the resources being referenced inside the package.</span></span> <span data-ttu-id="236fd-127">Cela inclut toutes les ressources HTML, JavaScript, CSS et image.</span><span class="sxs-lookup"><span data-stu-id="236fd-127">This includes all the HTML, JavaScript, CSS and image resources.</span></span>

<span data-ttu-id="236fd-128">L’Action Kaizala plus élémentaire se compose de trois pages HTML qui sont affichées lorsque</span><span class="sxs-lookup"><span data-stu-id="236fd-128">The most basic Kaizala Action consists of three HTML pages that are displayed when</span></span>
*   <span data-ttu-id="236fd-129">L’Action Kaizal est appelée à partir de la Palette de l’Action dans l’application cliente - mode Création</span><span class="sxs-lookup"><span data-stu-id="236fd-129">The Kaizal Action is invoked from the Action Palette in the client app - Creation view</span></span>
*   <span data-ttu-id="236fd-130">Un utilisateur tente de répondre à une instance de carte Action publiée sur la zone de conversation dans l’application cliente - affichage de réponse</span><span class="sxs-lookup"><span data-stu-id="236fd-130">A user tries to respond to a Action card instance posted on the Chat Canvas in the client app - Response view</span></span>
*   <span data-ttu-id="236fd-131">Un utilisateur essaie d’afficher le résumé de toutes les réponses validée pour une instance d’Action spécifique - affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="236fd-131">A user tries to view the summary of all responses posted for a specific Action instace - Summary view</span></span>

<span data-ttu-id="236fd-132">Pour interagir avec l’application de client Kaizala, vous pouvez utiliser l' [Interface API JavaScript KASClient.js](KASClient/README.md) que nous fournissons.</span><span class="sxs-lookup"><span data-stu-id="236fd-132">To interact with the Kaizala client app, you can use the [KASClient.js JavaScript API](KASClient/README.md) that we provide.</span></span>


