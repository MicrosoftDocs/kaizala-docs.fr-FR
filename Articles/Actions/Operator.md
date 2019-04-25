# <a name="chat-card-customization---operators"></a>Personnalisation des cartes de conversation-opérateurs 

Dans certains cas, il peut être nécessaire que différents utilisateurs aient besoin d'afficher différentes cartes de conversation, qui peuvent être basées sur certains attributs. Afin d'activer ce type de scénario, Kaizala fournit des opérateurs, qui permet aux créateurs d'actions de personnaliser les vues de carte de conversation pour la même instance d'action différemment pour différents scénarios/utilisateurs.

## <a name="lets-take-an-example"></a>Prenons l'exemple suivant:

Imaginons que nous voulons afficher l'affichage de la carte différemment par rapport à l'expéditeur. En utilisant des opérateurs, nous pouvons facilement atteindre ce scénario, en Voici la vue de conversation personnalisée:  


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

Ici, vous pouvez observer que l'opérateur «conditional_value» obtient une valeur booléenne de l'opérateur imbriqué «is_it_me» qui est encore imbriquée avec l'opérateur «property_value». De même, il peut être facilement étendu à n'importe quel scénario, même un plus complexe. De plus, l'entrée suivante doit être ajoutée au manifeste du package: ActionStoreSchema: "<name of the action store schema definition file>". Pour plus d'informations, reportez-vous au [schéma JSON du manifeste du package](package_manifest_schema.md) .


 
## <a name="list-of-supported-operators"></a>Liste des opérateurs pris en charge: 

> **Remarque** : les variables x, y, z utilisées dans les exemples de syntaxe peuvent être des valeurs simples ou des résultats renvoyés par des opérateurs imbriqués 


