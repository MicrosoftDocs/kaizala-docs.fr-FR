#   <a name="app-apis"></a><span data-ttu-id="9449a-101">API d’application :</span><span class="sxs-lookup"><span data-stu-id="9449a-101">App APIs:</span></span>

| <span data-ttu-id="9449a-102">**API**</span><span class="sxs-lookup"><span data-stu-id="9449a-102">**API**</span></span> | <span data-ttu-id="9449a-103">Description</span><span class="sxs-lookup"><span data-stu-id="9449a-103">Description</span></span> | <span data-ttu-id="9449a-104">Paramètre de demande</span><span class="sxs-lookup"><span data-stu-id="9449a-104">Request Parameter</span></span> | <span data-ttu-id="9449a-105">Sortie de réponse</span><span class="sxs-lookup"><span data-stu-id="9449a-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="9449a-106">**getUsersDetailsAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-106">**getUsersDetailsAsync**</span></span> | <span data-ttu-id="9449a-107">Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leur ID</span><span class="sxs-lookup"><span data-stu-id="9449a-107">Gets users' details (name, pic, phone number, etc.) against their ids</span></span> | <span data-ttu-id="9449a-108">userIds tableau des ID d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9449a-108">userIds array of user ids</span></span> | <span data-ttu-id="9449a-109">*JSON d’infos utilisateur*</span><span class="sxs-lookup"><span data-stu-id="9449a-109">*JSON of user info*</span></span> |
| <span data-ttu-id="9449a-110">**showContactPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-110">**showContactPickerAsync**</span></span> | <span data-ttu-id="9449a-111">Affiche un sélecteur de contact natif et renvoie un tableau de détails de tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9449a-111">Shows a native contact picker, and returns an array of all the selected users' detail</span></span> | <ul><li><span data-ttu-id="9449a-112">*titre du sélecteur de Contact*</span><span class="sxs-lookup"><span data-stu-id="9449a-112">*title of Contact Picker*</span></span></li><li><span data-ttu-id="9449a-113">*selectedMutableUser* - tableau des ID utilisateur sélectionné</span><span class="sxs-lookup"><span data-stu-id="9449a-113">*selectedMutableUser* - array of selected userIds</span></span></li><li><span data-ttu-id="9449a-114">*selectedImmutableUser* - tableau des ID utilisateur sélectionné fixe</span><span class="sxs-lookup"><span data-stu-id="9449a-114">*selectedImmutableUser* - array of fixed selected userIds</span></span></li><li><span data-ttu-id="9449a-115">*isSingleSelection* - seule sélection dans le sélecteur de contacts</span><span class="sxs-lookup"><span data-stu-id="9449a-115">*isSingleSelection* - single selection in Contact Picker</span></span></li></ul> | <span data-ttu-id="9449a-116">Tableau des détails de tous les utilisateurs (*Tableau de JSON*)</span><span class="sxs-lookup"><span data-stu-id="9449a-116">Array of all the selected users' details (*Array of JSON*)</span></span> |
| <span data-ttu-id="9449a-117">**showImagePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-117">**showImagePickerAsync**</span></span> | <span data-ttu-id="9449a-118">Affiche un sélecteur d’images natif et renvoie le chemin d’accès de l’image sélectionnée</span><span class="sxs-lookup"><span data-stu-id="9449a-118">Shows a native image picker, and returns the selected image path</span></span> | | <span data-ttu-id="9449a-119">*Emplacement de l’image sélectionnée*</span><span class="sxs-lookup"><span data-stu-id="9449a-119">*Selected image location*</span></span> |
| <span data-ttu-id="9449a-120">**showAttachmentPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-120">**showAttachmentPickerAsync**</span></span> | <span data-ttu-id="9449a-121">Affiche un sélecteur de pièce jointe dans la couche native</span><span class="sxs-lookup"><span data-stu-id="9449a-121">Displays an attachment picker in the native layer</span></span> | <ul><li><span data-ttu-id="9449a-122">*supportedTypes* - tableau des types de pièce jointe pris en charge pour le sélecteur</span><span class="sxs-lookup"><span data-stu-id="9449a-122">*supportedTypes* - array of supported attachment types for the picker</span></span></li><li><span data-ttu-id="9449a-123">propriétés supplémentaires pour configurer le sélecteur</span><span class="sxs-lookup"><span data-stu-id="9449a-123">additional props to configure the picker</span></span></li></ul> | |
| <span data-ttu-id="9449a-124">**downloadAttachmentAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-124">**downloadAttachmentAsync**</span></span> | <span data-ttu-id="9449a-125">Télécharger la pièce jointe spécifiée</span><span class="sxs-lookup"><span data-stu-id="9449a-125">Download the attachment specified</span></span> | <ul><li><span data-ttu-id="9449a-126">*avec un chemin d’accès de serveur valide pour télécharger des pièces jointes*</span><span class="sxs-lookup"><span data-stu-id="9449a-126">*attachment with a valid server path to download*</span></span></li><li><span data-ttu-id="9449a-127">rappel à la fin du téléchargement</span><span class="sxs-lookup"><span data-stu-id="9449a-127">callback on download completion</span></span></li></ul> | |
| <span data-ttu-id="9449a-128">**cancelAttachmentDownloadAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-128">**cancelAttachmentDownloadAsync**</span></span> | <span data-ttu-id="9449a-129">Annuler une opération de téléchargement en file d’attente d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="9449a-129">Cancel a download operation queued for an attachment</span></span> | <span data-ttu-id="9449a-130">pièce jointe</span><span class="sxs-lookup"><span data-stu-id="9449a-130">attachment</span></span> | |
| <span data-ttu-id="9449a-131">**showPlacePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-131">**showPlacePickerAsync**</span></span> | <span data-ttu-id="9449a-132">Affiche un sélecteur de place natif et renvoie le lieu sélectionné (lt, lg, n)</span><span class="sxs-lookup"><span data-stu-id="9449a-132">Shows a native place picker, and returns the selected place (lt, lg, n)</span></span> | <span data-ttu-id="9449a-133">Emplacement sélectionné</span><span class="sxs-lookup"><span data-stu-id="9449a-133">Selected location</span></span> | <span data-ttu-id="9449a-134">Latitude/longitude</span><span class="sxs-lookup"><span data-stu-id="9449a-134">Latitude/longitude</span></span> |
| <span data-ttu-id="9449a-135">**showLocationOnMap**</span><span class="sxs-lookup"><span data-stu-id="9449a-135">**showLocationOnMap**</span></span> | <span data-ttu-id="9449a-136">Emplacement de donné s’ouvre des cartes natives avec</span><span class="sxs-lookup"><span data-stu-id="9449a-136">Opens up native maps with given location</span></span> | <span data-ttu-id="9449a-137">Type de [KASLocation](KASLocation.md)</span><span class="sxs-lookup"><span data-stu-id="9449a-137">[KASLocation](KASLocation.md) type</span></span> | |
| <span data-ttu-id="9449a-138">**showDurationPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-138">**showDurationPickerAsync**</span></span> | <span data-ttu-id="9449a-139">Affiche un sélecteur de durée native avec jour/heure/minute</span><span class="sxs-lookup"><span data-stu-id="9449a-139">Shows a native duration picker with day/hour/minute</span></span> | <span data-ttu-id="9449a-140">Durée par défaut à afficher dans le sélecteur</span><span class="sxs-lookup"><span data-stu-id="9449a-140">Default duration to be shown on picker</span></span> | |
| <span data-ttu-id="9449a-141">**isTalkBackEnabledAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-141">**isTalkBackEnabledAsync**</span></span> | <span data-ttu-id="9449a-142">Indique si talkback est activé ou non</span><span class="sxs-lookup"><span data-stu-id="9449a-142">Gets whether talkback is enabled or not</span></span> | | <span data-ttu-id="9449a-143">Bool�en</span><span class="sxs-lookup"><span data-stu-id="9449a-143">Boolean</span></span> |
| <span data-ttu-id="9449a-144">**generateUUIDAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-144">**generateUUIDAsync**</span></span> | <span data-ttu-id="9449a-145">Obtient le nouvel UUID</span><span class="sxs-lookup"><span data-stu-id="9449a-145">Gets the new UUID</span></span> | | <span data-ttu-id="9449a-146">Uuid nouvellement créé</span><span class="sxs-lookup"><span data-stu-id="9449a-146">Newly generated uuid</span></span> |
| <span data-ttu-id="9449a-147">**getCurrentDeviceLocationAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-147">**getCurrentDeviceLocationAsync**</span></span> | <span data-ttu-id="9449a-148">Obtient l’emplacement actuel du périphérique</span><span class="sxs-lookup"><span data-stu-id="9449a-148">Gets the current device location</span></span> | | |
| <span data-ttu-id="9449a-149">**getAppLocaleAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-149">**getAppLocaleAsync**</span></span> | <span data-ttu-id="9449a-150">Obtient les paramètres régionaux application-langue dans laquelle l’application s’affiche, utile pour localiser les chaînes de l’Action</span><span class="sxs-lookup"><span data-stu-id="9449a-150">Gets the current app locale -language in which the app is rendered, useful for localizing Action's strings</span></span> | | <span data-ttu-id="9449a-151">Locale</span><span class="sxs-lookup"><span data-stu-id="9449a-151">Locale</span></span> |
| <span data-ttu-id="9449a-152">**getConversationParticipantsCountAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-152">**getConversationParticipantsCountAsync**</span></span> | <span data-ttu-id="9449a-153">Obtient tous les participants-ID de la conversation en cours</span><span class="sxs-lookup"><span data-stu-id="9449a-153">Gets all the participant-ids of the current conversation</span></span> | | <span data-ttu-id="9449a-154">Nombre de participants</span><span class="sxs-lookup"><span data-stu-id="9449a-154">Count of participants</span></span> |
| <span data-ttu-id="9449a-155">**getConversationNameAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-155">**getConversationNameAsync**</span></span> | <span data-ttu-id="9449a-156">Obtient le nom actuel de la conversation</span><span class="sxs-lookup"><span data-stu-id="9449a-156">Gets the current conversation name</span></span> | | <span data-ttu-id="9449a-157">Nom de la conversation</span><span class="sxs-lookup"><span data-stu-id="9449a-157">Name of the conversation</span></span> |
| <span data-ttu-id="9449a-158">**dismissCurrentScreen**</span><span class="sxs-lookup"><span data-stu-id="9449a-158">**dismissCurrentScreen**</span></span> | <span data-ttu-id="9449a-159">Faire disparaître l’écran actuel (création, réponse ou résumé)</span><span class="sxs-lookup"><span data-stu-id="9449a-159">Dismiss the current screen (Creation, Response, or Summary)</span></span> | | |
| <span data-ttu-id="9449a-160">**ShowProgressBar indique**</span><span class="sxs-lookup"><span data-stu-id="9449a-160">**showProgressBar**</span></span> | <span data-ttu-id="9449a-161">Affiche une barre de progression de l ' écran complète native avec le texte donné</span><span class="sxs-lookup"><span data-stu-id="9449a-161">Shows a native full sreen progress bar with the given text</span></span> | <span data-ttu-id="9449a-162">Texte à afficher</span><span class="sxs-lookup"><span data-stu-id="9449a-162">Text to display</span></span> | |
| <span data-ttu-id="9449a-163">**hideProgressBar**</span><span class="sxs-lookup"><span data-stu-id="9449a-163">**hideProgressBar**</span></span> | <span data-ttu-id="9449a-164">Masque la barre de progression en cours, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="9449a-164">Hides the current progress bar, if any</span></span> | | |
| <span data-ttu-id="9449a-165">**getCurrentUserIdAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-165">**getCurrentUserIdAsync**</span></span> | <span data-ttu-id="9449a-166">Obtient le nom d’utilisateur qui a ouvert l’Action en cours</span><span class="sxs-lookup"><span data-stu-id="9449a-166">Gets the current user id who has opened the Action</span></span> | | <span data-ttu-id="9449a-167">User ID</span><span class="sxs-lookup"><span data-stu-id="9449a-167">User ID</span></span> |
| <span data-ttu-id="9449a-168">**showImageImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="9449a-168">**showImageImmersiveView**</span></span> | <span data-ttu-id="9449a-169">Affiche l’Image en mode immersif</span><span class="sxs-lookup"><span data-stu-id="9449a-169">Shows Image in Immersive view</span></span> | <span data-ttu-id="9449a-170">Tableau d’url d’images</span><span class="sxs-lookup"><span data-stu-id="9449a-170">Array of images url</span></span> | |
| <span data-ttu-id="9449a-171">**openAttachmentImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="9449a-171">**openAttachmentImmersiveView**</span></span> | <span data-ttu-id="9449a-172">Ouvrir la pièce jointe en mode immersif</span><span class="sxs-lookup"><span data-stu-id="9449a-172">Open attachment in Immersive view</span></span> | <span data-ttu-id="9449a-173">Objet Attachment</span><span class="sxs-lookup"><span data-stu-id="9449a-173">Attachment object</span></span> | |
| <span data-ttu-id="9449a-174">**hasStorageAccessForAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="9449a-174">**hasStorageAccessForAttachmentType**</span></span> | <span data-ttu-id="9449a-175">vérifie si application dispose d’un accès en lecture/écriture pour le stockage</span><span class="sxs-lookup"><span data-stu-id="9449a-175">checks whether app has read/write access to the storage</span></span> | <span data-ttu-id="9449a-176">Type de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="9449a-176">Attachment type</span></span> | |
| <span data-ttu-id="9449a-177">**generateBase64ThumbnailAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-177">**generateBase64ThumbnailAsync**</span></span> | <span data-ttu-id="9449a-178">Génère une image miniature en Base64</span><span class="sxs-lookup"><span data-stu-id="9449a-178">Generates Base64 thumbnail for an image</span></span> | <span data-ttu-id="9449a-179">localPath pour l’imageAttachment dont miniature doit être généré</span><span class="sxs-lookup"><span data-stu-id="9449a-179">localPath for the imageAttachment whose thumbnail needs to be generated</span></span> | |
| <span data-ttu-id="9449a-180">**getFontSizeMultiplierAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-180">**getFontSizeMultiplierAsync**</span></span> | <span data-ttu-id="9449a-181">Obtient le multiplicateur de taille de police de texte de grande taille - courant uniquement nécessaire pour iOS</span><span class="sxs-lookup"><span data-stu-id="9449a-181">Gets the font size multiplier for large text -   Current only required by iOS</span></span> | | |
| <span data-ttu-id="9449a-182">**getLocalizedStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-182">**getLocalizedStringsAsync**</span></span> | <span data-ttu-id="9449a-183">Obtient le dictionnaire des chaînes localisées en fonction de paramètres régionaux application en cours</span><span class="sxs-lookup"><span data-stu-id="9449a-183">Gets the localized strings' dictionary based on current app locale</span></span> | <span data-ttu-id="9449a-184">Chaînes doivent être fournis dans le package, par exemple : strings_en.json, strings_hi.json, etc..</span><span class="sxs-lookup"><span data-stu-id="9449a-184">Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.</span></span>    | <span data-ttu-id="9449a-185">Chaînes JSON</span><span class="sxs-lookup"><span data-stu-id="9449a-185">Strings JSON</span></span> |
| <span data-ttu-id="9449a-186">**logToReport**</span><span class="sxs-lookup"><span data-stu-id="9449a-186">**logToReport**</span></span> | <span data-ttu-id="9449a-187">Enregistre une erreur pour « Envoyer le rapport »</span><span class="sxs-lookup"><span data-stu-id="9449a-187">Logs an error for "Send report"</span></span> | <span data-ttu-id="9449a-188">Type de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="9449a-188">Attachment type</span></span> | |
| <span data-ttu-id="9449a-189">**isCurrentUserO365SubscribedAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-189">**isCurrentUserO365SubscribedAsync**</span></span> | <span data-ttu-id="9449a-190">Vérifie si l’abonné utilisateur un O365 actuel</span><span class="sxs-lookup"><span data-stu-id="9449a-190">Checks if the current user an O365 subscriber</span></span> | | <span data-ttu-id="9449a-191">Bool�en</span><span class="sxs-lookup"><span data-stu-id="9449a-191">Boolean</span></span> |
| <span data-ttu-id="9449a-192">**registerHardwareBackPressCallback**</span><span class="sxs-lookup"><span data-stu-id="9449a-192">**registerHardwareBackPressCallback**</span></span> | <span data-ttu-id="9449a-193">Enregistre un rappel à exécuter sur matériel, appuyez sur le bouton précédent (pour Android)</span><span class="sxs-lookup"><span data-stu-id="9449a-193">Registers a callback to be executed on hardware back button press (for Android)</span></span> | | |
| <span data-ttu-id="9449a-194">**initLocalizationStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="9449a-194">**initLocalizationStringsAsync**</span></span> | <span data-ttu-id="9449a-195">Initialise le mappage des chaînes de la localisation</span><span class="sxs-lookup"><span data-stu-id="9449a-195">Initializes the localization strings' map</span></span> | <span data-ttu-id="9449a-196">Dictionnaire - feuille de route des chaînes</span><span class="sxs-lookup"><span data-stu-id="9449a-196">Dictionary  - the strings' map</span></span> | <span data-ttu-id="9449a-197">Success(Boolean) indique la réussite ou l’échec de l’initialisation</span><span class="sxs-lookup"><span data-stu-id="9449a-197">Success(Boolean) denotes the success/failure of the initialization</span></span> |
| <span data-ttu-id="9449a-198">**getString**</span><span class="sxs-lookup"><span data-stu-id="9449a-198">**getString**</span></span> |   <span data-ttu-id="9449a-199">Retourne une chaîne de fichier des chaînes localisées</span><span class="sxs-lookup"><span data-stu-id="9449a-199">Returns a string from the localized strings' file</span></span> |<span data-ttu-id="9449a-200">stringid d'</span><span class="sxs-lookup"><span data-stu-id="9449a-200">stringId</span></span> ||


