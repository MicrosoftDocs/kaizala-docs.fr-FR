# <a name="kaizala-actions"></a><span data-ttu-id="f2e9e-101">Actions Kaizala</span><span class="sxs-lookup"><span data-stu-id="f2e9e-101">Kaizala Actions</span></span>

## <a name="overview"></a><span data-ttu-id="f2e9e-102">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f2e9e-102">Overview</span></span>
<span data-ttu-id="f2e9e-103">Actions Kaizala sont base « unités de travail » qui permettent aux utilisateurs d’obtenir leur travail dans un contexte à l’intérieur de Kaizala conversationnel.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-103">Kaizala Actions are basic 'units of work' that help users to get their work done within a conversational context inside Kaizala.</span></span> <span data-ttu-id="f2e9e-104">Certaines de ces Actions comme tâche, enquête, sondage, etc. sont expédié out-de-the-box.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-104">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box.</span></span> <span data-ttu-id="f2e9e-105">Ces Actions peuvent être découverts au sein de l’application Kaizala et peuvent être appelées dans une conversation à partir de la Palette de l’Action.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-105">These Actions can be discovered within the Kaizala app and can be invoked in a chat from the Action Palette.</span></span> <span data-ttu-id="f2e9e-106">[En savoir plus](https://support.office.com/en-us/article/Kaizala-Actions-1EACC59A-DD14-43E9-B6B0-3C78773D5496).</span><span class="sxs-lookup"><span data-stu-id="f2e9e-106">[Read More](https://support.office.com/en-us/article/Kaizala-Actions-1EACC59A-DD14-43E9-B6B0-3C78773D5496).</span></span>

<span data-ttu-id="f2e9e-107">Bien que les besoins de chaque organisation varient et ils nécessiterait fonctionnalités seraient très différentes de besoins de toute autre organisation.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-107">We understand that the needs of every organization vary and they would require functionalities that would be very different from the needs of any other organization.</span></span> <span data-ttu-id="f2e9e-108">Par conséquent, Kaizala permet le développement d’Actions personnalisées Kaizala qui peuvent être effectuées par des développeurs tiers 3e.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-108">Hence Kaizala enables development of custom Kaizala Actions that can be done by 3rd Party developers.</span></span> <span data-ttu-id="f2e9e-109">Ces Actions personnalisées peuvent être déployées sur un groupe, mappé au sein d’un contexte d’organisation.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-109">These custom Actions can be deployed to a group, mapped within an organization context.</span></span></br>

<span data-ttu-id="f2e9e-110">Toutes les Actions qui sont publiées sur un ensemble d’utilisateurs peuvent être appelées par leur Action avait été ajoutée à tous les groupes.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-110">All Actions that are published to a set of users can be invoked by them on any groups that Action had been added to.</span></span> 

> <span data-ttu-id="f2e9e-111">**Remarque :** Actions personnalisées peuvent uniquement être ajoutées aux groupes de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-111">**Note:** Custom Actions can only be added to organization groups.</span></span>

