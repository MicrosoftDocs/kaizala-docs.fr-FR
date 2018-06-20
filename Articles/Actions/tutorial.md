# <a name="practice-tutorial-creating-a-new-kaizala-action"></a><span data-ttu-id="abdac-101">Didacticiel pratique : Création d’une nouvelle Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="abdac-101">Practice Tutorial: Creating a new Kaizala Action</span></span> 

## <a name="overview"></a><span data-ttu-id="abdac-102">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="abdac-102">Overview</span></span> 
<span data-ttu-id="abdac-103">Dans ce didacticiel, nous allons créer une Action personnalisée de Kaizala utilisant l’Action framework extensible fourni par la plate-forme Kaizala.</span><span class="sxs-lookup"><span data-stu-id="abdac-103">In this tutorial, we will create a custom Kaizala Action utilizing the extensible Action framework provided by the Kaizala platform.</span></span>

<span data-ttu-id="abdac-104">Nous allons créer une Action « Demander des commentaires » qui permettra aux utilisateurs Kaizala demander des commentaires d’autres utilisateurs en termes de-1 à 5 étoiles – questions posées ainsi que les commentaires qu’il souhaite fournir.</span><span class="sxs-lookup"><span data-stu-id="abdac-104">We will create an “Ask Feedback” Action which will allow Kaizala users to ask for feedback from other users in terms of 1-to-5 star ratings on questions asked – along with any comments they would like to provide.</span></span>  

