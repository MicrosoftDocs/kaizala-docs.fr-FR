# <a name="practice-tutorial-creating-a-new-kaizala-action"></a>Didacticiel pratique: création d'une action Kaizala 

## <a name="overview"></a>Vue d'ensemble 
Dans ce didacticiel, nous allons créer une action Kaizala personnalisée à l'aide de l'infrastructure d'action extensible fournie par la plateforme Kaizala.

Nous allons créer une action «Ask Feedback» qui permettra aux utilisateurs de Kaizala de demander des commentaires d'autres utilisateurs en termes de évaluations de 1 à 5 étoiles sur les questions posées, ainsi que les commentaires qu'ils aimeraient fournir.  

Vous pouvez télécharger des exemples d'actions Kaizala à partir de [ici](https://manage.kaiza.la/MiniApps/DownloadSDK).

## <a name="pre-requisites"></a>Conditions préalables 
* Un smartphone (Android/iOS) sur lequel l'application Kaizala est installée 
* Un compte Office 365 
* Accès à un éditeur HTML/JS (bloc-notes/Visual Studio code/etc.) 

## <a name="steps-to-create-a-sample-action"></a>Étapes de création d'un exemple d'action

*   **Étape 1:** Créer un répertoire pour votre package d'action  
    * Créez un nouveau répertoire sur votre bureau & nom «SampleAction». 
    * Placez tous les fichiers suivants dans ce répertoire.

*   **Étape 2:** Définir un modèle de données pour votre action 
    * Tout d'abord, nous devons définir le modèle de données qui sera utilisé dans notre action personnalisée. 
    * Les actions Kaizala sont des modèles de données basés sur des formulaires. Nous devons d'abord définir les «questions» à inclure dans notre formulaire. 
    * Étant donné qu'il s'agit d'une action «Ask Feedback», nous prévoyons d'utiliser deux éléments de données 
        * Notation numérique (valeur 1 à 5) 
        * Commentaire/commentaire textuel, le cas échéant  

    *   L'infrastructure des formulaires Kaizala prend en charge les types de questions suivants:

        | Type de question | Description |
        | :---: | :---: | 
        | SingleSelect | Question à choix unique avec options |
        | MultiSelect | Questions à choix multiples avec options | 
        | Text | Question avec une réponse en texte brut |
        | Numérique | Question avec une réponse numérique | 
        | Emplacement | Question avec une réponse de localisation | 
        | DateTime
 | Question avec réponse DateTime | 
        | Image | Question avec une image comme réponse | 
    

    * Pour nos deux questions, nous allons utiliser le type de question «Numeric» & «Text» pour les commentaires & de numéro de classement 
        * Créez un fichier appelé «appModel. JSON» et placez le contenu suivant dans le fichier. Le fichier contient les deux questions indiquées dans Order 
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
        * Remarque: le code ci-dessus contient également des métadonnées supplémentaires qui seront abordées plus loin (hors de portée pour cette session) 
        * Enregistrer le fichier
        
*   **Étape 3:** Définir un affichage pour la création de la demande de commentaires  
    *   Nous allons maintenant créer un nouveau fichier HTML qui sera utilisé pour créer de nouvelles instances de notre action Kaizala 
    *   Il s'agit de l'affichage qui est appelé lorsque l'icône est exploitée à partir de la palette. Dans cet affichage, nous aimerions leur demander ce qu'ils aimeraient envoyer. 
    * Créez un fichier nommé «CreationView. html» et placez le code HTML ci-dessous dans le fichier 
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
    *   Enregistrer le fichier 
