# <a name="chat-card-customization---operators"></a>Personnalisation d’une carte - opérateurs de conversation 

Dans certains scénarios, il peut se produire un besoin où différents utilisateurs devront peut-être afficher la carte de conversation différent, qui peut-être être basée sur certains attributs. Afin d’activer des scénarios, Kaizala fournit des opérateurs, qui permet aux créateurs de Action de personnaliser les vues de carte de conversation pour la même instance d’Action différentes pour différents scénarios/utilisateurs.

## <a name="lets-take-an-example"></a>Prenons un exemple :

Supposons que nous voulons afficher la vue de carte différemment à l’expéditeur à ses destinataires. À l’aide des opérateurs, nous pouvons obtenir facilement ce scénario, sous est l’affichage conversation personnalisé JSON pour cela :  


```json

                  { 

                      "schemaVersion": 3, 

                      "schema": { 

                        "type": "container", 

                        "layout": "vertical", 

                        "children": [ 

                          { 

                            "type": "text", 

                            "string": "Title: ${Form.title}" 

                          }, 

                          { 

                            "type": "text", 

                            "string": "Who am I: ${Operators.custom_text}" 

                          } 

                        ] 

                      }, 

                      "Operators": { 

                        "custom_text": { 

                          "operator": "conditional_value", 

                          "condition": { 

                            "operator": "is_it_me", 

                            "value": { 

                              "operator": "property_value", 

                              "property": "creator", 

                              "src": "local" 

                            } 

                          }, 

                          "value": "Sender", 

                          "default": "Receiver" 

                        } 

                      } 

                  } 
```

Ici, vous pouvez observer cet opérateur « conditional_value » obtenir la valeur de type Boolean à partir de l’opérateur imbriquée « is_it_me » plus imbriqué avec l’opérateur « nom ». De même, il peut facilement être étendu à n’importe lequel de ces scénarios, même complexe un. 

 
## <a name="list-of-supported-operators"></a>Liste des opérateurs pris en charge : 

> **Remarque** : les variables x, y, z utilisés dans les exemples de syntaxe, peuvent être des valeurs simples ou des résultats renvoyés par des opérateurs imbriqués 