| Nom de l'opérateur |Nom du paramètre |Type de paramètre |Fonctionnalité  |Syntaxe |Syntaxe réduite | Remarque |
|--------|------|------|----|----|----|----|
|Valeur conditionnelle  |1. condition 2. Valeur 3. Par défaut|1. booléen 2. Valeur JSON 3. Valeur JSON | Cet opérateur est utilisé pour renvoyer une valeur spécifiée, si une condition définie est true. Si la condition a la valeur false, elle renvoie la valeur false.|{</br>«opérateur»: «conditional_value», «condition»: x, «value»: {y}, «default»: {z}</br>}| ["conditional_value", X, Y, Z] ||
|Égal à |1. valeur 2. Value |    1. String 2. String |Cet opérateur renvoie la valeur true si les valeurs fournies (valeur1, valeur2) sont égales. Sinon, renvoie false. |    {</br>«opérateur»: «EQ», «value1»: x, «valeur2»: y </br>} |["EQ", x, y] ||
|FormatProfileName  |1. propriété 2. Src |1. chaîne 2. PropertyType| Obtient la propriété de SRC «PropertyType» et met en forme la liste des ID utilisateur de la manière suivante:</br></br>' <Name de l'utilisateur 1> & n plus' </br></br>n est le nombre d'utilisateurs présents dans la liste 1 |{</br>«opérateur»: «format_profile_names»,</br>"Property": x, "src":P ropertyType</br>}|["format_profile_names", PropertyType, x] |PropertyType</br>{</br>  serveur local</br>} </br></br>1. cet opérateur part du principe que la propriété x fournie renvoie un tableau d'ID utilisateur. </br></br>2. UserName1 vous indique si l'utilisateur connecté est présent dans la liste des ID utilisateur.|
|FormatString|1. format 2. AGRS|1. chaîne 2. tableau d'arguments attendus par la chaîne de mise en forme|Cet opérateur permet de mettre en forme une chaîne à l'aide de spécificateurs de format.</br></br>Cet opérateur est identique à tout autre opérateur de chaîne de format présent dans CPP ou Java |{</br>«opérateur»: «FORMAT_STRING», «format»: x, «args»: [y, z...]</br>}|["FORMAT_STRING", x, [y, z...]]|X peut contenir des spécificateurs comme% s,% d etc, et les opérateurs attendent que les arguments soient présents dans le même type dans le même ordre </br></br>Par exemple, la chaîne peut être</br>{</br>«opérateur»: «FORMAT_STRING»,</br>«format»: «mon nom est% s et mon âge est de% d»,</br>"args": [y, z]</br>}</br></br>Où y est une variable de chaîne et z un entier|
|IsCurrentUser|1. Value|1. UUID compare l'UUID (UserId) fourni avec l'UUID (UserId) de l'utilisateur connecté en cours. Elle renvoie la valeur true si elle correspond à et renvoie false dans le cas contraire. |{</br>«opérateur»: «is_it_me»,</br>«valeur»: x</br>}|["is_it_me" x]|
|JSONPathValue|1.1. Entité 2. chemin d'accès|1. EntityType 2. chemin d'accès JSON valide| Extrait la valeur résidant sur la clé dans l'entité JSON du type donné.  Elle renvoie la première valeur rencontrée dans le chemin d'accès. |{</br>«opérateur»: «jsonpath_value»,</br>"Entity": EntityType,</br>"chemin d'accès": ValidJsonPath</br>}|["jsonpath_value", EntityType, ValidJsonPath]|{</br>«opérateur»:</br>«jsonpath_value»,</br>«entité»: message,</br>"chemin d'accès": "$.. SenderName</br>}</br></br>"$.." Parcourir de manière récursive</br></br>"$." Parcourir uniquement le 1er niveau d'entité|
|MessageConversationName|1. Value|1. messageId|Renvoie le nom de la conversation à laquelle appartient le message auquel l'ID messageId donné appartient.|{"opérateur": "message_conversation_name", "valeur": x}|["message_conversation_name", x]|
|MessageCreationTime|1. Value|1. messageId|Renvoie la chaîne d'horodatage lisible par l'utilisateur pour l'horodatage de création du message avec un messageId donné |{</br>«opérateur»: «message_creation_time»,</br>«valeur»: x</br>}|["message_creation_time", x]|
|ProfileName|1. ID|1. UUID|Renvoyer le nom d'affichage de l'utilisateur lorsque le UUID (UserId) est fourni |{</br>«opérateur»: «profile_name», «ID»: x</br>}|["profile_name", x]|
|PropertyValue|1. SRC 2. Property|1. PropertyType 2. String|Obtient la propriété à partir de la propriété SRC PropertyType.|{</br>«opérateur»: «property_value»,</br>"Property": x, "src": PropertyType</br>}|["property_value", PropertyType, x]|PropertyType</br></br>{</br>serveur local</br>}|
|AdditionOperation |1. Arg1 | 1. tableau d'arguments nécessaires à l'opération d'ajout |Il évalue toutes les valeurs à l'intérieur des arguments et les ajoute |{</br>"opérateur": "addition",</br>«args»: [{</br>«opérateur»..</br>}, 2, 4]</br>} |["addition", [1, 2, 3]]|Assurez-vous d'évaluer les arguments qui génèrent un type flottant|
|SubtractionOperation |1. Arg1 2. Arg2|1. argument à partir duquel soustraire</br>2. argument qui doit être soustrait|Il évalue à la fois les valeurs à l'intérieur des arguments et soustrait le second du premier.|{</br>"opérateur": "soustraction",</br>«arg1»:</br>{</br>«opérateur»..</br>}, </br>«Arg2»: 2</br>}|["Subtraction", [4, 3]] |Assurez-vous d'évaluer les arguments qui génèrent un type flottant|
MultiplicationOperation |1. Arg1|1. tableau d'arguments requis par une opération de multiplication | Il évalue toutes les valeurs à l'intérieur des arguments et les multiplie |{</br>"opérateur": "multiplication", </br>«args»: [</br>{</br>«opérateur»..</br>}, 2, 4]</br>}|["multiplication", [1, 2, 3]|Assurez-vous d'évaluer les arguments qui génèrent un type flottant|
|DivisionOperation |1. Arg1</br>2. Arg2|1. argument à partir duquel diviser </br>2. argument qui doit être divisé  |Il évalue à la fois les valeurs à l'intérieur des arguments et divise le deuxième du premier.|{</br>"opérateur": "Division",</br>«arg1»:</br>{</br>«opérateur»..</br>}, </br>«Arg2»: 2</br>} |["Division", [4, 3]] |Assurez-vous d'évaluer les arguments qui génèrent un type flottant |
|ModuloOperation |1. Arg1 </br>2. Arg2|1. argument à partir duquel diviser </br> 2. argument qui doit être divisé pour obtenir le reste|Il évalue à la fois les valeurs à l'intérieur des arguments et divise le deuxième du premier et renvoie le reste |{</br>«opérateur»: «modulo»,</br>«arg1»:</br>{</br>«opérateur»..</br>},</br>«Arg2»: 2</br>}|["Modulo", [4, 3]] |Assurez-vous d'évaluer les arguments qui génèrent un type flottant |

