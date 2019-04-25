# <a name="customizing-chatcanvascardview"></a><span data-ttu-id="d7fdb-101">Personnalisation de ChatCanvasCardView</span><span class="sxs-lookup"><span data-stu-id="d7fdb-101">Customizing ChatCanvasCardView</span></span>

<span data-ttu-id="d7fdb-102">Contrairement aux vues de création, de réponse et de résumé html, les affichages de conversation sont des affichages natifs.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-102">Unlike the creation, response and summary views that are html, chat views are native views.</span></span> <span data-ttu-id="d7fdb-103">Pour personnaliser la vue de la carte de conversation, vous devez fournir un JSON de la disposition de la carte, ainsi que les valeurs de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-103">To customize the chat card view, you will need to provide a json of the card layout as well as the values in the view.</span></span> <span data-ttu-id="d7fdb-104">En l'absence d'une vue de carte de canevas de conversation personnalisée, la valeur par défaut est affichage carte de conversation avec le texte du titre de l'application.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-104">In the absence of a customized chat canvas card view, the default would be chat card view with the text of app title.</span></span> 

## <a name="views-and-their-supported-properties"></a><span data-ttu-id="d7fdb-105">Vues et leurs propriétés prises en charge</span><span class="sxs-lookup"><span data-stu-id="d7fdb-105">Views and their supported properties</span></span>
<span data-ttu-id="d7fdb-106">Vous trouverez ci-dessous différents types de sous-vues/widgets, ainsi que leurs propriétés personnalisables.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-106">Below are different types of sub-views/widgets along with their customizable properties.</span></span> <span data-ttu-id="d7fdb-107">Peu de propriétés sont marquées avec <sup>iOS</sup> , indiquant qu'elles ne s'appliquent qu'à IOS _(et n'ont aucun effet sur Android)_.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-107">Few properties are marked with <sup>iOS</sup>  indicating that they are applicable only on iOS _(and will have no effect on android)_.</span></span>

### <a name="container--view"></a><span data-ttu-id="d7fdb-108">Conteneur/vue</span><span class="sxs-lookup"><span data-stu-id="d7fdb-108">Container / View</span></span>

