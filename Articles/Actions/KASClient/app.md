#   <a name="app-apis"></a><span data-ttu-id="efbe8-101">API d'application:</span><span class="sxs-lookup"><span data-stu-id="efbe8-101">App APIs:</span></span>

| <span data-ttu-id="efbe8-102">**API**</span><span class="sxs-lookup"><span data-stu-id="efbe8-102">**API**</span></span> | <span data-ttu-id="efbe8-103">Description</span><span class="sxs-lookup"><span data-stu-id="efbe8-103">Description</span></span> | <span data-ttu-id="efbe8-104">Paramètre de requête</span><span class="sxs-lookup"><span data-stu-id="efbe8-104">Request Parameter</span></span> | <span data-ttu-id="efbe8-105">Sortie de la réponse</span><span class="sxs-lookup"><span data-stu-id="efbe8-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="efbe8-106">**getUsersDetailsAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-106">**getUsersDetailsAsync**</span></span> | <span data-ttu-id="efbe8-107">Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leurs ID.</span><span class="sxs-lookup"><span data-stu-id="efbe8-107">Gets users' details (name, pic, phone number, etc.) against their ids</span></span> | <span data-ttu-id="efbe8-108">Tableau des ID utilisateur</span><span class="sxs-lookup"><span data-stu-id="efbe8-108">userIds array of user ids</span></span> | <span data-ttu-id="efbe8-109">*JSON des informations utilisateur*</span><span class="sxs-lookup"><span data-stu-id="efbe8-109">*JSON of user info*</span></span> |
| <span data-ttu-id="efbe8-110">**showContactPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-110">**showContactPickerAsync**</span></span> | <span data-ttu-id="efbe8-111">Affiche un sélecteur de contacts natif et renvoie un tableau de tous les détails des utilisateurs sélectionnés</span><span class="sxs-lookup"><span data-stu-id="efbe8-111">Shows a native contact picker, and returns an array of all the selected users' detail</span></span> | <ul><li><span data-ttu-id="efbe8-112">*titre du sélecteur de contacts*</span><span class="sxs-lookup"><span data-stu-id="efbe8-112">*title of Contact Picker*</span></span></li><li><span data-ttu-id="efbe8-113">*selectedMutableUser* -tableau d'ID utilisateur sélectionnés</span><span class="sxs-lookup"><span data-stu-id="efbe8-113">*selectedMutableUser* - array of selected userIds</span></span></li><li><span data-ttu-id="efbe8-114">*selectedImmutableUser* : tableau des ID utilisateur sélectionnés fixes</span><span class="sxs-lookup"><span data-stu-id="efbe8-114">*selectedImmutableUser* - array of fixed selected userIds</span></span></li><li><span data-ttu-id="efbe8-115">*isSingleSelection* -sélection unique dans le sélecteur de contacts</span><span class="sxs-lookup"><span data-stu-id="efbe8-115">*isSingleSelection* - single selection in Contact Picker</span></span></li></ul> | <span data-ttu-id="efbe8-116">Tableau de tous les détails des utilisateurs sélectionnés (*tableau de JSON*)</span><span class="sxs-lookup"><span data-stu-id="efbe8-116">Array of all the selected users' details (*Array of JSON*)</span></span> |
| <span data-ttu-id="efbe8-117">**showImagePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-117">**showImagePickerAsync**</span></span> | <span data-ttu-id="efbe8-118">Affiche un sélecteur d'image native et renvoie le chemin d'accès à l'image sélectionnée</span><span class="sxs-lookup"><span data-stu-id="efbe8-118">Shows a native image picker, and returns the selected image path</span></span> | | <span data-ttu-id="efbe8-119">*Emplacement de l'image sélectionnée*</span><span class="sxs-lookup"><span data-stu-id="efbe8-119">*Selected image location*</span></span> |
| <span data-ttu-id="efbe8-120">**showAttachmentPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-120">**showAttachmentPickerAsync**</span></span> | <span data-ttu-id="efbe8-121">Affiche un sélecteur de pièces jointes dans la couche native</span><span class="sxs-lookup"><span data-stu-id="efbe8-121">Displays an attachment picker in the native layer</span></span> | <ul><li><span data-ttu-id="efbe8-122">*supportedTypes* -tableau de types de pièces jointes pris en charge pour le sélecteur</span><span class="sxs-lookup"><span data-stu-id="efbe8-122">*supportedTypes* - array of supported attachment types for the picker</span></span></li><li><span data-ttu-id="efbe8-123">autres propriétés permettant de configurer le sélecteur</span><span class="sxs-lookup"><span data-stu-id="efbe8-123">additional props to configure the picker</span></span></li></ul> | |
| <span data-ttu-id="efbe8-124">**downloadAttachmentAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-124">**downloadAttachmentAsync**</span></span> | <span data-ttu-id="efbe8-125">Télécharger la pièce jointe spécifiée</span><span class="sxs-lookup"><span data-stu-id="efbe8-125">Download the attachment specified</span></span> | <ul><li><span data-ttu-id="efbe8-126">*pièce jointe avec un chemin d'accès de serveur valide à télécharger*</span><span class="sxs-lookup"><span data-stu-id="efbe8-126">*attachment with a valid server path to download*</span></span></li><li><span data-ttu-id="efbe8-127">rappel à la fin du téléchargement</span><span class="sxs-lookup"><span data-stu-id="efbe8-127">callback on download completion</span></span></li></ul> | |
| <span data-ttu-id="efbe8-128">**cancelAttachmentDownloadAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-128">**cancelAttachmentDownloadAsync**</span></span> | <span data-ttu-id="efbe8-129">Annuler une opération de téléchargement en file d'attente pour une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="efbe8-129">Cancel a download operation queued for an attachment</span></span> | <span data-ttu-id="efbe8-130">pièce jointe</span><span class="sxs-lookup"><span data-stu-id="efbe8-130">attachment</span></span> | |
| <span data-ttu-id="efbe8-131">**showPlacePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-131">**showPlacePickerAsync**</span></span> | <span data-ttu-id="efbe8-132">Affiche un sélecteur d'emplacement natif et renvoie le lieu sélectionné (LT, LG, n)</span><span class="sxs-lookup"><span data-stu-id="efbe8-132">Shows a native place picker, and returns the selected place (lt, lg, n)</span></span> | <span data-ttu-id="efbe8-133">Emplacement sélectionné</span><span class="sxs-lookup"><span data-stu-id="efbe8-133">Selected location</span></span> | <span data-ttu-id="efbe8-134">Latitude/Longitude</span><span class="sxs-lookup"><span data-stu-id="efbe8-134">Latitude/longitude</span></span> |
| <span data-ttu-id="efbe8-135">**showLocationOnMap**</span><span class="sxs-lookup"><span data-stu-id="efbe8-135">**showLocationOnMap**</span></span> | <span data-ttu-id="efbe8-136">Ouvre les cartes natives avec l'emplacement donné</span><span class="sxs-lookup"><span data-stu-id="efbe8-136">Opens up native maps with given location</span></span> | <span data-ttu-id="efbe8-137">Type [KASLocation](KASLocation.md)</span><span class="sxs-lookup"><span data-stu-id="efbe8-137">[KASLocation](KASLocation.md) type</span></span> | |
| <span data-ttu-id="efbe8-138">**showDurationPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-138">**showDurationPickerAsync**</span></span> | <span data-ttu-id="efbe8-139">Affiche un sélecteur de durée native avec jour/heure/minute</span><span class="sxs-lookup"><span data-stu-id="efbe8-139">Shows a native duration picker with day/hour/minute</span></span> | <span data-ttu-id="efbe8-140">Durée par défaut à afficher sur le sélecteur</span><span class="sxs-lookup"><span data-stu-id="efbe8-140">Default duration to be shown on picker</span></span> | |
| <span data-ttu-id="efbe8-141">**isTalkBackEnabledAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-141">**isTalkBackEnabledAsync**</span></span> | <span data-ttu-id="efbe8-142">Obtient une valeur indiquant si Talkback est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="efbe8-142">Gets whether talkback is enabled or not</span></span> | | <span data-ttu-id="efbe8-143">Booléen</span><span class="sxs-lookup"><span data-stu-id="efbe8-143">Boolean</span></span> |
| <span data-ttu-id="efbe8-144">**generateUUIDAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-144">**generateUUIDAsync**</span></span> | <span data-ttu-id="efbe8-145">Obtient le nouvel UUID</span><span class="sxs-lookup"><span data-stu-id="efbe8-145">Gets the new UUID</span></span> | | <span data-ttu-id="efbe8-146">UUID nouvellement généré</span><span class="sxs-lookup"><span data-stu-id="efbe8-146">Newly generated uuid</span></span> |
| <span data-ttu-id="efbe8-147">**getCurrentDeviceLocationAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-147">**getCurrentDeviceLocationAsync**</span></span> | <span data-ttu-id="efbe8-148">Obtient l'emplacement actuel de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="efbe8-148">Gets the current device location</span></span> | | |
| <span data-ttu-id="efbe8-149">**getAppLocaleAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-149">**getAppLocaleAsync**</span></span> | <span data-ttu-id="efbe8-150">Obtient la langue locale de l'application en cours dans laquelle l'application est rendue, utile pour la localisation des chaînes de l'action.</span><span class="sxs-lookup"><span data-stu-id="efbe8-150">Gets the current app locale -language in which the app is rendered, useful for localizing Action's strings</span></span> | | <span data-ttu-id="efbe8-151">Locale</span><span class="sxs-lookup"><span data-stu-id="efbe8-151">Locale</span></span> |
| <span data-ttu-id="efbe8-152">**getConversationParticipantsCountAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-152">**getConversationParticipantsCountAsync**</span></span> | <span data-ttu-id="efbe8-153">Obtient tous les ID de participant de la conversation actuelle.</span><span class="sxs-lookup"><span data-stu-id="efbe8-153">Gets all the participant-ids of the current conversation</span></span> | | <span data-ttu-id="efbe8-154">Nombre de participants</span><span class="sxs-lookup"><span data-stu-id="efbe8-154">Count of participants</span></span> |
| <span data-ttu-id="efbe8-155">**getConversationNameAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-155">**getConversationNameAsync**</span></span> | <span data-ttu-id="efbe8-156">Obtient le nom de la conversation actuelle.</span><span class="sxs-lookup"><span data-stu-id="efbe8-156">Gets the current conversation name</span></span> | | <span data-ttu-id="efbe8-157">Nom de la conversation</span><span class="sxs-lookup"><span data-stu-id="efbe8-157">Name of the conversation</span></span> |
| <span data-ttu-id="efbe8-158">**dismissCurrentScreen**</span><span class="sxs-lookup"><span data-stu-id="efbe8-158">**dismissCurrentScreen**</span></span> | <span data-ttu-id="efbe8-159">Faire disparaître l'écran actuel (création, réponse ou résumé)</span><span class="sxs-lookup"><span data-stu-id="efbe8-159">Dismiss the current screen (Creation, Response, or Summary)</span></span> | | |
| <span data-ttu-id="efbe8-160">**showProgressBar**</span><span class="sxs-lookup"><span data-stu-id="efbe8-160">**showProgressBar**</span></span> | <span data-ttu-id="efbe8-161">Affiche une barre de progression Sreen complète native avec le texte donné</span><span class="sxs-lookup"><span data-stu-id="efbe8-161">Shows a native full sreen progress bar with the given text</span></span> | <span data-ttu-id="efbe8-162">Texte à afficher</span><span class="sxs-lookup"><span data-stu-id="efbe8-162">Text to display</span></span> | |
| <span data-ttu-id="efbe8-163">**hideProgressBar**</span><span class="sxs-lookup"><span data-stu-id="efbe8-163">**hideProgressBar**</span></span> | <span data-ttu-id="efbe8-164">Masque la barre de progression actuelle, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="efbe8-164">Hides the current progress bar, if any</span></span> | | |
| <span data-ttu-id="efbe8-165">**getCurrentUserIdAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-165">**getCurrentUserIdAsync**</span></span> | <span data-ttu-id="efbe8-166">Obtient l'ID d'utilisateur actuel qui a ouvert l'action.</span><span class="sxs-lookup"><span data-stu-id="efbe8-166">Gets the current user id who has opened the Action</span></span> | | <span data-ttu-id="efbe8-167">ID utilisateur</span><span class="sxs-lookup"><span data-stu-id="efbe8-167">User ID</span></span> |
| <span data-ttu-id="efbe8-168">**showImageImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="efbe8-168">**showImageImmersiveView**</span></span> | <span data-ttu-id="efbe8-169">Affiche l'image en mode immersif</span><span class="sxs-lookup"><span data-stu-id="efbe8-169">Shows Image in Immersive view</span></span> | <span data-ttu-id="efbe8-170">Tableau de l'URL des images</span><span class="sxs-lookup"><span data-stu-id="efbe8-170">Array of images url</span></span> | |
| <span data-ttu-id="efbe8-171">**openAttachmentImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="efbe8-171">**openAttachmentImmersiveView**</span></span> | <span data-ttu-id="efbe8-172">Ouvrir la pièce jointe en mode immersif</span><span class="sxs-lookup"><span data-stu-id="efbe8-172">Open attachment in Immersive view</span></span> | <span data-ttu-id="efbe8-173">Objet Attachment</span><span class="sxs-lookup"><span data-stu-id="efbe8-173">Attachment object</span></span> | |
| <span data-ttu-id="efbe8-174">**hasStorageAccessForAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="efbe8-174">**hasStorageAccessForAttachmentType**</span></span> | <span data-ttu-id="efbe8-175">vérifie si l'application dispose d'un accès en lecture/écriture au stockage</span><span class="sxs-lookup"><span data-stu-id="efbe8-175">checks whether app has read/write access to the storage</span></span> | <span data-ttu-id="efbe8-176">Type de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="efbe8-176">Attachment type</span></span> | |
| <span data-ttu-id="efbe8-177">**generateBase64ThumbnailAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-177">**generateBase64ThumbnailAsync**</span></span> | <span data-ttu-id="efbe8-178">Génère une miniature Base64 pour une image</span><span class="sxs-lookup"><span data-stu-id="efbe8-178">Generates Base64 thumbnail for an image</span></span> | <span data-ttu-id="efbe8-179">localPath pour le imageAttachment dont la miniature doit être générée</span><span class="sxs-lookup"><span data-stu-id="efbe8-179">localPath for the imageAttachment whose thumbnail needs to be generated</span></span> | |
| <span data-ttu-id="efbe8-180">**getFontSizeMultiplierAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-180">**getFontSizeMultiplierAsync**</span></span> | <span data-ttu-id="efbe8-181">Obtient le multiplicateur de taille de police pour le texte de grande taille-actuel uniquement requis par iOS</span><span class="sxs-lookup"><span data-stu-id="efbe8-181">Gets the font size multiplier for large text -   Current only required by iOS</span></span> | | |
| <span data-ttu-id="efbe8-182">**getLocalizedStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-182">**getLocalizedStringsAsync**</span></span> | <span data-ttu-id="efbe8-183">Obtient le dictionnaire des chaînes localisées en fonction des paramètres régionaux de l'application actuelle</span><span class="sxs-lookup"><span data-stu-id="efbe8-183">Gets the localized strings' dictionary based on current app locale</span></span> | <span data-ttu-id="efbe8-184">Les chaînes doivent être fournies dans le package avec des noms tels que: strings_en. JSON, strings_hi. JSON, etc.</span><span class="sxs-lookup"><span data-stu-id="efbe8-184">Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.</span></span>    | <span data-ttu-id="efbe8-185">Chaînes JSON</span><span class="sxs-lookup"><span data-stu-id="efbe8-185">Strings JSON</span></span> |
| <span data-ttu-id="efbe8-186">**logToReport**</span><span class="sxs-lookup"><span data-stu-id="efbe8-186">**logToReport**</span></span> | <span data-ttu-id="efbe8-187">Enregistre une erreur pour «envoyer un rapport»</span><span class="sxs-lookup"><span data-stu-id="efbe8-187">Logs an error for "Send report"</span></span> | <span data-ttu-id="efbe8-188">Type de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="efbe8-188">Attachment type</span></span> | |
| <span data-ttu-id="efbe8-189">**isCurrentUserO365SubscribedAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-189">**isCurrentUserO365SubscribedAsync**</span></span> | <span data-ttu-id="efbe8-190">Vérifie si l'utilisateur actuel est un abonné O365</span><span class="sxs-lookup"><span data-stu-id="efbe8-190">Checks if the current user an O365 subscriber</span></span> | | <span data-ttu-id="efbe8-191">Booléen</span><span class="sxs-lookup"><span data-stu-id="efbe8-191">Boolean</span></span> |
| <span data-ttu-id="efbe8-192">**registerHardwareBackPressCallback**</span><span class="sxs-lookup"><span data-stu-id="efbe8-192">**registerHardwareBackPressCallback**</span></span> | <span data-ttu-id="efbe8-193">Enregistre un rappel à exécuter sur une pression de bouton de retour matériel (pour Android)</span><span class="sxs-lookup"><span data-stu-id="efbe8-193">Registers a callback to be executed on hardware back button press (for Android)</span></span> | | |
| <span data-ttu-id="efbe8-194">**initLocalizationStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="efbe8-194">**initLocalizationStringsAsync**</span></span> | <span data-ttu-id="efbe8-195">Initialise le mappage des chaînes de localisation.</span><span class="sxs-lookup"><span data-stu-id="efbe8-195">Initializes the localization strings' map</span></span> | <span data-ttu-id="efbe8-196">Dictionary-le mappage des chaînes</span><span class="sxs-lookup"><span data-stu-id="efbe8-196">Dictionary  - the strings' map</span></span> | <span data-ttu-id="efbe8-197">Success (Boolean) indique la réussite ou l'échec de l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="efbe8-197">Success(Boolean) denotes the success/failure of the initialization</span></span> |
| <span data-ttu-id="efbe8-198">**getString**</span><span class="sxs-lookup"><span data-stu-id="efbe8-198">**getString**</span></span> |   <span data-ttu-id="efbe8-199">Renvoie une chaîne à partir du fichier de chaînes localisées</span><span class="sxs-lookup"><span data-stu-id="efbe8-199">Returns a string from the localized strings' file</span></span> |<span data-ttu-id="efbe8-200">stringId</span><span class="sxs-lookup"><span data-stu-id="efbe8-200">stringId</span></span> ||


