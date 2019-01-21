---
ms.openlocfilehash: f33333ae61040460dc0386fee6a1f1cc118128be
ms.sourcegitcommit: 04ef38ff8e68cf1697371551aed1ffb254a69649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2019
ms.locfileid: "29379428"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [formulaire](../modules/kasclient.form.md)

# <a name="module-form"></a>Module : formulaire

## <a name="index"></a>Index

### <a name="creation"></a>Création

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

## <a name="creation"></a>Création

<a id="initformasync"></a>

###  <a name="initformasync"></a>initFormAsync

▸ **initFormAsync**(rappel : *`function`*) :`void`

Initialise et renvoie un objet de formulaire vide basé sur le fichier de formulaire par défaut dans le package

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*formulaire @param {KASForm} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="submitformrequestv2"></a>

###  <a name="submitformrequestv2"></a>submitFormRequestV2

▸ **submitFormRequestV2**(formulaire : *[KASForm](../classes/kasclient.kasform.md)*, shouldDismiss? : *`boolean`*, shouldSendToSubscribers? : *`boolean`*) :`void`

Envoie le formulaire nouvellement créé en tant que demande. Cette action entraîne une nouvelle carte de conversation

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| formulaire | [KASForm](../classes/kasclient.kasform.md) | - |  \- |
| `Default value`shouldDismiss | `boolean` | false |  valeur True si le formulaire doit être fermé après l’envoi ; False dans le cas contraire |
| `Default value`shouldSendToSubscribers | `boolean` | true |

**Renvoie :** `void`

___

<a id="submitformrequestwithoutdismiss"></a>

###  <a name="submitformrequestwithoutdismiss"></a>submitFormRequestWithoutDismiss

▸ **submitFormRequestWithoutDismiss**(formulaire : *[KASForm](../classes/kasclient.kasform.md)*, shouldInflate : *`boolean`*) :`void`

Envoie le formulaire nouvellement créé en tant que demande. Cette action entraîne une nouvelle carte de conversation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| formulaire | [KASForm](../classes/kasclient.kasform.md) |  \- |
| shouldInflate | `boolean` |  Boolean – devrait pas augmenter |

**Renvoie :** `void`

___

<a id="updateform"></a>

###  <a name="updateform"></a>updateForm

▸ **updateForm**(champs : *`string`*, shouldInflate : *`boolean`*, rappel : *`function`*) :`void`

Utilisez cette option pour apporter des modifications dans les champs de formulaire comme titre, description et paramètres.

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
| champs | `string` |  chaîne JSON de champs qui nécessitent la mise à jour |
| shouldInflate | `boolean` |  Boolean – devrait pas augmenter |
| callback | `function` |  avec sous Paramètres :<br><br>\*valeur true réussite @param {boolean} si la mise à jour a réussi ; False dans le cas contraire |

**Renvoie :** `void`

___

## <a name="response"></a>Réponse

<a id="canrespondtoformasync"></a>

###  <a name="canrespondtoformasync"></a>canRespondToFormAsync

▸ **canRespondToFormAsync**(rappel : *`function`*) :`void`

Indique si l’utilisateur actuel peut répondre à l’écran

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {boolean} canRespond true en cours si l’utilisateur est autorisé à répondre |

**Renvoie :** `void`

___

<a id="getformasync"></a>

###  <a name="getformasync"></a>getFormAsync

▸ **getFormAsync**(rappel : *`function`*) :`void`

Obtient l’objet de formulaire associé à la carte de conversation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*formulaire @param {KASForm} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getformstatusasync"></a>

###  <a name="getformstatusasync"></a>getFormStatusAsync

▸ **getFormStatusAsync**(rappel : *`function`*) :`void`

Obtient l’état du formulaire associé à la carte de conversation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {boolean} isActive true si le formulaire n’est pas encore terminée.<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getmyformresponsesasync"></a>

###  <a name="getmyformresponsesasync"></a>getMyFormResponsesAsync

▸ **getMyFormResponsesAsync**(rappel : *`function`*, onlyCurrentResponse? : *`boolean`*) :`void`

Obtient toutes les réponses de l’utilisateur actuel par rapport à l’écran

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  avec les paramètres ci-dessous :<br><br>\*@param {KASFormResponse\[\]} réponses peuvent être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |
| `Default value`onlyCurrentResponse | `boolean` | true |  Applicable d’Actions de réponse où cette méthode retourne uniquement la réponse en cours dans le contexte, définissez cet indicateur sur false pour extraire toutes les réponses à la place. Valeur par défaut est true |