*   **Étape 4:** Inclure le kit de développement logiciel (SDK) Kaizala Forms JS 
    * Pour faciliter l'utilisation de l'infrastructure de formulaires par les développeurs, Kaizala fournit une bibliothèque de wrappers JavaScript que vous pouvez inclure dans vos actions personnalisées. 
    * Téléchargez le fichier sous & Placez-le dans le même répertoire que votre datamodel. JSON et CreationView. html 
      *   [Kit de développement logiciel (SDK) Kaizala Forms js ](https://manage.kaiza.la/MiniApps/downloadSDK). [En savoir plus](KASClient/README.md)
 
 
 
 
*   **Étape 5:** Utiliser le kit de développement logiciel (SDK) Kaizala Forms JS pour envoyer le formulaire   
    * Ajoutez l'extrait de code suivant dans <head> l'élément de votre fichier «CreationView. html» pour faire référence au kit de développement logiciel (SDK) de Kaizala FORMs js 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * À présent, lorsque l'utilisateur clique sur envoyer, nous devons vérifier qu'il a entré une question pour demander des commentaires sur – et créer l'instance de formulaire  
    * Nous devons également instancier le formulaire au chargement de la page. Ajoutez l'extrait de code JavaScript suivant à votre fichier «CreationView. html <head> » à l'intérieur de l'élément 
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

    *   Enregistrer le fichier

*   **Étape 6:** Créer le manifeste du package d'action   
    *   Maintenant que nous avons un semblance de ce que nous souhaitons obtenir et créé une vue, nous allons maintenant créer le fichier manifeste de package qui se rapporte à ces fichiers. 
    * Le fichier manifeste de package fournit des informations essentielles sur la plateforme Kaizala pour qu'il reconnaisse et exécute votre action Kaizala personnalisée. 
    * Nous allons créer un manifeste de package et spécifier les éléments suivants: 
        * Nom d'affichage de votre action Kaizala 
        * ID personnalisé pour l'action 
        * Mappage de la vue de création à notre page CreationView. html 

    * Avant d'avoir besoin d'une icône pour le package d'action. Téléchargez le [fichier d'icône](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & enregistrez-le sous le titre Icon. png dans le même dossier que les autres fichiers.

    * Créez un fichier appelé «Package. JSON» et ajoutez un extrait de code suivant au fichier. Vérifiez que vous modifiez l'ID de sorte que votre action soit unique/distincte 
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
    * Vous pouvez configurer la carte qui apparaît sur la zone de conversation de conversation Kaizala en spécifiant les chaînes dans le manifeste du package.  
    * Modifiez l'objet «views» dans votre manifeste de package pour qu'il corresponde à l'extrait de code suivant:
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
    * Enregistrer le fichier

*   **Étape 7:** Créer l'affichage des réponses   
    * À présent, nous allons créer l'affichage qui s'affiche pour Kaizala les utilisateurs qui répondent à une instance de notre action. 
    * Créer un nouveau fichier appeler ResponseView. html et insérer l'extrait de code ci-dessous dans le fichier 
    * Nous allons effectuer les opérations suivantes: 
        * Ajouter une case d'option pour l'évaluation 
        * Préparer un objet de réponse à un formulaire et du code pour envoyer le formulaire 
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
           «views»: {              "CreationView": {                  "labelHeader": "feedback requested                  ", "SourceLocation": "CreationView.                        html"              }, "ChatCanvasCardView"                 : {" labelResponded ":" vous avez fourni des commentaires. "                  ," labelRespondToForm ":" envoyer des commentaires                  "," isResponseEditable "              : true              }," ResponseView "  : {" labelHeader ":" envoyer des commentaires "                 ," SourceLocation ":" ResponseView. html              "}              ," ResponseResultsView ":  {" labelPageHeader ":" feedback Summary "                 ," SourceLocation ":" SummaryView. html "              }     }        `````
 
 
*   **Étape 9:** Créer le package d'action Kaizala 
    * ComPresser tous les fichiers dans un fichier. zip unique 
    * Assurez-vous que le code postal n'inclut pas d'autre répertoire dans celui-ci, mais que les fichiers sont présents dans le répertoire racine du code postal.

*   **Étape 10:** Connectez-vous au portail de gestion Kaizala  
    * Ouvrez une fenêtre de navigateur et accédez àhttps://manage.kaiza.la/ 
    * Dans le coin supérieur gauche, cliquez sur se connecter. 
    * Entrez vos informations d'identification Office 365 pour vous connecter au portail. Si besoin, accorder des autorisations au portail de gestion pour accéder aux informations de votre profil (nécessaire uniquement pour la première fois) 
    * Appuyez sur «Ajouter un numéro de téléphone» dans le coin supérieur droit & vérifier votre numéro de téléphone 

*   **Étape 11:** Télécharger le package d'action  
    * Accéder à «actions» à l'aide de la barre de navigation gauche 
    * Dans la liste déroulante à droite: sélectionnez «Importer une action» et cliquez sur Démarrer. 
    * Cliquez sur Télécharger, puis sélectionnez le fichier zip que vous avez créé. 
    * Cliquez sur Importer.
    * Une fois le package importé, confirmez les actions à nouveau. Votre action doit apparaître sous «créé par cet ID»
    * Vous pouvez tester cette action en suivant les [](test.md) étapes ci-dessous.

*   **Étape 12:** Créer un groupe Kaizala  
    * Sur le portail de gestion Kaizala, accédez à «groupes» à l'aide de la barre de navigation gauche. 
    * Appuyez sur «créer un groupe» 
    * Nommer le groupe «test des actions Kaizala» 
    * Vérifier que le groupe apparaît sur votre application Kaizala

*   **Étape 13:** Publier l'action dans le groupe  
    * Accéder à «groupes» à l'aide de la barre de navigation gauche 
    * Appuyez sur le nom du groupe que vous avez créé à l'étape 13. 
    * Appuyez sur l'onglet «actions» 
    * Sélectionnez l'action que vous avez créée à l'étape 12 & cliquez sur Ajouter une action. Votre action Kaizala personnalisée doit maintenant apparaître sous l'onglet découvrir

*   **Étape 14:** Utiliser une action Kaizala personnalisée  
    * Ajoutez l'action personnalisée à votre palette et utilisez-la dans votre groupe. 

 
 
 
 
 
