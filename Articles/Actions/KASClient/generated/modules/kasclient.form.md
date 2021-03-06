[](../README.md) > [](../modules/kasclient.md) > [Formulaire](../modules/kasclient.form.md) KASClient

# <a name="module-form"></a>Module: formulaire

## <a name="index"></a>Index

### <a name="creation"></a>Sa

* [initFormAsync](kasclient.form.md#initformasync)
* [submitFormRequestV2](kasclient.form.md#submitformrequestv2)
* [submitFormRequestWithoutDismiss](kasclient.form.md#submitformrequestwithoutdismiss)
* [updateForm](kasclient.form.md#updateform)
### <a name="response"></a>Réponse

* [canRespondToFormAsync](kasclient.form.md#canrespondtoformasync)
* [getFormAsync](kasclient.form.md#getformasync)
* [getFormStatusAsync](kasclient.form.md#getformstatusasync)
* [getMyFormResponsesAsync](kasclient.form.md#getmyformresponsesasync)
* [sumbitFormResponse](kasclient.form.md#sumbitformresponse)
* [sumbitFormResponseWithoutDismiss](kasclient.form.md#sumbitformresponsewithoutdismiss)
### <a name="summary"></a>Résumé

* [FormSummaryCallback](kasclient.form.md#formsummarycallback)
* [addCommentOnForm](kasclient.form.md#addcommentonform)
* [closeForm](kasclient.form.md#closeform)
* [copyFormAndForward](kasclient.form.md#copyformandforward)
* [executeActionFetchQueryAsync](kasclient.form.md#executeactionfetchqueryasync)
* [fetchFormAsync](kasclient.form.md#fetchformasync)
* [fetchFormInfosAsync](kasclient.form.md#fetchforminfosasync)
* [getActionInstanceLocalDataCacheAsync](kasclient.form.md#getactioninstancelocaldatacacheasync)
* [getActionPackageLocalDataCacheAsync](kasclient.form.md#getactionpackagelocaldatacacheasync)
* [getFormReactionAsync](kasclient.form.md#getformreactionasync)
* [getFormSummaryAsync](kasclient.form.md#getformsummaryasync)
* [getFormURLAsync](kasclient.form.md#getformurlasync)
* [getFormUserCapabilitiesAsync](kasclient.form.md#getformusercapabilitiesasync)
* [isSubscribed](kasclient.form.md#issubscribed)
* [likeForm](kasclient.form.md#likeform)
* [sendRemindersToRespond](kasclient.form.md#sendreminderstorespond)
* [shareFormURL](kasclient.form.md#shareformurl)
* [showAllReactions](kasclient.form.md#showallreactions)
* [updateActionInstanceLocalDataCacheAsync](kasclient.form.md#updateactioninstancelocaldatacacheasync)
* [updateActionPackageLocalDataCacheAsync](kasclient.form.md#updateactionpackagelocaldatacacheasync)
* [updateFormPropertiesAsync](kasclient.form.md#updateformpropertiesasync)

---

## <a name="creation"></a>Sa

<a id="initformasync"></a>

###  <a name="initformasync"></a>initFormAsync

▸ **initFormAsync**(callback: *`function`*):`void`

Initialise et renvoie un objet Form vide basé sur le fichier de formulaire par défaut présent dans le package.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
KASClient.Form.initFormAsync(function (form, error) {
     if (error != null) {
         // use form
     }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param formulaire {KASForm} peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="submitformrequestv2"></a>

###  <a name="submitformrequestv2"></a>submitFormRequestV2

▸ **submitFormRequestV2**(Form: *[KASForm](../classes/kasclient.kasform.md)*, shouldDismiss?: *`boolean`*, shouldSendToSubscribers?: *`boolean`*):`void`

Envoie le formulaire nouvellement créé sous la forme d’une requête. Cela aboutit à une nouvelle carte de conversation

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| formulaire | [KASForm](../classes/kasclient.kasform.md) | - |  \- |
| `Default value`shouldDismiss | `boolean` | false |  true si le formulaire doit être fermé lors de l’envoi; false dans le cas contraire |
| `Default value`shouldSendToSubscribers | `boolean` | true |  applicable dans les groupes publics, définie sur false si la demande n’est pas destinée aux abonnés |

**Renvoie:**`void`

___
<a id="submitformrequestwithoutdismiss"></a>

###  <a name="submitformrequestwithoutdismiss"></a>submitFormRequestWithoutDismiss

▸ **submitFormRequestWithoutDismiss**(Form: *[KASForm](../classes/kasclient.kasform.md)*, shouldInflate: *`boolean`*):`void`

Envoie le formulaire nouvellement créé sous la forme d’une requête. Cela aboutit à une nouvelle carte de conversation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| formulaire | [KASForm](../classes/kasclient.kasform.md) |  \- |
| shouldInflate | `boolean` |  Boolean – doit être gonflé/non |

**Renvoie:**`void`

___
<a id="updateform"></a>

###  <a name="updateform"></a>updateForm

▸ **updateForm**(Fields *`string`*:, shouldInflate *`boolean`*:, callback *`function`*:):`void`

Utilisez pour apporter des modifications aux champs de formulaire comme le titre, la description et les paramètres.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
  var fieldsToUpdate = {"title" : "<updated title", "exp" : "<expiry time>",
           "vis" : "<result visibility - set as sender/all/admin>", "Description": "<Updated survey desc>"};
  KASClient.Form.updateForm(JSON.stringify(fieldsToUpdate), false, function(success) {
       if(success) {
         //do something
       }
   });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| champs | `string` |  chaîne JSON de champs nécessitant une mise à jour |
| shouldInflate | `boolean` |  Boolean – doit être gonflé/non |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} Success true si la mise à jour a réussi; false dans le cas contraire |

**Renvoie:**`void`

___

## <a name="response"></a>Réponse

<a id="canrespondtoformasync"></a>

###  <a name="canrespondtoformasync"></a>canRespondToFormAsync

▸ **canRespondToFormAsync**(callback: *`function`*):`void`

Indique si l’utilisateur actuel peut répondre au formulaire.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} canRespond true si l’utilisateur actuel est autorisé à répondre |

**Renvoie:**`void`

___
<a id="getformasync"></a>

###  <a name="getformasync"></a>getFormAsync

▸ **getFormAsync**(callback: *`function`*):`void`

Obtient l’objet de formulaire associé à la carte de conversation.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param formulaire {KASForm} peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="getformstatusasync"></a>

###  <a name="getformstatusasync"></a>getFormStatusAsync

▸ **getFormStatusAsync**(callback: *`function`*):`void`

Obtient l’état du formulaire associé à la carte de conversation.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} isActive true si le formulaire n’a pas encore expiré<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="getmyformresponsesasync"></a>

###  <a name="getmyformresponsesasync"></a>getMyFormResponsesAsync

▸ **getMyFormResponsesAsync**(callback: *`function`*, onlyCurrentResponse?: *`boolean`*):`void`

Obtient toutes les réponses de l’utilisateur actuel sur le formulaire.

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  avec les paramètres suivants:<br><br>\*@param les réponses\[\]{KASFormResponse} peuvent être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |
| `Default value`onlyCurrentResponse | `boolean` | true |  Applicable aux actions de réponse pour lesquelles cette méthode renvoie uniquement la réponse actuelle dans le contexte, affectez la valeur false à cet indicateur pour extraire toutes les réponses à la place. La valeur par défaut est true |

**Renvoie:**`void`

___
<a id="sumbitformresponse"></a>

###  <a name="sumbitformresponse"></a>sumbitFormResponse

▸ **sumbitFormResponse**(questionToAnswerMap: *`JSON`*, responseId: *`string`*, isEdit: *`boolean`*, showInChatCanvas: *`boolean`*, isAnonymous: *`boolean`*):`void`

Envoie une nouvelle réponse au formulaire associé à la carte de conversation cette opération va faire disparaître l’écran actuel.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var questionToAnswerMap = { "0": "answer" };
KASClient.Form.sumbitFormResponse(questionToAnswerMap, null, false, false, false);
```

#### <a name="note"></a>Remarque

```
questionToAnswerMap is a map which has key as question Id and value as the response to the question
Say question of id 1 is of type "Text" which means it takes string as response. You should define it like {1: "<answer>"}
```

La valeur de la propriété Response pour _[KASQuestionType](../enums/kasclient.kasquestiontype.md)_ doit être:
*   **Single Select** : option ID (String). par exemple, «1»
*   **MultiSelect** : tableau JSON des ID d’option. par exemple, JSON. stringify\[(1,\]3)
*   **Text** : String. par exemple, «factice»
*   **Numérique** : nombre. par exemple, 543
*   **Location** : JSON _[KASLocation](../classes/kasclient.kaslocation.md)_ Object. par exemple, JSON. stringify (location. toJSON ()) ou JSON. stringify ({"LG": 70,4, "lt": 18,6, "n": "Address"})
*   **DateTime** : horodatage de l’époque dans millieseconds. par exemple, 1550651524074
*   **Image** : chemin d’accès à l’image. par exemple, «file://imagePath.png»
*   **AttachmentList** : JSON tableau d’objets _[KASAttachment](../classes/kasclient.kasattachment.md)_ . par exemple, JSON. stringify (pièces jointes), les pièces jointes sont un tableau de KASAttachment
*   **PhoneNumber** : JSON _[KASPhoneNumber](../classes/kasclient.kasphonenumber.md)_ objet. par exemple, fils. stringify (phoneNumber. toJSON ()) ou JSON. stringify ({"CC": "+ 91", "PN": "98XXXXXXX6"})
*   **DateOnly** : chaîne de date (aaaa-mm-jj). par exemple, «2019-04-17»

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  ID de la question pour répondre au mappage |
| responseId | `string` |  à remplir si la réponse actuelle est une modification ou mise à jour d’une précédente |
| isEdit | `boolean` |  indique si la réponse actuelle est une modification ou mise à jour d’une précédente |
| showInChatCanvas | `boolean` |  indique si une carte de conversation distincte doit être créée pour cette réponse ou non. |
| isAnonymous | `boolean` |  indique si la réponse doit être inscrite comme anonyme ou non |

**Renvoie:**`void`

___
<a id="sumbitformresponsewithoutdismiss"></a>

###  <a name="sumbitformresponsewithoutdismiss"></a>sumbitFormResponseWithoutDismiss

▸ **sumbitFormResponseWithoutDismiss**(questionToAnswerMap: *`JSON`*, responseId: *`string`*, isEdit: *`boolean`*, showInChatCanvas: *`boolean`*, isAnonymous: *`boolean`*):`void`

Envoie une nouvelle réponse au formulaire associé à la carte de conversation qui ne refermera pas l’écran actuel.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var questionToAnswerMap = { "0": "answer" };
KASClient.Form.sumbitFormResponseWithoutDismiss(questionToAnswerMap, null, false, false, false);
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  ID de la question pour répondre au mappage (voir _[sumbitFormResponse](kasclient.form.md#sumbitformresponse)_ pour plus d’informations) |
| responseId | `string` |  à remplir si la réponse actuelle est une modification ou mise à jour d’une précédente |
| isEdit | `boolean` |  indique si la réponse actuelle est une modification ou mise à jour d’une précédente |
| showInChatCanvas | `boolean` |  indique si une carte de conversation distincte doit être créée pour cette réponse ou non. |
| isAnonymous | `boolean` |  indique si la réponse doit être inscrite comme anonyme ou non |

**Renvoie:**`void`

___

## <a name="summary"></a>Résumé

<a id="formsummarycallback"></a>

###  <a name="formsummarycallback"></a>FormSummaryCallback

**Ƭ FormSummaryCallback**:*`function`*

#### <a name="type-declaration"></a>Déclaration de type
▸ (flatSummary: *[KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)*, ProcessedSummary: *[KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)*, Error: *`string`*):`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| flatSummary | [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md) |
| processedSummary | [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md) |
| error | `string` |

**Renvoie:**`void`

___
<a id="addcommentonform"></a>

###  <a name="addcommentonform"></a>addCommentOnForm

▸ **addCommentOnForm**(Commentaire: *`string`*):`void`

Demandes d’ajout d’un commentaire à un formulaire

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| commentaire | `string` |

**Renvoie:**`void`

___
<a id="closeform"></a>

###  <a name="closeform"></a>closeForm

▸ **closeForm**():`void`

Ferme le formulaire associé à la carte, aucune réponse n’est autorisée.

**Renvoie:**`void`

___
<a id="copyformandforward"></a>

###  <a name="copyformandforward"></a>copyFormAndForward

▸ **copyFormAndForward**():`void`

Lance le sélecteur de conversation pour transférer une copie du formulaire existant en tant que nouvelle carte de conversation

**Renvoie:**`void`

___
<a id="executeactionfetchqueryasync"></a>

###  <a name="executeactionfetchqueryasync"></a>executeActionFetchQueryAsync

▸ **executeActionFetchQueryAsync**(formid: *`string`*, fetchJsonQueryId: *`string`*, fetchJsonQueryParams: *`JSON`*, callback: *`function`*):`void`

Récupère les lignes/réponses de l’instance d’action (ou formulaire) à l’aide d’une requête FetchJson (SQL au format JSON). À l’aide de cette API, vous pouvez exécuter des requêtes enrichies sur toutes les lignes et obtenir des résultats détaillés ou résumés. Ces requêtes doivent être mentionnées dans la procédure appModel de l’action pour permettre aux développeurs d’actions d’avoir des autorisations au niveau de la requête. Il est possible d’exécuter une requête de ce type avec uniquement l’ID de requête et les valeurs d’espace réservé requises, le cas échéant.
#### <a name="note"></a>Remarque

1.  La colonne d’instance d’action/les ID de question seront utilisés comme ID d’attribut de la requête FetchJson
2.  La sortie sera une liste de lignes, chaque ligne contenant des paires ID-valeur de colonne

#### <a name="sample-usage"></a>Exemple d’utilisation

```
// AppModel questions: ResponderName (0) | City (1) | FavoriteMovie (2)
// Query (q123): SELECT question0 WHERE question1="@param1" AND question2="@param2"
// To fetch responders from "Mumbai" whose favorite movie is "Harry Potter"
var params = { "@param1": "Mumbai", "@param2": "Harry Potter"};
KASClient.Form.executeActionFetchQueryAsync("XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", "q123", params, function (result, error) {
   if (!error) {
       for (var i = 0; i < result.rows.length; i++) {
           var row = result.rows[i];
           console.log("Responder name: " + row["0"]);
       }
   }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| formId | `string` |  ID de l’instance de l’action (ou formulaire) dont les lignes doivent être extraites |
| fetchJsonQueryId | `string` |  ID de requête FetchJson (mentionné dans le package d’action) |
| fetchJsonQueryParams | `JSON` |  Mappage des espaces réservés des paramètres de requête aux valeurs |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {JSON} fetchJsonResult-le résultat de la requête FetchJson<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="fetchformasync"></a>

###  <a name="fetchformasync"></a>fetchFormAsync

▸ **fetchFormAsync**(formid: *`string`*, callback: *`function`*):`void`

Récupère une instance d’action (ou un formulaire) pour l’ID donné. Il tente d’abord d’obtenir l’instance localement, puis de l’extraire du serveur comme secours.
#### <a name="note"></a>Remarque

Une action peut extraire des instances de lui-même ou d’une autre action qui appartient à son propre appGroup

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| formId | `string` |  ID de l’instance à extraire |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param de l’instance de l’action de formulaire {KASForm} (ou formulaire)<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="fetchforminfosasync"></a>

###  <a name="fetchforminfosasync"></a>fetchFormInfosAsync

▸ **fetchFormInfosAsync**(Request: *[KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)*, callback: *`function`*):`void`

Récupère une instance d’action (ou un formulaire) informations d’un package d’action. Ceci est utile dans l’accès aux données d’action croisée, où une action peut extraire les lignes/réponses de l’instance d’une autre action-cette API est utilisée pour extraire l’ID d’instance requis pour extraire des lignes.
#### <a name="note"></a>Remarque

Une action peut extraire des instances de lui-même ou d’une autre action qui appartient à son propre appGroup

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var request = new KASClient.KASFormInfoRequest();
request.packageId = "some-package-id";
request.scopeId = "XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"; // Group id

KASClient.Form.fetchFormInfosAsync(request, function (response, error) {
   if (!error) {
       for (var i = 0; i < response.formInfos.length; i++) {
           var formInfo = response.formInfos[i]; // KASFormInfo
           console.log("Instance id: " + formInfo.id);
           console.log("Instance title: " + formInfo.title);
       }
   }
})
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| sollicit | [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md) |  Requête contenant les paramètres de l’API |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {KASFormInfoResponse} réponses-réponse contenant des informations d’instance (ou de formulaire) d’action<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="getactioninstancelocaldatacacheasync"></a>

###  <a name="getactioninstancelocaldatacacheasync"></a>getActionInstanceLocalDataCacheAsync

▸ **getActionInstanceLocalDataCacheAsync**(callback: *`function`*):`void`

Récupère les propriétés ActionInstance à partir du cache de données local si celles-ci sont stockées au niveau d’une instance d’action. Par conséquent, les données locales enregistrées pour l’instance d’action particulière seront retournées par cette API.
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas de messages historiques.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
KASClient.Form.getActionInstanceLocalDataCacheAsync(function (actionPackageProperties, error) {
     if (error == null && actionPackageProperties != null && actionPackageProperties.properties) {
          if (actionPackageProperties.properties.hasOwnProperty("prop1") {
             console.log(actionPackageProperties.properties["prop1"]);
          }
     }
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {KASActionProperties} Actionpropriétés ActionInstance/propriétés du formulaire<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="getactionpackagelocaldatacacheasync"></a>

###  <a name="getactionpackagelocaldatacacheasync"></a>getActionPackageLocalDataCacheAsync

▸ **getActionPackageLocalDataCacheAsync**(callback: *`function`*):`void`

Extrait les propriétés de package d’action à partir du cache de données local s’il en existe une quelconque, ces propriétés sont enregistrées au niveau du package d’action. Par conséquent, toutes les instances d’action créées à partir de ce package d’action recevront les mêmes données.
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas de messages historiques.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
KASClient.Form.getActionPackageLocalDataCacheAsync(function (actionPackageProperties, error) {
     if (error == null && actionPackageProperties != null && actionPackageProperties.properties) {
          if (actionPackageProperties.properties.hasOwnProperty("prop1") {
             console.log(actionPackageProperties.properties["prop1"]);
          }
     }
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param les propriétés de package d’action actionPackageProperties {KASActionPackageProperties}<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="getformreactionasync"></a>

###  <a name="getformreactionasync"></a>getFormReactionAsync

▸ **getFormReactionAsync**(callback: *`function`*):`void`

Obtient la réaction consolidée (j’aime et les commentaires) de la carte de conversation associée au formulaire.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param la réaction {KASFormReaction} peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="getformsummaryasync"></a>

###  <a name="getformsummaryasync"></a>getFormSummaryAsync

▸ **getFormSummaryAsync**(MostUpdatedCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*, notifyCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*):`void`

Obtient les réponses plates de tous les utilisateurs et le résumé traité de toutes les réponses associées au formulaire. Il nécessite deux rappels:
#### <a name="note"></a>Remarque

Ceci est utile lorsque le réseau est en regard/déconnecté, de sorte que le résumé peut immédiatement être affiché avec les données actuelles dont nous disposons, mais avec une option permettant de l’actualiser ultérieurement à l’arrivée des données les plus récentes à partir du serveur. Aucun des rappels n’est obligatoire, donc si le 1er est Nil, cette méthode peut être utilisée pour toujours extraire le résumé du serveur, et si 2nd est Nil, il peut être utilisé pour toujours extraire le résumé à partir de la base de données locale!

#### <a name="sample-usage"></a>Exemple d’utilisation

```
KASClient.Form.getFormSummaryAsync(
   // Data fetched from database
   function (flatSummary, processedSummary, error) {
      if (error != null) {
      }
   },
   // Data fetched from server
   function (flatSummary, processedSummary, error) {
      if (error != null) {
      }
   })
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| mostUpdatedCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  pour obtenir immédiatement le récapitulatif le plus mis à jour à partir de la base de données locale. Elle comporte les paramètres suivants:<br><br>\*@param {KASFormFlatSummary} flatSummary peut être null en cas d’erreur<br><br>\*@param {KASFormProcessedSummary} processedSummary peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |
| notifyCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  pour recevoir une notification avec le dernier Résumé extrait du serveur. Elle comporte les paramètres suivants:<br><br>\*@param {KASFormFlatSummary} flatSummary peut être null en cas d’erreur<br><br>\*@param {KASFormProcessedSummary} processedSummary peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="getformurlasync"></a>

###  <a name="getformurlasync"></a>getFormURLAsync

▸ **getFormURLAsync**(callback: *`function`*):`void`

Obtient l’URL de fichier à partir du serveur contenant les réponses plates associées au formulaire.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} URL peut être null en cas d’erreur<br><br>\*message d’erreur @param {String} en cas d’erreur, NULL sinon |

**Renvoie:**`void`

___
<a id="getformusercapabilitiesasync"></a>

###  <a name="getformusercapabilitiesasync"></a>getFormUserCapabilitiesAsync

▸ **getFormUserCapabilitiesAsync**(callback: *`function`*):`void`

Obtient les autorisations de formulaire

#### <a name="sample-usage"></a>Exemple d’utilisation

```
KASClient.Form.getFormUserCapabilitiesAsync(function (permissions, error) {
    if(!error) {
        canRespond = permissions.canRespond;
        canSendReminder = permissions.canSendReminder;
        shouldSeeSummary = permissions.shouldSeeSummary;
    }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param les autorisations {KASFormUserCapabilities}<br><br>\*@param chaîne d’erreur d’erreur de type {String} en cas d’erreur; NULL dans le cas contraire |

**Renvoie:**`void`

___
<a id="issubscribed"></a>

###  <a name="issubscribed"></a>isSubscribed

▸ **isSubscribed**(callback: *`function`*):`void`

Obtient une valeur indiquant si l’utilisateur actuel est abonné ou non.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} isSubscribed true si l’abonné utilisateur actuel |

**Renvoie:**`void`

___
<a id="likeform"></a>

###  <a name="likeform"></a>likeForm

▸ **likeForm**():`void`

Demandes d’ajout d’un nombre similaire à un formulaire, le nombre peut diminuer si l’utilisateur actuel a déjà aimé le formulaire.

**Renvoie:**`void`

___
<a id="sendreminderstorespond"></a>

###  <a name="sendreminderstorespond"></a>sendRemindersToRespond

▸ **sendRemindersToRespond**():`void`

Envoie un rappel (une nouvelle carte de conversation) à la carte existante

**Renvoie:**`void`

___
<a id="shareformurl"></a>

###  <a name="shareformurl"></a>shareFormURL

▸ **shareFormURL**(URL: *`string`*):`void`

Partager l’URL de résultats extraite de l’écran de serveur-lancer le partage natif pour l’URL du formulaire

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| url | `string` |  à partager |

**Renvoie:**`void`

___
<a id="showallreactions"></a>

###  <a name="showallreactions"></a>showAllReactions

▸ **showAllReactions**(showcomments,?: *`boolean`*):`void`

Affiche tous les écrans de réaction (j’aime et commentaires) sur le formulaire

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`showcomments, | `boolean` | true |  true si les commentaires doivent également être affichés; false dans le cas contraire |

**Renvoie:**`void`

___
<a id="updateactioninstancelocaldatacacheasync"></a>

###  <a name="updateactioninstancelocaldatacacheasync"></a>updateActionInstanceLocalDataCacheAsync

▸ **updateActionInstanceLocalDataCacheAsync**(Actionpropriétés: *[KASActionProperties](../classes/kasclient.kasactionproperties.md)*, callback: *`function`*):`void`

Met à jour/enregistre les propriétés ActionInstance données dans le cache de données local ces propriétés sont stockées au niveau de l’instance de l’action. Par conséquent, chaque instance d’action peut enregistrer des données locales dans le cache et celle-ci ne sera accessible que par cette instance particulière.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var actionPackageProperties = KASClient.KASActionPackageProperties.fromJSON(JSON.parse("{}"));
actionPackageProperties.properties = JSON.parse("{}");
actionPackageProperties.properties[prop1] = value1;
KASClient.Form.updateActionInstanceLocalDataCacheAsync(actionPackageProperties, function(success, error) {
     if(!error) {
     }
});
```
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas de messages historiques.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| Actionpropriétés | [KASActionProperties](../classes/kasclient.kasactionproperties.md) |  ActionInstance/propriétés de formulaire à mettre à jour/enregistrer |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} Success indique si la mise à jour a réussi ou non.<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="updateactionpackagelocaldatacacheasync"></a>

###  <a name="updateactionpackagelocaldatacacheasync"></a>updateActionPackageLocalDataCacheAsync

▸ **updateActionPackageLocalDataCacheAsync**(ActionPackageProperties: *[KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md)*, callback: *`function`*):`void`

Met à jour/enregistre les propriétés de package d’action données dans le cache de données local ces propriétés sont enregistrées au niveau du package d’action. Les données sont donc partagées entre toutes les instances d’action créées à partir de ce package d’action.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var actionPackageProperties = KASClient.KASActionPackageProperties.fromJSON(JSON.parse("{}"));
actionPackageProperties.properties = JSON.parse("{}");
actionPackageProperties.properties[prop1] = value1;
KASClient.Form.updateActionPackageLocalDataCacheAsync(actionPackageProperties, function(success, error) {
     if(!error) {
     }
});
```
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas de messages historiques.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| actionPackageProperties | [KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md) |  Propriétés du package d’action à mettre à jour/enregistrer |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} Success indique si la mise à jour a réussi ou non.<br><br>\*@param valeur de chaîne JSON de l’erreur {String} pour l’objet KASError contenant un code d’erreur et/ou une description. |

**Renvoie:**`void`

___
<a id="updateformpropertiesasync"></a>

###  <a name="updateformpropertiesasync"></a>updateFormPropertiesAsync

▸ **updateFormPropertiesAsync**(propertyUpdates: * [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md)[]*, notifyUsers: * `string`[]*, notification: *`string`*, callback: *`function`*, shouldSendToSubscribers?: *`boolean`*):`void`

Publier une demande pour mettre à jour les propriétés associées au formulaire

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var updateProperties = [];
var currentFormProperty = new KASClient.KASFormProperty(); // type: KASFormProperty
currentFormProperty.name = "<name>";
currentFormProperty.value = "<value>";
var property1ToAdd = KASClient.KASFormPropertyUpdateFactory.addProperty(currentFormProperty); //use updateValueInProperty in case of existing form property
updateProperties.push(property1ToAdd);
var notifyUsersList = [];
// notifyUsersList.push(<"uid1">);
// notifyUsersList.push("<uid2>");
KASClient.Form.updateFormPropertiesAsync(updateProperties, notifyUsersList, notificationMessage, function (success) {
  if (success) {
  }
});
```

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| propertyUpdates | [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md) [] | - |  un tableau de toutes les informations de mise à jour qui sont nécessaires pour être effectuées, des informations de mise à jour peuvent être créées à l’aide de KASFormPropertyUpdateFactory |
| notifyUsers | `string`[] | - |  Envoyer des notifications de type émission à ces ID d’utilisateur concernant cette mise à jour |
| Notification | `string` | - |  message de notification d’envoi |
| callback | `function` | - |  avec les paramètres suivants:<br><br>\*@param {Boolean} Success indique si la mise à jour a réussi ou non. |
| `Default value`shouldSendToSubscribers | `boolean` | false |  Champ facultatif (valeur false par défaut) applicable uniquement dans les groupes publics. Si la valeur est définie sur true, les mises à jour des propriétés atteindront également les abonnés d’un groupe public. |

**Renvoie:**`void`

___

