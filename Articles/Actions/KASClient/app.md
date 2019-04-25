#   <a name="app-apis"></a>API d'application:

| **API** | Description | Paramètre de requête | Sortie de la réponse |
| :---: | :---: | :---: | :--- |
| **getUsersDetailsAsync** | Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leurs ID. | Tableau des ID utilisateur | *JSON des informations utilisateur* |
| **showContactPickerAsync** | Affiche un sélecteur de contacts natif et renvoie un tableau de tous les détails des utilisateurs sélectionnés | <ul><li>*titre du sélecteur de contacts*</li><li>*selectedMutableUser* -tableau d'ID utilisateur sélectionnés</li><li>*selectedImmutableUser* : tableau des ID utilisateur sélectionnés fixes</li><li>*isSingleSelection* -sélection unique dans le sélecteur de contacts</li></ul> | Tableau de tous les détails des utilisateurs sélectionnés (*tableau de JSON*) |
| **showImagePickerAsync** | Affiche un sélecteur d'image native et renvoie le chemin d'accès à l'image sélectionnée | | *Emplacement de l'image sélectionnée* |
| **showAttachmentPickerAsync** | Affiche un sélecteur de pièces jointes dans la couche native | <ul><li>*supportedTypes* -tableau de types de pièces jointes pris en charge pour le sélecteur</li><li>autres propriétés permettant de configurer le sélecteur</li></ul> | |
| **downloadAttachmentAsync** | Télécharger la pièce jointe spécifiée | <ul><li>*pièce jointe avec un chemin d'accès de serveur valide à télécharger*</li><li>rappel à la fin du téléchargement</li></ul> | |
| **cancelAttachmentDownloadAsync** | Annuler une opération de téléchargement en file d'attente pour une pièce jointe | pièce jointe | |
| **showPlacePickerAsync** | Affiche un sélecteur d'emplacement natif et renvoie le lieu sélectionné (LT, LG, n) | Emplacement sélectionné | Latitude/Longitude |
| **showLocationOnMap** | Ouvre les cartes natives avec l'emplacement donné | Type [KASLocation](KASLocation.md) | |
| **showDurationPickerAsync** | Affiche un sélecteur de durée native avec jour/heure/minute | Durée par défaut à afficher sur le sélecteur | |
| **isTalkBackEnabledAsync** | Obtient une valeur indiquant si Talkback est activé ou non. | | Booléen |
| **generateUUIDAsync** | Obtient le nouvel UUID | | UUID nouvellement généré |
| **getCurrentDeviceLocationAsync** | Obtient l'emplacement actuel de l'appareil. | | |
| **getAppLocaleAsync** | Obtient la langue locale de l'application en cours dans laquelle l'application est rendue, utile pour la localisation des chaînes de l'action. | | Locale |
| **getConversationParticipantsCountAsync** | Obtient tous les ID de participant de la conversation actuelle. | | Nombre de participants |
| **getConversationNameAsync** | Obtient le nom de la conversation actuelle. | | Nom de la conversation |
| **dismissCurrentScreen** | Faire disparaître l'écran actuel (création, réponse ou résumé) | | |
| **showProgressBar** | Affiche une barre de progression Sreen complète native avec le texte donné | Texte à afficher | |
| **hideProgressBar** | Masque la barre de progression actuelle, le cas échéant. | | |
| **getCurrentUserIdAsync** | Obtient l'ID d'utilisateur actuel qui a ouvert l'action. | | ID utilisateur |
| **showImageImmersiveView** | Affiche l'image en mode immersif | Tableau de l'URL des images | |
| **openAttachmentImmersiveView** | Ouvrir la pièce jointe en mode immersif | Objet Attachment | |
| **hasStorageAccessForAttachmentType** | vérifie si l'application dispose d'un accès en lecture/écriture au stockage | Type de pièce jointe | |
| **generateBase64ThumbnailAsync** | Génère une miniature Base64 pour une image | localPath pour le imageAttachment dont la miniature doit être générée | |
| **getFontSizeMultiplierAsync** | Obtient le multiplicateur de taille de police pour le texte de grande taille-actuel uniquement requis par iOS | | |
| **getLocalizedStringsAsync** | Obtient le dictionnaire des chaînes localisées en fonction des paramètres régionaux de l'application actuelle | Les chaînes doivent être fournies dans le package avec des noms tels que: strings_en. JSON, strings_hi. JSON, etc.    | Chaînes JSON |
| **logToReport** | Enregistre une erreur pour «envoyer un rapport» | Type de pièce jointe | |
| **isCurrentUserO365SubscribedAsync** | Vérifie si l'utilisateur actuel est un abonné O365 | | Booléen |
| **registerHardwareBackPressCallback** | Enregistre un rappel à exécuter sur une pression de bouton de retour matériel (pour Android) | | |
| **initLocalizationStringsAsync** | Initialise le mappage des chaînes de localisation. | Dictionary-le mappage des chaînes | Success (Boolean) indique la réussite ou l'échec de l'initialisation. |
| **getString** |   Renvoie une chaîne à partir du fichier de chaînes localisées |stringId ||


##  <a name="get-user-info"></a>Obtenir des informations sur l'utilisateur

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

##  <a name="show-image-picker"></a>Afficher le sélecteur d'images

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a>Obtenir l'emplacement actuel de l'appareil

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a>Sélecteur de lieux

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a>Afficher l'emplacement sur les cartes

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a>Afficher un message d'erreur (Alert ou Toast)

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a>Obtenir la langue actuelle utilisée par l'application

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a>Obtenir le nom de la conversation actuelle

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a>Faire disparaître l'écran de l'action actuellement ouverte

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a>Afficher la barre de progression Native

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a>Masquer la barre de progression Native

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a>Obtenir l'ID d'utilisateur actuel

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a>Appuyez sur le bouton inscrire pour obtenir une pression sur le matériel (Android)

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a>Localisation de l'action

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

##  <a name="printf-for-action"></a>printf () pour l'action

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
