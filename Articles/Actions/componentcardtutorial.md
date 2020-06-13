# <a name="create-an-action-using-component-card-controls"></a><span data-ttu-id="7fe40-101">Créer une action à l’aide de contrôles de carte de composant</span><span class="sxs-lookup"><span data-stu-id="7fe40-101">Create an Action using Component Card Controls</span></span> 

## <a name="overview"></a><span data-ttu-id="7fe40-102">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="7fe40-102">Overview</span></span>
<span data-ttu-id="7fe40-103">Dans cet article, nous allons aborder les différents contrôles de cartes de composants pouvant être utilisés dans une action à l’aide de l’infrastructure de cartes de composants.</span><span class="sxs-lookup"><span data-stu-id="7fe40-103">In this article, we will cover the various component cards controls which can be used in an action using component card framework.</span></span>

<span data-ttu-id="7fe40-104">Les contrôles pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe40-104">The following are the controls supported</span></span>
* <span data-ttu-id="7fe40-105">Zone de texte/zone de texte numérique</span><span class="sxs-lookup"><span data-stu-id="7fe40-105">Text Box / Numeric Text Box</span></span>
* <span data-ttu-id="7fe40-106">Location</span><span class="sxs-lookup"><span data-stu-id="7fe40-106">Location</span></span>
* <span data-ttu-id="7fe40-107">Zone de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="7fe40-107">Attachment Box</span></span>
* <span data-ttu-id="7fe40-108">Case à cocher à sélection unique</span><span class="sxs-lookup"><span data-stu-id="7fe40-108">Single Select Check-Box</span></span>
* <span data-ttu-id="7fe40-109">Curseur avec zone de texte</span><span class="sxs-lookup"><span data-stu-id="7fe40-109">Slider with Text Box</span></span>
* <span data-ttu-id="7fe40-110">Contrôle de date</span><span class="sxs-lookup"><span data-stu-id="7fe40-110">Date Control</span></span>
* <span data-ttu-id="7fe40-111">Contrôle d’heure</span><span class="sxs-lookup"><span data-stu-id="7fe40-111">Time Control</span></span>
* <span data-ttu-id="7fe40-112">Zone de texte</span><span class="sxs-lookup"><span data-stu-id="7fe40-112">Text Area</span></span>
* <span data-ttu-id="7fe40-113">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="7fe40-113">Dropdown</span></span>


<span data-ttu-id="7fe40-114">Nous allons répertorier les modifications de fichier nécessaires pour activer le contrôle dans une carte personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7fe40-114">We will list down the file changes needed to enable the control in a custom card.</span></span> <span data-ttu-id="7fe40-115">Vous devrez ajouter les détails suivants dans les fichiers correspondants, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7fe40-115">You will need to add the following details in the corresponding files as given below.</span></span>

## <a name="creation-view"></a><span data-ttu-id="7fe40-116">Vue de création</span><span class="sxs-lookup"><span data-stu-id="7fe40-116">Creation view</span></span>
<span data-ttu-id="7fe40-117">Ce qui suit contient l’extrait de code qui doit se trouver dans une page (par exemple :  \<div id='page_1'\> ... \</div\> ) dans « CreationView.html ».</span><span class="sxs-lookup"><span data-stu-id="7fe40-117">The following contains the code snippet that should go inside a page (eg: \<div id='page_1'\>...\</div\>) in "CreationView.html".</span></span>

* <span data-ttu-id="7fe40-118">Zone de texte **/zone de texte numérique :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-118">**Text Box / Numeric Text Box:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="7fe40-119">Pour la zone de texte numérique, l’extrait de code reste identique.</span><span class="sxs-lookup"><span data-stu-id="7fe40-119">For the numeric text box, the code snippet remains the same.</span></span> <span data-ttu-id="7fe40-120">Seule la modification obligatoire est que le type d’entrée doit être « nombre » au lieu de « texte ».</span><span class="sxs-lookup"><span data-stu-id="7fe40-120">Only change required is that the input type should be "number" instead of "text".</span></span>

  `````
    <div class='section-div'>
    <div id='LABEL1' class='field-label'>
    </div>
    <input id='INPUT1' type='text' contenteditable='true' class='textbox-1'>
    </div>
  `````

* <span data-ttu-id="7fe40-121">**Emplacement :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné).</span><span class="sxs-lookup"><span data-stu-id="7fe40-121">**Location:** This control has a LABEL ID (to prompt the user as to what data the control is for).</span></span>

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
  
* <span data-ttu-id="7fe40-122">**Zone de pièces jointes :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour pointer vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-122">**Attachment Box:** This control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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
 
