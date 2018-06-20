#   <a name="form-creation-flow-apis"></a><span data-ttu-id="c1f1b-101">Formulaire de flux de création API :</span><span class="sxs-lookup"><span data-stu-id="c1f1b-101">Form creation flow APIs:</span></span>

| <span data-ttu-id="c1f1b-102">**API**</span><span class="sxs-lookup"><span data-stu-id="c1f1b-102">**API**</span></span> | <span data-ttu-id="c1f1b-103">Description</span><span class="sxs-lookup"><span data-stu-id="c1f1b-103">Description</span></span> | <span data-ttu-id="c1f1b-104">Paramètre de demande</span><span class="sxs-lookup"><span data-stu-id="c1f1b-104">Request Parameter</span></span> | <span data-ttu-id="c1f1b-105">Sortie de réponse</span><span class="sxs-lookup"><span data-stu-id="c1f1b-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="c1f1b-106">**initFormAsync**</span><span class="sxs-lookup"><span data-stu-id="c1f1b-106">**initFormAsync**</span></span> | <span data-ttu-id="c1f1b-107">Initialise et renvoie un objet de formulaire vide basé sur le fichier de formulaire par défaut dans le package</span><span class="sxs-lookup"><span data-stu-id="c1f1b-107">Initializes and returns an empty form object based on the default form file present in the package</span></span> |  | <span data-ttu-id="c1f1b-108">Form, objet</span><span class="sxs-lookup"><span data-stu-id="c1f1b-108">Form Object</span></span> |
| <span data-ttu-id="c1f1b-109">**submitFormRequest**</span><span class="sxs-lookup"><span data-stu-id="c1f1b-109">**submitFormRequest**</span></span> | <span data-ttu-id="c1f1b-110">Envoie le formulaire nouvellement créé en tant que demande.</span><span class="sxs-lookup"><span data-stu-id="c1f1b-110">Submits the newly created form as a request.</span></span> <span data-ttu-id="c1f1b-111">Cette action entraîne une nouvelle carte de conversation</span><span class="sxs-lookup"><span data-stu-id="c1f1b-111">This results a new conversation card</span></span> | <ul><li><span data-ttu-id="c1f1b-112">Formulaire</span><span class="sxs-lookup"><span data-stu-id="c1f1b-112">Form</span></span></li><li><span data-ttu-id="c1f1b-113">Boolean – devrait pas augmenter</span><span class="sxs-lookup"><span data-stu-id="c1f1b-113">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="c1f1b-114">**submitFormRequestWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="c1f1b-114">**submitFormRequestWithoutDismiss**</span></span> | <span data-ttu-id="c1f1b-115">Envoie le formulaire nouvellement créé en tant que demande.</span><span class="sxs-lookup"><span data-stu-id="c1f1b-115">Submits the newly created form as a request.</span></span> <span data-ttu-id="c1f1b-116">Cette action entraîne une nouvelle carte de conversation</span><span class="sxs-lookup"><span data-stu-id="c1f1b-116">This results a new conversation card</span></span> |<ul><li><span data-ttu-id="c1f1b-117">Formulaire</span><span class="sxs-lookup"><span data-stu-id="c1f1b-117">Form</span></span></li><li><span data-ttu-id="c1f1b-118">Boolean – devrait pas augmenter</span><span class="sxs-lookup"><span data-stu-id="c1f1b-118">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="c1f1b-119">**updateForm**</span><span class="sxs-lookup"><span data-stu-id="c1f1b-119">**updateForm**</span></span> | <span data-ttu-id="c1f1b-120">Utilisé pour apporter des modifications dans les champs de formulaire comme titre, description et paramètres</span><span class="sxs-lookup"><span data-stu-id="c1f1b-120">Used for making changes in form fields like title, description and settings</span></span> | <ul><li><span data-ttu-id="c1f1b-121">Champs qui nécessitent la mise à jour</span><span class="sxs-lookup"><span data-stu-id="c1f1b-121">Fields that require updation</span></span></li><li><span data-ttu-id="c1f1b-122">Boolean – devrait pas augmenter</span><span class="sxs-lookup"><span data-stu-id="c1f1b-122">Boolean – should inflate/not</span></span></li></ul> | |

##  <a name="initialize-a-form"></a><span data-ttu-id="c1f1b-123">Initialisation d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="c1f1b-123">Initialize a Form</span></span>

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a><span data-ttu-id="c1f1b-124">Envoyer le formulaire nouvellement créé</span><span class="sxs-lookup"><span data-stu-id="c1f1b-124">Submit the newly created Form</span></span>

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


##  <a name="update-form"></a><span data-ttu-id="c1f1b-125">Formulaire de mise à jour</span><span class="sxs-lookup"><span data-stu-id="c1f1b-125">Update Form</span></span>

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