**Renvoie :** `void`

___

<a id="sumbitformresponse"></a>

###  <a name="sumbitformresponse"></a>sumbitFormResponse

▸ **sumbitFormResponse**(questionToAnswerMap : *`JSON`*, responseId : *`string`*, isEdit : *`boolean`*, showInChatCanvas : *`boolean`*, é anonyme : *`boolean`*) :`void`

Envoie une réponse par rapport à la forme associée à la carte de conversation ce sera faire disparaître l’écran en cours

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var questionToAnswerMap = JSON.parse("{}");
questionToAnswerMap[0] = answer;
KASClient.Form.sumbitFormResponse(questionToAnswerMap,
   null,
   false,
   false,
   false);
```

#### <a name="note"></a>Remarque

```
questionToAnswerMap is a map which has key as question Id and value as the response to the question
Say question is of type "text" which means it takes text as response. You should define it like
var question = new KASClient.KASQuestion();
question.id = 1;
question.type = KASClient.KASQuestionType.Text;
question.title = "Enter your name";
This KASQuestion is to be added to form.questions[] array.
Now questionToAnswerMap for this should look like this {1: "<answer>"}
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  id de la question pour répondre aux mappage |
| responseId | `string` |  à remplir si la réponse en cours est une modification/mise à jour une précédente |
| isEdit | `boolean` |  Indique si la réponse en cours est une modification/mise à jour une précédente |
| showInChatCanvas | `boolean` |  Indique si une carte de conversation distinct doit être créé pour cette réponse ou non |
| é anonyme | `boolean` |  Indique si la réponse doit être enregistrée en tant qu’anonyme ou non |

**Renvoie :** `void`

___

<a id="sumbitformresponsewithoutdismiss"></a>

###  <a name="sumbitformresponsewithoutdismiss"></a>sumbitFormResponseWithoutDismiss

▸ **sumbitFormResponseWithoutDismiss**(questionToAnswerMap : *`JSON`*, responseId : *`string`*, isEdit : *`boolean`*, showInChatCanvas : *`boolean`*, é anonyme : *`boolean`*) :`void`

Envoie une réponse par rapport à la forme associée à la carte de conversation, cela ne faire disparaître l’écran en cours

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var questionToAnswerMap = JSON.parse("{}");
questionToAnswerMap[0] = answer;
KASClient.Form.sumbitFormResponseWithoutDismiss(questionToAnswerMap,
   null,
   false,
   false,
   false);
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  id de la question pour répondre aux mappage |
| responseId | `string` |  à remplir si la réponse en cours est une modification/mise à jour une précédente |
| isEdit | `boolean` |  Indique si la réponse en cours est une modification/mise à jour une précédente |
| showInChatCanvas | `boolean` |  Indique si une carte de conversation distinct doit être créé pour cette réponse ou non |
| é anonyme | `boolean` |  Indique si la réponse doit être enregistrée en tant qu’anonyme ou non |

**Renvoie :** `void`

___

## <a name="summary"></a>Résumé

<a id="formsummarycallback"></a>

###  <a name="formsummarycallback"></a>FormSummaryCallback

**Ƭ FormSummaryCallback**:*`function`*

#### <a name="type-declaration"></a>Déclaration de type
▸ (flatSummary : *[KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)*, processedSummary : *[KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)*, erreur : *`string`*) :`void`

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| flatSummary | [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md) |
| processedSummary | [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md) |
| error | `string` |

**Renvoie :** `void`

___

<a id="addcommentonform"></a>

###  <a name="addcommentonform"></a>addCommentOnForm

▸ **addCommentOnForm**(commentaire : *`string`*) :`void`

Demandes d’ajout d’un commentaire à un formulaire

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| commentaire | `string` |

**Renvoie :** `void`

___

<a id="closeform"></a>

###  <a name="closeform"></a>closeForm

▸ **closeForm**() :`void`

Ferme le formulaire associé à la carte, aucune réponse ne sera autorisée supplémentaire

**Renvoie :** `void`

___

<a id="copyformandforward"></a>

###  <a name="copyformandforward"></a>copyFormAndForward

▸ **copyFormAndForward**() :`void`

Lance le sélecteur de conversation pour transférer une copie du formulaire existant en tant qu’une nouvelle carte de conversation

**Renvoie :** `void`

___

<a id="getactioninstancelocaldatacacheasync"></a>