| Nom de l’opérateur |Nom de paramètre |Type de paramètre |Fonctionnalités  |Syntaxe |Syntaxe réduite | Remarque |
|--------|------|------|----|----|----|----|
|Valeur conditionnelle  |1. condition 2. Valeur 3. Default (Défaut)|1. valeur booléenne 2. Valeur JSON 3. Valeur JSON | Cet opérateur est utilisé pour renvoyer une valeur spécifiée, si une condition définie est true. Si la condition a la valeur false, elle renvoie la valeur false.|{</br>« opérateur » : « conditional_value », « condition » :, « valeur x » : {y}, « default » : {z}</br>}| [« conditional_value », X, Y, Z] ||
|Égal à |1. valeur de 2 valeur |    1. chaîne 2 |Cet opérateur retourne la valeur true si les valeurs fournies (valeur1, valeur2) sont égales. Sinon, elle renvoie la valeur false |    {</br>« opérateur » : « eq », « value1 » : x, « valeur2 » : y </br>} |[« eq », x, y] ||
|FormatProfileName  |1. propriété 2. Src |1. PropertyType 2 de chaîne| Obtient la propriété Src « PropertyType » et met en forme de la liste des ID utilisateur en tant que :</br></br>« < nom d’utilisateur 1 > & n plus » </br></br>n est le nombre d’utilisateurs présents dans la liste - 1 |{</br>« opérateur » : « format_profile_names »,</br>« propriété » : x, « src » : PropertyType</br>}|[« format_profile_names », PropertyType, x] |PropertyType</br>{</br>  serveur local,</br>} </br></br>1. cet opérateur suppose que la propriété x fourni renvoie le tableau des ID utilisateur </br></br>2. UserName1 vous est si l’utilisateur connecté actuel est présent dans la liste des ID utilisateur.|
|FormatString|1. format 2. Agrs|1. tableau d’arguments de chaîne 2 prévu par la chaîne de Format|Cet opérateur permet de mettre en forme une chaîne à l’aide des spécificateurs de format.</br></br>Cet opérateur est identique à tout autre format chaîne opérateur présent dans RPC ou java |{</br>« opérateur » : « format_string », « format » : x, « args » : [y, z...]</br>}|[« format_string », x, [y, z …]]|X peut contenir les spécificateurs comme %s, %d etc. et les opérateurs attend les arguments à présent de même type dans le même ordre </br></br>Pour par exemple, la chaîne peut être</br>{</br>« opérateur » : « format_string »,</br>« format » : « Mon nom est %s et mon âge est %d, »</br>« args » : [y, z]</br>}</br></br>Où y est une variable de chaîne et z est un entier|
|IsCurrentUser|1 valeur de|1. uuid compare l’uuid fourni (UserId) avec l’uuid (UserId) de l’utilisateur actuellement connecté. Elle renvoie la valeur true si elle correspond au et renvoie la valeur false dans le cas contraire |{</br>« opérateur » : « is_it_me »,</br>« valeur » : x</br>}|[« is_it_me » x]|
|JSONPathValue|1. 1. Chemin d’accès de 2 entité|1 le chemin d’accès valide json EntityType 2| Extrait la valeur résidant dans la clé dans json entité du type donné.  Elle renvoie la première valeur détectée dans le chemin d’accès. |{</br>« opérateur » : « jsonpath_value »,</br>« entité » : EntityType,</br>« chemin d’accès » : ValidJsonPath</br>}|[« jsonpath_value », EntityType, ValidJsonPath]|{</br>« opérateur » :</br>« jsonpath_value »,</br>« entité » : Message,</br>« chemin d’accès » : « $... SenderName »</br>}</br></br>"$.." Parcourir de manière récursive</br></br>"$." Parcourir uniquement 1er niveau d’entité|
|MessageConversationName|1. valeur|1. messageId|Renvoie le nom de la conversation à laquelle le message avec donné messageId appartient.|{« opérateur » : « message_conversation_name », « valeur » : x}|[« message_conversation_name », x]|
|MessageCreationTime|1. valeur|1. messageId|Retourne l’horodatage lisible humaine de chaîne pour l’horodatage de la création du message avec un donné messageId |{</br>« opérateur » : « message_creation_time »,</br>« valeur » : x</br>}|[« message_creation_time », x]|
|ProfileName|1. id de|1. uuid|Renvoyer le nom complet de l’utilisateur lorsque uuid (UserId) est fourni. |{</br>« opérateur » : « saisie », « id » : x</br>}|[« saisie », x]|
|PropertyValue|1.dans Src 2, propriété|1 chaîne de 2 PropertyType|Obtient la propriété de la Src PropertyType|{</br>« opérateur » : « nom »,</br>« propriété » : x, « src » : PropertyType</br>}|[« nom », PropertyType, x]|PropertyType</br></br>{</br>serveur local,</br>}|
|AdditionOperation |1. Arg1 | 1. tableau d’arguments requis par l’opération d’addition |Elle évalue toutes les valeurs dans les arguments et les ajoute |{</br>« opérateur » : « ajout »,</br>« args » : [{</br>« opérateur »...</br>}, 2, 4]</br>} |[« plus », [1, 2, 3]]|Veillez à évaluer args entraînant flottante type|
|SubtractionOperation |1.arg1 2.Arg2|1. argument à partir de laquelle soustraire</br>2. argument qui doit être soustrait|Elle évalue les valeurs dans les arguments et soustrait l’autre à partir du premier|{</br>« opérateur » : « soustraction »,</br>« arg1 » :</br>{</br>« opérateur »...</br>}, </br>« arg2 » : 2</br>}|[« soustraction, » [4, 3]] |Veillez à évaluer args entraînant flottante type|
MultiplicationOperation |1. Arg1|1. tableau d’arguments requis par une opération de multiplication | Elle évalue toutes les valeurs dans les arguments et multiplie les |{</br>« opérateur » : « multiplication », </br>« args » : [</br>{</br>« opérateur »...</br>}, 2, 4]</br>}|[« multiplication », [1, 2, 3]|Veillez à évaluer args entraînant flottante type|
|DivisionOperation |1. Arg1</br>2. Arg2|1. argument à partir de laquelle diviser </br>2. argument qui doit être divisée  |Elle évalue les valeurs dans les arguments et divise le deuxième élément à partir du premier|{</br>« opérateur » : « division »,</br>« arg1 » :</br>{</br>« opérateur »...</br>}, </br>« arg2 » : 2</br>} |[« division », [4, 3]] |Veillez à évaluer args entraînant flottante type |
|ModuloOperation |1. Arg1 </br>2. Arg2|1. argument à partir de laquelle diviser </br> 2. argument qui doit être divisée pour obtenir le reste|Elle évalue les valeurs dans les arguments et divise le deuxième élément à partir du premier et retourne le reste |{</br>« opérateur » : « modulo »</br>« arg1 » :</br>{</br>« opérateur »...</br>},</br>« arg2 » : 2</br>}|[« modulo » [4, 3]] |Veillez à évaluer args entraînant flottante type |

