#   <a name="form-creation-flow-apis"></a><span data-ttu-id="6be1e-101">API de flux de création de formulaire:</span><span class="sxs-lookup"><span data-stu-id="6be1e-101">Form creation flow APIs:</span></span>

| <span data-ttu-id="6be1e-102">**API**</span><span class="sxs-lookup"><span data-stu-id="6be1e-102">**API**</span></span> | <span data-ttu-id="6be1e-103">Description</span><span class="sxs-lookup"><span data-stu-id="6be1e-103">Description</span></span> | <span data-ttu-id="6be1e-104">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="6be1e-104">Request Parameter</span></span> | <span data-ttu-id="6be1e-105">Sortie de la réponse</span><span class="sxs-lookup"><span data-stu-id="6be1e-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="6be1e-106">**initFormAsync**</span><span class="sxs-lookup"><span data-stu-id="6be1e-106">**initFormAsync**</span></span> | <span data-ttu-id="6be1e-107">Initialise et renvoie un objet Form vide basé sur le fichier de formulaire par défaut présent dans le package.</span><span class="sxs-lookup"><span data-stu-id="6be1e-107">Initializes and returns an empty form object based on the default form file present in the package</span></span> |  | <span data-ttu-id="6be1e-108">Form, objet</span><span class="sxs-lookup"><span data-stu-id="6be1e-108">Form Object</span></span> |
| <span data-ttu-id="6be1e-109">**submitFormRequest**</span><span class="sxs-lookup"><span data-stu-id="6be1e-109">**submitFormRequest**</span></span> | <span data-ttu-id="6be1e-110">Envoie le formulaire nouvellement créé sous la forme d'une requête.</span><span class="sxs-lookup"><span data-stu-id="6be1e-110">Submits the newly created form as a request.</span></span> <span data-ttu-id="6be1e-111">Cela aboutit à une nouvelle carte de conversation</span><span class="sxs-lookup"><span data-stu-id="6be1e-111">This results a new conversation card</span></span> | <ul><li><span data-ttu-id="6be1e-112">Formulaire</span><span class="sxs-lookup"><span data-stu-id="6be1e-112">Form</span></span></li><li><span data-ttu-id="6be1e-113">Boolean – doit être gonflé/non</span><span class="sxs-lookup"><span data-stu-id="6be1e-113">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="6be1e-114">**submitFormRequestWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="6be1e-114">**submitFormRequestWithoutDismiss**</span></span> | <span data-ttu-id="6be1e-115">Envoie le formulaire nouvellement créé sous la forme d'une requête.</span><span class="sxs-lookup"><span data-stu-id="6be1e-115">Submits the newly created form as a request.</span></span> <span data-ttu-id="6be1e-116">Cela aboutit à une nouvelle carte de conversation</span><span class="sxs-lookup"><span data-stu-id="6be1e-116">This results a new conversation card</span></span> |<ul><li><span data-ttu-id="6be1e-117">Formulaire</span><span class="sxs-lookup"><span data-stu-id="6be1e-117">Form</span></span></li><li><span data-ttu-id="6be1e-118">Boolean – doit être gonflé/non</span><span class="sxs-lookup"><span data-stu-id="6be1e-118">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="6be1e-119">**updateForm**</span><span class="sxs-lookup"><span data-stu-id="6be1e-119">**updateForm**</span></span> | <span data-ttu-id="6be1e-120">Utilisé pour apporter des modifications aux champs de formulaire comme le titre, la description et les paramètres</span><span class="sxs-lookup"><span data-stu-id="6be1e-120">Used for making changes in form fields like title, description and settings</span></span> | <ul><li><span data-ttu-id="6be1e-121">Champs nécessitant une mise à jour</span><span class="sxs-lookup"><span data-stu-id="6be1e-121">Fields that require updation</span></span></li><li><span data-ttu-id="6be1e-122">Boolean – doit être gonflé/non</span><span class="sxs-lookup"><span data-stu-id="6be1e-122">Boolean – should inflate/not</span></span></li></ul> | |

##  <a name="initialize-a-form"></a><span data-ttu-id="6be1e-123">Initialiser un formulaire</span><span class="sxs-lookup"><span data-stu-id="6be1e-123">Initialize a Form</span></span>

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a><span data-ttu-id="6be1e-124">Envoyer le formulaire nouvellement créé</span><span class="sxs-lookup"><span data-stu-id="6be1e-124">Submit the newly created Form</span></span>

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


##  <a name="update-form"></a><span data-ttu-id="6be1e-125">Formulaire de mise à jour</span><span class="sxs-lookup"><span data-stu-id="6be1e-125">Update Form</span></span>

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