###  <a name="getactioninstancelocaldatacacheasync"></a>getActionInstanceLocalDataCacheAsync

▸ **getActionInstanceLocalDataCacheAsync**(rappel : *`function`*) :`void`

Récupère les propriétés ActionInstance à partir du cache de données local, le cas échéant ces propriétés sont stockées à une action au niveau de l’instance. Ainsi, les données locales enregistrées pour l’instance de l’action particulière seront renvoyées par cette API.
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas d’historique des messages.

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {KASActionProperties} actionProperties ActionInstance/formulaire Propriétés<br><br>\*chaîne json d’erreur de @param {chaîne} pour l’objet KASError contenant la description et/ou le code d’erreur. |

**Renvoie :** `void`

___

<a id="getactionpackagelocaldatacacheasync"></a>

###  <a name="getactionpackagelocaldatacacheasync"></a>getActionPackageLocalDataCacheAsync

▸ **getActionPackageLocalDataCacheAsync**(rappel : *`function`*) :`void`

Récupère les propriétés de Package d’Action à partir du cache de données local, le cas échéant ces propriétés sont enregistrées au niveau du lot d’action. Pour toutes les instances de l’action créés à partir de ce package action reçoit les mêmes données.
#### <a name="note"></a>Remarque

Cette API ne fonctionne pas comme prévu en cas d’historique des messages.

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {KASActionPackageProperties} actionPackageProperties propriétés d’Action de Package<br><br>\*chaîne json d’erreur de @param {chaîne} pour l’objet KASError contenant la description et/ou le code d’erreur. |

**Renvoie :** `void`

___

<a id="getformreactionasync"></a>

###  <a name="getformreactionasync"></a>getFormReactionAsync

▸ **getFormReactionAsync**(rappel : *`function`*) :`void`

Obtient la réaction consolidée (J’aime et commentaires) de la carte de conversation associée au formulaire

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*réaction @param {KASFormReaction} peut être nulle en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getformsummaryasync"></a>

###  <a name="getformsummaryasync"></a>getFormSummaryAsync

▸ **getFormSummaryAsync**(mostUpdatedCallback : *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*, notifyCallback : *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*) :`void`

Obtient plat réponses par tous les utilisateurs et traités résumé à partir de toutes les réponses associé au formulaire. Elle nécessite deux rappels :
#### <a name="note"></a>Remarque

Cela est utile lorsque le réseau est peu fiable/déconnecté, ce résumé peut être affiché immédiatement avec les données présentes, que nous avons, mais avec une option pour actualiser une version ultérieure sur réception des données les plus récentes à partir du serveur. Aucun des rappels sont obligatoires, si 1er est nul, cette méthode peut être utilisée pour extraire toujours résumé du serveur et si 2ème est zéro, cela peut être utilisé pour extraire toujours résumé de base de données locale !

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
| mostUpdatedCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  Pour obtenir immédiatement le résumé de la plus à jour à partir de la base de données locale. Il a paramètres ci-dessous :<br><br>\*@param {KASFormFlatSummary} flatSummary peut être une valeur null en cas d’erreur<br><br>\*@param {KASFormProcessedSummary} processedSummary peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |
| notifyCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  Pour recevoir un avertissement la synthèse le plus récent extraites du serveur. Il a paramètres ci-dessous :<br><br>\*@param {KASFormFlatSummary} flatSummary peut être une valeur null en cas d’erreur<br><br>\*@param {KASFormProcessedSummary} processedSummary peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getformurlasync"></a>

###  <a name="getformurlasync"></a>getFormURLAsync

▸ **getFormURLAsync**(rappel : *`function`*) :`void`

Obtient l’url du fichier contenant les réponses plats associés au formulaire de serveur

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*url @param {chaîne} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getformusercapabilitiesasync"></a>

###  <a name="getformusercapabilitiesasync"></a>getFormUserCapabilitiesAsync

▸ **getFormUserCapabilitiesAsync**(rappel : *`function`*) :`void`

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*autorisations @param {KASFormUserCapabilities}<br><br>\*chaîne d’erreur erreur @param {chaîne} en cas d’erreur ; Sinon, valeur null |

**Renvoie :** `void`

___

<a id="issubscribed"></a>

###  <a name="issubscribed"></a>isSubscribed

▸ **isSubscribed**(rappel : *`function`*) :`void`

Détermine si l’utilisateur actuel est abonné ou non

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*abonné de la valeur true si les utilisateurs isSubscribed @param {boolean} |