> <span data-ttu-id="f2e9e-112">**Remarque :** [Portail de gestion Kaizala](https://manage.kaiza.la) est la passerelle pour tout développement, test et publication de nouvelles Actions Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-112">**Note :** [Kaizala Management Portal](https://manage.kaiza.la) is the gateway for all development, testing and publishing of new Kaizala Actions.</span></span>

## <a name="understanding-kaizala-action"></a><span data-ttu-id="f2e9e-113">Présentation Kaizala Action</span><span class="sxs-lookup"><span data-stu-id="f2e9e-113">Understanding Kaizala Action</span></span>

<span data-ttu-id="f2e9e-114">Une Action Kaizala contient actuellement quatre différentes vues qui peuvent être définis comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f2e9e-114">A Kaizala Action currently contains four different views that can be defined as below:</span></span>

* <span data-ttu-id="f2e9e-115">**Mode Création** lorsqu’une Action est appelée à partir de la palette</span><span class="sxs-lookup"><span data-stu-id="f2e9e-115">A **creation view** when an Action is invoked from the palette</span></span>
* <span data-ttu-id="f2e9e-116">Une **vue de carte** qui apparaît sur la zone de conversation lorsqu’une instance de l’Action est envoyé</span><span class="sxs-lookup"><span data-stu-id="f2e9e-116">A **card view** that appears on the chat canvas when an instance of the Action is sent</span></span>
* <span data-ttu-id="f2e9e-117">Une **vue répondeur** pour répondre à l’Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="f2e9e-117">A **responder view** for users to respond to the Kaizala Action</span></span>
* <span data-ttu-id="f2e9e-118">Un **affichage de synthèse** pour afficher les réponses agrégées</span><span class="sxs-lookup"><span data-stu-id="f2e9e-118">A **summary view** to view aggregated responses</span></span>

<span data-ttu-id="f2e9e-119">Par exemple, dans Out-of-Box(OOB) Kaizala enquête Action :</span><span class="sxs-lookup"><span data-stu-id="f2e9e-119">For instance, in Out-of-Box(OOB) Kaizala Survey Action:</span></span>

| <span data-ttu-id="f2e9e-120">Vue</span><span class="sxs-lookup"><span data-stu-id="f2e9e-120">View</span></span> | <span data-ttu-id="f2e9e-121">Exemple de vue dans Action d’enquête prêtes à l’emploi</span><span class="sxs-lookup"><span data-stu-id="f2e9e-121">Sample view in OOB Survey Action</span></span> |
|------|----------------------------------|
| <span data-ttu-id="f2e9e-122">Mode Création</span><span class="sxs-lookup"><span data-stu-id="f2e9e-122">Creation view</span></span>| ![](../images/CreationView.png)|
| <span data-ttu-id="f2e9e-123">Affichage de carte</span><span class="sxs-lookup"><span data-stu-id="f2e9e-123">Card view</span></span> |![](../images/Chatcard.png) |
| <span data-ttu-id="f2e9e-124">Vue répondeur</span><span class="sxs-lookup"><span data-stu-id="f2e9e-124">Responder view</span></span> |![](../images/ResponseView.png) |
| <span data-ttu-id="f2e9e-125">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="f2e9e-125">Summary view</span></span> |![](../images/SummaryView.png) |

<span data-ttu-id="f2e9e-126">Dans Actions personnalisées, vous pouvez créer des affichages personnalisés qui correspondent aux au-dessus de vues.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-126">In custom Actions, you can create custom views that correspond to above views.</span></span>

## <a name="create-a-new-kaizala-action"></a><span data-ttu-id="f2e9e-127">Créer une nouvelle Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="f2e9e-127">Create a new Kaizala Action</span></span>
<span data-ttu-id="f2e9e-128">Vous pouvez créer de nouvelles Actions Kaizala qui tirent parti de réseau de personnes de Kaizala et les fonctionnalités mobiles pour créer des expériences de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="f2e9e-128">You can create new Kaizala Actions that leverage Kaizala’s people network and mobile capabilities to create compelling experiences in the following ways:</span></span>

* <span data-ttu-id="f2e9e-129">**Concevoir** une nouvelle Action Kaizala via le portail de gestion Kaizala - vous pouvez créer une Action personnalisée de Kaizala par le biais de l’interface du Concepteur d’Action en s’appuyant sur les modèles d’Action existantes.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-129">**Design** a new Kaizala Action through the Kaizala Management Portal - You can design a custom Kaizala Action through the Action Designer interface by building on the existing Action templates.</span></span> [<span data-ttu-id="f2e9e-130">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="f2e9e-130">Read More</span></span>](https://support.office.com/en-us/article/Kaizala-Actions-1eacc59a-dd14-43e9-b6b0-3c78773d5496?ui=en-US&rs=en-US&ad=US)
* <span data-ttu-id="f2e9e-131">**Développer** une nouvelle Action Kaizala - vous pouvez créer des Actions Kaizala nouveau complexes qui fournissent des fonctionnalités personnalisées à l’aide de technologies web tels que HTML, CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-131">**Develop** a new Kaizala Action - You can create complex new Kaizala Actions that provide custom functionality using web technologies like HTML, CSS and JavaScript.</span></span> <span data-ttu-id="f2e9e-132">Suivez les liens ci-dessous pour en savoir plus sur les différentes étapes du développement d’une Action Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-132">Follow the links below to learn about various stages of developement of a Kaizala Action.</span></span>
    *   [<span data-ttu-id="f2e9e-133">Anatomie d’un package de l’Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="f2e9e-133">Anatomy of a Kaizala Action package</span></span>](anatomy.md)
    *   [<span data-ttu-id="f2e9e-134">Mise en route</span><span class="sxs-lookup"><span data-stu-id="f2e9e-134">Get Started</span></span>](get_started.md)
    *   [<span data-ttu-id="f2e9e-135">Développer</span><span class="sxs-lookup"><span data-stu-id="f2e9e-135">Develop</span></span>](develop.md)
    *   [<span data-ttu-id="f2e9e-136">Publier</span><span class="sxs-lookup"><span data-stu-id="f2e9e-136">Publish</span></span>](publish.md)

<span data-ttu-id="f2e9e-137">Toutes les Actions Kaizala doivent respecter les [instructions](validation.md) pour pouvoir être publiés sur les clients Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f2e9e-137">All Kaizala Actions need to adhere to the [guidelines](validation.md) to be eligible to be published to Kaizala clients.</span></span>

## <a name="build-your-first-kaizala-action"></a><span data-ttu-id="f2e9e-138">Créer votre première Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="f2e9e-138">Build your first Kaizala Action</span></span>

<span data-ttu-id="f2e9e-139">Vous pouvez essayer de création de votre première Action Kaizala en suivant notre simple [didacticiel](tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="f2e9e-139">You can try out building your first Kaizala Action by following our simple [tutorial](tutorial.md)</span></span>

## <a name="download-sample-action-packages"></a><span data-ttu-id="f2e9e-140">Téléchargez des exemples de Packages de Action</span><span class="sxs-lookup"><span data-stu-id="f2e9e-140">Download Sample Action Packages</span></span>

*  [<span data-ttu-id="f2e9e-141">Exemples d’Actions</span><span class="sxs-lookup"><span data-stu-id="f2e9e-141">Sample Actions</span></span>](https://manage.kaiza.la/MiniApps/DownloadSDK)