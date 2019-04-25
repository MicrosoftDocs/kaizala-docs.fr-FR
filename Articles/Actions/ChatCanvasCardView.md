# <a name="customizing-chatcanvascardview"></a>Personnalisation de ChatCanvasCardView

Contrairement aux vues de création, de réponse et de résumé html, les affichages de conversation sont des affichages natifs. Pour personnaliser la vue de la carte de conversation, vous devez fournir un JSON de la disposition de la carte, ainsi que les valeurs de l'affichage. En l'absence d'une vue de carte de canevas de conversation personnalisée, la valeur par défaut est affichage carte de conversation avec le texte du titre de l'application. 

## <a name="views-and-their-supported-properties"></a>Vues et leurs propriétés prises en charge
Vous trouverez ci-dessous différents types de sous-vues/widgets, ainsi que leurs propriétés personnalisables. Peu de propriétés sont marquées avec <sup>iOS</sup> , indiquant qu'elles ne s'appliquent qu'à IOS _(et n'ont aucun effet sur Android)_.

### <a name="container--view"></a>Conteneur/vue

<ol>
<li>ID (facultatif, mais doit être unique)</li>
<li><sup>iOS</sup> visible</li>
<li>type _(n'importe quel type de sous-affichage mentionné ici)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</li>
<li>backgroundColor _(uniquement le code hexadécimal autorisé ici)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>enfants _(tableau de sous-affichages)_</li>
<li>mise en page _(verticale/horizontale en cas d'inspécification, par défaut, verticale)_</li>
<li>verticalAlignment _(haut/bas/centre/stretchiOS-comment les enfants seront alignés verticalement)_</li>
<li>horizontalAlignment _ (Left/Right/Center/spaceBetween<sup>iOS</sup> /spaceAround<sup>iOS</sup>): comment les enfants seront alignés horizontalement. _</li>
<li>initialHeight<sup>iOS</sup> _une propriété iOS uniquement utilisée dans le conteneur de niveau supérieur qui est utilisée pour afficher la carte avant que la dimension exacte ne soit vérifiée. Il est vivement recommandé d'utiliser cette propriété pour une expérience plus homogène!_</li>
</ol>

### <a name="text"></a>Text

<ol>
<li>ID (facultatif, mais doit être unique)</li>
<li><sup>iOS</sup> visible</li>
<li>type _(n'importe quel type de sous-affichage mentionné ici)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</li>
<li>backgroundColor _(uniquement le code hexadécimal autorisé ici)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>chaîne</li>
<li>FontSize _(famille de polices est toujours la valeur par défaut du système, pour éviter les problèmes de rendu)_</li>
<li>textColor _(uniquement code hexadécimal autorisé ici)_</li>
<li>ellipsizeMode _(Head/Middle/tail)_</li>
<li>maxNumberOfLines _(0 pour aucune limite, sinon le texte est tronqué en fonction du ellipsizeMode)_</li>
</ol>


### <a name="image"></a>Image

<ol>
<li>ID (facultatif, mais doit être unique)</li>
<li><sup>iOS</sup> visible</li>
<li>type _(n'importe quel type de sous-affichage mentionné ici)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>poids _(pourcentage de la largeur/hauteur de la vue parent en cas de disposition horizontale/verticale, respectivement)_</li>
<li>backgroundColor _(uniquement le code hexadécimal autorisé ici)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>source</li>
<li>contentMode _ (aspectFit/aspectFill/étirer/répéter<sup>iOS</sup>) _</li>
</ol>



## <a name="binding-data-with-views"></a>Liaison de données avec des vues
* __Form__
  * $\{Form. title}
  * $\{Form. Expiry}- _Output est une chaîne de date-heure_
  * $\{Form. questions}
  * $\{Form. questions. Length}
  * $\{Form. questions [questionId]. title}
  * $\{Form. questions [questionId]. options}
  * $\{Form. questions [questionId]. options. Length}
  * $\{Form. questions [questionId]. options [optionId]. Text}
  * $\{Form. questions [questionId]. options [optionId]. pictureUrl}
  * $\{Form. Properties}
  * $\{Form. Properties. Length}
  * $\{Form. Properties [propertyName]}
  * $\{Form. Properties [propertyName]. Value}
  * $\{Form. Properties [propertyName]. Length}- _pour la propriété Array/Set type_
* __MyLatestResponse__
  * $\{MyLatestResponse. sendTime}- _Output est une chaîne date-heure_
  * $\{MyLatestResponse. questionToAnswerMap [questionId]}
* __Summary__
  * $\{Résumé. totalResponseCount}
  * $\{Résumé. totalParticipantsCount}
  * $\{Résumé. targetResponderCount}

Par ailleurs, il est possible d'utiliser ces variables comme espaces réservés, comme:  
_«Merci pour votre rapport sur les actualités: $ {Form. Properties [newsDescription]. Value}»_

## <a name="operations"></a>Opérations

Dans certains cas, il peut être nécessaire que différents utilisateurs aient besoin d'afficher différentes cartes de conversation, qui peuvent être basées sur certains attributs. Afin d'activer ce type de scénario, Kaizala fournit des [opérateurs](Operator.md), qui permet aux créateurs d'actions de personnaliser les vues de carte de conversation pour la même instance d'action différemment pour différents scénarios/utilisateurs.

Par exemple, vous pouvez choisir d'afficher une autre vue carte pour les utilisateurs qui n'ont pas effectué le travail et une autre vue carte pour les utilisateurs qui ont effectué le travail. Cette opération peut être étendue à n'importe quel type de scénario susceptible de se produire.

## <a name="how-to-provide-the-json-schema"></a>Comment fournir le schéma JSON
Dans le fichier manifeste _(package. Json)_ d'un package, placez le nom de fichier JSON sous la clé **SourceLocation** dans **ChatCanvasCardView** Voici un exemple de capture instantanée de package. JSON:

![capture instantanée de package. JSON](./chatcardviewjson.png)

## <a name="example-chatcanvascardview-source-file"></a>Exemple de fichier source ChatCanvasCardView
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