##  <a name="get-user-info"></a><span data-ttu-id="efbe8-201">Obtenir des informations sur l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="efbe8-201">Get user info</span></span>

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

##  <a name="show-contact-picker"></a><span data-ttu-id="efbe8-202">Afficher le sélecteur de contacts</span><span class="sxs-lookup"><span data-stu-id="efbe8-202">Show contact picker</span></span>

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a><span data-ttu-id="efbe8-203">Afficher le sélecteur d'images</span><span class="sxs-lookup"><span data-stu-id="efbe8-203">Show image picker</span></span>

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a><span data-ttu-id="efbe8-204">Obtenir l'emplacement actuel de l'appareil</span><span class="sxs-lookup"><span data-stu-id="efbe8-204">Get current device location</span></span>

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a><span data-ttu-id="efbe8-205">Sélecteur de lieux</span><span class="sxs-lookup"><span data-stu-id="efbe8-205">Place picker</span></span>

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a><span data-ttu-id="efbe8-206">Afficher l'emplacement sur les cartes</span><span class="sxs-lookup"><span data-stu-id="efbe8-206">Show location on maps</span></span>

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a><span data-ttu-id="efbe8-207">Afficher un message d'erreur (Alert ou Toast)</span><span class="sxs-lookup"><span data-stu-id="efbe8-207">Show error message (alert or toast)</span></span>

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a><span data-ttu-id="efbe8-208">Obtenir la langue actuelle utilisée par l'application</span><span class="sxs-lookup"><span data-stu-id="efbe8-208">Get current language used by the app</span></span>

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a><span data-ttu-id="efbe8-209">Obtenir le nom de la conversation actuelle</span><span class="sxs-lookup"><span data-stu-id="efbe8-209">Get the name of the current conversation</span></span>

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a><span data-ttu-id="efbe8-210">Faire disparaître l'écran de l'action actuellement ouverte</span><span class="sxs-lookup"><span data-stu-id="efbe8-210">Dismiss the currently opened Action's screen</span></span>

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a><span data-ttu-id="efbe8-211">Afficher la barre de progression Native</span><span class="sxs-lookup"><span data-stu-id="efbe8-211">Show native progress bar</span></span>

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a><span data-ttu-id="efbe8-212">Masquer la barre de progression Native</span><span class="sxs-lookup"><span data-stu-id="efbe8-212">Hide native progress bar</span></span>

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a><span data-ttu-id="efbe8-213">Obtenir l'ID d'utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="efbe8-213">Get current user id</span></span>

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a><span data-ttu-id="efbe8-214">Appuyez sur le bouton inscrire pour obtenir une pression sur le matériel (Android)</span><span class="sxs-lookup"><span data-stu-id="efbe8-214">Register for hardware back button press (Android)</span></span>

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a><span data-ttu-id="efbe8-215">Localisation de l'action</span><span class="sxs-lookup"><span data-stu-id="efbe8-215">Localization for Action</span></span>

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

##  <a name="printf-for-action"></a><span data-ttu-id="efbe8-216">printf () pour l'action</span><span class="sxs-lookup"><span data-stu-id="efbe8-216">printf() for Action</span></span>

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
