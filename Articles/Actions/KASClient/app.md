#   <a name="app-apis"></a>API d’application :

| **API** | Description | Paramètre de demande | Sortie de réponse |
| :---: | :---: | :---: | :--- |
| **getUsersDetailsAsync** | Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leur ID | userIds tableau des ID d’utilisateur | *JSON d’infos utilisateur* |
| **showContactPickerAsync** | Affiche un sélecteur de contact natif et renvoie un tableau de détails de tous les utilisateurs | <ul><li>*titre du sélecteur de Contact*</li><li>*selectedMutableUser* - tableau des ID utilisateur sélectionné</li><li>*selectedImmutableUser* - tableau des ID utilisateur sélectionné fixe</li><li>*isSingleSelection* - seule sélection dans le sélecteur de contacts</li></ul> | Tableau des détails de tous les utilisateurs (*Tableau de JSON*) |
| **showImagePickerAsync** | Affiche un sélecteur d’images natif et renvoie le chemin d’accès de l’image sélectionnée | | *Emplacement de l’image sélectionnée* |
| **showAttachmentPickerAsync** | Affiche un sélecteur de pièce jointe dans la couche native | <ul><li>*supportedTypes* - tableau des types de pièce jointe pris en charge pour le sélecteur</li><li>propriétés supplémentaires pour configurer le sélecteur</li></ul> | |
| **downloadAttachmentAsync** | Télécharger la pièce jointe spécifiée | <ul><li>*avec un chemin d’accès de serveur valide pour télécharger des pièces jointes*</li><li>rappel à la fin du téléchargement</li></ul> | |
| **cancelAttachmentDownloadAsync** | Annuler une opération de téléchargement en file d’attente d’une pièce jointe | pièce jointe | |
| **showPlacePickerAsync** | Affiche un sélecteur de place natif et renvoie le lieu sélectionné (lt, lg, n) | Emplacement sélectionné | Latitude/longitude |
| **showLocationOnMap** | Emplacement de donné s’ouvre des cartes natives avec | Type de [KASLocation](KASLocation.md) | |
| **showDurationPickerAsync** | Affiche un sélecteur de durée native avec jour/heure/minute | Durée par défaut à afficher dans le sélecteur | |
| **isTalkBackEnabledAsync** | Indique si talkback est activé ou non | | Bool�en |
| **generateUUIDAsync** | Obtient le nouvel UUID | | Uuid nouvellement créé |
| **getCurrentDeviceLocationAsync** | Obtient l’emplacement actuel du périphérique | | |
| **getAppLocaleAsync** | Obtient les paramètres régionaux application-langue dans laquelle l’application s’affiche, utile pour localiser les chaînes de l’Action | | Locale |
| **getConversationParticipantsCountAsync** | Obtient tous les participants-ID de la conversation en cours | | Nombre de participants |
| **getConversationNameAsync** | Obtient le nom actuel de la conversation | | Nom de la conversation |
| **dismissCurrentScreen** | Faire disparaître l’écran actuel (création, réponse ou résumé) | | |
| **ShowProgressBar indique** | Affiche une barre de progression de l ' écran complète native avec le texte donné | Texte à afficher | |
| **hideProgressBar** | Masque la barre de progression en cours, le cas échéant | | |
| **getCurrentUserIdAsync** | Obtient le nom d’utilisateur qui a ouvert l’Action en cours | | User ID |
| **showImageImmersiveView** | Affiche l’Image en mode immersif | Tableau d’url d’images | |
| **openAttachmentImmersiveView** | Ouvrir la pièce jointe en mode immersif | Objet Attachment | |
| **hasStorageAccessForAttachmentType** | vérifie si application dispose d’un accès en lecture/écriture pour le stockage | Type de pièce jointe | |
| **generateBase64ThumbnailAsync** | Génère une image miniature en Base64 | localPath pour l’imageAttachment dont miniature doit être généré | |
| **getFontSizeMultiplierAsync** | Obtient le multiplicateur de taille de police de texte de grande taille - courant uniquement nécessaire pour iOS | | |
| **getLocalizedStringsAsync** | Obtient le dictionnaire des chaînes localisées en fonction de paramètres régionaux application en cours | Chaînes doivent être fournis dans le package, par exemple : strings_en.json, strings_hi.json, etc..    | Chaînes JSON |
| **logToReport** | Enregistre une erreur pour « Envoyer le rapport » | Type de pièce jointe | |
| **isCurrentUserO365SubscribedAsync** | Vérifie si l’abonné utilisateur un O365 actuel | | Bool�en |
| **registerHardwareBackPressCallback** | Enregistre un rappel à exécuter sur matériel, appuyez sur le bouton précédent (pour Android) | | |
| **initLocalizationStringsAsync** | Initialise le mappage des chaînes de la localisation | Dictionnaire - feuille de route des chaînes | Success(Boolean) indique la réussite ou l’échec de l’initialisation |
| **getString** |   Retourne une chaîne de fichier des chaînes localisées |stringid d' ||


##  <a name="get-user-info"></a>Obtenir les informations utilisateur

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

##  <a name="show-contact-picker"></a>Afficher le sélecteur de contacts

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a>Afficher le sélecteur d’images

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a>Obtenir l’emplacement actuel de l’unité

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a>Sélecteur d’emplacement

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a>Afficher l’emplacement sur les cartes

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a>Afficher le message d’erreur (alerte ou toast)

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a>Obtenir la langue en cours utilisé par l’application

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a>Obtenir le nom de la conversation en cours

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a>Ignorer l’écran de l’Action actuellement ouvert.

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a>Afficher la barre de progression native

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a>Masquer la barre de progression native

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a>Obtenir l’id d’utilisateur actuel

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a>S’inscrire pour appuyer sur le bouton précédent de matériel (Android)

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a>Localisation d’Action

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

##  <a name="printf-for-action"></a>printf() d’Action

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
