# <a name="customizing-chatcanvascardview"></a><span data-ttu-id="3cf4e-101">Personnalisation de ChatCanvasCardView</span><span class="sxs-lookup"><span data-stu-id="3cf4e-101">Customizing ChatCanvasCardView</span></span>

<span data-ttu-id="3cf4e-102">Contrairement à la création, réponse et affichages de synthèse sont html, conversation affichages sont native.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-102">Unlike the creation, response and summary views that are html, chat views are native views.</span></span> <span data-ttu-id="3cf4e-103">Pour personnaliser l’affichage de carte de conversation, vous devrez fournir un json de la disposition de la carte, ainsi que les valeurs dans la vue.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-103">To customize the chat card view, you will need to provide a json of the card layout as well as the values in the view.</span></span> <span data-ttu-id="3cf4e-104">En l’absence d’une conversation personnalisée un canevas affichage carte, la valeur par défaut est affichage de carte de conversation avec le texte de titre de l’application.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-104">In the absence of a customized chat canvas card view, the default would be chat card view with the text of app title.</span></span> 

## <a name="views-and-their-supported-properties"></a><span data-ttu-id="3cf4e-105">Vues et leurs propriétés prises en charge</span><span class="sxs-lookup"><span data-stu-id="3cf4e-105">Views and their supported properties</span></span>
<span data-ttu-id="3cf4e-106">Vous trouverez ci-dessous les différents types de sub-views/widgets ainsi que leurs propriétés personnalisables.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-106">Below are different types of sub-views/widgets along with their customizable properties.</span></span> <span data-ttu-id="3cf4e-107">Certaines propriétés sont marquées avec <sup>iOS</sup> indiquant qu’ils sont applicables uniquement sur iOS _(et n’a aucun effet sur android)_.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-107">Few properties are marked with <sup>iOS</sup>  indicating that they are applicable only on iOS _(and will have no effect on android)_.</span></span>

### <a name="container--view"></a><span data-ttu-id="3cf4e-108">Conteneur / afficher</span><span class="sxs-lookup"><span data-stu-id="3cf4e-108">Container / View</span></span>