* <span data-ttu-id="7fe40-123">Case **à cocher à sélection unique :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID de case à cocher (pour pointer vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-123">**Single select Check-Box:** This control has a LABEL ID (to prompt the user as to what data the control is for) and a CHECKBOX ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="7fe40-124">L’ID doit être préfixé avec la case à cocher (par exemple : CHECKBOX1).</span><span class="sxs-lookup"><span data-stu-id="7fe40-124">The ID should be prefixed with CHECKBOX (eg: CHECKBOX1).</span></span> <span data-ttu-id="7fe40-125">Les ID des options individuelles doivent être mappés à la case à cocher parent.</span><span class="sxs-lookup"><span data-stu-id="7fe40-125">The IDs of the individual options should be mapped to the parent checkbox.</span></span> <span data-ttu-id="7fe40-126">De plus, ce contrôle ne peut pas être rendu facultatif par défaut, la première option est sélectionnée lors du rendu du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7fe40-126">Also, this control cannot be made optional as by default, the first option will be selected when the form is rendered.</span></span>

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
  
* <span data-ttu-id="7fe40-127">**Curseur avec zone de texte :** Ce contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour entrer une valeur numérique directement).</span><span class="sxs-lookup"><span data-stu-id="7fe40-127">**Slider with TextBox:** This control has a LABEL ID (to prompt the user as to what data the control is for) and a INPUT ID (to enter a numerical value directly).</span></span> <span data-ttu-id="7fe40-128">Il ne peut pas être rendu facultatif par défaut, car le curseur sera toujours initialisé avec une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fe40-128">It cannot be made optional as by default as the slider will always be initialized with a default value.</span></span>

  `````
    <div class='section-div slider-with-textbox'>
    <div id='LABEL6' class='field-label'>
    </div>
    <input id='INPUT6' type='range' class='slider-bar'>
    <input class='slider-textbox' type='number'>
    </input>
    </div>
  `````

* <span data-ttu-id="7fe40-129">**Contrôle de date :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-129">**Date Control:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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


* <span data-ttu-id="7fe40-130">**Contrôle de l’heure :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-130">**Time Control:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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
    
* <span data-ttu-id="7fe40-131">**Zone de texte :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-131">**Text Area:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>

  `````
    <div class='section-div'>
    <div id='LABEL9' class='field-label'>
    </div>
    <textarea id='INPUT9' contenteditable='true' class='text-area'>
    </textarea>
    </div>
  `````
 
* <span data-ttu-id="7fe40-132">**Liste déroulante :** Chaque contrôle possède un ID d’étiquette (pour inviter l’utilisateur à quelles données le contrôle est destiné) et un ID d’entrée (pour qu’il pointe vers la valeur qui doit être insérée).</span><span class="sxs-lookup"><span data-stu-id="7fe40-132">**Dropdown:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="7fe40-133">Ce contrôle ne peut pas être rendu facultatif.</span><span class="sxs-lookup"><span data-stu-id="7fe40-133">This control cannot be made optional.</span></span>

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

## <a name="summary-view"></a><span data-ttu-id="7fe40-134">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="7fe40-134">Summary View</span></span>
<span data-ttu-id="7fe40-135">Il s’agit de l’extrait de code qui doit se trouver dans le conteneur "SummaryView.html".</span><span class="sxs-lookup"><span data-stu-id="7fe40-135">This is the code snippet that should go inside container in "SummaryView.html".</span></span> <span data-ttu-id="7fe40-136">Le suffixe de la réponse dans l’ID est le numéro de question dans AppModel auquel la question a été mappée (en partant de 1).</span><span class="sxs-lookup"><span data-stu-id="7fe40-136">The suffix of ANSWER in the id is the question number in AppModel to which the question has been mapped (starting from 1).</span></span> <span data-ttu-id="7fe40-137">Vous trouverez ci-dessous un exemple de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7fe40-137">Below is a an example for any control.</span></span> <span data-ttu-id="7fe40-138">Le nombre de réponses dans le AppModel doit être égal au nombre de sections du SummaryView.html.</span><span class="sxs-lookup"><span data-stu-id="7fe40-138">The number of answers in the AppModel should be equal to the number of sections in the "SummaryView.html".</span></span>

  `````
      <div class='section-div-summary'>
      <div id='ANSWER_1' class='field-label-summary'>
      </div>
      <label class='answer-label'>
      </label>
      </div>
  ````` 
    
## <a name="appmodel-file"></a><span data-ttu-id="7fe40-139">Fichier AppModel</span><span class="sxs-lookup"><span data-stu-id="7fe40-139">AppModel File</span></span>
<span data-ttu-id="7fe40-140">Il s’agit de l’extrait de code qui doit figurer dans la section « AppModel.jsonConfig » où le modèle de données est défini, le titre correspond à l’affichage du Résumé correspondant aux données réelles entrées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7fe40-140">This is the code snippet that should go inside "AppModel.jsonConfig" where the data model is defined - the title will correspond to the what the Summary View will display corresponding to the actual data entered by the user.</span></span>
<span data-ttu-id="7fe40-141">Vous trouverez ci-dessous un exemple de contrôle TextBox.</span><span class="sxs-lookup"><span data-stu-id="7fe40-141">Below is a an example for TextBox control.</span></span> <span data-ttu-id="7fe40-142">Un format similaire doit également être suivi pour d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="7fe40-142">A similar format needs to be followed for other controls as well.</span></span> <span data-ttu-id="7fe40-143">Veuillez noter que pour les pièces jointes, le type doit être « AttachmentList » et pour location le type doit être « location ».</span><span class="sxs-lookup"><span data-stu-id="7fe40-143">Please note that for Attachment the type should be "AttachmentList" and for Location the type should be "Location".</span></span>
  ````` 
      {
      "title": "Name",
      "type": "Text"
      }
  `````

