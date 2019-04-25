[](../README.md) > [](../modules/kasclient.md) > [Application](../modules/kasclient.app.md) KASClient

# <a name="module-app"></a>Module: App

## <a name="index"></a>Index

### <a name="functions"></a>Fonctions

* [cancelAttachmentDownloadAsync](kasclient.app.md#cancelattachmentdownloadasync)
* [dismissCurrentScreen](kasclient.app.md#dismisscurrentscreen)
* [downloadAttachmentAsync](kasclient.app.md#downloadattachmentasync)
* [generateBase64ThumbnailAsync](kasclient.app.md#generatebase64thumbnailasync)
* [generateUUIDAsync](kasclient.app.md#generateuuidasync)
* [getAppLocaleAsync](kasclient.app.md#getapplocaleasync)
* [getCalendarNameAsync](kasclient.app.md#getcalendarnameasync)
* [getConversationDetailsAsync](kasclient.app.md#getconversationdetailsasync)
* [getCurrentDeviceLocationAsync](kasclient.app.md#getcurrentdevicelocationasync)
* [getCurrentLocale](kasclient.app.md#getcurrentlocale)
* [getDeviceIdAsync](kasclient.app.md#getdeviceidasync)
* [getDeviceLocationAsync](kasclient.app.md#getdevicelocationasync)
* [getFontSizeMultiplierAsync](kasclient.app.md#getfontsizemultiplierasync)
* [getForwardContextAsync](kasclient.app.md#getforwardcontextasync)
* [getIsAppTimeFormat24HoursAsync](kasclient.app.md#getisapptimeformat24hoursasync)
* [getLocalizedStringsAsync](kasclient.app.md#getlocalizedstringsasync)
* [getLocationAddressAsync](kasclient.app.md#getlocationaddressasync)
* [getMapImageAsBase64Async](kasclient.app.md#getmapimageasbase64async)
* [getO365UserDetailsAsync](kasclient.app.md#geto365userdetailsasync)
* [getPackageCustomSettingsAsync](kasclient.app.md#getpackagecustomsettingsasync)
* [getUsersDetailsAsync](kasclient.app.md#getusersdetailsasync)
* [hideProgressBar](kasclient.app.md#hideprogressbar)
* [isAttachmentDownloadingAsync](kasclient.app.md#isattachmentdownloadingasync)
* [isAuthenticationTyepSupportedAsync](kasclient.app.md#isauthenticationtyepsupportedasync)
* [isTalkBackEnabledAsync](kasclient.app.md#istalkbackenabledasync)
* [logToReport](kasclient.app.md#logtoreport)
* [openAttachmentImmersiveView](kasclient.app.md#openattachmentimmersiveview)
* [openImmersiveViewForAttachmentList](kasclient.app.md#openimmersiveviewforattachmentlist)
* [performAuthenticationAsync](kasclient.app.md#performauthenticationasync)
* [performHTTPRequest](kasclient.app.md#performhttprequest)
* [printf](kasclient.app.md#printf)
* [readTalkBackMessage](kasclient.app.md#readtalkbackmessage)
* [registerHardwareBackPressCallback](kasclient.app.md#registerhardwarebackpresscallback)
* [setNativeToolbarProperties](kasclient.app.md#setnativetoolbarproperties)
* [setUserStrings](kasclient.app.md#setuserstrings)
* [showAttachmentPickerAsync](kasclient.app.md#showattachmentpickerasync)
* [showBarcodeScannerAsync](kasclient.app.md#showbarcodescannerasync)
* [showContactPickerAsync](kasclient.app.md#showcontactpickerasync)
* [showDurationPickerAsync](kasclient.app.md#showdurationpickerasync)
* [showImageImmersiveView](kasclient.app.md#showimageimmersiveview)
* [showImagePickerAsync](kasclient.app.md#showimagepickerasync)
* [showLocationOnMap](kasclient.app.md#showlocationonmap)
* [showNativeErrorMessage](kasclient.app.md#shownativeerrormessage)
* [showPlacePickerAsync](kasclient.app.md#showplacepickerasync)
* [showProgressBar](kasclient.app.md#showprogressbar)
* [showQRcodeScannerAsync](kasclient.app.md#showqrcodescannerasync)
* [showUserProfileAsync](kasclient.app.md#showuserprofileasync)
* [startChatAsync](kasclient.app.md#startchatasync)

---

## <a name="functions"></a>Fonctions

<a id="cancelattachmentdownloadasync"></a>

###  <a name="cancelattachmentdownloadasync"></a>cancelAttachmentDownloadAsync

▸ **cancelAttachmentDownloadAsync**(attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, callback *`function`*:):`void`

Annuler une opération de téléchargement en file d'attente pour une pièce jointe

#### <a name="sample-usage"></a>Exemple d'utilisation

```
 var attachmentsList = JSON.parse(form.properties[0].value);
 for (var i = 0; i < attachmentsList.length; i++)
 {
      var attachmentItem = attachmentsList[i];
      var attachment = KASClient.KASAttachment.fromJSON(attachmentItem);
      KASClient.App.cancelAttachmentDownloadAsync(attachment);
 }
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| pièce jointe | [KASAttachment](../classes/kasclient.kasattachment.md) |  \- |
| callback | `function` |  avec une erreur param-chaîne d'erreur en cas d'erreur; NULL dans le cas contraire |

**Renvoie:**`void`

___

<a id="dismisscurrentscreen"></a>

###  <a name="dismisscurrentscreen"></a>dismissCurrentScreen

▸ **dismissCurrentScreen**():`void`

Faire disparaître l'écran de l'action actuellement ouverte (création, réponse ou résumé)

**Renvoie:**`void`

___

<a id="downloadattachmentasync"></a>

###  <a name="downloadattachmentasync"></a>downloadAttachmentAsync

▸ **downloadAttachmentAsync**(attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, callback *`function`*:):`void`

Télécharger la pièce jointe spécifiée

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var imageAttachment =  new KASClient.KASAttachment();
imageAttachment.type = KASClient.KASAttachmentType.Image;
imageAttachment.serverPath = "<server path>";
imageAttachment.fileName = "<file name>";
KASClient.App.downloadAttachmentAsync(imageAttachment, function(downloadedAttachment, error){
     if (!error) {
        console.log(downloadedAttachment); //KASAttachment
     }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| pièce jointe | [KASAttachment](../classes/kasclient.kasattachment.md) |  pièce jointe avec un chemin d'accès de serveur valide à télécharger |
| callback | `function` |  rappel à la fin du téléchargement avec les paramètres suivants<br><br>\*@param {KASAttachment} downloadedAttachment la pièce jointe qui a été téléchargée<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="generatebase64thumbnailasync"></a>

###  <a name="generatebase64thumbnailasync"></a>generateBase64ThumbnailAsync

▸ **generateBase64ThumbnailAsync**(LocalPath: *`string`*, callback: *`function`*):`void`

Génère une miniature Base64 pour une image dont la fonction localPath est donnée

#### <a name="sample-usage"></a>Exemple d'utilisation

```
KASClient.App.generateBase64ThumbnailAsync(localPath, function (thumbnail, error) {
    if (error == null && thumbnail != null) {
       //use the thumbnail data and update required dom
     }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| localPath | `string` |  localPath pour le imageAttachment dont la miniature doit être générée |
| callback | `function` |  avec les paramètres suivants:<br><br>\*miniature de @param {String} valeur base64<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="generateuuidasync"></a>

###  <a name="generateuuidasync"></a>generateUUIDAsync

▸ **generateUUIDAsync**(callback: *`function`*):`void`

Obtient le nouvel UUID

#### <a name="sample-usage"></a>Exemple d'utilisation

```
 KASClient.App.generateUUIDAsync(function (uuid, error) {
    console.log("generatedUUIDAsync", uuid);
    ...
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} UUID nouvellement généré<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getapplocaleasync"></a>

###  <a name="getapplocaleasync"></a>getAppLocaleAsync

▸ **getAppLocaleAsync**(callback: *`function`*):`void`

Obtient les paramètres régionaux de l'application en cours, la langue dans laquelle l'application est rendue, utile pour la localisation des chaînes MiniApp

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} locale peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getcalendarnameasync"></a>

###  <a name="getcalendarnameasync"></a>getCalendarNameAsync

▸ **getCalendarNameAsync**(callback: *`function`*):`void`

Obtient le paramètre de calendrier système actuel. Ceci est principalement destiné à iOS pour identifier le nom du calendrier défini dans les paramètres du téléphone (par exemple, grégorien, japonais ou Buddhists).

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} calendarName peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getconversationdetailsasync"></a>

###  <a name="getconversationdetailsasync"></a>getConversationDetailsAsync

▸ **getConversationDetailsAsync**(callback: *`function`*):`void`

Obtient les propriétés associées à une conversation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param les propriétés de conversation de résultats {KASConversationDetails}<br><br>\*@param valeur de chaîne JSON de l'erreur {String} pour l'objet KASError contenant un code d'erreur et/ou une description. |

**Renvoie:**`void`

___

<a id="getcurrentdevicelocationasync"></a>

###  <a name="getcurrentdevicelocationasync"></a>getCurrentDeviceLocationAsync

▸ **getCurrentDeviceLocationAsync**(callback: *`function`*):`void`

Obtient l'emplacement actuel de l'appareil.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
 KASClient.App.getCurrentDeviceLocationAsync(function (location, error){
     if(error != null) {
          return;
     }
     //use location(KASLocation) as the device location
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param l'emplacement {String} peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getcurrentlocale"></a>

###  <a name="getcurrentlocale"></a>getCurrentLocale

▸ **getCurrentLocale**():`string`

**Renvoie:**`string`

___

<a id="getdeviceidasync"></a>

###  <a name="getdeviceidasync"></a>getDeviceIdAsync

▸ **getDeviceIdAsync**(callback: *`function`*):`void`

Obtient deviceId

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} deviceId provenant du service d'enchaînement<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getdevicelocationasync"></a>

###  <a name="getdevicelocationasync"></a>getDeviceLocationAsync

▸ **getDeviceLocationAsync**(callback: *`function`*):`void`

Obtient l'emplacement du périphérique stocké précédemment.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param l'emplacement {String} peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getfontsizemultiplierasync"></a>

###  <a name="getfontsizemultiplierasync"></a>getFontSizeMultiplierAsync

▸ **getFontSizeMultiplierAsync**(callback: *`function`*):`void`

Obtient le multiplicateur de taille de police pour le texte long. Actuel uniquement requis par iOS.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants<br><br>\*@param de multiplicateur {String}<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getforwardcontextasync"></a>

###  <a name="getforwardcontextasync"></a>getForwardContextAsync

▸ **getForwardContextAsync**(callback: *`function`*):`void`

Obtient les détails du contexte de transfert, par exemple: la création de la carte est en mode transmis.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {JSON} renvoie les détails de contexte dans la structure JSON |

**Renvoie:**`void`

___

<a id="getisapptimeformat24hoursasync"></a>

###  <a name="getisapptimeformat24hoursasync"></a>getIsAppTimeFormat24HoursAsync

▸ **getIsAppTimeFormat24HoursAsync**(callback: *`function`*):`void`

Obtient le format d'heure de l'application actuel est 24hours ou non, le format d'heure sélectionné par l'utilisateur, utile pour la mise en forme des chaînes de temps de date correctement.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} isAppTimeFormat24Hours peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getlocalizedstringsasync"></a>

###  <a name="getlocalizedstringsasync"></a>getLocalizedStringsAsync

▸ **getLocalizedStringsAsync**(callback: *`function`*):`void`

Obtient le dictionnaire des chaînes localisées en fonction des paramètres régionaux de l'application actuelle. Les chaînes doivent être fournies dans le package avec des noms tels\_que: Strings en\_. JSON, Strings Hi. JSON, etc.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
KASClient.App.getLocalizedStringsAsync(function (strings, error) {
    if (error != null) {
        return;
    }
    //use the localized strings array
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*les chaînes de @param {JSON} peuvent être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getlocationaddressasync"></a>

###  <a name="getlocationaddressasync"></a>getLocationAddressAsync

▸ **getLocationAddressAsync**(params: *[KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md)*, callback: *`function`*):`void`

Obtenir la chaîne d'adresse pour les coordonnées spécifiées

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var params = new KASClient.KASLocationAddressParams();
params.latitude =  <latitude value>;
params.longitude =  <longitude value>;
KASClient.App.getLocationAddressAsync(params,
    function (address, error) {
        if (!error) {
           // do something with address - a JSON returned by google structure can be found at https://developers.google.com/maps/documentation/geocoding/intro#GeocodingResponses
        }
    }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| params | [KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md) |  KASLocationAddressParams |
| callback | `function` |  rappel de la récupération d'adresses avec les paramètres suivants<br><br>\*emplacement de @param {JSON} un JSON contenant une longitude latitute et d'autres informations<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getmapimageasbase64async"></a>

###  <a name="getmapimageasbase64async"></a>getMapImageAsBase64Async

▸ **getMapImageAsBase64Async**(params: *[KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md)*, callback: *`function`*):`void`

Téléchargez l'image 64 de base de Map pour les coordonnées spécifiées.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
KASClient.App.getMapImageAsBase64Async(params, function (attachmentString, error) {
        if (!error) {
            blobString = "data:image/jpeg;base64," + attachmentString;
            //use blobString as base64 data
        }
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| params | [KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md) |  KASLocationStaticMapImageParams |
| callback | `function` |  fin du téléchargement avec les paramètres suivants<br><br>\*@param {String} attachmentString base64 de la pièce jointe<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="geto365userdetailsasync"></a>

###  <a name="geto365userdetailsasync"></a>getO365UserDetailsAsync

▸ **getO365UserDetailsAsync**(callback: *`function`*):`void`

Obtient les détails de l'utilisateur O365 actuellement connecté

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {JSON} renvoie le UserDetails dans la structure JSON |

**Renvoie:**`void`

___

<a id="getpackagecustomsettingsasync"></a>

###  <a name="getpackagecustomsettingsasync"></a>getPackageCustomSettingsAsync

▸ **getPackageCustomSettingsAsync**(callback: *`function`*):`void`

Obtient tous les paramètres de personnalisation d'un package (utilisé dans le cas des packages de type 4 et de leur base).

#### <a name="sample-usage"></a>Exemple d'utilisation

```
KASClient.App.getPackageCustomSettingsAsync(function (settings, error) {
      if (error != null) {
          return;
      }
     //settings contains the settings json defined at the package level
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*les paramètres de @param {JSON} peuvent être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="getusersdetailsasync"></a>

###  <a name="getusersdetailsasync"></a>getUsersDetailsAsync

▸ **getUsersDetailsAsync**(userids: * `string`[]*, callback: *`function`*):`void`

Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leurs ID.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var userIds = ["<uid1>", "<uid2>",...];
KASClient.App.getUsersDetailsAsync(userIds, function (users, error) {
      if (error != null) {
          return;
      }
      var userInfo1 = users[<uid1>];
      var userInfo2 = users[<uid2>];
      ...
  });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userIds | `string`[] |  Tableau des ID d'utilisateur |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Dictionary<UserId: String, UserInfo: KASUser>} userIdToInfoMap (les détails des utilisateurs par rapport à leurs ID) peuvent être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="hideprogressbar"></a>

###  <a name="hideprogressbar"></a>hideProgressBar

▸ **hideProgressBar**():`void`

Masque la barre de progression actuelle, le cas échéant.

**Renvoie:**`void`

___

<a id="isattachmentdownloadingasync"></a>

###  <a name="isattachmentdownloadingasync"></a>isAttachmentDownloadingAsync

▸ **isAttachmentDownloadingAsync**(attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, callback *`function`*:):`void`

Télécharger la pièce jointe spécifiée

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var attachmentJson = {
  ty: 3,
  afn: "131490_Desert (1) (4).pdf",
  lpu: "",
  spu: '<server path>',
  asb: 846941,
  id:''
};
var attachment = KASClient.KASAttachment.fromJSON(attachmentJson);
KASClient.App.isAttachmentDownloadingAsync(attachment, function(isAttachmentDownloadingOrDownLoaded, error){
     if (!error) {
        console.log(isAttachmentDownloadingOrDownLoaded); //boolean
     }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| pièce jointe | [KASAttachment](../classes/kasclient.kasattachment.md) |  pièce jointe avec un chemin d'accès de serveur valide à télécharger |
| callback | `function` |  rappel à la fin du téléchargement avec les paramètres suivants<br><br>\*@param {Boolean} indicateur isAttachmentDownloadingOrDownLoaded représentant si la pièce jointe est en téléchargement/téléchargée<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="isauthenticationtyepsupportedasync"></a>

###  <a name="isauthenticationtyepsupportedasync"></a>isAuthenticationTyepSupportedAsync

▸ **isAuthenticationTyepSupportedAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, callback: *`function`*):`void`

Vérifie si l'authentification de type est possible ou non.

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  type d'authentification. |
| callback | `function` | - |  avec les paramètres suivants:<br><br>\*@param {Boolean} isSuccessful true si l'impression des doigts est possible<br><br>\*@param {String} code motif reasonCode pourquoi l'impression par doigt n'est pas possible |

**Renvoie:**`void`

___

<a id="istalkbackenabledasync"></a>

###  <a name="istalkbackenabledasync"></a>isTalkBackEnabledAsync

▸ **isTalkBackEnabledAsync**(callback: *`function`*):`void`

Obtient une valeur indiquant si Talkback est activé ou non.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} talkBackEnabled true si Talkback est activé |

**Renvoie:**`void`

___

<a id="logtoreport"></a>

###  <a name="logtoreport"></a>logToReport

▸ **logToReport**(Data: *`string`*):`void`

Enregistre les données pour «envoyer un rapport»

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| data | `string` |  string |

**Renvoie:**`void`

___

<a id="openattachmentimmersiveview"></a>

###  <a name="openattachmentimmersiveview"></a>openAttachmentImmersiveView

▸ **openAttachmentImmersiveView**(AttachmentObj: *[KASAttachment](../classes/kasclient.kasattachment.md)*):`void`

Ouvrir la pièce jointe en mode immersif.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| attachmentObj | [KASAttachment](../classes/kasclient.kasattachment.md) |   |

**Renvoie:**`void`

___

<a id="openimmersiveviewforattachmentlist"></a>

###  <a name="openimmersiveviewforattachmentlist"></a>openImmersiveViewForAttachmentList

▸ **openImmersiveViewForAttachmentList**(AttachmentList: * [KASAttachment](../classes/kasclient.kasattachment.md)[]*, atIndex?: *`number`*):`void`

Ouvrir la pièce jointe en mode immersif.

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| attachmentList | [KASAttachment](../classes/kasclient.kasattachment.md) [] | - |
| `Default value`atIndex | `number` | 0 |

**Renvoie:**`void`

___

<a id="performauthenticationasync"></a>

###  <a name="performauthenticationasync"></a>performAuthenticationAsync

▸ **performAuthenticationAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, callback: *`function`*):`void`

Si le type d'authentification est autorisé, cette API effectue l'authentification et renvoie l'État Success/false sinon elle renvoie une chaîne d'erreur indiquant pourquoi l'authentification n'est pas possible.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
KASClient.App.performAuthenticationAsync(KASAuthenticationType.Password, function (isSuccessful, reasonCode) {
      if (!isSuccessful) {
          console.log(resonCode);
      }
});
```

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  type d'authentification. |
| callback | `function` | - |  avec les paramètres suivants:<br><br>\*@param {Boolean} isSuccessful true si le formulaire n'a pas encore expiré<br><br>\*@param {String} code de motif de reasonCode en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="performhttprequest"></a>

###  <a name="performhttprequest"></a>performHTTPRequest

▸ **performHTTPRequest**(URL: *`string`*, parametersJSON: *`string`*, callback: *`function`*):`void`

effectue une requête HTTP et renvoie la réponse comme indiqué ci-dessous:

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var url = "<url>";
var parametersJson = JSON.stringify({ "method" : "GET" });
KASClient.App.performHTTPRequest(url, parametersJson, function (response, error) {
      if (!error) {
          //use the response
      }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| url | `string` |  URL de base à ouvrir |
| parametersJSON | `string` |  les jsonString contenant des paramètres peuvent être fournis en tant que valeur null.<br><br> S'il est fourni comme null, une demande adressée à l'URL fournie ci-dessus sera créée. Les paramètres incluent l'en-tête de demande, les paramètres de requête (vides par défaut), la méthode de demande (GET par défaut) et le corps de la demande (le corps à valider si la méthode de demande est POST. vide par défaut.) Les clés des paramètres sont les suivantes:<br><br> a.) "méthode": méthode Request. exemple: «POST». la valeur par défaut est «GET».<br><br> b.) "requestBody": corps de la demande en cas de "POST". la valeur par défaut est vide.<br><br> c.) "requestHeaders": en-têtes à envoyer avec la demande. doit être un JSON avec<br> clé en tant qu'en-tête et valeur de la requête comme valeur souhaitée. la valeur par défaut est vide.<br><br> d.) "queryParameters": paramètres de requête. seront codées dans l'URL. doit être un JSON avec<br> clé comme nom de paramètre et valeur comme valeur. la valeur par défaut est vide.<br><br> e.) «requestResourcePath»: est ajouté à l'URL de base. la valeur par défaut est vide. |
| callback | `function` |  rappel avec les paramètres suivants:<br><br>\*@param le corps de réponse de réponse de type {String} a renvoyé<br><br> Il peut s'agit de deux configurations possibles:<br><br> Si la demande était une réussite, elle renvoie jsonString avec les clés suivantes:<br><br> a.) «HttpResponseCode»: code de réponse de la demande.<br><br> b.) "HttpResponseHeader": les en-têtes HTTP de réponse<br><br> c.) "HttpResponseBody": le corps de la réponse a été renvoyé pour une demande.<br><br> S'il y a eu une erreur réseau, il retourne:<br><br> a.) «HttpErrorCode»: le code d'erreur<br><br> b.) "HttpErrorMessage": le message d'erreur par exemple. URL inCorrecte, impossible de se connecter à l'hôte, etc.<br><br>\*@param erreur d'erreur de type {String}, le cas échéant: Ceci inclut le code d'erreur standard défini dans la documentation de KASClient. |

**Renvoie:**`void`

___

<a id="printf"></a>

###  <a name="printf"></a>printf

▸ **printf**(main: *`string`*,... args: * `any`[]*):`string`

Renvoie une valeur de type String.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| grands | `string` |
| `Rest`args | `any`[] |  Tableau d'arguments. |

**Renvoie:**`string`

___

<a id="readtalkbackmessage"></a>

###  <a name="readtalkbackmessage"></a>readTalkBackMessage

▸ **readTalkBackMessage**(talkBackMessage: *`string`*):`void`

Lit le texte si TalkBack/VoiceOver est activé.

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| talkBackMessage | `string` |

**Renvoie:**`void`

___

<a id="registerhardwarebackpresscallback"></a>

###  <a name="registerhardwarebackpresscallback"></a>registerHardwareBackPressCallback

▸ **registerHardwareBackPressCallback**(callback?: *`function`*):`void`

Enregistre un rappel à exécuter sur une pression de bouton de retour matériel (pour Android)

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`DoCallBack | `function` |  null |  méthode à exécuter |

**Renvoie:**`void`

___

<a id="setnativetoolbarproperties"></a>

###  <a name="setnativetoolbarproperties"></a>setNativeToolbarProperties

▸ **setNativeToolbarProperties**(propriétés: *[KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md)*):`void`

Définit peu de propriétés lors de l'utilisation de la barre d'outils Native

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var nativeToolbarProps = new KASClient.KASNativeToolbarProperties();
nativeToolbarProps.icon = "<image>"
nativeToolbarProps.title = "<title>";
nativeToolbarProps.subtitle = "<subtitle>";
KASClient.App.setNativeToolbarProperties(nativeToolbarProps);
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| propriétés | [KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md) |   |

**Renvoie:**`void`

___

<a id="setuserstrings"></a>

###  <a name="setuserstrings"></a>setUserStrings

▸ **setUserStrings**(strings?: *`JSON`*):`void`

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| `Default value`String | `JSON` |  null |

**Renvoie:**`void`

___

<a id="showattachmentpickerasync"></a>

###  <a name="showattachmentpickerasync"></a>showAttachmentPickerAsync

▸ **showAttachmentPickerAsync**(SupportedTypes: * [KASAttachmentType](../enums/kasclient.kasattachmenttype.md)[]*, props: *`JSON`*, callback: *`function`*):`void`

Affiche un sélecteur de pièces jointes dans la couche native

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var attachmentsTypesToShow = [];
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Image);
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Document);
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Audio);
KASClient.App.showAttachmentPickerAsync(attachmentsTypesToShow, null, function (selectedAttachments, error) {
      if (error != null) {
                      return;
      }
      if (selectedAttachments && selectedAttachments.length > 0) {
          for (var i = 0; i < selectedAttachments.length; i++) {
              if (selectedAttachments[i].type == KASClient.KASAttachmentType.Image) {
                    this.imageAttachmentList.push(selectedAttachments[i]);
              }
              ...
           }...
      }
});
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| supportedTypes | [KASAttachmentType](../enums/kasclient.kasattachmenttype.md) [] |  Tableau des types de pièces jointes pris en charge pour le sélecteur. |
| Propriétés | `JSON` |  autres propriétés permettant de configurer le sélecteur |
| callback | `function` |  avec les paramètres suivants<br><br>\*@param {KASAttachment\[\]} selectedAttachments chaîne de pièces jointes sélectionnées<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="showbarcodescannerasync"></a>

###  <a name="showbarcodescannerasync"></a>showBarcodeScannerAsync

▸ **showBarcodeScannerAsync**(callback: *`function`*):`void`

Lance le scanneur de codes-barres et renvoie l'objet analysé

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} barcodeInfo peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="showcontactpickerasync"></a>

###  <a name="showcontactpickerasync"></a>showContactPickerAsync

▸ **showContactPickerAsync**(title: *`string`*, selectedMutableUser: * `string`[]*, selectedImmutableUser: * `string`[]*, isSingleSelection: *`boolean`*, callback: *`function`*):`void`

Affiche un sélecteur de contacts natif et renvoie un tableau de tous les détails de l'utilisateur sélectionné

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| title | `string` |  du sélecteur de contacts |
| selectedMutableUser | `string`[] |  Tableau d'ID utilisateur sélectionnés |
| selectedImmutableUser | `string`[] |  Tableau des identificateurs de l'utilisateur sélectionnés |
| isSingleSelection | `boolean` |  sélection unique dans le sélecteur de contacts |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {KASUser\[\]} selectedUsers (tableau des détails de l'utilisateur) peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:** `void` Tableau de tous les détails des utilisateurs sélectionnés (tableau de JSON)
#### <a name="sample-usage"></a>Exemple d'utilisation
```
var alreadySelectedUserIds = [];
KASClient.App.showContactPickerAsync("<picker title>", alreadySelectedUserIds, [], true, function (selectedUsers, error) {
    if (error == null && selectedUsers != null && selectedUsers.length > 0) {
        var selectedUser = selectedUsers[0]; //KASUser
        console.log(selectedUser.id);
    }
});
```

___

<a id="showdurationpickerasync"></a>

###  <a name="showdurationpickerasync"></a>showDurationPickerAsync

▸ **showDurationPickerAsync**(defaultDurationInMinutes: *`number`*, callback: *`function`*):`void`

Affiche un sélecteur de durée native avec jour/heure/minute

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| defaultDurationInMinutes | `number` |  durée par défaut à afficher sur le sélecteur |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {nombre} durationInMinutes sélection de la durée en minutes<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="showimageimmersiveview"></a>

###  <a name="showimageimmersiveview"></a>showImageImmersiveView

▸ **showImageImmersiveView**(urls?: * `string`[]*, currentImageIndex?: *`number`*):`void`

Affiche l'image en mode immersif.

#### <a name="sample-usage"></a>Exemple d'utilisation

```
var urlArray = ["path1", "path2"];
KASClient.App.showImageImmersiveView(urlArray);
```

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`URL | `string`[] |  [] |  Tableau des images URL: |
| `Default value`currentImageIndex | `number` | 0 |

**Renvoie:**`void`

___

<a id="showimagepickerasync"></a>

###  <a name="showimagepickerasync"></a>showImagePickerAsync

▸ **showImagePickerAsync**(callback: *`function`*):`void`

Affiche un sélecteur d'image native et renvoie le chemin d'accès à l'image sélectionnée

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} selectedImagePath peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:** `void` Emplacement de l'image sélectionnée

___

<a id="showlocationonmap"></a>

###  <a name="showlocationonmap"></a>showLocationOnMap

▸ **showLocationOnMap**(Location: *[KASLocation](../classes/kasclient.kaslocation.md)*):`void`

indique un emplacement particulier, comme indiqué dans KASLocation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| location | [KASLocation](../classes/kasclient.kaslocation.md) |   |

**Renvoie:**`void`

___

<a id="shownativeerrormessage"></a>

###  <a name="shownativeerrormessage"></a>showNativeErrorMessage

▸ **showNativeErrorMessage**(message: *`string`*):`void`

Affiche une alerte native (pour iOS) ou un toast (pour Android) avec le message

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| message | `string` |   |

**Renvoie:**`void`

___

<a id="showplacepickerasync"></a>

###  <a name="showplacepickerasync"></a>showPlacePickerAsync

▸ **showPlacePickerAsync**(callback: *`function`*):`void`

Affiche un sélecteur d'emplacement natif et renvoie le lieu sélectionné (LT, LG, n)

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {KASLocation} selectedLocation peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="showprogressbar"></a>

###  <a name="showprogressbar"></a>showProgressBar

▸ **showProgressBar**(Text: *`string`*):`void`

Affiche une barre de progression Sreen complète native avec le texte donné

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| text | `string` |   |

**Renvoie:**`void`

___

<a id="showqrcodescannerasync"></a>

###  <a name="showqrcodescannerasync"></a>showQRcodeScannerAsync

▸ **showQRcodeScannerAsync**(callback: *`function`*):`void`

Lance l'analyseur de code QR et renvoie l'objet analysé

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {String} qrCodeInfo peut être null en cas d'erreur<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="showuserprofileasync"></a>

###  <a name="showuserprofileasync"></a>showUserProfileAsync

▸ **showUserProfileAsync**(UserID: *`string`*, isMiniProfile: *`boolean`*, callback: *`function`*):`void`

Affiche la page de profil/les détails d'un utilisateur

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  de l'utilisateur dont le profil doit être affiché |
| isMiniProfile | `boolean` |  indique s'il faut afficher d'abord le mini-profil |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} Success true si elle réussit, false dans le cas contraire<br><br>\*message d'erreur @param {String} en cas d'erreur, NULL sinon |

**Renvoie:**`void`

___

<a id="startchatasync"></a>

###  <a name="startchatasync"></a>startChatAsync

▸ **startChatAsync**(UserID: *`string`*, callback: *`function`*):`void`

Démarre la conversation avec un utilisateur

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  de l'utilisateur |
| callback | `function` |  avec les paramètres suivants:<br><br>\*@param {Boolean} réussite<br><br>\*erreur @param {chaîne} |

**Renvoie:**`void`

___