##  <a name="get-user-info"></a><span data-ttu-id="9449a-201">Obtenir les informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="9449a-201">Get user info</span></span>

```typescript
/**
  * Gets users' details (name, pic, phone number, etc.) against their ids
  * @param {string[]} userIds array of user ids
  * @param {Callback} callback with below parameters:
  * * * * @param {Dictionary<UserId: string, UserInfo: KASUser>} userIdToInfoMap (users' details against their ids) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getUsersDetailsAsync(userIds: string[], callback: function(userIdToInfoMap: {}, error: string))
```

##  <a name="show-contact-picker"></a><span data-ttu-id="9449a-202">Afficher le sélecteur de contacts</span><span class="sxs-lookup"><span data-stu-id="9449a-202">Show contact picker</span></span>

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a><span data-ttu-id="9449a-203">Afficher le sélecteur d’images</span><span class="sxs-lookup"><span data-stu-id="9449a-203">Show image picker</span></span>

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a><span data-ttu-id="9449a-204">Obtenir l’emplacement actuel de l’unité</span><span class="sxs-lookup"><span data-stu-id="9449a-204">Get current device location</span></span>

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a><span data-ttu-id="9449a-205">Sélecteur d’emplacement</span><span class="sxs-lookup"><span data-stu-id="9449a-205">Place picker</span></span>

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a><span data-ttu-id="9449a-206">Afficher l’emplacement sur les cartes</span><span class="sxs-lookup"><span data-stu-id="9449a-206">Show location on maps</span></span>

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a><span data-ttu-id="9449a-207">Afficher le message d’erreur (alerte ou toast)</span><span class="sxs-lookup"><span data-stu-id="9449a-207">Show error message (alert or toast)</span></span>

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a><span data-ttu-id="9449a-208">Obtenir la langue en cours utilisé par l’application</span><span class="sxs-lookup"><span data-stu-id="9449a-208">Get current language used by the app</span></span>

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a><span data-ttu-id="9449a-209">Obtenir le nom de la conversation en cours</span><span class="sxs-lookup"><span data-stu-id="9449a-209">Get the name of the current conversation</span></span>

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a><span data-ttu-id="9449a-210">Ignorer l’écran de l’Action actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="9449a-210">Dismiss the currently opened Action's screen</span></span>

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a><span data-ttu-id="9449a-211">Afficher la barre de progression native</span><span class="sxs-lookup"><span data-stu-id="9449a-211">Show native progress bar</span></span>

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a><span data-ttu-id="9449a-212">Masquer la barre de progression native</span><span class="sxs-lookup"><span data-stu-id="9449a-212">Hide native progress bar</span></span>

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a><span data-ttu-id="9449a-213">Obtenir l’id d’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="9449a-213">Get current user id</span></span>

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a><span data-ttu-id="9449a-214">S’inscrire pour appuyer sur le bouton précédent de matériel (Android)</span><span class="sxs-lookup"><span data-stu-id="9449a-214">Register for hardware back button press (Android)</span></span>

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a><span data-ttu-id="9449a-215">Localisation d’Action</span><span class="sxs-lookup"><span data-stu-id="9449a-215">Localization for Action</span></span>

```typescript
/**
  * Gets the localized strings' dictionary based on current app locale.
  * Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.
  * @param {Callback} callback with below parameters:
  * * * * @param {JSON} strings can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getLocalizedStringsAsync(callback: (strings: JSON, error: string))
```

##  <a name="printf-for-action"></a><span data-ttu-id="9449a-216">printf() d’Action</span><span class="sxs-lookup"><span data-stu-id="9449a-216">printf() for Action</span></span>

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