## <a name="configuration-file"></a><span data-ttu-id="7fe40-144">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="7fe40-144">Configuration File</span></span>
    
<span data-ttu-id="7fe40-145">Il s’agit de l’extrait de code qui doit figurer dans le fichier « Config.js ».</span><span class="sxs-lookup"><span data-stu-id="7fe40-145">This is the code snippet that should go inside "Config.js" file.</span></span> <span data-ttu-id="7fe40-146">Dans SUBMIT_IDS vous devez placer l’ID d’entrée du contrôle dans la même séquence que les questions sont présentes dans l’AppModel.</span><span class="sxs-lookup"><span data-stu-id="7fe40-146">In SUBMIT_IDS you need to put the INPUT ID of the control in the same sequence as the questions are present in the AppModel.</span></span> <span data-ttu-id="7fe40-147">Si vous souhaitez le faire facultatif, ajoutez-le dans le dictionnaire OPTIONAL_IDS avec le numéro de page correspondant-si aucun élément n’est facultatif dans une page, assignez un tableau vide à la page correspondante (comme indiqué dans l’exemple pour page_2).</span><span class="sxs-lookup"><span data-stu-id="7fe40-147">In case you want to make it optional, please add it in the OPTIONAL_IDS dictionary with corresponding page number - in case nothing in a page is optional, assign an empty array to the corresponding page (as seen in the example for page_2).</span></span> <span data-ttu-id="7fe40-148">Les étiquettes de question facultatives seront automatiquement ajoutées à la chaîne' (facultatif) 'lors du rendu du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7fe40-148">Optional question labels will automatically be appended with the string '(optional)' when the form is rendered.</span></span> <span data-ttu-id="7fe40-149">Vous trouverez ci-dessous un exemple de contrôle TextBox.</span><span class="sxs-lookup"><span data-stu-id="7fe40-149">Below is a an example for TextBox control.</span></span> <span data-ttu-id="7fe40-150">Tous les contrôles auront un format similaire.</span><span class="sxs-lookup"><span data-stu-id="7fe40-150">All controls will have a similar format.</span></span> <span data-ttu-id="7fe40-151">Notez que pour les images et l’emplacement, nous n’avons pas besoin d’une entrée dans SUBMIT_IDS.</span><span class="sxs-lookup"><span data-stu-id="7fe40-151">Please note that for Images and Location, we don't need an entry in SUBMIT_IDS.</span></span>

  `````
    var SUBMIT_IDS = ['INPUT1'];
    var OPTIONAL_IDS = {
    "page_1": ["INPUT1"],
    "page_2": []
    };// in case you have a page 2 where all questions are mandatory
  `````

## <a name="localized-strings-file---strings_enjson"></a><span data-ttu-id="7fe40-152">Fichier de chaînes localisées-strings_en.js</span><span class="sxs-lookup"><span data-stu-id="7fe40-152">Localized Strings File - strings_en.json</span></span>
<span data-ttu-id="7fe40-153">Il s’agit de l’extrait de code qui doit figurer dans le fichier de chaînes dans lequel les chaînes sont définies.</span><span class="sxs-lookup"><span data-stu-id="7fe40-153">This is the code snippet that should go inside the strings file where the strings are defined.</span></span> <span data-ttu-id="7fe40-154">Pour une zone de texte avec l’ID en tant que INPUT1, une étiquette est associée qui demande à l’utilisateur ce qu’est la question ; Il y a ensuite un espace réservé facultatif qui apparaît sous la forme d’un texte fantôme à l’intérieur de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="7fe40-154">For a textbox with ID as INPUT1 there is a label associated which prompts the user as to what the question is; then there is an optional placeholder which appears as a ghost-text inside the textbox.</span></span> <span data-ttu-id="7fe40-155">Il s’agit d’un exemple de contrôle TextBox.</span><span class="sxs-lookup"><span data-stu-id="7fe40-155">This is an example of Textbox control.</span></span> <span data-ttu-id="7fe40-156">Tous les contrôles auront le même format.</span><span class="sxs-lookup"><span data-stu-id="7fe40-156">All controls will have similar format.</span></span>

  `````
    "LABEL1": "Please enter your name",
    "INPUT1_placeholder": "Tap to enter name"
  `````

