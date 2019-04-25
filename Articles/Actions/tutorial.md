# <a name="practice-tutorial-creating-a-new-kaizala-action"></a><span data-ttu-id="d5b68-101">Didacticiel pratique: création d'une action Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-101">Practice Tutorial: Creating a new Kaizala Action</span></span> 

## <a name="overview"></a><span data-ttu-id="d5b68-102">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="d5b68-102">Overview</span></span> 
<span data-ttu-id="d5b68-103">Dans ce didacticiel, nous allons créer une action Kaizala personnalisée à l'aide de l'infrastructure d'action extensible fournie par la plateforme Kaizala.</span><span class="sxs-lookup"><span data-stu-id="d5b68-103">In this tutorial, we will create a custom Kaizala Action utilizing the extensible Action framework provided by the Kaizala platform.</span></span>

<span data-ttu-id="d5b68-104">Nous allons créer une action «Ask Feedback» qui permettra aux utilisateurs de Kaizala de demander des commentaires d'autres utilisateurs en termes de évaluations de 1 à 5 étoiles sur les questions posées, ainsi que les commentaires qu'ils aimeraient fournir.</span><span class="sxs-lookup"><span data-stu-id="d5b68-104">We will create an “Ask Feedback” Action which will allow Kaizala users to ask for feedback from other users in terms of 1-to-5 star ratings on questions asked – along with any comments they would like to provide.</span></span>  

<span data-ttu-id="d5b68-105">Vous pouvez télécharger des exemples d'actions Kaizala à partir de [ici](https://manage.kaiza.la/MiniApps/DownloadSDK).</span><span class="sxs-lookup"><span data-stu-id="d5b68-105">You can download sample Kaizala Action packages from [here](https://manage.kaiza.la/MiniApps/DownloadSDK).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="d5b68-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="d5b68-106">Pre-requisites</span></span> 
* <span data-ttu-id="d5b68-107">Un smartphone (Android/iOS) sur lequel l'application Kaizala est installée</span><span class="sxs-lookup"><span data-stu-id="d5b68-107">A smartphone (Android/iOS) with Kaizala app installed</span></span> 
* <span data-ttu-id="d5b68-108">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="d5b68-108">An Office365 Account</span></span> 
* <span data-ttu-id="d5b68-109">Accès à un éditeur HTML/JS (bloc-notes/Visual Studio code/etc.)</span><span class="sxs-lookup"><span data-stu-id="d5b68-109">Access to an HTML/JS editor (notepad/Visual Studio Code/etc.)</span></span> 

## <a name="steps-to-create-a-sample-action"></a><span data-ttu-id="d5b68-110">Étapes de création d'un exemple d'action</span><span class="sxs-lookup"><span data-stu-id="d5b68-110">Steps to create a sample Action</span></span>

*   <span data-ttu-id="d5b68-111">**Étape 1:** Créer un répertoire pour votre package d'action</span><span class="sxs-lookup"><span data-stu-id="d5b68-111">**Step 1:** Create a new directory for your Action package</span></span>  
    * <span data-ttu-id="d5b68-112">Créez un nouveau répertoire sur votre bureau & nom «SampleAction».</span><span class="sxs-lookup"><span data-stu-id="d5b68-112">Create a new directory on your desktop & name it “SampleAction”</span></span> 
    * <span data-ttu-id="d5b68-113">Placez tous les fichiers suivants dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="d5b68-113">Place all the subsequent files in this directory</span></span>

