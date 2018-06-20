# <a name="practice-tutorial-creating-a-new-kaizala-action"></a>Didacticiel pratique : Création d’une nouvelle Action Kaizala 

## <a name="overview"></a>Vue d'ensemble 
Dans ce didacticiel, nous allons créer une Action personnalisée de Kaizala utilisant l’Action framework extensible fourni par la plate-forme Kaizala.

Nous allons créer une Action « Demander des commentaires » qui permettra aux utilisateurs Kaizala demander des commentaires d’autres utilisateurs en termes de-1 à 5 étoiles – questions posées ainsi que les commentaires qu’il souhaite fournir.  

Vous pouvez télécharger des exemples de packages de Kaizala Action à partir [d’ici](https://manage.kaiza.la/MiniApps/DownloadSDK).

## <a name="pre-requisites"></a>Conditions préalables 
* Un smartphone (Android/iOS) avec Kaizala application installée 
* Un compte Office 365 
* Accès à un éditeur HTML/JS (bloc-notes/Visual Studio Code/etc..) 

## <a name="steps-to-create-a-sample-action"></a>Étapes de création d’un Action de l’exemple

*   **Étape 1 :** Créer un nouveau répertoire pour votre package d’Action  
    * Créez un nouveau répertoire sur votre bureau et nommez-la « SampleAction » 
    * Placez tous les fichiers suivants dans ce répertoire

*   **Étape 2 :** Définir un modèle de données pour votre Action 
    * Tout d’abord, nous devons définir le modèle de données qui sera utilisé dans notre Action personnalisée 
    * Les Actions Kaizala sont actuellement les modèles de formulaire en fonction de données. Par conséquent, nous devez d’abord définir les questions que nous devons à inclure dans le formulaire. 
    * Dans la mesure où il s’agit d’une action « Demander des commentaires » – nous sera planifier l’utilisation de deux types de données 
        * Classement numérique (valeur 1 à 5) 
        * Commentaire/Verbatim commentaires le cas échéant  

    *   Infrastructure Kaizala Forms prend en charge sous types de questions :

        | Type de question | Description |
        | :---: | :---: | 
        | SingleSelect | Question à choix unique avec des options |
        | MultiSelect | Question à choix multiple avec options | 
        | Texte | Question avec une réponse en texte brut |
        | Numérique | Question avec une réponse numérique | 
        | Emplacement | Question avec une réponse de l’emplacement | 
        | Date/heure | Question réponse DateTime | 
        | Image | Question avec une image en tant que réponse | 
    

    * Pour notre deux questions, nous allons utiliser Type Question 'Numérique' et 'Texte' d’évaluation respectivement de numéro et commentaires 
        * Créer un nouveau fichier nommé « appModel.json » et placer le contenu suivant dans le fichier. Le fichier contient les deux questions répertoriées dans l’ordre 
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
        * Remarque : Au-dessus de code contient également des métadonnées supplémentaires, vous découvrirez (hors de la portée de cette session) 
        * Enregistrez le fichier
        
*   **Étape 3 :** Définir un affichage pour la création de la demande de commentaires  
    *   Nous allons maintenant créer un nouveau fichier HTML qui sera utilisé pour créer de nouvelles instances de notre Action Kaizala 
    *   Il s’agit de l’affichage qui est appelée lorsque l’utilisateur clique sur l’icône de la palette. Dans cet affichage, nous souhaitons lui demander quel qu’il souhaite commentaires sur. 
    * Créez un fichier appelé « CreationView.html » et place la sous HTML dans le fichier 
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
    *   Enregistrez le fichier 
*   **Étape 4 :** Inclure le Kit de développement Kaizala Forms JS 
    * Pour faciliter aux développeurs de tirer parti de l’Infrastructure de formulaires, Kaizala fournit une bibliothèque de wrappers JavaScript que vous pouvez inclure dans vos Actions personnalisées 
    * Téléchargez le fichier ci-dessous & placer dans le même répertoire que votre datamodel.json et le CreationView.html 
      *   [Kit de développement logiciel Kaizala Forms JS ](https://manage.kaiza.la/MiniApps/downloadSDK). [En savoir plus](KASClient/README.md)
 
 
 
 
*   **Étape 5 :** Utiliser le Kit de développement Kaizala Forms JS pour envoyer le formulaire   
    * Ajouter l’extrait de code suivant dans le <head> élément de votre « CreationView.html » pour désigner le Kit de développement Kaizala Forms JS 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * Maintenant, lorsque l’utilisateur clique sur Envoyer, nous devons vérifier qu’il a entré une question à poser des commentaires sur – et créer l’Instance de formulaire  
    * Nous devons également instancier le formulaire sur le chargement de la page. Ajouter l’extrait de code JavaScript suivant à votre « CreationView.html » à l’intérieur de la <head> élément 
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

    *   Enregistrez le fichier

*   **Étape 6 :** Créer le manifeste de package d’Action   
    *   Maintenant que nous avons un semblance de ce que nous souhaitons atteindre et créé un affichage, nous allons maintenant créer le fichier manifeste de package qui fait référence à ces fichiers. 
    * Fichier manifeste de package fournit des informations essentielles pour la plate-forme Kaizala pour qu’il reconnaisse et exécuter l’action Kaizala personnalisée. 
    * Nous créer un manifeste de package et spécifier les éléments suivants : 
        * Nom d’affichage pour votre Action Kaizala 
        * Code personnalisé pour l’Action 
        * Mappage de l’affichage de la création à la page CreationView.html 

    * Avant que nous devons une icône pour le package de l’Action. Téléchargez le [fichier d’icône](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) et enregistrez-le sous icon.png dans le même dossier que les autres fichiers.

    * Créer un nouveau fichier nommé « package.json » et ajoutez suivant extrait le fichier. Assurez-vous que vous modifiez l’id pour rendre votre Action unique/distincts 
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
    * Vous pouvez configurer la carte qui apparaît dans la zone de conversation Kaizala en spécifiant les chaînes dans le manifeste du package.  
    * Modifier l’objet « Affichages » dans votre manifeste du package pour la correspondance de le ci-dessous extrait de code :
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
    * Enregistrez le fichier

*   **Étape 7 :** Créer la vue de réponse   
    * Maintenant, nous allons créer l’affichage qui apparaît aux utilisateurs Kaizala répondre à une instance de notre action 
    * Créer un nouvel appel fichier ResponseView.html et insérer le ci-dessous extrait de code dans le fichier 
    * Il effectue les opérations suivantes 
        * Ajouter la case d’option pour l’évaluation 
        * Préparer un objet de réponse de formulaire et du code pour envoyer le formulaire 
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

 
 
 
 
 
