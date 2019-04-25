#   <a name="form-response-flow-apis"></a>API de flux de réponse de formulaire:

| **API** | Description | Paramètre de requête | Sortie de la réponse |
| :---: | :---: | :---: | :--- |
| **canRespondToFormAsync** | Indique si l'utilisateur actuel peut répondre au formulaire. |  | canRespond (Boolean)-true si l'utilisateur actuel est autorisé à répondre |
| **getFormAsync** | | | Objet Form |
| **getFormStatusAsync** | Obtient l'état du formulaire associé à la carte de conversation. | | isActive (Boolean)-true si le formulaire n'a pas encore expiré |
| **getMyFormResponsesAsync** | Obtient toutes les réponses de l'utilisateur actuel sur le formulaire. | | Tableau d'objets Response |
| **sumbitFormResponse** | Envoie une nouvelle réponse au formulaire associé à la carte de conversation: fait disparaître l'écran actuel |  <ul><li>questionToAnswerMap (JSON)-ID de question pour le mappage des réponses</li><li>responseId (chaîne) à remplir si la réponse actuelle est une modification ou mise à jour d'une précédente</li><li>isEdit (Boolean) indique si la réponse actuelle est une modification ou mise à jour d'une précédente.</li><li>showInChatCanvas (Boolean) indique si une carte de conversation distincte doit être créée pour cette réponse ou non.</li><li>isAnonymous (Boolean) indique si la réponse doit être inscrite en tant que anonyme ou non</li></ul> | |
| **sumbitFormResponseWithoutDismiss** | Envoie une nouvelle réponse au formulaire associé à la carte de conversation sans faire disparaître l'écran actuel. |  <ul><li>questionToAnswerMap (JSON)-ID de question pour le mappage des réponses</li><li>responseId (chaîne) à remplir si la réponse actuelle est une modification ou mise à jour d'une précédente</li><li>isEdit (Boolean) indique si la réponse actuelle est une modification ou mise à jour d'une précédente.</li><li>showInChatCanvas (Boolean) indique si une carte de conversation distincte doit être créée pour cette réponse ou non.</li><li>isAnonymous (Boolean) indique si la réponse doit être inscrite en tant que anonyme ou non</li></ul> | |


##  <a name="get-the-associated-form"></a>Obtenir le formulaire associé

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a>Vérifiez si le formulaire associé a expiré ou non.

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a>Obtenir toutes les réponses de l'utilisateur actuel

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a>Envoyer une nouvelle réponse pour le formulaire associé

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