*   <span data-ttu-id="d5b68-114">**Étape 2:** Définir un modèle de données pour votre action</span><span class="sxs-lookup"><span data-stu-id="d5b68-114">**Step 2:** Define a data model for your Action</span></span> 
    * <span data-ttu-id="d5b68-115">Tout d'abord, nous devons définir le modèle de données qui sera utilisé dans notre action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d5b68-115">First, we need to define the data model which will be used in our custom Action</span></span> 
    * <span data-ttu-id="d5b68-116">Les actions Kaizala sont des modèles de données basés sur des formulaires.</span><span class="sxs-lookup"><span data-stu-id="d5b68-116">The Kaizala Actions are currently form based data models.</span></span> <span data-ttu-id="d5b68-117">Nous devons d'abord définir les «questions» à inclure dans notre formulaire.</span><span class="sxs-lookup"><span data-stu-id="d5b68-117">So, we will first need to define the ‘questions’ we need to include in our form.</span></span> 
    * <span data-ttu-id="d5b68-118">Étant donné qu'il s'agit d'une action «Ask Feedback», nous prévoyons d'utiliser deux éléments de données</span><span class="sxs-lookup"><span data-stu-id="d5b68-118">Since this is a “Ask Feedback” action – we will plan to use two pieces of data</span></span> 
        * <span data-ttu-id="d5b68-119">Notation numérique (valeur 1 à 5)</span><span class="sxs-lookup"><span data-stu-id="d5b68-119">Numeric rating (value 1 to 5)</span></span> 
        * <span data-ttu-id="d5b68-120">Commentaire/commentaire textuel, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="d5b68-120">Comment/Verbatim feedback if any</span></span>  

    *   <span data-ttu-id="d5b68-121">L'infrastructure des formulaires Kaizala prend en charge les types de questions suivants:</span><span class="sxs-lookup"><span data-stu-id="d5b68-121">Kaizala Forms infrastructure supports below question types:</span></span>

        | <span data-ttu-id="d5b68-122">Type de question</span><span class="sxs-lookup"><span data-stu-id="d5b68-122">Question Type</span></span> | <span data-ttu-id="d5b68-123">Description</span><span class="sxs-lookup"><span data-stu-id="d5b68-123">Description</span></span> |
        | :---: | :---: | 
        | <span data-ttu-id="d5b68-124">SingleSelect</span><span class="sxs-lookup"><span data-stu-id="d5b68-124">SingleSelect</span></span> | <span data-ttu-id="d5b68-125">Question à choix unique avec options</span><span class="sxs-lookup"><span data-stu-id="d5b68-125">Single choice question with options</span></span> |
        | <span data-ttu-id="d5b68-126">MultiSelect</span><span class="sxs-lookup"><span data-stu-id="d5b68-126">MultiSelect</span></span> | <span data-ttu-id="d5b68-127">Questions à choix multiples avec options</span><span class="sxs-lookup"><span data-stu-id="d5b68-127">Multiple choice question with options</span></span> | 
        | <span data-ttu-id="d5b68-128">Text</span><span class="sxs-lookup"><span data-stu-id="d5b68-128">Text</span></span> | <span data-ttu-id="d5b68-129">Question avec une réponse en texte brut</span><span class="sxs-lookup"><span data-stu-id="d5b68-129">Question with a plain text answer</span></span> |
        | <span data-ttu-id="d5b68-130">Numérique</span><span class="sxs-lookup"><span data-stu-id="d5b68-130">Numeric</span></span> | <span data-ttu-id="d5b68-131">Question avec une réponse numérique</span><span class="sxs-lookup"><span data-stu-id="d5b68-131">Question with a numeric answer</span></span> | 
        | <span data-ttu-id="d5b68-132">Emplacement</span><span class="sxs-lookup"><span data-stu-id="d5b68-132">Location</span></span> | <span data-ttu-id="d5b68-133">Question avec une réponse de localisation</span><span class="sxs-lookup"><span data-stu-id="d5b68-133">Question with a location answer</span></span> | 
        | <span data-ttu-id="d5b68-134">DateTime
</span><span class="sxs-lookup"><span data-stu-id="d5b68-134">DateTime</span></span> | <span data-ttu-id="d5b68-135">Question avec réponse DateTime</span><span class="sxs-lookup"><span data-stu-id="d5b68-135">Question with DateTime answer</span></span> | 
        | <span data-ttu-id="d5b68-136">Image</span><span class="sxs-lookup"><span data-stu-id="d5b68-136">Image</span></span> | <span data-ttu-id="d5b68-137">Question avec une image comme réponse</span><span class="sxs-lookup"><span data-stu-id="d5b68-137">Question with a picture as an answer</span></span> | 
    

    * <span data-ttu-id="d5b68-138">Pour nos deux questions, nous allons utiliser le type de question «Numeric» & «Text» pour les commentaires & de numéro de classement</span><span class="sxs-lookup"><span data-stu-id="d5b68-138">For our two questions we will use Question Type of 'Numeric' & 'Text' for Rating number & comments respectively</span></span> 
        * <span data-ttu-id="d5b68-139">Créez un fichier appelé «appModel. JSON» et placez le contenu suivant dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d5b68-139">Create a new file called “appModel.json” and place the following content in the file.</span></span> <span data-ttu-id="d5b68-140">Le fichier contient les deux questions indiquées dans Order</span><span class="sxs-lookup"><span data-stu-id="d5b68-140">The file contains the two questions listed in order</span></span> 
        `````
        { 
            "questions": [{ 
                    "title": "Rating", 
                    "type": "Numeric" 
                }, 
                { 
                    "title": "Comments", 
                    "type": "Text" 
                } 
            ], 
            "title": "Ask Feedback", 
            "visibility": "All", 
            "isAnonymous": false, 
            "isResponseAppended": false 
        } 
        `````
        * <span data-ttu-id="d5b68-141">Remarque: le code ci-dessus contient également des métadonnées supplémentaires qui seront abordées plus loin (hors de portée pour cette session)</span><span class="sxs-lookup"><span data-stu-id="d5b68-141">Note: Above code also contains additional metadata we will learn about later (out of scope for this session)</span></span> 
        * <span data-ttu-id="d5b68-142">Enregistrer le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-142">Save the file</span></span>
        
