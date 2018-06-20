#   <a name="form-summary-flow-apis"></a><span data-ttu-id="f41aa-101">Formulaire de flux synthèse API :</span><span class="sxs-lookup"><span data-stu-id="f41aa-101">Form summary flow APIs:</span></span>

| <span data-ttu-id="f41aa-102">**API**</span><span class="sxs-lookup"><span data-stu-id="f41aa-102">**API**</span></span> | <span data-ttu-id="f41aa-103">Description</span><span class="sxs-lookup"><span data-stu-id="f41aa-103">Description</span></span> | <span data-ttu-id="f41aa-104">Paramètre de demande</span><span class="sxs-lookup"><span data-stu-id="f41aa-104">Request Parameter</span></span> | <span data-ttu-id="f41aa-105">Sortie de réponse</span><span class="sxs-lookup"><span data-stu-id="f41aa-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f41aa-106">**shouldSeeFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-106">**shouldSeeFormSummaryAsync**</span></span> | <span data-ttu-id="f41aa-107">Détermine si le formulaire de synthèse est visible à l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="f41aa-107">Gets whether the form summary is visible to the current user</span></span> |  | <span data-ttu-id="f41aa-108">*shouldSeeSummary ((valeur booléenne))* - true si l’utilisateur actuel est autorisé à voir Résumé</span><span class="sxs-lookup"><span data-stu-id="f41aa-108">*shouldSeeSummary (boolean)* - true if current user is allowed to see summary</span></span> |
| <span data-ttu-id="f41aa-109">**getFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-109">**getFormSummaryAsync**</span></span> | <span data-ttu-id="f41aa-110">Obtient les réponses à tous les utilisateurs et résumé traité à partir de toutes les réponses associés au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-110">Gets responses by all the users, and processed summary from all the responses associated with the form</span></span> | <span data-ttu-id="f41aa-111">Implique le rappel de synthèse de formulaire à deux dimensions et de traitement de rappel de synthèse de formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-111">Involves flat form summary callback and processed form summary callback</span></span> | <span data-ttu-id="f41aa-112">Objets de synthèse</span><span class="sxs-lookup"><span data-stu-id="f41aa-112">Summary objects</span></span> |
| <span data-ttu-id="f41aa-113">**getFlatFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-113">**getFlatFormSummaryAsync**</span></span> | <span data-ttu-id="f41aa-114">Obtient les réponses plats par tous les utilisateurs associés au formulaire (il est recommandé d’utiliser des getFormSummary() au lieu de cela)</span><span class="sxs-lookup"><span data-stu-id="f41aa-114">Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="f41aa-115">*flatSummary* – objet résumé</span><span class="sxs-lookup"><span data-stu-id="f41aa-115">*flatSummary* – summary object</span></span> |
| <span data-ttu-id="f41aa-116">**getProcessedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-116">**getProcessedFormSummaryAsync**</span></span> | <span data-ttu-id="f41aa-117">Obtient le résumé traité à partir de toutes les réponses associé au formulaire (il est recommandé d’utiliser des getFormSummary() au lieu de cela)</span><span class="sxs-lookup"><span data-stu-id="f41aa-117">Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="f41aa-118">*processedSummary* – objet résumé</span><span class="sxs-lookup"><span data-stu-id="f41aa-118">*processedSummary* – summary object</span></span> |
| <span data-ttu-id="f41aa-119">**getAggregatedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-119">**getAggregatedFormSummaryAsync**</span></span> | <span data-ttu-id="f41aa-120">Obtient agrégées récapitulative à partir de toutes les réponses associés au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-120">Gets aggregated summary from all the responses associated with the form</span></span> | | <span data-ttu-id="f41aa-121">*aggregatedSummary* – objet résumé</span><span class="sxs-lookup"><span data-stu-id="f41aa-121">*aggregatedSummary* – summary object</span></span> |
| <span data-ttu-id="f41aa-122">**getFormURLAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-122">**getFormURLAsync**</span></span> | <span data-ttu-id="f41aa-123">Obtient l’url du fichier contenant les réponses plats associés au formulaire de serveur</span><span class="sxs-lookup"><span data-stu-id="f41aa-123">Gets the file url from server containing flat responses associated with the form</span></span> | | <span data-ttu-id="f41aa-124">Url</span><span class="sxs-lookup"><span data-stu-id="f41aa-124">Url</span></span> |
| <span data-ttu-id="f41aa-125">**shareFormURL**</span><span class="sxs-lookup"><span data-stu-id="f41aa-125">**shareFormURL**</span></span> | <span data-ttu-id="f41aa-126">Lance le partage native écran pour l’url du formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-126">Launches native share screen for the form url</span></span> | <span data-ttu-id="f41aa-127">URL à partager</span><span class="sxs-lookup"><span data-stu-id="f41aa-127">Url to be shared</span></span> | |
| <span data-ttu-id="f41aa-128">**getFormReactionAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-128">**getFormReactionAsync**</span></span> | <span data-ttu-id="f41aa-129">Obtient la réaction consolidée (J’aime et commentaires) de la carte de conversation associée au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-129">Gets the consolidated reaction (likes and comments) of the conversation card associated with the form</span></span> | | <span data-ttu-id="f41aa-130">Objet réaction</span><span class="sxs-lookup"><span data-stu-id="f41aa-130">Reaction object</span></span> |
| <span data-ttu-id="f41aa-131">**showAllReactions**</span><span class="sxs-lookup"><span data-stu-id="f41aa-131">**showAllReactions**</span></span> | <span data-ttu-id="f41aa-132">Affiche tous les la réaction écran (J’aime et commentaires) par rapport à l’écran</span><span class="sxs-lookup"><span data-stu-id="f41aa-132">Shows all the reaction screen (likes and comments) against the form</span></span> | | |
| <span data-ttu-id="f41aa-133">**likeForm**</span><span class="sxs-lookup"><span data-stu-id="f41aa-133">**likeForm**</span></span> | <span data-ttu-id="f41aa-134">Pour ajouter un décompte similaire à un formulaire, le nombre de demandes peuvent entraîner une diminution si l’utilisateur actuel a aimé déjà le formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-134">Requests to add a like count to a form, the count may decrease if the current user has already liked the form</span></span> | | |
| <span data-ttu-id="f41aa-135">**addCommentOnForm**</span><span class="sxs-lookup"><span data-stu-id="f41aa-135">**addCommentOnForm**</span></span> | <span data-ttu-id="f41aa-136">Demandes d’ajout d’un commentaire à un formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-136">Requests to add a comment to a form</span></span> | | |
| <span data-ttu-id="f41aa-137">**respondToForm**</span><span class="sxs-lookup"><span data-stu-id="f41aa-137">**respondToForm**</span></span> | <span data-ttu-id="f41aa-138">Demandes d’ajout d’une réponse à un formulaire, en lançant l’écran de réponse</span><span class="sxs-lookup"><span data-stu-id="f41aa-138">Requests to add a response to a form, by launching response screen</span></span> | | |
| <span data-ttu-id="f41aa-139">**sendRemindersToRespond**</span><span class="sxs-lookup"><span data-stu-id="f41aa-139">**sendRemindersToRespond**</span></span> | <span data-ttu-id="f41aa-140">Envoie un rappel (une nouvelle carte de conversation) par rapport à la carte existante</span><span class="sxs-lookup"><span data-stu-id="f41aa-140">Sends a reminder (a new conversation card) against the existing card</span></span> | | |
| <span data-ttu-id="f41aa-141">**copyFormAndForward**</span><span class="sxs-lookup"><span data-stu-id="f41aa-141">**copyFormAndForward**</span></span> | <span data-ttu-id="f41aa-142">Lance le sélecteur de conversation pour transférer une copie du formulaire existant en tant qu’une nouvelle carte de conversation</span><span class="sxs-lookup"><span data-stu-id="f41aa-142">Launches the conversation picker to forward a copy of the existing form as a new conversation card</span></span> | | |
| <span data-ttu-id="f41aa-143">**updateFormPropertiesAsync**</span><span class="sxs-lookup"><span data-stu-id="f41aa-143">**updateFormPropertiesAsync**</span></span> | <span data-ttu-id="f41aa-144">Publier une demande pour mettre à jour les propriétés associées à l’écran</span><span class="sxs-lookup"><span data-stu-id="f41aa-144">Post a request to update the properties associated with the form</span></span> |  <ul><li><span data-ttu-id="f41aa-145">*propertyUpdates* - un tableau de toutes les infos de mise à jour qui sont nécessaires pour être effectuée – *tableau de KASFormPropertyUpdateInfo*</span><span class="sxs-lookup"><span data-stu-id="f41aa-145">*propertyUpdates* - an array of all update infos that are needed to be performed – *array of KASFormPropertyUpdateInfo*</span></span></li><li><span data-ttu-id="f41aa-146">*notifyUsers* - envoyer des notifications push pour ces noms d’utilisateurs concernant cette mise à jour – *tableau de chaînes*</span><span class="sxs-lookup"><span data-stu-id="f41aa-146">*notifyUsers* - send push notifications to these user ids regarding this update – *array of strings*</span></span></li><li><span data-ttu-id="f41aa-147">*notificationMessage* - de message de notification push *chaîne*</span><span class="sxs-lookup"><span data-stu-id="f41aa-147">*notificationMessage* - push notification message *string*</span></span></li></ul> | <span data-ttu-id="f41aa-148">*Success(Boolean)* - indique la réussite ou l’échec de la mise à jour</span><span class="sxs-lookup"><span data-stu-id="f41aa-148">*Success(Boolean)* - denotes the success/failure of the update</span></span>|