**Renvoie :** `void`

___

<a id="likeform"></a>

###  <a name="likeform"></a>likeForm

▸ **likeForm**() :`void`

Pour ajouter un décompte similaire à un formulaire, le nombre de demandes peuvent entraîner une diminution si l’utilisateur actuel a aimé déjà le formulaire

**Renvoie :** `void`

___

<a id="sendreminderstorespond"></a>

###  <a name="sendreminderstorespond"></a>sendRemindersToRespond

▸ **sendRemindersToRespond**() :`void`

Envoie un rappel (une nouvelle carte de conversation) par rapport à la carte existante

**Renvoie :** `void`

___

<a id="shareformurl"></a>

###  <a name="shareformurl"></a>shareFormURL

▸ **shareFormURL**(url : *`string`*) :`void`

Partager l’url du résultat extraite serveur - lance partager native écran pour l’url du formulaire

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| url | `string` |  à partager |

**Renvoie :** `void`

___

<a id="showallreactions"></a>

###  <a name="showallreactions"></a>showAllReactions

▸ **showAllReactions**(showComments? : *`boolean`*) :`void`

Affiche tous les la réaction écran (J’aime et commentaires) par rapport à l’écran

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`showComments | `boolean` | true |  valeur True si les commentaires doivent également être affichés ; False dans le cas contraire |

**Renvoie :** `void`

___

<a id="updateactioninstancelocaldatacacheasync"></a>

###  <a name="updateactioninstancelocaldatacacheasync"></a>updateActionInstanceLocalDataCacheAsync

▸ **updateActionInstanceLocalDataCacheAsync**(actionProperties : *[KASActionProperties](../classes/kasclient.kasactionproperties.md)*, rappel : *`function`*) :`void`

Mises à jour/enregistre les propriétés ActionInstance donnée dans le cache de données local que ces propriétés sont stockées au niveau instance de l’action. Pour chaque instance de l’action peut enregistrer certaines données locales dans le cache et il seulement sera accessible par cette instance particulière

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

Cette API ne fonctionne pas comme prévu en cas d’historique des messages.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| actionProperties | [KASActionProperties](../classes/kasclient.kasactionproperties.md) |  Propriétés du ActionInstance/formulaire pour être mis à jour/enregistré |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*réussite @param {boolean} indique si la mise à jour est réussie ou non<br><br>\*chaîne json d’erreur de @param {chaîne} pour l’objet KASError contenant la description et/ou le code d’erreur. |

**Renvoie :** `void`

___

<a id="updateactionpackagelocaldatacacheasync"></a>

###  <a name="updateactionpackagelocaldatacacheasync"></a>updateActionPackageLocalDataCacheAsync

▸ **updateActionPackageLocalDataCacheAsync**(actionPackageProperties : *[KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md)*, rappel : *`function`*) :`void`

Mises à jour/enregistre les propriétés du Package Action donné dans le cache de données local que ces propriétés sont enregistrées au niveau du lot d’action. Ainsi, les données sont partagées entre toutes les instances de l’action créés à partir de ce package d’action.

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

Cette API ne fonctionne pas comme prévu en cas d’historique des messages.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| actionPackageProperties | [KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md) |  Propriétés du Package action soit mis à jour/enregistré |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*réussite @param {boolean} indique si la mise à jour est réussie ou non<br><br>\*chaîne json d’erreur de @param {chaîne} pour l’objet KASError contenant la description et/ou le code d’erreur. |

**Renvoie :** `void`

___

<a id="updateformpropertiesasync"></a>

###  <a name="updateformpropertiesasync"></a>updateFormPropertiesAsync

▸ **updateFormPropertiesAsync**(propertyUpdates : *[] [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md)*, notifyUsers : * `string`[]*, notificationMessage : *`string`*, rappel : *`function`*) :`void`

Publier une demande pour mettre à jour les propriétés associées à l’écran

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

| Nom | Type | Description |
| ------ | ------ | ------ |
| propertyUpdates | [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md) [] |  un tableau de toutes les infos de mise à jour qui sont nécessaires pour être effectuée, mise à jour infos peuvent être créés à l’aide de KASFormPropertyUpdateFactory |
| notifyUsers | `string`[] |  envoyer des notifications push à ces noms d’utilisateurs concernant cette mise à jour |
| notificationMessage | `string` |  message de notification push |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*réussite @param {boolean} indique si la mise à jour est réussie ou non |

**Renvoie :** `void`

___