*   <span data-ttu-id="d5b68-143">**Étape 3:** Définir un affichage pour la création de la demande de commentaires</span><span class="sxs-lookup"><span data-stu-id="d5b68-143">**Step 3:** Define a view for creating the request for feedback</span></span>  
    *   <span data-ttu-id="d5b68-144">Nous allons maintenant créer un nouveau fichier HTML qui sera utilisé pour créer de nouvelles instances de notre action Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-144">We will now create a new HTML file which will be used to create new instances of  our Kaizala Action</span></span> 
    *   <span data-ttu-id="d5b68-145">Il s'agit de l'affichage qui est appelé lorsque l'icône est exploitée à partir de la palette.</span><span class="sxs-lookup"><span data-stu-id="d5b68-145">This is the view that is invoked when the icon is tapped from the palette.</span></span> <span data-ttu-id="d5b68-146">Dans cet affichage, nous aimerions leur demander ce qu'ils aimeraient envoyer.</span><span class="sxs-lookup"><span data-stu-id="d5b68-146">In this view, we would like to ask them what they would like feedback on.</span></span> 
    * <span data-ttu-id="d5b68-147">Créez un fichier nommé «CreationView. html» et placez le code HTML ci-dessous dans le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-147">Create a new file called “CreationView.html” and place the below HTML in the file</span></span> 
        `````
        <html> 
         
        <head> 
        </head> 
         
        <body onload="onCreatePageLoad()"> 
            <br/> <br/> 
            <div> 
                <p>What would you like feedback on?</p> 
                <br/> <br/> 
                <input type="text" name="description" id="description" placeholder="Enter question text here" value=""> 
            </div> 
            <br/> <br/> 
            <div> 
                <input type="submit" name="submit" value="Submit" onclick="submitData()"> 
            </div> 
        </body> 
         
        </html> 
        `````
    *   <span data-ttu-id="d5b68-148">Enregistrer le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-148">Save the file</span></span> 
