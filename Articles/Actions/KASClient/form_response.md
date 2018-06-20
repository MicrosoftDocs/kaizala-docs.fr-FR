#   <a name="form-response-flow-apis"></a>Formulaire de flux de réponse API :

| **API** | Description | Paramètre de demande | Sortie de réponse |
| :---: | :---: | :---: | :--- |
| **canRespondToFormAsync** | Indique si l’utilisateur actuel peut répondre à l’écran |  | canRespond (Boolean) : true si l’utilisateur actuel est autorisé à répondre |
| **getFormAsync** | | | Objet de formulaire |
| **getFormStatusAsync** | Obtient l’état du formulaire associé à la carte de conversation | | isActive (Boolean) : true si le formulaire n’est pas encore terminée. |
| **getMyFormResponsesAsync** | Obtient toutes les réponses de l’utilisateur actuel par rapport à l’écran | | Tableau d’objets de réponse |
| **sumbitFormResponse** | Envoie une réponse par rapport à la forme associée à la carte de conversation – ferme l’écran en cours |  <ul><li>questionToAnswerMap (JSON) - id question pour répondre aux mappage</li><li>responseId(string) à remplir si la réponse en cours est une modification/mise à jour une précédente</li><li>isEdit (boolean) indique si la réponse en cours est une modification/mise à jour une précédente</li><li>showInChatCanvas(Boolean) indique si une carte de conversation distinct doit être créé pour cette réponse ou non</li><li>isAnonymous(boolean) indique si la réponse doit être enregistrée en tant qu’anonyme ou non</li></ul> | |
| **sumbitFormResponseWithoutDismiss** | Envoie une réponse par rapport à la forme associée à la carte de conversation sans faire disparaître l’écran en cours |  <ul><li>questionToAnswerMap (JSON) - id question pour répondre aux mappage</li><li>responseId(string) à remplir si la réponse en cours est une modification/mise à jour une précédente</li><li>isEdit (boolean) indique si la réponse en cours est une modification/mise à jour une précédente</li><li>showInChatCanvas(Boolean) indique si une carte de conversation distinct doit être créé pour cette réponse ou non</li><li>isAnonymous(boolean) indique si la réponse doit être enregistrée en tant qu’anonyme ou non</li></ul> | |


##  <a name="get-the-associated-form"></a>Obtenir la forme associée

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a>Vérifier si le formulaire associé est arrivé à expiration ou non

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a>Obtenir toutes les réponses de l’utilisateur actuel

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
