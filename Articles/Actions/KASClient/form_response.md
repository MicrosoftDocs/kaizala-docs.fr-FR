#   <a name="form-response-flow-apis"></a><span data-ttu-id="f8f06-101">API de flux de réponse de formulaire:</span><span class="sxs-lookup"><span data-stu-id="f8f06-101">Form response flow APIs:</span></span>

| <span data-ttu-id="f8f06-102">**API**</span><span class="sxs-lookup"><span data-stu-id="f8f06-102">**API**</span></span> | <span data-ttu-id="f8f06-103">Description</span><span class="sxs-lookup"><span data-stu-id="f8f06-103">Description</span></span> | <span data-ttu-id="f8f06-104">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="f8f06-104">Request Parameter</span></span> | <span data-ttu-id="f8f06-105">Sortie de la réponse</span><span class="sxs-lookup"><span data-stu-id="f8f06-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f8f06-106">**canRespondToFormAsync**</span><span class="sxs-lookup"><span data-stu-id="f8f06-106">**canRespondToFormAsync**</span></span> | <span data-ttu-id="f8f06-107">Indique si l'utilisateur actuel peut répondre au formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8f06-107">Gets whether the current user can respond to the form</span></span> |  | <span data-ttu-id="f8f06-108">canRespond (Boolean)-true si l'utilisateur actuel est autorisé à répondre</span><span class="sxs-lookup"><span data-stu-id="f8f06-108">canRespond (Boolean) - true if current user is allowed to respond</span></span> |
| <span data-ttu-id="f8f06-109">**getFormAsync**</span><span class="sxs-lookup"><span data-stu-id="f8f06-109">**getFormAsync**</span></span> | | | <span data-ttu-id="f8f06-110">Objet Form</span><span class="sxs-lookup"><span data-stu-id="f8f06-110">Form object</span></span> |
| <span data-ttu-id="f8f06-111">**getFormStatusAsync**</span><span class="sxs-lookup"><span data-stu-id="f8f06-111">**getFormStatusAsync**</span></span> | <span data-ttu-id="f8f06-112">Obtient l'état du formulaire associé à la carte de conversation.</span><span class="sxs-lookup"><span data-stu-id="f8f06-112">Gets the status of the form associated with the conversation card</span></span> | | <span data-ttu-id="f8f06-113">isActive (Boolean)-true si le formulaire n'a pas encore expiré</span><span class="sxs-lookup"><span data-stu-id="f8f06-113">isActive (Boolean) - true if the form is not yet expired</span></span> |
| <span data-ttu-id="f8f06-114">**getMyFormResponsesAsync**</span><span class="sxs-lookup"><span data-stu-id="f8f06-114">**getMyFormResponsesAsync**</span></span> | <span data-ttu-id="f8f06-115">Obtient toutes les réponses de l'utilisateur actuel sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8f06-115">Gets all the responses of the current user against the form</span></span> | | <span data-ttu-id="f8f06-116">Tableau d'objets Response</span><span class="sxs-lookup"><span data-stu-id="f8f06-116">Array of response objects</span></span> |
| <span data-ttu-id="f8f06-117">**sumbitFormResponse**</span><span class="sxs-lookup"><span data-stu-id="f8f06-117">**sumbitFormResponse**</span></span> | <span data-ttu-id="f8f06-118">Envoie une nouvelle réponse au formulaire associé à la carte de conversation: fait disparaître l'écran actuel</span><span class="sxs-lookup"><span data-stu-id="f8f06-118">Submits a new response against the form associated with the conversation card – dismisses the current screen</span></span> |  <ul><li><span data-ttu-id="f8f06-119">questionToAnswerMap (JSON)-ID de question pour le mappage des réponses</span><span class="sxs-lookup"><span data-stu-id="f8f06-119">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="f8f06-120">responseId (chaîne) à remplir si la réponse actuelle est une modification ou mise à jour d'une précédente</span><span class="sxs-lookup"><span data-stu-id="f8f06-120">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="f8f06-121">isEdit (Boolean) indique si la réponse actuelle est une modification ou mise à jour d'une précédente.</span><span class="sxs-lookup"><span data-stu-id="f8f06-121">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="f8f06-122">showInChatCanvas (Boolean) indique si une carte de conversation distincte doit être créée pour cette réponse ou non.</span><span class="sxs-lookup"><span data-stu-id="f8f06-122">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="f8f06-123">isAnonymous (Boolean) indique si la réponse doit être inscrite en tant que anonyme ou non</span><span class="sxs-lookup"><span data-stu-id="f8f06-123">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |
| <span data-ttu-id="f8f06-124">**sumbitFormResponseWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="f8f06-124">**sumbitFormResponseWithoutDismiss**</span></span> | <span data-ttu-id="f8f06-125">Envoie une nouvelle réponse au formulaire associé à la carte de conversation sans faire disparaître l'écran actuel.</span><span class="sxs-lookup"><span data-stu-id="f8f06-125">Submits a new response against the form associated with the conversation card without dismissing the current screen</span></span> |  <ul><li><span data-ttu-id="f8f06-126">questionToAnswerMap (JSON)-ID de question pour le mappage des réponses</span><span class="sxs-lookup"><span data-stu-id="f8f06-126">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="f8f06-127">responseId (chaîne) à remplir si la réponse actuelle est une modification ou mise à jour d'une précédente</span><span class="sxs-lookup"><span data-stu-id="f8f06-127">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="f8f06-128">isEdit (Boolean) indique si la réponse actuelle est une modification ou mise à jour d'une précédente.</span><span class="sxs-lookup"><span data-stu-id="f8f06-128">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="f8f06-129">showInChatCanvas (Boolean) indique si une carte de conversation distincte doit être créée pour cette réponse ou non.</span><span class="sxs-lookup"><span data-stu-id="f8f06-129">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="f8f06-130">isAnonymous (Boolean) indique si la réponse doit être inscrite en tant que anonyme ou non</span><span class="sxs-lookup"><span data-stu-id="f8f06-130">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |


##  <a name="get-the-associated-form"></a><span data-ttu-id="f8f06-131">Obtenir le formulaire associé</span><span class="sxs-lookup"><span data-stu-id="f8f06-131">Get the associated Form</span></span>

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a><span data-ttu-id="f8f06-132">Vérifiez si le formulaire associé a expiré ou non.</span><span class="sxs-lookup"><span data-stu-id="f8f06-132">Check if the associated form is expired or not</span></span>

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a><span data-ttu-id="f8f06-133">Obtenir toutes les réponses de l'utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="f8f06-133">Get all the responses of the current user</span></span>

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a><span data-ttu-id="f8f06-134">Envoyer une nouvelle réponse pour le formulaire associé</span><span class="sxs-lookup"><span data-stu-id="f8f06-134">Submit a new response for the associated Form</span></span>

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