<span data-ttu-id="abdac-105">Vous pouvez télécharger des exemples de packages de Kaizala Action à partir [d’ici](https://manage.kaiza.la/MiniApps/DownloadSDK).</span><span class="sxs-lookup"><span data-stu-id="abdac-105">You can download sample Kaizala Action packages from [here](https://manage.kaiza.la/MiniApps/DownloadSDK).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="abdac-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="abdac-106">Pre-requisites</span></span> 
* <span data-ttu-id="abdac-107">Un smartphone (Android/iOS) avec Kaizala application installée</span><span class="sxs-lookup"><span data-stu-id="abdac-107">A smartphone (Android/iOS) with Kaizala app installed</span></span> 
* <span data-ttu-id="abdac-108">Un compte Office 365</span><span class="sxs-lookup"><span data-stu-id="abdac-108">An Office365 Account</span></span> 
* <span data-ttu-id="abdac-109">Accès à un éditeur HTML/JS (bloc-notes/Visual Studio Code/etc..)</span><span class="sxs-lookup"><span data-stu-id="abdac-109">Access to an HTML/JS editor (notepad/Visual Studio Code/etc.)</span></span> 

## <a name="steps-to-create-a-sample-action"></a><span data-ttu-id="abdac-110">Étapes de création d’un Action de l’exemple</span><span class="sxs-lookup"><span data-stu-id="abdac-110">Steps to create a sample Action</span></span>

*   <span data-ttu-id="abdac-111">**Étape 1 :** Créer un nouveau répertoire pour votre package d’Action</span><span class="sxs-lookup"><span data-stu-id="abdac-111">**Step 1:** Create a new directory for your Action package</span></span>  
    * <span data-ttu-id="abdac-112">Créez un nouveau répertoire sur votre bureau et nommez-la « SampleAction »</span><span class="sxs-lookup"><span data-stu-id="abdac-112">Create a new directory on your desktop & name it “SampleAction”</span></span> 
    * <span data-ttu-id="abdac-113">Placez tous les fichiers suivants dans ce répertoire</span><span class="sxs-lookup"><span data-stu-id="abdac-113">Place all the subsequent files in this directory</span></span>

*   <span data-ttu-id="abdac-114">**Étape 2 :** Définir un modèle de données pour votre Action</span><span class="sxs-lookup"><span data-stu-id="abdac-114">**Step 2:** Define a data model for your Action</span></span> 
    * <span data-ttu-id="abdac-115">Tout d’abord, nous devons définir le modèle de données qui sera utilisé dans notre Action personnalisée</span><span class="sxs-lookup"><span data-stu-id="abdac-115">First, we need to define the data model which will be used in our custom Action</span></span> 
    * <span data-ttu-id="abdac-116">Les Actions Kaizala sont actuellement les modèles de formulaire en fonction de données.</span><span class="sxs-lookup"><span data-stu-id="abdac-116">The Kaizala Actions are currently form based data models.</span></span> <span data-ttu-id="abdac-117">Par conséquent, nous devez d’abord définir les questions que nous devons à inclure dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="abdac-117">So, we will first need to define the ‘questions’ we need to include in our form.</span></span> 
    * <span data-ttu-id="abdac-118">Dans la mesure où il s’agit d’une action « Demander des commentaires » – nous sera planifier l’utilisation de deux types de données</span><span class="sxs-lookup"><span data-stu-id="abdac-118">Since this is a “Ask Feedback” action – we will plan to use two pieces of data</span></span> 
        * <span data-ttu-id="abdac-119">Classement numérique (valeur 1 à 5)</span><span class="sxs-lookup"><span data-stu-id="abdac-119">Numeric rating (value 1 to 5)</span></span> 
        * <span data-ttu-id="abdac-120">Commentaire/Verbatim commentaires le cas échéant</span><span class="sxs-lookup"><span data-stu-id="abdac-120">Comment/Verbatim feedback if any</span></span>  

    *   <span data-ttu-id="abdac-121">Infrastructure Kaizala Forms prend en charge sous types de questions :</span><span class="sxs-lookup"><span data-stu-id="abdac-121">Kaizala Forms infrastructure supports below question types:</span></span>

        | <span data-ttu-id="abdac-122">Type de question</span><span class="sxs-lookup"><span data-stu-id="abdac-122">Question Type</span></span> | <span data-ttu-id="abdac-123">Description</span><span class="sxs-lookup"><span data-stu-id="abdac-123">Description</span></span> |
        | :---: | :---: | 
        | <span data-ttu-id="abdac-124">SingleSelect</span><span class="sxs-lookup"><span data-stu-id="abdac-124">SingleSelect</span></span> | <span data-ttu-id="abdac-125">Question à choix unique avec des options</span><span class="sxs-lookup"><span data-stu-id="abdac-125">Single choice question with options</span></span> |
        | <span data-ttu-id="abdac-126">MultiSelect</span><span class="sxs-lookup"><span data-stu-id="abdac-126">MultiSelect</span></span> | <span data-ttu-id="abdac-127">Question à choix multiple avec options</span><span class="sxs-lookup"><span data-stu-id="abdac-127">Multiple choice question with options</span></span> | 
        | <span data-ttu-id="abdac-128">Texte</span><span class="sxs-lookup"><span data-stu-id="abdac-128">Text</span></span> | <span data-ttu-id="abdac-129">Question avec une réponse en texte brut</span><span class="sxs-lookup"><span data-stu-id="abdac-129">Question with a plain text answer</span></span> |
        | <span data-ttu-id="abdac-130">Numérique</span><span class="sxs-lookup"><span data-stu-id="abdac-130">Numeric</span></span> | <span data-ttu-id="abdac-131">Question avec une réponse numérique</span><span class="sxs-lookup"><span data-stu-id="abdac-131">Question with a numeric answer</span></span> | 
        | <span data-ttu-id="abdac-132">Emplacement</span><span class="sxs-lookup"><span data-stu-id="abdac-132">Location</span></span> | <span data-ttu-id="abdac-133">Question avec une réponse de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="abdac-133">Question with a location answer</span></span> | 
        | <span data-ttu-id="abdac-134">Date/heure</span><span class="sxs-lookup"><span data-stu-id="abdac-134">DateTime</span></span> | <span data-ttu-id="abdac-135">Question réponse DateTime</span><span class="sxs-lookup"><span data-stu-id="abdac-135">Question with DateTime answer</span></span> | 
        | <span data-ttu-id="abdac-136">Image</span><span class="sxs-lookup"><span data-stu-id="abdac-136">Image</span></span> | <span data-ttu-id="abdac-137">Question avec une image en tant que réponse</span><span class="sxs-lookup"><span data-stu-id="abdac-137">Question with a picture as an answer</span></span> | 
    

    * <span data-ttu-id="abdac-138">Pour notre deux questions, nous allons utiliser Type Question 'Numérique' et 'Texte' d’évaluation respectivement de numéro et commentaires</span><span class="sxs-lookup"><span data-stu-id="abdac-138">For our two questions we will use Question Type of 'Numeric' & 'Text' for Rating number & comments respectively</span></span> 
        * <span data-ttu-id="abdac-139">Créer un nouveau fichier nommé « appModel.json » et placer le contenu suivant dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="abdac-139">Create a new file called “appModel.json” and place the following content in the file.</span></span> <span data-ttu-id="abdac-140">Le fichier contient les deux questions répertoriées dans l’ordre</span><span class="sxs-lookup"><span data-stu-id="abdac-140">The file contains the two questions listed in order</span></span> 
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
        * <span data-ttu-id="abdac-141">Remarque : Au-dessus de code contient également des métadonnées supplémentaires, vous découvrirez (hors de la portée de cette session)</span><span class="sxs-lookup"><span data-stu-id="abdac-141">Note: Above code also contains additional metadata we will learn about later (out of scope for this session)</span></span> 
        * <span data-ttu-id="abdac-142">Enregistrez le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-142">Save the file</span></span>
        
*   <span data-ttu-id="abdac-143">**Étape 3 :** Définir un affichage pour la création de la demande de commentaires</span><span class="sxs-lookup"><span data-stu-id="abdac-143">**Step 3:** Define a view for creating the request for feedback</span></span>  
    *   <span data-ttu-id="abdac-144">Nous allons maintenant créer un nouveau fichier HTML qui sera utilisé pour créer de nouvelles instances de notre Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="abdac-144">We will now create a new HTML file which will be used to create new instances of  our Kaizala Action</span></span> 
    *   <span data-ttu-id="abdac-145">Il s’agit de l’affichage qui est appelée lorsque l’utilisateur clique sur l’icône de la palette.</span><span class="sxs-lookup"><span data-stu-id="abdac-145">This is the view that is invoked when the icon is tapped from the palette.</span></span> <span data-ttu-id="abdac-146">Dans cet affichage, nous souhaitons lui demander quel qu’il souhaite commentaires sur.</span><span class="sxs-lookup"><span data-stu-id="abdac-146">In this view, we would like to ask them what they would like feedback on.</span></span> 
    * <span data-ttu-id="abdac-147">Créez un fichier appelé « CreationView.html » et place la sous HTML dans le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-147">Create a new file called “CreationView.html” and place the below HTML in the file</span></span> 
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
    *   <span data-ttu-id="abdac-148">Enregistrez le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-148">Save the file</span></span> 
*   <span data-ttu-id="abdac-149">**Étape 4 :** Inclure le Kit de développement Kaizala Forms JS</span><span class="sxs-lookup"><span data-stu-id="abdac-149">**Step 4:** Include the Kaizala Forms JS SDK</span></span> 
    * <span data-ttu-id="abdac-150">Pour faciliter aux développeurs de tirer parti de l’Infrastructure de formulaires, Kaizala fournit une bibliothèque de wrappers JavaScript que vous pouvez inclure dans vos Actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="abdac-150">To make it easy for developers to leverage the Forms Infrastructure, Kaizala provides a JavaScript wrapper library that you can include in your custom Actions</span></span> 
    * <span data-ttu-id="abdac-151">Téléchargez le fichier ci-dessous & placer dans le même répertoire que votre datamodel.json et le CreationView.html</span><span class="sxs-lookup"><span data-stu-id="abdac-151">Download the file below & place it in the same directory as your datamodel.json and CreationView.html</span></span> 
      *   <span data-ttu-id="abdac-152">[Kit de développement logiciel Kaizala Forms JS ](https://manage.kaiza.la/MiniApps/downloadSDK).</span><span class="sxs-lookup"><span data-stu-id="abdac-152">[Kaizala Forms JS SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span></span> [<span data-ttu-id="abdac-153">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="abdac-153">Read more</span></span>](KASClient/README.md)
 
 
 
 
*   <span data-ttu-id="abdac-154">**Étape 5 :** Utiliser le Kit de développement Kaizala Forms JS pour envoyer le formulaire</span><span class="sxs-lookup"><span data-stu-id="abdac-154">**Step 5:** Use the Kaizala Forms JS SDK to submit form</span></span>   
    * <span data-ttu-id="abdac-155">Ajouter l’extrait de code suivant dans le <head> élément de votre « CreationView.html » pour désigner le Kit de développement Kaizala Forms JS</span><span class="sxs-lookup"><span data-stu-id="abdac-155">Add the following code snippet in the <head> element of your “CreationView.html” to refer to the Kaizala Forms JS SDK</span></span> 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * <span data-ttu-id="abdac-156">Maintenant, lorsque l’utilisateur clique sur Envoyer, nous devons vérifier qu’il a entré une question à poser des commentaires sur – et créer l’Instance de formulaire</span><span class="sxs-lookup"><span data-stu-id="abdac-156">Now, when the user clicks submit, we need to verify that he has entered a question to ask feedback on – and create the Form Instance</span></span>  
    * <span data-ttu-id="abdac-157">Nous devons également instancier le formulaire sur le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="abdac-157">We also need to instantiate the form on page load.</span></span> <span data-ttu-id="abdac-158">Ajouter l’extrait de code JavaScript suivant à votre « CreationView.html » à l’intérieur de la <head> élément</span><span class="sxs-lookup"><span data-stu-id="abdac-158">Add the following JavaScript snippet to your “CreationView.html” inside the <head> element</span></span> 
        `````
            <script type="text/javascript"> 
                var _form; // type: KASForm
         
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

    *   <span data-ttu-id="abdac-159">Enregistrez le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-159">Save the file</span></span>

*   <span data-ttu-id="abdac-160">**Étape 6 :** Créer le manifeste de package d’Action</span><span class="sxs-lookup"><span data-stu-id="abdac-160">**Step 6:** Create the Action package manifest</span></span>   
    *   <span data-ttu-id="abdac-161">Maintenant que nous avons un semblance de ce que nous souhaitons atteindre et créé un affichage, nous allons maintenant créer le fichier manifeste de package qui fait référence à ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="abdac-161">Now that we have a semblance of what we want to achieve and successfully created a view – we will now create the package manifest file that refers to these files.</span></span> 
    * <span data-ttu-id="abdac-162">Fichier manifeste de package fournit des informations essentielles pour la plate-forme Kaizala pour qu’il reconnaisse et exécuter l’action Kaizala personnalisée.</span><span class="sxs-lookup"><span data-stu-id="abdac-162">Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span> 
    * <span data-ttu-id="abdac-163">Nous créer un manifeste de package et spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abdac-163">We will create a package manifest and specify the following things:</span></span> 
        * <span data-ttu-id="abdac-164">Nom d’affichage pour votre Action Kaizala</span><span class="sxs-lookup"><span data-stu-id="abdac-164">Display name for your Kaizala Action</span></span> 
        * <span data-ttu-id="abdac-165">Code personnalisé pour l’Action</span><span class="sxs-lookup"><span data-stu-id="abdac-165">Custom Id for the Action</span></span> 
        * <span data-ttu-id="abdac-166">Mappage de l’affichage de la création à la page CreationView.html</span><span class="sxs-lookup"><span data-stu-id="abdac-166">Mapping of the creation view to our CreationView.html page</span></span> 

    * <span data-ttu-id="abdac-167">Avant que nous devons une icône pour le package de l’Action.</span><span class="sxs-lookup"><span data-stu-id="abdac-167">Before that we will need an icon for the Action package.</span></span> <span data-ttu-id="abdac-168">Téléchargez le [fichier d’icône](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) et enregistrez-le sous icon.png dans le même dossier que les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="abdac-168">Download the [icon file](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & save it as icon.png in the same folder as the other files.</span></span>

    * <span data-ttu-id="abdac-169">Créer un nouveau fichier nommé « package.json » et ajoutez suivant extrait le fichier.</span><span class="sxs-lookup"><span data-stu-id="abdac-169">Create a new file called “package.json” and add following snippet to the file.</span></span> <span data-ttu-id="abdac-170">Assurez-vous que vous modifiez l’id pour rendre votre Action unique/distincts</span><span class="sxs-lookup"><span data-stu-id="abdac-170">Ensure that you edit the id to make your Action unique/distinct</span></span> 
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
    * <span data-ttu-id="abdac-171">Vous pouvez configurer la carte qui apparaît dans la zone de conversation Kaizala en spécifiant les chaînes dans le manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="abdac-171">You can configure the card that appears on Kaizala chat canvas by specifying the strings in the package manifest.</span></span>  
    * <span data-ttu-id="abdac-172">Modifier l’objet « Affichages » dans votre manifeste du package pour la correspondance de le ci-dessous extrait de code :</span><span class="sxs-lookup"><span data-stu-id="abdac-172">Modify the “Views” object in you package manifest to match the below snippet:</span></span>
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
    * <span data-ttu-id="abdac-173">Enregistrez le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-173">Save the file</span></span>

*   <span data-ttu-id="abdac-174">**Étape 7 :** Créer la vue de réponse</span><span class="sxs-lookup"><span data-stu-id="abdac-174">**Step 7:** Create the response view</span></span>   
    * <span data-ttu-id="abdac-175">Maintenant, nous allons créer l’affichage qui apparaît aux utilisateurs Kaizala répondre à une instance de notre action</span><span class="sxs-lookup"><span data-stu-id="abdac-175">Now we will create the view that appears to Kaizala users responding to an instance of our action</span></span> 
    * <span data-ttu-id="abdac-176">Créer un nouvel appel fichier ResponseView.html et insérer le ci-dessous extrait de code dans le fichier</span><span class="sxs-lookup"><span data-stu-id="abdac-176">Create a new file call ResponseView.html and insert the below snippet in the file</span></span> 
    * <span data-ttu-id="abdac-177">Il effectue les opérations suivantes</span><span class="sxs-lookup"><span data-stu-id="abdac-177">We will do the following</span></span> 
        * <span data-ttu-id="abdac-178">Ajouter la case d’option pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="abdac-178">Add radio button selection for the rating</span></span> 
        * <span data-ttu-id="abdac-179">Préparer un objet de réponse de formulaire et du code pour envoyer le formulaire</span><span class="sxs-lookup"><span data-stu-id="abdac-179">Prepare a form response object and code to submit the form</span></span> 
        ````` 
            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script> 
                    var _form; // type: KASForm
                    var _myFormResponses; // type: KASFormResponse[]
             
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
                    var _users; // type: Dictionary<UserId: KASUser>
             
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
                           _users = users;  // Document title would be the form title 
                           
                           document.getElementById("title").innerHTML = _form.title; 
                           
                           // Get all responses of the user, and find the average
                           var totalRating = 0;                        
                           var responseCount = 0;          
                           for (var userId in _users) {
                              var userResponses = _formSummary.getResponsesForUserId(userId); // type: Dictionary<QuestionId, string[]>
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
           "views": { 
                    "CreationView": { 
                        "labelHeader": "Feedback requested", 
                        "sourceLocation": "CreationView.html"            
                    }, 
                    "ChatCanvasCardView": {
                        "labelResponded": "You have provided feedback.", 
                        "labelRespondToForm": "PROVIDE FEEDBACK", 
                        "isResponseEditable": true 
                    }, 
                    "ResponseView": { 
                        "labelHeader": "Provide feedback",
                        "sourceLocation": "ResponseView.html" 
                    }, 
                    "ResponseResultsView": { 
                        "labelPageHeader": "Feedback summary"
                        "sourceLocation": "SummaryView.html" 
                    } 
           }       
         `````
 
 
*   **Step 9:** Create the Kaizala Action package 
    * Zip all the files into a single zip file 
    * Make sure that the zip does not include another directory inside it – but the files are present at the root directory of the zip

*   **Step 10:** Log in to the Kaizala Management Portal  
    * Open a browser window and navigate to https://manage.kaiza.la/ 
    * On the top left corner, click on “Sign In” 
    * Enter your Office365 credentials to log in to the portal. If requested, grant permissions to the management portal to access your profile information (needed only for the first time) 
    * Tap on “Add Phone number” on the top right hand corner & verify your phone number 

*   **Step 11:** Upload the action package  
    * Navigate to “Actions” using the left Navbar 
    * From the drop-down on the right – choose “Import Action” and click Start 
    * Click on upload – and select the zip file you created 
    * Click on import
    * Once the package is successfully imported, confirm by browsing to Actions again.You should see your Action listed under “created by this Id”
    * You can test this Action by following steps [here](test.md)

*   **Step 12:** Create a new Kaizala Group  
    * On Kaizala Management portal, navigate to “Groups” using the left navbar 
    * Tap on “Create Group” 
    * Name the group “Kaizala Actions Testing” 
    * Verify that the group appears on your Kaizala app

*   **Step 13:** Publish the Action to the Group  
    * Navigate to “Groups” using the left Navbar 
    * Tap on the group name you created in Step 13 
    * Tap on the “Actions” tab 
    * Select the Action you created in Step 12 & click “Add Action”. You should now see your custom Kaizala Action appearing on the Discover tab

*   **Step 14:** Use custom Kaizala Action  
    * Add the custom Action to your palette and use it in your group. 

 
 
 
 
 