<ol>
<li><span data-ttu-id="3cf4e-109">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="3cf4e-109">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="3cf4e-110">visible<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="3cf4e-110">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="3cf4e-111">Tapez _(tous les types de vue secondaire que nous avons mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-111">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="3cf4e-112">marge / marginTop / marginRight / marginBottom / marginLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-112">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="3cf4e-113">remplissage / paddingTop / paddingRight / paddingBottom / paddingLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-113">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="3cf4e-114">width</span><span class="sxs-lookup"><span data-stu-id="3cf4e-114">width</span></span></li>
<li><span data-ttu-id="3cf4e-115">height</span><span class="sxs-lookup"><span data-stu-id="3cf4e-115">height</span></span></li>
<li><span data-ttu-id="3cf4e-116">poids _(% taux de parent largeur/hauteur de la vue en cas de mises en page horizontaux/verticaux respectivement)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-116">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="3cf4e-117">backgroundColor _(uniquement code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-117">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="3cf4e-118">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="3cf4e-118">cornerRadius</span></span></li>
<li><span data-ttu-id="3cf4e-119">borderWidthiOS / borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="3cf4e-119">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="3cf4e-120">Children _(tableau de vues sous-sites)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-120">children _(array of sub-views)_</span></span></li>
<li><span data-ttu-id="3cf4e-121">mise en page _(quand verticale / horizontale n’est pas spécifié, par défaut verticale)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-121">layout _(vertical / horizontal � when unspecified, defaults to vertical)_</span></span></li>
<li><span data-ttu-id="3cf4e-122">verticalAlignment _(haut / bas / centre / stretchiOS - comment enfants seront alignés verticalement)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-122">verticalAlignment _(top / bottom / center / stretchiOS - how children will be aligned vertically)_</span></span></li>
<li><span data-ttu-id="3cf4e-123">horizontalAlignment _ (gauche/droite/centre/spaceBetween<sup></sup> iOS/spaceAround<sup>iOS</sup>) - comment enfants seront alignés horizontalement. _</span><span class="sxs-lookup"><span data-stu-id="3cf4e-123">horizontalAlignment _(left / right / center / spaceBetween<sup>iOS</sup> / spaceAround<sup>iOS</sup>) - how children will be aligned horizontally._</span></span></li>
<li><span data-ttu-id="3cf4e-124">initialHeight<sup>iOS</sup> _une seule propriété iOS utilisée dans le conteneur de plus haut est utilisé pour afficher la carte avant la dimension précise est établie. Il est fortement recommandé d’utiliser cette propriété pour une meilleure expérience !_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-124">initialHeight<sup>iOS</sup> � _an iOS only property used in the topmost container that is used to render the card before the accurate dimension is ascertained. It is strongly advised to use this property for a smoother experience!_</span></span></li>
</ol>

### <a name="text"></a><span data-ttu-id="3cf4e-125">Texte</span><span class="sxs-lookup"><span data-stu-id="3cf4e-125">Text</span></span>

<ol>
<li><span data-ttu-id="3cf4e-126">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="3cf4e-126">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="3cf4e-127">visible<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="3cf4e-127">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="3cf4e-128">Tapez _(tous les types de vue secondaire que nous avons mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-128">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="3cf4e-129">marge / marginTop / marginRight / marginBottom / marginLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-129">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="3cf4e-130">remplissage / paddingTop / paddingRight / paddingBottom / paddingLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-130">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="3cf4e-131">width</span><span class="sxs-lookup"><span data-stu-id="3cf4e-131">width</span></span></li>
<li><span data-ttu-id="3cf4e-132">height</span><span class="sxs-lookup"><span data-stu-id="3cf4e-132">height</span></span></li>
<li><span data-ttu-id="3cf4e-133">poids _(% taux de parent largeur/hauteur de la vue en cas de mises en page horizontaux/verticaux respectivement)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-133">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="3cf4e-134">backgroundColor _(uniquement code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-134">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="3cf4e-135">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="3cf4e-135">cornerRadius</span></span></li>
<li><span data-ttu-id="3cf4e-136">borderWidthiOS / borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="3cf4e-136">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="3cf4e-137">chaîne</span><span class="sxs-lookup"><span data-stu-id="3cf4e-137">string</span></span></li>
<li><span data-ttu-id="3cf4e-138">fontSize _(famille de polices est toujours du système par défaut, pour éviter les problèmes de rendu)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-138">fontSize _(font family is always System's default, to avoid rendering issues)_</span></span></li>
<li><span data-ttu-id="3cf4e-139">textColor _(uniquement code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-139">textColor _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="3cf4e-140">ellipsizeMode _(head / intermédiaire / Queue)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-140">ellipsizeMode _(head / middle / tail)_</span></span></li>
<li><span data-ttu-id="3cf4e-141">maxNumberOfLines _(0 pour aucune limite autre texte sera tronqué selon ellipsizeMode)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-141">maxNumberOfLines _(0 for no limit, else text will be truncated as per ellipsizeMode)_</span></span></li>
</ol>


### <a name="image"></a><span data-ttu-id="3cf4e-142">Image</span><span class="sxs-lookup"><span data-stu-id="3cf4e-142">Image</span></span>

<ol>
<li><span data-ttu-id="3cf4e-143">ID (facultatif, mais doit être unique)</span><span class="sxs-lookup"><span data-stu-id="3cf4e-143">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="3cf4e-144">visible<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="3cf4e-144">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="3cf4e-145">Tapez _(tous les types de vue secondaire que nous avons mentionné ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-145">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="3cf4e-146">marge / marginTop / marginRight / marginBottom / marginLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-146">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="3cf4e-147">remplissage / paddingTop / paddingRight / paddingBottom / paddingLeft</span><span class="sxs-lookup"><span data-stu-id="3cf4e-147">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="3cf4e-148">width</span><span class="sxs-lookup"><span data-stu-id="3cf4e-148">width</span></span></li>
<li><span data-ttu-id="3cf4e-149">height</span><span class="sxs-lookup"><span data-stu-id="3cf4e-149">height</span></span></li>
<li><span data-ttu-id="3cf4e-150">poids _(% taux de parent largeur/hauteur de la vue en cas de mises en page horizontaux/verticaux respectivement)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-150">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="3cf4e-151">backgroundColor _(uniquement code hexadécimal autorisé ici)_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-151">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="3cf4e-152">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="3cf4e-152">cornerRadius</span></span></li>
<li><span data-ttu-id="3cf4e-153">borderWidthiOS / borderColoriOS</span><span class="sxs-lookup"><span data-stu-id="3cf4e-153">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="3cf4e-154">source</span><span class="sxs-lookup"><span data-stu-id="3cf4e-154">source</span></span></li>
<li><span data-ttu-id="3cf4e-155">contentMode _ (aspectFit/aspectFill/étirer/répétez<sup>iOS</sup>) _</span><span class="sxs-lookup"><span data-stu-id="3cf4e-155">contentMode _(aspectFit / aspectFill / stretch / repeat<sup>iOS</sup>)_</span></span></li>
</ol>



## <a name="binding-data-with-views"></a><span data-ttu-id="3cf4e-156">Liaison de données avec des vues</span><span class="sxs-lookup"><span data-stu-id="3cf4e-156">Binding data with views</span></span>
* <span data-ttu-id="3cf4e-157">__Formulaire__</span><span class="sxs-lookup"><span data-stu-id="3cf4e-157">__Form__</span></span>
  * <span data-ttu-id="3cf4e-158">$\{Form.Title}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-158">$\{Form.title}</span></span>
  * <span data-ttu-id="3cf4e-159">$\{Form.Expiry} - _sortie est une chaîne de date-heure_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-159">$\{Form.expiry} - _output is a date-time string_</span></span>
  * <span data-ttu-id="3cf4e-160">$\{Form.questions}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-160">$\{Form.questions}</span></span>
  * <span data-ttu-id="3cf4e-161">$\{Form.questions.Length}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-161">$\{Form.questions.length}</span></span>
  * <span data-ttu-id="3cf4e-162">$\{Form.questions[questionId].Title}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-162">$\{Form.questions[questionId].title}</span></span>
  * <span data-ttu-id="3cf4e-163">$\{Form.questions[questionId].Options}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-163">$\{Form.questions[questionId].options}</span></span>
  * <span data-ttu-id="3cf4e-164">$\{Form.questions[questionId].Options.Length}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-164">$\{Form.questions[questionId].options.length}</span></span>
  * <span data-ttu-id="3cf4e-165">$\{Form.questions[questionId].Options[optionId].Text}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-165">$\{Form.questions[questionId].options[optionId].text}</span></span>
  * <span data-ttu-id="3cf4e-166">$\{Form.questions[questionId].Options[optionId].pictureUrl}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-166">$\{Form.questions[questionId].options[optionId].pictureUrl}</span></span>
  * <span data-ttu-id="3cf4e-167">$\{Form.Properties}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-167">$\{Form.properties}</span></span>
  * <span data-ttu-id="3cf4e-168">$\{Form.Properties.Length}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-168">$\{Form.properties.length}</span></span>
  * <span data-ttu-id="3cf4e-169">$\{Form.Properties[PropertyName]}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-169">$\{Form.properties[propertyName]}</span></span>
  * <span data-ttu-id="3cf4e-170">$\{Form.Properties[PropertyName].Value}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-170">$\{Form.properties[propertyName].value}</span></span>
  * <span data-ttu-id="3cf4e-171">$\{Form.Properties[PropertyName].Length} - _pour tableau/définir la propriété type_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-171">$\{Form.properties[propertyName].length} - _for Array/Set type property_</span></span>
* <span data-ttu-id="3cf4e-172">__MyLatestResponse__</span><span class="sxs-lookup"><span data-stu-id="3cf4e-172">__MyLatestResponse__</span></span>
  * <span data-ttu-id="3cf4e-173">$\{MyLatestResponse.sendTime} - _sortie est une chaîne de date-heure_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-173">$\{MyLatestResponse.sendTime} - _output is a date-time string_</span></span>
  * <span data-ttu-id="3cf4e-174">$\{MyLatestResponse.questionToAnswerMap[questionId]}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-174">$\{MyLatestResponse.questionToAnswerMap[questionId]}</span></span>
* <span data-ttu-id="3cf4e-175">__Résumé__</span><span class="sxs-lookup"><span data-stu-id="3cf4e-175">__Summary__</span></span>
  * <span data-ttu-id="3cf4e-176">$\{Summary.totalResponseCount}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-176">$\{Summary.totalResponseCount}</span></span>
  * <span data-ttu-id="3cf4e-177">$\{Summary.totalParticipantsCount}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-177">$\{Summary.totalParticipantsCount}</span></span>
  * <span data-ttu-id="3cf4e-178">$\{Summary.targetResponderCount}</span><span class="sxs-lookup"><span data-stu-id="3cf4e-178">$\{Summary.targetResponderCount}</span></span>

<span data-ttu-id="3cf4e-179">Un peut également utiliser ces variables comme espaces réservés, tels que :</span><span class="sxs-lookup"><span data-stu-id="3cf4e-179">Also one can use these variables as placeholders, like:</span></span>  
<span data-ttu-id="3cf4e-180">_« Je vous remercie de votre rapport news : ${Form.properties[newsDescription].value} »_</span><span class="sxs-lookup"><span data-stu-id="3cf4e-180">_"Thanks for your news report: ${Form.properties[newsDescription].value}"_</span></span>

## <a name="operations"></a><span data-ttu-id="3cf4e-181">Opérations</span><span class="sxs-lookup"><span data-stu-id="3cf4e-181">Operations</span></span>

<span data-ttu-id="3cf4e-182">Dans certains scénarios, il peut se produire un besoin où différents utilisateurs devront peut-être afficher la carte de conversation différent, qui peut-être être basée sur certains attributs.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-182">In some scenarios, there may arise a need where different users may need to view different chat card, that may be based on some attributes.</span></span> <span data-ttu-id="3cf4e-183">Afin d’activer des scénarios, Kaizala fournit des [opérateurs](Operator.md), qui permet aux créateurs de Action personnaliser les affichages de carte de conversation pour la même instance d’Action différentes pour différents scénarios/utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-183">In order to enable such scenarios, Kaizala provides [operators](Operator.md), that enables Action Creators to personalise chat card views for the same Action instance differently for different scenarios/users.</span></span>

<span data-ttu-id="3cf4e-184">Par exemple, vous pouvez choisir d’afficher une vue carte différentes pour les utilisateurs qui n’ont pas terminé le travail et un affichage autre carte pour les utilisateurs qui ont terminé le travail.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-184">For example, you may choose to show a different card view for users who have not completed the job, and a different card view for users who have completed the job.</span></span> <span data-ttu-id="3cf4e-185">Cela peut être étendu à n’importe quel type de scénarios qui peuvent survenir.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-185">This can be extended to any type of scenarios that may arise.</span></span>

## <a name="how-to-provide-the-json-schema"></a><span data-ttu-id="3cf4e-186">Comment fournir le schéma json</span><span class="sxs-lookup"><span data-stu-id="3cf4e-186">How to provide the json schema</span></span>
<span data-ttu-id="3cf4e-187">Dans le fichier manifeste _(package.json)_ d’un package de placer le nom de fichier JSON sous **sourceLocation** clé **ChatCanvasCardView** ci-dessous est un instantané de package.json :</span><span class="sxs-lookup"><span data-stu-id="3cf4e-187">In the manifest _(package.json)_ file of a package put the JSON file name under **sourceLocation** key in **ChatCanvasCardView** Below is a sample snapshot from package.json:</span></span>

![capture instantanée de package.json](./chatcardviewjson.png)

## <a name="example-chatcanvascardview-source-file"></a><span data-ttu-id="3cf4e-189">Exemple de fichier de code source ChatCanvasCardView</span><span class="sxs-lookup"><span data-stu-id="3cf4e-189">Example ChatCanvasCardView source file</span></span>
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
