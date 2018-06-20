#   <a name="form-response-flow-apis"></a><span data-ttu-id="9da8c-101">Formulaire de flux de réponse API :</span><span class="sxs-lookup"><span data-stu-id="9da8c-101">Form response flow APIs:</span></span>

| <span data-ttu-id="9da8c-102">**API**</span><span class="sxs-lookup"><span data-stu-id="9da8c-102">**API**</span></span> | <span data-ttu-id="9da8c-103">Description</span><span class="sxs-lookup"><span data-stu-id="9da8c-103">Description</span></span> | <span data-ttu-id="9da8c-104">Paramètre de demande</span><span class="sxs-lookup"><span data-stu-id="9da8c-104">Request Parameter</span></span> | <span data-ttu-id="9da8c-105">Sortie de réponse</span><span class="sxs-lookup"><span data-stu-id="9da8c-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="9da8c-106">**canRespondToFormAsync**</span><span class="sxs-lookup"><span data-stu-id="9da8c-106">**canRespondToFormAsync**</span></span> | <span data-ttu-id="9da8c-107">Indique si l’utilisateur actuel peut répondre à l’écran</span><span class="sxs-lookup"><span data-stu-id="9da8c-107">Gets whether the current user can respond to the form</span></span> |  | <span data-ttu-id="9da8c-108">canRespond (Boolean) : true si l’utilisateur actuel est autorisé à répondre</span><span class="sxs-lookup"><span data-stu-id="9da8c-108">canRespond (Boolean) - true if current user is allowed to respond</span></span> |
| <span data-ttu-id="9da8c-109">**getFormAsync**</span><span class="sxs-lookup"><span data-stu-id="9da8c-109">**getFormAsync**</span></span> | | | <span data-ttu-id="9da8c-110">Objet de formulaire</span><span class="sxs-lookup"><span data-stu-id="9da8c-110">Form object</span></span> |
| <span data-ttu-id="9da8c-111">**getFormStatusAsync**</span><span class="sxs-lookup"><span data-stu-id="9da8c-111">**getFormStatusAsync**</span></span> | <span data-ttu-id="9da8c-112">Obtient l’état du formulaire associé à la carte de conversation</span><span class="sxs-lookup"><span data-stu-id="9da8c-112">Gets the status of the form associated with the conversation card</span></span> | | <span data-ttu-id="9da8c-113">isActive (Boolean) : true si le formulaire n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="9da8c-113">isActive (Boolean) - true if the form is not yet expired</span></span> |
| <span data-ttu-id="9da8c-114">**getMyFormResponsesAsync**</span><span class="sxs-lookup"><span data-stu-id="9da8c-114">**getMyFormResponsesAsync**</span></span> | <span data-ttu-id="9da8c-115">Obtient toutes les réponses de l’utilisateur actuel par rapport à l’écran</span><span class="sxs-lookup"><span data-stu-id="9da8c-115">Gets all the responses of the current user against the form</span></span> | | <span data-ttu-id="9da8c-116">Tableau d’objets de réponse</span><span class="sxs-lookup"><span data-stu-id="9da8c-116">Array of response objects</span></span> |
| <span data-ttu-id="9da8c-117">**sumbitFormResponse**</span><span class="sxs-lookup"><span data-stu-id="9da8c-117">**sumbitFormResponse**</span></span> | <span data-ttu-id="9da8c-118">Envoie une réponse par rapport à la forme associée à la carte de conversation – ferme l’écran en cours</span><span class="sxs-lookup"><span data-stu-id="9da8c-118">Submits a new response against the form associated with the conversation card – dismisses the current screen</span></span> |  <ul><li><span data-ttu-id="9da8c-119">questionToAnswerMap (JSON) - id question pour répondre aux mappage</span><span class="sxs-lookup"><span data-stu-id="9da8c-119">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="9da8c-120">responseId(string) à remplir si la réponse en cours est une modification/mise à jour une précédente</span><span class="sxs-lookup"><span data-stu-id="9da8c-120">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="9da8c-121">isEdit (boolean) indique si la réponse en cours est une modification/mise à jour une précédente</span><span class="sxs-lookup"><span data-stu-id="9da8c-121">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="9da8c-122">showInChatCanvas(Boolean) indique si une carte de conversation distinct doit être créé pour cette réponse ou non</span><span class="sxs-lookup"><span data-stu-id="9da8c-122">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="9da8c-123">isAnonymous(boolean) indique si la réponse doit être enregistrée en tant qu’anonyme ou non</span><span class="sxs-lookup"><span data-stu-id="9da8c-123">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |
| <span data-ttu-id="9da8c-124">**sumbitFormResponseWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="9da8c-124">**sumbitFormResponseWithoutDismiss**</span></span> | <span data-ttu-id="9da8c-125">Envoie une réponse par rapport à la forme associée à la carte de conversation sans faire disparaître l’écran en cours</span><span class="sxs-lookup"><span data-stu-id="9da8c-125">Submits a new response against the form associated with the conversation card without dismissing the current screen</span></span> |  <ul><li><span data-ttu-id="9da8c-126">questionToAnswerMap (JSON) - id question pour répondre aux mappage</span><span class="sxs-lookup"><span data-stu-id="9da8c-126">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="9da8c-127">responseId(string) à remplir si la réponse en cours est une modification/mise à jour une précédente</span><span class="sxs-lookup"><span data-stu-id="9da8c-127">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="9da8c-128">isEdit (boolean) indique si la réponse en cours est une modification/mise à jour une précédente</span><span class="sxs-lookup"><span data-stu-id="9da8c-128">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="9da8c-129">showInChatCanvas(Boolean) indique si une carte de conversation distinct doit être créé pour cette réponse ou non</span><span class="sxs-lookup"><span data-stu-id="9da8c-129">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="9da8c-130">isAnonymous(boolean) indique si la réponse doit être enregistrée en tant qu’anonyme ou non</span><span class="sxs-lookup"><span data-stu-id="9da8c-130">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |


##  <a name="get-the-associated-form"></a><span data-ttu-id="9da8c-131">Obtenir la forme associée</span><span class="sxs-lookup"><span data-stu-id="9da8c-131">Get the associated Form</span></span>

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a><span data-ttu-id="9da8c-132">Vérifier si le formulaire associé est arrivé à expiration ou non</span><span class="sxs-lookup"><span data-stu-id="9da8c-132">Check if the associated form is expired or not</span></span>

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a><span data-ttu-id="9da8c-133">Obtenir toutes les réponses de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="9da8c-133">Get all the responses of the current user</span></span>

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a><span data-ttu-id="9da8c-134">Envoyer une nouvelle réponse pour le formulaire associé</span><span class="sxs-lookup"><span data-stu-id="9da8c-134">Submit a new response for the associated Form</span></span>

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