*   <span data-ttu-id="d5b68-149">**Étape 4:** Inclure le kit de développement logiciel (SDK) Kaizala Forms JS</span><span class="sxs-lookup"><span data-stu-id="d5b68-149">**Step 4:** Include the Kaizala Forms JS SDK</span></span> 
    * <span data-ttu-id="d5b68-150">Pour faciliter l'utilisation de l'infrastructure de formulaires par les développeurs, Kaizala fournit une bibliothèque de wrappers JavaScript que vous pouvez inclure dans vos actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d5b68-150">To make it easy for developers to leverage the Forms Infrastructure, Kaizala provides a JavaScript wrapper library that you can include in your custom Actions</span></span> 
    * <span data-ttu-id="d5b68-151">Téléchargez le fichier sous & Placez-le dans le même répertoire que votre datamodel. JSON et CreationView. html</span><span class="sxs-lookup"><span data-stu-id="d5b68-151">Download the file below & place it in the same directory as your datamodel.json and CreationView.html</span></span> 
      *   <span data-ttu-id="d5b68-152">[Kit de développement logiciel (SDK) Kaizala Forms js ](https://manage.kaiza.la/MiniApps/downloadSDK).</span><span class="sxs-lookup"><span data-stu-id="d5b68-152">[Kaizala Forms JS SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span></span> [<span data-ttu-id="d5b68-153">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="d5b68-153">Read more</span></span>](KASClient/README.md)
 
 
 
 
*   <span data-ttu-id="d5b68-154">**Étape 5:** Utiliser le kit de développement logiciel (SDK) Kaizala Forms JS pour envoyer le formulaire</span><span class="sxs-lookup"><span data-stu-id="d5b68-154">**Step 5:** Use the Kaizala Forms JS SDK to submit form</span></span>   
    * <span data-ttu-id="d5b68-155">Ajoutez l'extrait de code suivant dans <head> l'élément de votre fichier «CreationView. html» pour faire référence au kit de développement logiciel (SDK) de Kaizala FORMs js</span><span class="sxs-lookup"><span data-stu-id="d5b68-155">Add the following code snippet in the <head> element of your “CreationView.html” to refer to the Kaizala Forms JS SDK</span></span> 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * <span data-ttu-id="d5b68-156">À présent, lorsque l'utilisateur clique sur envoyer, nous devons vérifier qu'il a entré une question pour demander des commentaires sur – et créer l'instance de formulaire</span><span class="sxs-lookup"><span data-stu-id="d5b68-156">Now, when the user clicks submit, we need to verify that he has entered a question to ask feedback on – and create the Form Instance</span></span>  
    * <span data-ttu-id="d5b68-157">Nous devons également instancier le formulaire au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="d5b68-157">We also need to instantiate the form on page load.</span></span> <span data-ttu-id="d5b68-158">Ajoutez l'extrait de code JavaScript suivant à votre fichier «CreationView. html <head> » à l'intérieur de l'élément</span><span class="sxs-lookup"><span data-stu-id="d5b68-158">Add the following JavaScript snippet to your “CreationView.html” inside the <head> element</span></span> 
        `````
            <script type="text/javascript"> 
                var _form; // type: KASForm
         
                // Below will be called on onload of CreationView.html 
                function onCreatePageLoad() { 
                    KASClient.Form.initFormAsync (function (form, error) { 
                        if (error != null) { 
                            showAlert("Error:initFormAsync:" + error); 
                            return; 
                        } 
                        _form = form; 
                    }); 
                } 
         
                function submitData() {
                    var description = document.getElementById("description").value; 
                    if (description == null || description == "") { 
                        KASClient.App.showNativeErrorMessage("Please enter the details for what you would like feedback on."); 
                    } else { 
                        // Set the description to form title 
                        _form.title = description; 
         
                        // Finally send the request 
                        KASClient.Form.submitFormRequest(_form); 
                    } 
                } 
            </script>
        `````

    *   <span data-ttu-id="d5b68-159">Enregistrer le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-159">Save the file</span></span>

*   <span data-ttu-id="d5b68-160">**Étape 6:** Créer le manifeste du package d'action</span><span class="sxs-lookup"><span data-stu-id="d5b68-160">**Step 6:** Create the Action package manifest</span></span>   
    *   <span data-ttu-id="d5b68-161">Maintenant que nous avons un semblance de ce que nous souhaitons obtenir et créé une vue, nous allons maintenant créer le fichier manifeste de package qui se rapporte à ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="d5b68-161">Now that we have a semblance of what we want to achieve and successfully created a view – we will now create the package manifest file that refers to these files.</span></span> 
    * <span data-ttu-id="d5b68-162">Le fichier manifeste de package fournit des informations essentielles sur la plateforme Kaizala pour qu'il reconnaisse et exécute votre action Kaizala personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d5b68-162">Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span> 
    * <span data-ttu-id="d5b68-163">Nous allons créer un manifeste de package et spécifier les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d5b68-163">We will create a package manifest and specify the following things:</span></span> 
        * <span data-ttu-id="d5b68-164">Nom d'affichage de votre action Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-164">Display name for your Kaizala Action</span></span> 
        * <span data-ttu-id="d5b68-165">ID personnalisé pour l'action</span><span class="sxs-lookup"><span data-stu-id="d5b68-165">Custom Id for the Action</span></span> 
        * <span data-ttu-id="d5b68-166">Mappage de la vue de création à notre page CreationView. html</span><span class="sxs-lookup"><span data-stu-id="d5b68-166">Mapping of the creation view to our CreationView.html page</span></span> 

    * <span data-ttu-id="d5b68-167">Avant d'avoir besoin d'une icône pour le package d'action.</span><span class="sxs-lookup"><span data-stu-id="d5b68-167">Before that we will need an icon for the Action package.</span></span> <span data-ttu-id="d5b68-168">Téléchargez le [fichier d'icône](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & enregistrez-le sous le titre Icon. png dans le même dossier que les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="d5b68-168">Download the [icon file](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & save it as icon.png in the same folder as the other files.</span></span>

    * <span data-ttu-id="d5b68-169">Créez un fichier appelé «Package. JSON» et ajoutez un extrait de code suivant au fichier.</span><span class="sxs-lookup"><span data-stu-id="d5b68-169">Create a new file called “package.json” and add following snippet to the file.</span></span> <span data-ttu-id="d5b68-170">Vérifiez que vous modifiez l'ID de sorte que votre action soit unique/distincte</span><span class="sxs-lookup"><span data-stu-id="d5b68-170">Ensure that you edit the id to make your Action unique/distinct</span></span> 
        `````
        { 
            "id": "com.microsoft.mobile.kaizala.swads.FeedbackSample", 
            "schemaVersion": 1, 
            "version": 1,
            "minorVersion": 1,
            "providerName": "Microsoft Inc.", 
            "displayName": "Ask Feedback", 
            "description": "Custom action to collect feedback.", 
            "icon": "icon.png", 
            "appModel": "appModel.json", 
            "views": { 
                "CreationView": { 
                    "labelHeader": "Feedback requested", 
                    "sourceLocation": "CreationView.html" 
                } 
            } 
        }
        `````
    * <span data-ttu-id="d5b68-171">Vous pouvez configurer la carte qui apparaît sur la zone de conversation de conversation Kaizala en spécifiant les chaînes dans le manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="d5b68-171">You can configure the card that appears on Kaizala chat canvas by specifying the strings in the package manifest.</span></span>  
    * <span data-ttu-id="d5b68-172">Modifiez l'objet «views» dans votre manifeste de package pour qu'il corresponde à l'extrait de code suivant:</span><span class="sxs-lookup"><span data-stu-id="d5b68-172">Modify the “Views” object in you package manifest to match the below snippet:</span></span>
        `````
        "views": { 
                    "CreationView": { 
                        "labelHeader": "Feedback requested", 
                        "sourceLocation": "CreationView.html"            
                    }, 
                    "ChatCanvasCardView": { 
                        "labelResponded": "You have provided feedback.", 
                        "labelRespondToForm": "PROVIDE FEEDBACK", 
                        "isResponseEditable": true 
                    } 
        }   
        `````
    * <span data-ttu-id="d5b68-173">Enregistrer le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-173">Save the file</span></span>

*   <span data-ttu-id="d5b68-174">**Étape 7:** Créer l'affichage des réponses</span><span class="sxs-lookup"><span data-stu-id="d5b68-174">**Step 7:** Create the response view</span></span>   
    * <span data-ttu-id="d5b68-175">À présent, nous allons créer l'affichage qui s'affiche pour Kaizala les utilisateurs qui répondent à une instance de notre action.</span><span class="sxs-lookup"><span data-stu-id="d5b68-175">Now we will create the view that appears to Kaizala users responding to an instance of our action</span></span> 
    * <span data-ttu-id="d5b68-176">Créer un nouveau fichier appeler ResponseView. html et insérer l'extrait de code ci-dessous dans le fichier</span><span class="sxs-lookup"><span data-stu-id="d5b68-176">Create a new file call ResponseView.html and insert the below snippet in the file</span></span> 
    * <span data-ttu-id="d5b68-177">Nous allons effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="d5b68-177">We will do the following</span></span> 
        * <span data-ttu-id="d5b68-178">Ajouter une case d'option pour l'évaluation</span><span class="sxs-lookup"><span data-stu-id="d5b68-178">Add radio button selection for the rating</span></span> 
        * <span data-ttu-id="d5b68-179">Préparer un objet de réponse à un formulaire et du code pour envoyer le formulaire</span><span class="sxs-lookup"><span data-stu-id="d5b68-179">Prepare a form response object and code to submit the form</span></span> 
        ````` 
            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script> 
                    var _form; // type: KASForm
                    var _myFormResponses; // type: KASFormResponse[]
             
                    // Below will be called on onload of ResponseView.html 
                    function onResponsePageLoad() { 
                        KASClient.Form.getFormAsync(function (form, error) { 
                            if (error != null) { 
                                KASClient.App.showNativeErrorMessage("Error:getFormAsync:" + error); 
                                return; 
                            } 
                            _form = form; 
                            
                            // Document title would be the form title
                            document.getElementById("title").innerHTML = _form.title;
                            
                            KASClient.Form.getMyFormResponsesAsync(function (responses, error) { 
                                if (error != null) { 
                                    KASClient.App.showNativeErrorMessage("Error:getMyFormResponsesAsync:" + error); 
                                    return; 
                                } 
                                _myFormResponses = responses;
                                
                                // Render previous response, if any
                                if (isCurrentUserResponded()) {
                                    var rating = _myFormResponses[0].questionToAnswerMap["0"];
                                    var remark = _myFormResponses[0].questionToAnswerMap["1"];

                                    var options = document.getElementsByName('option');
                                    options[rating - 1].checked = true;

                                    document.getElementById("description").value = remark;
                                    document.getElementById("description").placeholder = "";
                                }
                            }); 
                        }); 
                    } 
             
                    function submitData() { 
                        var selectedOption = getSelectedOption(); 
                        var remark = document.getElementById("description").value; 
                        submitFormResponse(selectedOption, remark); 
                    } 
             
                    function getSelectedOption() { 
                        // Check which radio button is checked 
                        var options = document.getElementsByName('option'); 
                        for (var i = 0; i < options.length; i++) { 
                            if (options[i].checked) { 
                                return parseInt(options[i].value); 
                            } 
                        } 
                    } 
             
                    // Below will be called when responder submits a new response 
                    function submitFormResponse(selectedOption, remark) { 
                        if (remark == null || remark == "") { 
                            KASClient.App.showNativeErrorMessage("Please fill remark"); 
                        } else if (selectedOption == "") { 
                            KASClient.App.showNativeErrorMessage("Please select one option"); 
                        } else { 
                            // For submitting response a question-answer 
                            // map is required, lets create that! 
                            var questionToAnswerMap = JSON.parse("{}"); 
                            questionToAnswerMap[0] = selectedOption; 
                            questionToAnswerMap[1] = remark; 
             
                            var responseId = null; 
                            var isEditingPreviousResponse = false;
                            
                            // If there is a previous response, update it
                            if (isCurrentUserResponded()) {
                                responseId = _myFormResponses[0].id;
                                isEditingPreviousResponse = true;
                            }
             
                            // Finally submit the response 
                            KASClient.Form.sumbitFormResponse(questionToAnswerMap, responseId, isEditingPreviousResponse); 
                        } 
                    }
                    
                    function isCurrentUserResponded() {
                        return _myFormResponses && _myFormResponses.length > 0;
                    }
                </script> 
            </head> 
             
            <body onload="onResponsePageLoad()"> 
                <br/> <br/> 
                <div> 
                    <p id="title"></p> 
                </div> 
                <div> 
                    <br/> <br/> 
                    <div> 
                        <p>Select your rating:</p> 
                        <br/> <br/> 
                        <div> 
                            <label>1</label> 
                            <input type="radio" name="option" id="option0" value="1" checked> 
                        </div> 
                        <div> 
                            <label>2</label> 
                            <input type="radio" name="option" id="option1" value="2"> 
                        </div> 
                        <div> 
                            <label>3</label> 
                            <input type="radio" name="option" id="option2" value="3"> 
                        </div> 
                        <div> 
                            <label>4</label> 
                            <input type="radio" name="option" id="option3" value="4"> 
                        </div> 
                        <div> 
                            <label>5</label> 
                            <input type="radio" name="option" id="option4" value="5"> 
                        </div> 
                    </div> 
                    <br/> <br/> 
                    <div> 
                        <p>Comments</p> 
                        <input type="text" name="description" id="description" placeholder="Please enter your comments here."> 
                    </div> 
                    <br/> <br/> 
                </div> 
                <div class="footer"> 
                    <input type="submit" name="submit" value="Submit" onclick="submitData()"> 
                </div> 
            </body> 
             
            </html> 
            `````
*   **Step 8:** Create the summary view   
    * Now we will create the view that appears to Kaizala users viewing the summary of the action 
    * Create a new file call SummaryView.html and insert the below snippet in the file. This will create a summary view of the total ratings and comments

            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script type="text/javascript"> 
                    // Globals 
                    var _form; // type: KASForm 
                    var _myFormResponses; // type: KASFormResponse[]
                    var _formSummary; // type: KASFormFlatSummary 
                    var _users; // type: Dictionary<UserId: KASUser>
             
                    // Below will be called on onload of SummaryView.html 
                    function onSummaryPageLoad() {            
                        KASClient.Form.getFormAsync(function (form, error) {                
                           if (error != null) {                    
                              KASClient.App.showNativeErrorMessage("Error:getFormAsync:" + error);                    
                              return;                
                           }                
                           _form = form;
                           KASClient.App.showProgressBar("Fetching summary");
                           KASClient.Form.getFormSummaryAsync(
                              function (flatSummary, processedSummary, error) { // In this callback data is fetched from local database
                                 if (error != null) {                    
                                    KASClient.App.showNativeErrorMessage("Error:getFormSummaryAsync:callback1:" + error);                    
                                    return;                
                                 } 
                                 onGetSummary(flatSummary);
                              },
                              function (flatSummary, processedSummary, error) { // In this callback data is fetched from server
                                 KASClient.App.hideProgressBar();
                                 if (error != null) {                    
                                    KASClient.App.showNativeErrorMessage("Error:getFormSummaryAsync:callback2:" + error);                    
                                    return;                
                                 }
                                 onGetSummary(flatSummary);
                              }
                           );           
                        });        
                     }

                     function onGetSummary(summary) {
                        _formSummary = summary;                    
                        KASClient.App.getUsersDetailsAsync(_formSummary.getRespondedUserIds(), function (users,
                           error) {                        
                           if (error != null) {                            
                              KASClient.App.showNativeErrorMessage("Error:getUsersDetailsAsync:" + error);                            
                              return;                        
                           }                        
                           _users = users;  // Document title would be the form title 
                           
                           document.getElementById("title").innerHTML = _form.title; 
                           
                           // Get all responses of the user, and find the average
                           var totalRating = 0;                        
                           var responseCount = 0;          
                           for (var userId in _users) {
                              var userResponses = _formSummary.getResponsesForUserId(userId); // type: Dictionary<QuestionId, string[]>
                              totalRating += parseInt(userResponses["0"][0]);                            
                              responseCount += 1;                       
                           } 
                           
                           document.getElementById("avg").innerHTML = totalRating / responseCount;                    
                        });
                     }
                </script> 
            </head> 
             
            <body onload="onSummaryPageLoad()"> 
                <div class="header"> 
                    <p id="title">Title</p> 
                    <br/> <br/> 
                    <p id="rating">Average Rating: </p> 
                    <p id="avg">avg</p> 
                </div> 
            </body> 
             
            </html>

    

    * Edit the Views object in your package manifest to the following: 
        `````
           <span data-ttu-id="d5b68-180">«views»: {              "CreationView": {                  "labelHeader": "feedback requested                  ", "SourceLocation": "CreationView.                        html"              }, "ChatCanvasCardView"                 : {" labelResponded ":" vous avez fourni des commentaires. "                  ," labelRespondToForm ":" envoyer des commentaires                  "," isResponseEditable "              : true              }," ResponseView "  : {" labelHeader ":" envoyer des commentaires "                 ," SourceLocation ":" ResponseView. html              "}              ," ResponseResultsView ":  {" labelPageHeader ":" feedback Summary "                 ," SourceLocation ":" SummaryView. html "              }     }        \`\`\`\`\`</span><span class="sxs-lookup"><span data-stu-id="d5b68-180">"views": {              "CreationView": {                  "labelHeader": "Feedback requested",                  "sourceLocation": "CreationView.html"                         },              "ChatCanvasCardView": {                   "labelResponded": "You have provided feedback.",                  "labelRespondToForm": "PROVIDE FEEDBACK",                  "isResponseEditable": true              },              "ResponseView": {  "labelHeader": "Provide feedback",                   "sourceLocation": "ResponseView.html"              },              "ResponseResultsView": {  "labelPageHeader": "Feedback summary",                   "sourceLocation": "SummaryView.html"              }     }         \`\`\`\`\`</span></span>
 
 
*   <span data-ttu-id="d5b68-181">**Étape 9:** Créer le package d'action Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-181">**Step 9:** Create the Kaizala Action package</span></span> 
    * <span data-ttu-id="d5b68-182">ComPresser tous les fichiers dans un fichier. zip unique</span><span class="sxs-lookup"><span data-stu-id="d5b68-182">Zip all the files into a single zip file</span></span> 
    * <span data-ttu-id="d5b68-183">Assurez-vous que le code postal n'inclut pas d'autre répertoire dans celui-ci, mais que les fichiers sont présents dans le répertoire racine du code postal.</span><span class="sxs-lookup"><span data-stu-id="d5b68-183">Make sure that the zip does not include another directory inside it – but the files are present at the root directory of the zip</span></span>

*   <span data-ttu-id="d5b68-184">**Étape 10:** Connectez-vous au portail de gestion Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-184">**Step 10:** Log in to the Kaizala Management Portal</span></span>  
    * <span data-ttu-id="d5b68-185">Ouvrez une fenêtre de navigateur et accédez àhttps://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="d5b68-185">Open a browser window and navigate to https://manage.kaiza.la/</span></span> 
    * <span data-ttu-id="d5b68-186">Dans le coin supérieur gauche, cliquez sur se connecter.</span><span class="sxs-lookup"><span data-stu-id="d5b68-186">On the top left corner, click on “Sign In”</span></span> 
    * <span data-ttu-id="d5b68-187">Entrez vos informations d'identification Office 365 pour vous connecter au portail.</span><span class="sxs-lookup"><span data-stu-id="d5b68-187">Enter your Office365 credentials to log in to the portal.</span></span> <span data-ttu-id="d5b68-188">Si besoin, accorder des autorisations au portail de gestion pour accéder aux informations de votre profil (nécessaire uniquement pour la première fois)</span><span class="sxs-lookup"><span data-stu-id="d5b68-188">If requested, grant permissions to the management portal to access your profile information (needed only for the first time)</span></span> 
    * <span data-ttu-id="d5b68-189">Appuyez sur «Ajouter un numéro de téléphone» dans le coin supérieur droit & vérifier votre numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="d5b68-189">Tap on “Add Phone number” on the top right hand corner & verify your phone number</span></span> 

*   <span data-ttu-id="d5b68-190">**Étape 11:** Télécharger le package d'action</span><span class="sxs-lookup"><span data-stu-id="d5b68-190">**Step 11:** Upload the action package</span></span>  
    * <span data-ttu-id="d5b68-191">Accéder à «actions» à l'aide de la barre de navigation gauche</span><span class="sxs-lookup"><span data-stu-id="d5b68-191">Navigate to “Actions” using the left Navbar</span></span> 
    * <span data-ttu-id="d5b68-192">Dans la liste déroulante à droite: sélectionnez «Importer une action» et cliquez sur Démarrer.</span><span class="sxs-lookup"><span data-stu-id="d5b68-192">From the drop-down on the right – choose “Import Action” and click Start</span></span> 
    * <span data-ttu-id="d5b68-193">Cliquez sur Télécharger, puis sélectionnez le fichier zip que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="d5b68-193">Click on upload – and select the zip file you created</span></span> 
    * <span data-ttu-id="d5b68-194">Cliquez sur Importer.</span><span class="sxs-lookup"><span data-stu-id="d5b68-194">Click on import</span></span>
    * <span data-ttu-id="d5b68-195">Une fois le package importé, confirmez les actions à nouveau. Votre action doit apparaître sous «créé par cet ID»</span><span class="sxs-lookup"><span data-stu-id="d5b68-195">Once the package is successfully imported, confirm by browsing to Actions again.You should see your Action listed under “created by this Id”</span></span>
    * <span data-ttu-id="d5b68-196">Vous pouvez tester cette action en suivant les [](test.md) étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d5b68-196">You can test this Action by following steps [here](test.md)</span></span>

*   <span data-ttu-id="d5b68-197">**Étape 12:** Créer un groupe Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-197">**Step 12:** Create a new Kaizala Group</span></span>  
    * <span data-ttu-id="d5b68-198">Sur le portail de gestion Kaizala, accédez à «groupes» à l'aide de la barre de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="d5b68-198">On Kaizala Management portal, navigate to “Groups” using the left navbar</span></span> 
    * <span data-ttu-id="d5b68-199">Appuyez sur «créer un groupe»</span><span class="sxs-lookup"><span data-stu-id="d5b68-199">Tap on “Create Group”</span></span> 
    * <span data-ttu-id="d5b68-200">Nommer le groupe «test des actions Kaizala»</span><span class="sxs-lookup"><span data-stu-id="d5b68-200">Name the group “Kaizala Actions Testing”</span></span> 
    * <span data-ttu-id="d5b68-201">Vérifier que le groupe apparaît sur votre application Kaizala</span><span class="sxs-lookup"><span data-stu-id="d5b68-201">Verify that the group appears on your Kaizala app</span></span>

*   <span data-ttu-id="d5b68-202">**Étape 13:** Publier l'action dans le groupe</span><span class="sxs-lookup"><span data-stu-id="d5b68-202">**Step 13:** Publish the Action to the Group</span></span>  
    * <span data-ttu-id="d5b68-203">Accéder à «groupes» à l'aide de la barre de navigation gauche</span><span class="sxs-lookup"><span data-stu-id="d5b68-203">Navigate to “Groups” using the left Navbar</span></span> 
    * <span data-ttu-id="d5b68-204">Appuyez sur le nom du groupe que vous avez créé à l'étape 13.</span><span class="sxs-lookup"><span data-stu-id="d5b68-204">Tap on the group name you created in Step 13</span></span> 
    * <span data-ttu-id="d5b68-205">Appuyez sur l'onglet «actions»</span><span class="sxs-lookup"><span data-stu-id="d5b68-205">Tap on the “Actions” tab</span></span> 
    * <span data-ttu-id="d5b68-206">Sélectionnez l'action que vous avez créée à l'étape 12 & cliquez sur Ajouter une action.</span><span class="sxs-lookup"><span data-stu-id="d5b68-206">Select the Action you created in Step 12 & click “Add Action”.</span></span> <span data-ttu-id="d5b68-207">Votre action Kaizala personnalisée doit maintenant apparaître sous l'onglet découvrir</span><span class="sxs-lookup"><span data-stu-id="d5b68-207">You should now see your custom Kaizala Action appearing on the Discover tab</span></span>

*   <span data-ttu-id="d5b68-208">**Étape 14:** Utiliser une action Kaizala personnalisée</span><span class="sxs-lookup"><span data-stu-id="d5b68-208">**Step 14:** Use custom Kaizala Action</span></span>  
    * <span data-ttu-id="d5b68-209">Ajoutez l'action personnalisée à votre palette et utilisez-la dans votre groupe.</span><span class="sxs-lookup"><span data-stu-id="d5b68-209">Add the custom Action to your palette and use it in your group.</span></span> 

 
 
 
 
 