<ol>
<li><span data-ttu-id="d7fdb-109">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="d7fdb-109">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="d7fdb-110"><sup>iOS</sup> visible</span><span class="sxs-lookup"><span data-stu-id="d7fdb-110">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="d7fdb-111">type _(n'importe quel type de sous-affichage mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-111">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="d7fdb-112">Margin/marginTop/marginRight/marginBottom/marginLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-112">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="d7fdb-113">Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-113">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="d7fdb-114">width</span><span class="sxs-lookup"><span data-stu-id="d7fdb-114">width</span></span></li>
<li><span data-ttu-id="d7fdb-115">height</span><span class="sxs-lookup"><span data-stu-id="d7fdb-115">height</span></span></li>
<li><span data-ttu-id="d7fdb-116">poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-116">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="d7fdb-117">backgroundColor _(uniquement le code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-117">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="d7fdb-118">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="d7fdb-118">cornerRadius</span></span></li>
<li><span data-ttu-id="d7fdb-119">borderWidthiOS/borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="d7fdb-119">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="d7fdb-120">enfants _(tableau de sous-affichages)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-120">children _(array of sub-views)_</span></span></li>
<li><span data-ttu-id="d7fdb-121">mise en page _(verticale/horizontale en cas d'inspécification, par défaut, verticale)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-121">layout _(vertical / horizontal � when unspecified, defaults to vertical)_</span></span></li>
<li><span data-ttu-id="d7fdb-122">verticalAlignment _(haut/bas/centre/stretchiOS-comment les enfants seront alignés verticalement)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-122">verticalAlignment _(top / bottom / center / stretchiOS - how children will be aligned vertically)_</span></span></li>
<li><span data-ttu-id="d7fdb-123">horizontalAlignment _ (Left/Right/Center/spaceBetween<sup>iOS</sup> /spaceAround<sup>iOS</sup>): comment les enfants seront alignés horizontalement. _</span><span class="sxs-lookup"><span data-stu-id="d7fdb-123">horizontalAlignment _(left / right / center / spaceBetween<sup>iOS</sup> / spaceAround<sup>iOS</sup>) - how children will be aligned horizontally._</span></span></li>
<li><span data-ttu-id="d7fdb-124">initialHeight<sup>iOS</sup> _une propriété iOS uniquement utilisée dans le conteneur de niveau supérieur qui est utilisée pour afficher la carte avant que la dimension exacte ne soit vérifiée. Il est vivement recommandé d'utiliser cette propriété pour une expérience plus homogène!_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-124">initialHeight<sup>iOS</sup> � _an iOS only property used in the topmost container that is used to render the card before the accurate dimension is ascertained. It is strongly advised to use this property for a smoother experience!_</span></span></li>
</ol>

### <a name="text"></a><span data-ttu-id="d7fdb-125">Text</span><span class="sxs-lookup"><span data-stu-id="d7fdb-125">Text</span></span>

<ol>
<li><span data-ttu-id="d7fdb-126">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="d7fdb-126">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="d7fdb-127"><sup>iOS</sup> visible</span><span class="sxs-lookup"><span data-stu-id="d7fdb-127">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="d7fdb-128">type _(n'importe quel type de sous-affichage mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-128">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="d7fdb-129">Margin/marginTop/marginRight/marginBottom/marginLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-129">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="d7fdb-130">Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-130">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="d7fdb-131">width</span><span class="sxs-lookup"><span data-stu-id="d7fdb-131">width</span></span></li>
<li><span data-ttu-id="d7fdb-132">height</span><span class="sxs-lookup"><span data-stu-id="d7fdb-132">height</span></span></li>
<li><span data-ttu-id="d7fdb-133">poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-133">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="d7fdb-134">backgroundColor _(uniquement le code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-134">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="d7fdb-135">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="d7fdb-135">cornerRadius</span></span></li>
<li><span data-ttu-id="d7fdb-136">borderWidthiOS/borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="d7fdb-136">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="d7fdb-137">chaîne</span><span class="sxs-lookup"><span data-stu-id="d7fdb-137">string</span></span></li>
<li><span data-ttu-id="d7fdb-138">FontSize _(famille de polices est toujours la valeur par défaut du système, pour éviter les problèmes de rendu)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-138">fontSize _(font family is always System's default, to avoid rendering issues)_</span></span></li>
<li><span data-ttu-id="d7fdb-139">textColor _(uniquement code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-139">textColor _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="d7fdb-140">ellipsizeMode _(Head/Middle/tail)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-140">ellipsizeMode _(head / middle / tail)_</span></span></li>
<li><span data-ttu-id="d7fdb-141">maxNumberOfLines _(0 pour aucune limite, sinon le texte est tronqué en fonction du ellipsizeMode)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-141">maxNumberOfLines _(0 for no limit, else text will be truncated as per ellipsizeMode)_</span></span></li>
</ol>


### <a name="image"></a><span data-ttu-id="d7fdb-142">Image</span><span class="sxs-lookup"><span data-stu-id="d7fdb-142">Image</span></span>

<ol>
<li><span data-ttu-id="d7fdb-143">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="d7fdb-143">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="d7fdb-144"><sup>iOS</sup> visible</span><span class="sxs-lookup"><span data-stu-id="d7fdb-144">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="d7fdb-145">type _(n'importe quel type de sous-affichage mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-145">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="d7fdb-146">Margin/marginTop/marginRight/marginBottom/marginLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-146">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="d7fdb-147">Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</span><span class="sxs-lookup"><span data-stu-id="d7fdb-147">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="d7fdb-148">width</span><span class="sxs-lookup"><span data-stu-id="d7fdb-148">width</span></span></li>
<li><span data-ttu-id="d7fdb-149">height</span><span class="sxs-lookup"><span data-stu-id="d7fdb-149">height</span></span></li>
<li><span data-ttu-id="d7fdb-150">poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-150">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="d7fdb-151">backgroundColor _(uniquement le code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-151">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="d7fdb-152">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="d7fdb-152">cornerRadius</span></span></li>
<li><span data-ttu-id="d7fdb-153">borderWidthiOS/borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="d7fdb-153">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="d7fdb-154">source</span><span class="sxs-lookup"><span data-stu-id="d7fdb-154">source</span></span></li>
<li><span data-ttu-id="d7fdb-155">contentMode _ (aspectFit/aspectFill/étirer/répéter<sup>iOS</sup>) _</span><span class="sxs-lookup"><span data-stu-id="d7fdb-155">contentMode _(aspectFit / aspectFill / stretch / repeat<sup>iOS</sup>)_</span></span></li>
</ol>



## <a name="binding-data-with-views"></a><span data-ttu-id="d7fdb-156">Liaison de données avec des vues</span><span class="sxs-lookup"><span data-stu-id="d7fdb-156">Binding data with views</span></span>
* <span data-ttu-id="d7fdb-157">__Form__</span><span class="sxs-lookup"><span data-stu-id="d7fdb-157">__Form__</span></span>
  * <span data-ttu-id="d7fdb-158">$\{Form. title}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-158">$\{Form.title}</span></span>
  * <span data-ttu-id="d7fdb-159">$\{Form. Expiry}- _Output est une chaîne de date-heure_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-159">$\{Form.expiry} - _output is a date-time string_</span></span>
  * <span data-ttu-id="d7fdb-160">$\{Form. questions}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-160">$\{Form.questions}</span></span>
  * <span data-ttu-id="d7fdb-161">$\{Form. questions. Length}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-161">$\{Form.questions.length}</span></span>
  * <span data-ttu-id="d7fdb-162">$\{Form. questions [questionId]. title}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-162">$\{Form.questions[questionId].title}</span></span>
  * <span data-ttu-id="d7fdb-163">$\{Form. questions [questionId]. options}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-163">$\{Form.questions[questionId].options}</span></span>
  * <span data-ttu-id="d7fdb-164">$\{Form. questions [questionId]. options. Length}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-164">$\{Form.questions[questionId].options.length}</span></span>
  * <span data-ttu-id="d7fdb-165">$\{Form. questions [questionId]. options [optionId]. Text}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-165">$\{Form.questions[questionId].options[optionId].text}</span></span>
  * <span data-ttu-id="d7fdb-166">$\{Form. questions [questionId]. options [optionId]. pictureUrl}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-166">$\{Form.questions[questionId].options[optionId].pictureUrl}</span></span>
  * <span data-ttu-id="d7fdb-167">$\{Form. Properties}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-167">$\{Form.properties}</span></span>
  * <span data-ttu-id="d7fdb-168">$\{Form. Properties. Length}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-168">$\{Form.properties.length}</span></span>
  * <span data-ttu-id="d7fdb-169">$\{Form. Properties [propertyName]}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-169">$\{Form.properties[propertyName]}</span></span>
  * <span data-ttu-id="d7fdb-170">$\{Form. Properties [propertyName]. Value}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-170">$\{Form.properties[propertyName].value}</span></span>
  * <span data-ttu-id="d7fdb-171">$\{Form. Properties [propertyName]. Length}- _pour la propriété Array/Set type_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-171">$\{Form.properties[propertyName].length} - _for Array/Set type property_</span></span>
* <span data-ttu-id="d7fdb-172">__MyLatestResponse__</span><span class="sxs-lookup"><span data-stu-id="d7fdb-172">__MyLatestResponse__</span></span>
  * <span data-ttu-id="d7fdb-173">$\{MyLatestResponse. sendTime}- _Output est une chaîne date-heure_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-173">$\{MyLatestResponse.sendTime} - _output is a date-time string_</span></span>
  * <span data-ttu-id="d7fdb-174">$\{MyLatestResponse. questionToAnswerMap [questionId]}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-174">$\{MyLatestResponse.questionToAnswerMap[questionId]}</span></span>
* <span data-ttu-id="d7fdb-175">__Summary__</span><span class="sxs-lookup"><span data-stu-id="d7fdb-175">__Summary__</span></span>
  * <span data-ttu-id="d7fdb-176">$\{Résumé. totalResponseCount}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-176">$\{Summary.totalResponseCount}</span></span>
  * <span data-ttu-id="d7fdb-177">$\{Résumé. totalParticipantsCount}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-177">$\{Summary.totalParticipantsCount}</span></span>
  * <span data-ttu-id="d7fdb-178">$\{Résumé. targetResponderCount}</span><span class="sxs-lookup"><span data-stu-id="d7fdb-178">$\{Summary.targetResponderCount}</span></span>

<span data-ttu-id="d7fdb-179">Par ailleurs, il est possible d'utiliser ces variables comme espaces réservés, comme:</span><span class="sxs-lookup"><span data-stu-id="d7fdb-179">Also one can use these variables as placeholders, like:</span></span>  
<span data-ttu-id="d7fdb-180">_«Merci pour votre rapport sur les actualités: $ {Form. Properties [newsDescription]. Value}»_</span><span class="sxs-lookup"><span data-stu-id="d7fdb-180">_"Thanks for your news report: ${Form.properties[newsDescription].value}"_</span></span>

## <a name="operations"></a><span data-ttu-id="d7fdb-181">Opérations</span><span class="sxs-lookup"><span data-stu-id="d7fdb-181">Operations</span></span>

<span data-ttu-id="d7fdb-182">Dans certains cas, il peut être nécessaire que différents utilisateurs aient besoin d'afficher différentes cartes de conversation, qui peuvent être basées sur certains attributs.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-182">In some scenarios, there may arise a need where different users may need to view different chat card, that may be based on some attributes.</span></span> <span data-ttu-id="d7fdb-183">Afin d'activer ce type de scénario, Kaizala fournit des [opérateurs](Operator.md), qui permet aux créateurs d'actions de personnaliser les vues de carte de conversation pour la même instance d'action différemment pour différents scénarios/utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-183">In order to enable such scenarios, Kaizala provides [operators](Operator.md), that enables Action Creators to personalise chat card views for the same Action instance differently for different scenarios/users.</span></span>

<span data-ttu-id="d7fdb-184">Par exemple, vous pouvez choisir d'afficher une autre vue carte pour les utilisateurs qui n'ont pas effectué le travail et une autre vue carte pour les utilisateurs qui ont effectué le travail.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-184">For example, you may choose to show a different card view for users who have not completed the job, and a different card view for users who have completed the job.</span></span> <span data-ttu-id="d7fdb-185">Cette opération peut être étendue à n'importe quel type de scénario susceptible de se produire.</span><span class="sxs-lookup"><span data-stu-id="d7fdb-185">This can be extended to any type of scenarios that may arise.</span></span>

## <a name="how-to-provide-the-json-schema"></a><span data-ttu-id="d7fdb-186">Comment fournir le schéma JSON</span><span class="sxs-lookup"><span data-stu-id="d7fdb-186">How to provide the json schema</span></span>
<span data-ttu-id="d7fdb-187">Dans le fichier manifeste _(package. Json)_ d'un package, placez le nom de fichier JSON sous la clé **SourceLocation** dans **ChatCanvasCardView** Voici un exemple de capture instantanée de package. JSON:</span><span class="sxs-lookup"><span data-stu-id="d7fdb-187">In the manifest _(package.json)_ file of a package put the JSON file name under **sourceLocation** key in **ChatCanvasCardView** Below is a sample snapshot from package.json:</span></span>

![capture instantanée de package. JSON](./chatcardviewjson.png)

## <a name="example-chatcanvascardview-source-file"></a><span data-ttu-id="d7fdb-189">Exemple de fichier source ChatCanvasCardView</span><span class="sxs-lookup"><span data-stu-id="d7fdb-189">Example ChatCanvasCardView source file</span></span>
```json
{
    "schemaVersion": 1,
    "schema": {
        "type": "container",
        "initialHeight": 300,
        "layout": "vertical",
        "children": [
            {
                "type": "text",
                "paddingLeft": 10,
                "paddingRight": 10,
                "string": "${Form.properties[Property1].value}",
                "fontSize": 18,
                "fontStyle": "bold",
                "textColor": "#CE222E",
                "textAlignment": "left",
                "maxNumberOfLines": 2,
                "marginBottom": 10
            },
            {
                "type": "image",
                "height": 160,
                "source": "${Form.properties[CoverImageProperty].value}",
                "contentMode": "aspectFit",
                "backgroundColor": "#263749",
                "marginBottom": 10
            },
            {
                "type": "text",
                "paddingLeft": 10,
                "paddingRight": 10,
                "string": "${Form.properties[Property2].value}",
                "fontSize": 18,
                "fontStyle": "bold",
                "textColor": "#32495f",
                "textAlignment": "left",
                "maxNumberOfLines": 4,
                "marginBottom": 0
            }
        ]
    }
}
