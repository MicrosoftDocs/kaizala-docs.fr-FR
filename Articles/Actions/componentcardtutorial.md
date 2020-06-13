# <a name="create-an-action-using-component-card-controls"></a>Créer une action à l’aide de contrôles de carte de composant 

## <a name="overview"></a>Vue d’ensemble
Dans cet article, nous allons aborder les différents contrôles de cartes de composants pouvant être utilisés dans une action à l’aide de l’infrastructure de cartes de composants.

Les contrôles pris en charge sont les suivants :
* Zone de texte/zone de texte numérique
* Location
* Zone de pièce jointe
* Case à cocher à sélection unique
* Curseur avec zone de texte
* Contrôle de date
* Contrôle d’heure
* Zone de texte
* Liste déroulante


Nous allons répertorier les modifications de fichier nécessaires pour activer le contrôle dans une carte personnalisée. Vous devrez ajouter les détails suivants dans les fichiers correspondants, comme indiqué ci-dessous.

## <a name="creation-view"></a>Vue de création
Ce qui suit contient l’extrait de code qui doit se trouver dans une page (par exemple :  \<div id='page_1'\> ... \</div\> ) dans « CreationView.html ».

* Zone de texte **/zone de texte numérique :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée). Pour la zone de texte numérique, l’extrait de code reste identique. Seule la modification obligatoire est que le type d’entrée doit être « nombre » au lieu de « texte ».

  `````
    <div class='section-div'>
    <div id='LABEL1' class='field-label'>
    </div>
    <input id='INPUT1' type='text' contenteditable='true' class='textbox-1'>
    </div>
  `````

* **Emplacement :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné).

  `````
    <div class='section-div'>
    <div id='LABEL21' class='field-label'>
    </div>
    <img class='location-image' id='location'>
    <div style='padding: 8px 15pt 15pt; display: inline-flex;'>
    <div class='location-div1'>
    <label class='location-address' id='location_text'>
    </label>
    </div>
    <div class='location-div2'>
    <label id='refresh-location-text' onclick='refreshLocation();' class='refresh-location-text'>
    </label>
    </div>
    </div>
    </div>
  `````
  
* **Zone de pièces jointes :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour pointer vers la valeur qui doit être insérée).
    
  ````` 
      <div class='section-div'>
      <div id='LABEL4' class='field-label'>
      </div>
      <div id='INPUT4' class='scroll-div' title='Attachments'>
      <div class='horizontal-div'>
      <div class='attachment-div'>
      <img class='section-img' onclick='addAttachment()'>
      </div>
      </div>
      </div>
      </div>
  `````
 
* Case **à cocher à sélection unique :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID de case à cocher (pour pointer vers la valeur qui doit être insérée). L’ID doit être préfixé avec la case à cocher (par exemple : CHECKBOX1). Les ID des options individuelles doivent être mappés à la case à cocher parent. De plus, ce contrôle ne peut pas être rendu facultatif par défaut, la première option est sélectionnée lors du rendu du formulaire.

  `````
      <div class='section-div'>
      <div id='LABEL5' class='field-label'>
      </div>
      <div class='option-div' id='CHECKBOX1'>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_1' class='selected-label'>
      </label>
      </div>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_2' class='unselected-label'>
      </label>
      </div>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_3' class='unselected-label'>
      </label>
      </div>
      </div>
      </div>
  `````
  
* **Curseur avec zone de texte :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour entrer une valeur numérique directement). Il ne peut pas être rendu facultatif par défaut, car le curseur sera toujours initialisé avec une valeur par défaut.

  `````
    <div class='section-div slider-with-textbox'>
    <div id='LABEL6' class='field-label'>
    </div>
    <input id='INPUT6' type='range' class='slider-bar'>
    <input class='slider-textbox' type='number'>
    </input>
    </div>
  `````

* **Contrôle de date :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).
    
    `````
        <div class='section-div'>
        <div id='LABEL7' class='field-label'>
        </div>
        <div id='INPUT7' onClick='event_click(this)' class='textbox-1 image_right_date' value=''>
        </div>
        <div style='width: 0px; height: 0px; overflow: hidden;'>
        <input type='date' onChange='change_date_format(this)' class='textbox-1'>
        </div>
        </div>
  `````


