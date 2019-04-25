#   <a name="form-summary-flow-apis"></a>API de flux de synthèse de formulaire:

| **API** | Description | Paramètre de requête | Sortie de la réponse |
| :---: | :---: | :---: | :--- |
| **shouldSeeFormSummaryAsync** | Obtient une valeur indiquant si le résumé du formulaire est visible par l'utilisateur actuel. |  | *shouldSeeSummary (Boolean)* -true si l'utilisateur actuel est autorisé à afficher la synthèse |
| **getFormSummaryAsync** | Obtient les réponses de tous les utilisateurs et le résumé traité de toutes les réponses associées au formulaire. | Inclut le rappel de résumé de formulaire plat et le rappel de résumé de formulaire traité | Objets de synthèse |
| **getFlatFormSummaryAsync** | Obtient les réponses plates de tous les utilisateurs associés au formulaire (il est recommandé d'utiliser getFormSummary () à la place de celui-ci) | | *flatSummary* : objet de synthèse |
| **getProcessedFormSummaryAsync** | Obtient le résumé traité de toutes les réponses associées au formulaire (il est recommandé d'utiliser getFormSummary () à la place de celui-ci) | | *processedSummary* : objet de synthèse |
| **getAggregatedFormSummaryAsync** | Obtient une synthèse agrégée de toutes les réponses associées au formulaire. | | *aggregatedSummary* : objet de synthèse |
| **getFormURLAsync** | Obtient l'URL de fichier à partir du serveur contenant les réponses plates associées au formulaire. | | Url |
| **shareFormURL** | Lance l'écran de partage natif pour l'URL du formulaire | URL à partager | |
| **getFormReactionAsync** | Obtient la réaction consolidée (j'aime et les commentaires) de la carte de conversation associée au formulaire. | | Objet reAction |
| **showAllReactions** | Affiche tous les écrans de réaction (j'aime et commentaires) sur le formulaire | | |
| **likeForm** | Demandes d'ajout d'un nombre similaire à un formulaire, le nombre peut diminuer si l'utilisateur actuel a déjà aimé le formulaire. | | |
| **addCommentOnForm** | Demandes d'ajout d'un commentaire à un formulaire | | |
| **respondToForm** | Demandes d'ajout d'une réponse à un formulaire, en lançant l'écran de réponse | | |
| **sendRemindersToRespond** | Envoie un rappel (une nouvelle carte de conversation) à la carte existante | | |
| **copyFormAndForward** | Lance le sélecteur de conversation pour transférer une copie du formulaire existant en tant que nouvelle carte de conversation | | |
| **updateFormPropertiesAsync** | Publier une demande pour mettre à jour les propriétés associées au formulaire |  <ul><li>*propertyUpdates* -tableau de toutes les informations de mise à jour qui sont nécessaires à l'exécution – *tableau de KASFormPropertyUpdateInfo*</li><li>*notifyUsers* -envoyer des notifications de type émission à ces ID d'utilisateur concernant cette mise à jour – *tableau de chaînes*</li><li>*notification* - *chaîne* de message de notification de type poussé</li></ul> | *Success (Boolean)* : indique la réussite ou l'échec de la mise à jour|

##   <a name="get-the-summary-associated-with-the-form"></a>Obtenir le résumé associé au formulaire

```typescript 
/**
  * Gets flat responses by all the users, and processed summary from all the responses associated
  * with the form. It requires two callbacks:
  * @param {Callback} mostUpdatedCallback to immediately get the most updated summary from local database. It has below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  * @param {Callback} notifyCallback to get notified with the latest summary fetched from server. It has below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  *
  * This is useful when the network is flaky/disconnected, so that summary can
  * immediately be shown with the present data we have, but with an option to refresh
  * it later on arrival of latest data from server! None of the callbacks are mandatory,
  * so if 1st is nil, this method can be used to always fetch summary from server, and
  * if 2nd is nil, this can be used to always fetch summary from local database!
  */
  function getFormSummaryAsync(mostUpdatedCallback: function(flatSummary: KASFormFlatSummary, processedSummary: KASFormProcessedSummary, error: string),
                   notifyCallback: function(flatSummary: KASFormFlatSummary, processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a>Obtenir le résumé plat (toutes les réponses) associées au formulaire

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a>Obtenir le résumé traité (réponses agrégées) associées au formulaire

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a>Extraire (à partir du serveur) et obtenir l'URL de résultat (toutes les réponses) associées au formulaire

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a>Partager l'URL de résultats extraite à partir du serveur

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a>Obtenir toutes les réactions associées au formulaire

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a>Afficher toutes les réactions associées au formulaire

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a>Placer un comme sur le formulaire (à son tour, la carte de conversation associée)

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a>Afficher l'affichage des réponses pour le formulaire

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a>Rappeler aux autres personnes de répondre

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a>Transférer un nouveau formulaire dupliqué à partir du associé

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a>Fermer le formulaire (en lui transformeant des réponses)

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
