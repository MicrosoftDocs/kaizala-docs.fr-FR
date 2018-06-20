#   <a name="form-creation-flow-apis"></a>Formulaire de flux de création API :

| **API** | Description | Paramètre de demande | Sortie de réponse |
| :---: | :---: | :---: | :--- |
| **initFormAsync** | Initialise et renvoie un objet de formulaire vide basé sur le fichier de formulaire par défaut dans le package |  | Form, objet |
| **submitFormRequest** | Envoie le formulaire nouvellement créé en tant que demande. Cette action entraîne une nouvelle carte de conversation | <ul><li>Formulaire</li><li>Boolean – devrait pas augmenter</li></ul>| |
| **submitFormRequestWithoutDismiss** | Envoie le formulaire nouvellement créé en tant que demande. Cette action entraîne une nouvelle carte de conversation |<ul><li>Formulaire</li><li>Boolean – devrait pas augmenter</li></ul>| |
| **updateForm** | Utilisé pour apporter des modifications dans les champs de formulaire comme titre, description et paramètres | <ul><li>Champs qui nécessitent la mise à jour</li><li>Boolean – devrait pas augmenter</li></ul> | |

##  <a name="initialize-a-form"></a>Initialisation d’un formulaire

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a>Envoyer le formulaire nouvellement créé

```typescript
/**
  * Submits the newly created form as a request. This results a new conversation card
  * @param {KASForm} form
  */
  function submitFormRequest(form: KASForm)
  ```

```typescript
  /**
  * Submits the newly created form as a request. This results a new conversation card
  * @param {KASForm} form
  */
  function submitFormRequestWithoutDismiss(form: KASForm, shouldInflate: boolean)
  ```


##  <a name="update-form"></a>Formulaire de mise à jour

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