* **Contrôle de l’heure :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).
    
  `````
      <div class='section-div'>
      <div id='LABEL8' class='field-label'>
      </div>
      <div id='INPUT8' onClick='event_click(this)' class='textbox-1 image_right_time' value=''>
      </div>
      <div style='width: 0px; height: 0px; overflow: hidden;'>
      <input type='time' onChange='change_time_format(this)' class='textbox-1'>
      </div>
      </div>
  `````
    
* **Zone de texte :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).

  `````
    <div class='section-div'>
    <div id='LABEL9' class='field-label'>
    </div>
    <textarea id='INPUT9' contenteditable='true' class='text-area'>
    </textarea>
    </div>
  `````
 
* **Liste déroulante :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée). Ce contrôle ne peut pas être rendu facultatif.

  `````
      <div class='section-div'>
      <div id='LABEL10' class='field-label'>
      </div>
      <table id='INPUT10' class='feedbackSlderTable' title='TapBasedSlider'>
      </table>
      <div class='progressbar-outer-div'>
      <div class='progressbar-inner-div'>
      </div>
      </div>
      </div>
  `````

## <a name="summary-view"></a>Affichage de synthèse
Il s’agit de l’extrait de code qui doit se trouver dans le conteneur "SummaryView.html". Le suffixe de la réponse dans l’ID est le numéro de question dans AppModel auquel la question a été mappée (en partant de 1). Vous trouverez ci-dessous un exemple de contrôle. Le nombre de réponses dans le AppModel doit être égal au nombre de sections du SummaryView.html.

  `````
      <div class='section-div-summary'>
      <div id='ANSWER_1' class='field-label-summary'>
      </div>
      <label class='answer-label'>
      </label>
      </div>
  ````` 
    
## <a name="appmodel-file"></a>Fichier AppModel
Il s’agit de l’extrait de code qui doit figurer dans la section « AppModel.jsonConfig » où le modèle de données est défini, le titre correspond à l’affichage du Résumé correspondant aux données réelles entrées par l’utilisateur.
Vous trouverez ci-dessous un exemple de contrôle TextBox. Un format similaire doit également être suivi pour d’autres contrôles. Veuillez noter que pour les pièces jointes, le type doit être « AttachmentList » et pour location le type doit être « location ».
  ````` 
      {
      "title": "Name",
      "type": "Text"
      }
  `````

## <a name="configuration-file"></a>Fichier de configuration
    
Il s’agit de l’extrait de code qui doit figurer dans le fichier « Config.js ». Dans SUBMIT_IDS vous devez placer l’ID d’entrée du contrôle dans la même séquence que les questions sont présentes dans l’AppModel. Si vous souhaitez le faire facultatif, ajoutez-le dans le dictionnaire OPTIONAL_IDS avec le numéro de page correspondant-si aucun élément n’est facultatif dans une page, assignez un tableau vide à la page correspondante (comme indiqué dans l’exemple pour page_2). Les étiquettes de question facultatives seront automatiquement ajoutées à la chaîne' (facultatif) 'lors du rendu du formulaire. Vous trouverez ci-dessous un exemple de contrôle TextBox. Tous les contrôles auront un format similaire. Notez que pour les images et l’emplacement, nous n’avons pas besoin d’une entrée dans SUBMIT_IDS.

  `````
    var SUBMIT_IDS = ['INPUT1'];
    var OPTIONAL_IDS = {
    "page_1": ["INPUT1"],
    "page_2": []
    };// in case you have a page 2 where all questions are mandatory
  `````

## <a name="localized-strings-file---strings_enjson"></a>Fichier de chaînes localisées-strings_en.js
Il s’agit de l’extrait de code qui doit figurer dans le fichier de chaînes dans lequel les chaînes sont définies. Pour une zone de texte avec l’ID en tant que INPUT1, une étiquette est associée qui demande à l’utilisateur ce qu’est la question ; Il y a ensuite un espace réservé facultatif qui apparaît sous la forme d’un texte fantôme à l’intérieur de la zone de texte. Il s’agit d’un exemple de contrôle TextBox. Tous les contrôles auront le même format.

  `````
    "LABEL1": "Please enter your name",
    "INPUT1_placeholder": "Tap to enter name"
  `````

