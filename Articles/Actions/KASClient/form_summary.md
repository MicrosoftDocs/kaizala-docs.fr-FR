#   <a name="form-summary-flow-apis"></a>Formulaire de flux synthèse API :

| **API** | Description | Paramètre de demande | Sortie de réponse |
| :---: | :---: | :---: | :--- |
| **shouldSeeFormSummaryAsync** | Détermine si le formulaire de synthèse est visible à l’utilisateur actuel |  | *shouldSeeSummary ((valeur booléenne))* - true si l’utilisateur actuel est autorisé à voir Résumé |
| **getFormSummaryAsync** | Obtient les réponses à tous les utilisateurs et résumé traité à partir de toutes les réponses associés au formulaire | Implique le rappel de synthèse de formulaire à deux dimensions et de traitement de rappel de synthèse de formulaire | Objets de synthèse |
| **getFlatFormSummaryAsync** | Obtient les réponses plats par tous les utilisateurs associés au formulaire (il est recommandé d’utiliser des getFormSummary() au lieu de cela) | | *flatSummary* – objet résumé |
| **getProcessedFormSummaryAsync** | Obtient le résumé traité à partir de toutes les réponses associé au formulaire (il est recommandé d’utiliser des getFormSummary() au lieu de cela) | | *processedSummary* – objet résumé |
| **getAggregatedFormSummaryAsync** | Obtient agrégées récapitulative à partir de toutes les réponses associés au formulaire | | *aggregatedSummary* – objet résumé |
| **getFormURLAsync** | Obtient l’url du fichier contenant les réponses plats associés au formulaire de serveur | | Url |
| **shareFormURL** | Lance le partage native écran pour l’url du formulaire | URL à partager | |
| **getFormReactionAsync** | Obtient la réaction consolidée (J’aime et commentaires) de la carte de conversation associée au formulaire | | Objet réaction |
| **showAllReactions** | Affiche tous les la réaction écran (J’aime et commentaires) par rapport à l’écran | | |
| **likeForm** | Pour ajouter un décompte similaire à un formulaire, le nombre de demandes peuvent entraîner une diminution si l’utilisateur actuel a aimé déjà le formulaire | | |
| **addCommentOnForm** | Demandes d’ajout d’un commentaire à un formulaire | | |
| **respondToForm** | Demandes d’ajout d’une réponse à un formulaire, en lançant l’écran de réponse | | |
| **sendRemindersToRespond** | Envoie un rappel (une nouvelle carte de conversation) par rapport à la carte existante | | |
| **copyFormAndForward** | Lance le sélecteur de conversation pour transférer une copie du formulaire existant en tant qu’une nouvelle carte de conversation | | |
| **updateFormPropertiesAsync** | Publier une demande pour mettre à jour les propriétés associées à l’écran |  <ul><li>*propertyUpdates* - un tableau de toutes les infos de mise à jour qui sont nécessaires pour être effectuée – *tableau de KASFormPropertyUpdateInfo*</li><li>*notifyUsers* - envoyer des notifications push pour ces noms d’utilisateurs concernant cette mise à jour – *tableau de chaînes*</li><li>*notificationMessage* - de message de notification push *chaîne*</li></ul> | *Success(Boolean)* - indique la réussite ou l’échec de la mise à jour|

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

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a>Obtenir le résumé plat (toutes les réponses) associé au formulaire

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a>Obtenir le résumé traité (réponses agrégées) associé au formulaire

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a>Extraction (serveur) et obtenir l’url du résultat (toutes les réponses) associé au formulaire

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a>Partager le résultat qu'url extraites du serveur

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a>Obtenir tous les réactions associées au formulaire

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a>Afficher tous les réactions associées au formulaire

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a>Placez un type sur le formulaire (activer la carte de conversation associée)

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a>Afficher le mode de réponse pour le formulaire

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a>Rappeler les autres personnes doivent répondre

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a>Transférer un nouveau formulaire double de celle associée

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a>Fermer le formulaire (en activer les réponses lui)

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