##   <a name="get-the-summary-associated-with-the-form"></a><span data-ttu-id="f41aa-149">Obtenir le résumé associé au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-149">Get the summary associated with the Form</span></span>

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

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a><span data-ttu-id="f41aa-150">Obtenir le résumé plat (toutes les réponses) associé au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-150">Get the flat summary (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a><span data-ttu-id="f41aa-151">Obtenir le résumé traité (réponses agrégées) associé au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-151">Get the processed summary (aggregated responses) associated with the Form</span></span>

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a><span data-ttu-id="f41aa-152">Extraction (serveur) et obtenir l’url du résultat (toutes les réponses) associé au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-152">Fetch (from server) and get the result url (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a><span data-ttu-id="f41aa-153">Partager le résultat qu'url extraites du serveur</span><span class="sxs-lookup"><span data-stu-id="f41aa-153">Share the result url fetched from server</span></span>

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="f41aa-154">Obtenir tous les réactions associées au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-154">Get all the reactions associated with the Form</span></span>

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="f41aa-155">Afficher tous les réactions associées au formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-155">Show all the reactions associated with the Form</span></span>

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a><span data-ttu-id="f41aa-156">Placez un type sur le formulaire (activer la carte de conversation associée)</span><span class="sxs-lookup"><span data-stu-id="f41aa-156">Put a like on the Form (in turn the associated conversation card)</span></span>

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a><span data-ttu-id="f41aa-157">Afficher le mode de réponse pour le formulaire</span><span class="sxs-lookup"><span data-stu-id="f41aa-157">Show response view for the Form</span></span>

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a><span data-ttu-id="f41aa-158">Rappeler les autres personnes doivent répondre</span><span class="sxs-lookup"><span data-stu-id="f41aa-158">Remind other people to respond</span></span>

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a><span data-ttu-id="f41aa-159">Transférer un nouveau formulaire double de celle associée</span><span class="sxs-lookup"><span data-stu-id="f41aa-159">Forward a new Form duplicated from the associated one</span></span>

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a><span data-ttu-id="f41aa-160">Fermer le formulaire (en activer les réponses lui)</span><span class="sxs-lookup"><span data-stu-id="f41aa-160">Close the Form (in turn responses to it)</span></span>

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
