---
ms.openlocfilehash: f725f55c2e7e0c8c75d71275c7217497090b4f1a
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728013"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [application](../modules/kasclient.app.md)

# <a name="module-app"></a>Module : application

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
* [ShowProgressBar indique](kasclient.app.md#showprogressbar)
* [showQRcodeScannerAsync](kasclient.app.md#showqrcodescannerasync)
* [showUserProfileAsync](kasclient.app.md#showuserprofileasync)
* [startChatAsync](kasclient.app.md#startchatasync)

---

## <a name="functions"></a>Fonctions

<a id="cancelattachmentdownloadasync"></a>

###  <a name="cancelattachmentdownloadasync"></a>cancelAttachmentDownloadAsync

▸ **cancelAttachmentDownloadAsync**(pièces jointes : *[KASAttachment](../classes/kasclient.kasattachment.md)*, rappel : *`function`*) :`void`

Annuler une opération de téléchargement en file d’attente d’une pièce jointe

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| callback | `function` |  avec erreur param - chaîne d’erreur en cas d’erreur ; Sinon, valeur null |

**Renvoie :** `void`

___

<a id="dismisscurrentscreen"></a>

###  <a name="dismisscurrentscreen"></a>dismissCurrentScreen

▸ **dismissCurrentScreen**() :`void`

Ignorer l’écran de l’Action ouvert en cours (création, réponse ou résumé)

**Renvoie :** `void`

___

<a id="downloadattachmentasync"></a>

###  <a name="downloadattachmentasync"></a>downloadAttachmentAsync

▸ **downloadAttachmentAsync**(pièces jointes : *[KASAttachment](../classes/kasclient.kasattachment.md)*, rappel : *`function`*) :`void`

Télécharger la pièce jointe spécifiée

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| pièce jointe | [KASAttachment](../classes/kasclient.kasattachment.md) |  avec un chemin d’accès de serveur valide pour télécharger des pièces jointes |
| callback | `function` |  rappel à la fin du téléchargement avec sous Paramètres<br><br>\*@param {KASAttachment} downloadedAttachment la pièce jointe que vous avez téléchargée<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="generatebase64thumbnailasync"></a>

###  <a name="generatebase64thumbnailasync"></a>generateBase64ThumbnailAsync

▸ **generateBase64ThumbnailAsync**(localPath : *`string`*, rappel : *`function`*) :`void`

Génère la miniature en Base64 pour une image donnée dont localPath

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| localPath | `string` |  localPath pour l’imageAttachment dont miniature doit être généré |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*valeur de miniature la base64 @param {chaîne}<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="generateuuidasync"></a>

###  <a name="generateuuidasync"></a>generateUUIDAsync

▸ **generateUUIDAsync**(rappel : *`function`*) :`void`

Obtient le nouvel UUID

#### <a name="sample-usage"></a>Exemple d’utilisation

```
 KASClient.App.generateUUIDAsync(function (uuid, error) {
    console.log("generatedUUIDAsync", uuid);
    ...
 });
```

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*uuid @param {chaîne} généré récemment uuid<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getapplocaleasync"></a>

###  <a name="getapplocaleasync"></a>getAppLocaleAsync

▸ **getAppLocaleAsync**(rappel : *`function`*) :`void`

Obtient les paramètres régionaux application en cours, la langue dans laquelle l’application est affichée, utiles pour localiser les chaînes de MiniApp

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*paramètres régionaux @param {chaîne} peuvent être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getcalendarnameasync"></a>

###  <a name="getcalendarnameasync"></a>getCalendarNameAsync

▸ **getCalendarNameAsync**(rappel : *`function`*) :`void`

Obtient la valeur du calendrier système actuelle. Il s’agit principalement pour iOS pour identifier le nom du calendrier défini dans le paramètre de téléphone comme grégorien ou japonais ou Buddhists.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*calendarName @param {chaîne} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getconversationdetailsasync"></a>

###  <a name="getconversationdetailsasync"></a>getConversationDetailsAsync

▸ **getConversationDetailsAsync**(rappel : *`function`*) :`void`

Conversation Obtient les propriétés associées

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*propriétés de conversation résultat @param {KASConversationDetails}<br><br>\*chaîne json d’erreur de @param {chaîne} pour l’objet KASError contenant la description et/ou le code d’erreur. |

**Renvoie :** `void`

___

<a id="getcurrentdevicelocationasync"></a>

###  <a name="getcurrentdevicelocationasync"></a>getCurrentDeviceLocationAsync

▸ **getCurrentDeviceLocationAsync**(rappel : *`function`*) :`void`

Obtient l’emplacement actuel du périphérique

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*emplacement @param {chaîne} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getcurrentlocale"></a>

###  <a name="getcurrentlocale"></a>getCurrentLocale

▸ **getCurrentLocale**() :`string`

**Renvoie :** `string`

___

<a id="getdeviceidasync"></a>

###  <a name="getdeviceidasync"></a>getDeviceIdAsync

▸ **getDeviceIdAsync**(rappel : *`function`*) :`void`

Obtient l’ID de périphérique

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*ID de périphérique @param {chaîne} obtenue depuis le service integeration<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getdevicelocationasync"></a>

###  <a name="getdevicelocationasync"></a>getDeviceLocationAsync

▸ **getDeviceLocationAsync**(rappel : *`function`*) :`void`

Obtient l’emplacement du périphérique stocké précédemment

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*emplacement @param {chaîne} peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getfontsizemultiplierasync"></a>

###  <a name="getfontsizemultiplierasync"></a>getFontSizeMultiplierAsync

▸ **getFontSizeMultiplierAsync**(rappel : *`function`*) :`void`

Obtient le multiplicateur de taille de police de texte de grande taille. En cours est uniquement requis par iOS.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec sous Paramètres<br><br>\*Multiplicateur @param {chaîne}<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getforwardcontextasync"></a>

###  <a name="getforwardcontextasync"></a>getForwardContextAsync

▸ **getForwardContextAsync**(rappel : *`function`*) :`void`

Obtient les détails du contexte transférer tel que : création de carte est en mode transféré

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {Json} retourne les informations de contexte dans la structure de Json |

**Renvoie :** `void`

___

<a id="getisapptimeformat24hoursasync"></a>

###  <a name="getisapptimeformat24hoursasync"></a>getIsAppTimeFormat24HoursAsync

▸ **getIsAppTimeFormat24HoursAsync**(rappel : *`function`*) :`void`

Obtient l’heure application actuelle est au format 24hours ou non, le format d’heure sélectionné par l’utilisateur, utile pour la mise en forme des chaînes de temps date correctement

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {chaîne} isAppTimeFormat24Hours peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getlocalizedstringsasync"></a>

###  <a name="getlocalizedstringsasync"></a>getLocalizedStringsAsync

▸ **getLocalizedStringsAsync**(rappel : *`function`*) :`void`

Obtient un dictionnaire des chaînes localisées en fonction de paramètres régionaux application en cours. Chaînes doivent être fournis dans le package, par exemple : chaînes\_en.json, les chaînes\_hi.json, etc..

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {JSON} chaînes peuvent être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getlocationaddressasync"></a>

###  <a name="getlocationaddressasync"></a>getLocationAddressAsync

▸ **getLocationAddressAsync**(paramètres : *[KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md)*, rappel : *`function`*) :`void`

Obtenir la chaîne d’adresse pour les coordonnées spécifiées

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| paramètres | [KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md) |  KASLocationAddressParams |
| callback | `function` |  rappel à extraction adresse avec sous Paramètres<br><br>\*emplacement @param {JSON} a json contenant latitute longitude et autres informaion<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getmapimageasbase64async"></a>

###  <a name="getmapimageasbase64async"></a>getMapImageAsBase64Async

▸ **getMapImageAsBase64Async**(paramètres : *[KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md)*, rappel : *`function`*) :`void`

Télécharger l’image de base 64 de la feuille de route pour les coordonnées spécifiées

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| paramètres | [KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md) |  KASLocationStaticMapImageParams |
| callback | `function` |  à la fin du téléchargement avec sous Paramètres<br><br>\*valeur de base64 attachmentString @param {chaîne} de la pièce jointe<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="geto365userdetailsasync"></a>

###  <a name="geto365userdetailsasync"></a>getO365UserDetailsAsync

▸ **getO365UserDetailsAsync**(rappel : *`function`*) :`void`

Obtient les détails de cours O365 utilisateur connecté

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {Json} renvoie la UserDetails dans la structure de Json |

**Renvoie :** `void`

___

<a id="getpackagecustomsettingsasync"></a>

###  <a name="getpackagecustomsettingsasync"></a>getPackageCustomSettingsAsync

▸ **getPackageCustomSettingsAsync**(rappel : *`function`*) :`void`

Obtient tous les paramètres de personnalisation d’un package (utilisé en cas de packages de Type 4 et leur base).

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*paramètres @param {JSON} peuvent être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="getusersdetailsasync"></a>

###  <a name="getusersdetailsasync"></a>getUsersDetailsAsync

▸ **getUsersDetailsAsync**(userIds : * `string`[]*, rappel : *`function`*) :`void`

Obtient les détails des utilisateurs (nom, pic, numéro de téléphone, etc.) par rapport à leur ID

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| ID utilisateur | `string`[] |  tableau des ID utilisateur |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {Dictionary<UserId : chaîne UserInfo : KASUser>} userIdToInfoMap (détails des utilisateurs par rapport à leur ID) peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="hideprogressbar"></a>

###  <a name="hideprogressbar"></a>hideProgressBar

▸ **hideProgressBar**() :`void`

Masque la barre de progression en cours, le cas échéant

**Renvoie :** `void`

___

<a id="isattachmentdownloadingasync"></a>

###  <a name="isattachmentdownloadingasync"></a>isAttachmentDownloadingAsync

▸ **isAttachmentDownloadingAsync**(pièces jointes : *[KASAttachment](../classes/kasclient.kasattachment.md)*, rappel : *`function`*) :`void`

Télécharger la pièce jointe spécifiée

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| pièce jointe | [KASAttachment](../classes/kasclient.kasattachment.md) |  avec un chemin d’accès de serveur valide pour télécharger des pièces jointes |
| callback | `function` |  rappel à la fin du téléchargement avec sous Paramètres<br><br>\*@param {boolean} isAttachmentDownloadingOrDownLoaded indicateur représentant si la pièce jointe est téléchargé/de téléchargement<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="isauthenticationtyepsupportedasync"></a>

###  <a name="isauthenticationtyepsupportedasync"></a>isAuthenticationTyepSupportedAsync

▸ **isAuthenticationTyepSupportedAsync**(authenticationType? : *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, rappel : *`function`*) :`void`

Vérifie si l’authentification de type est possible ou non.

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType.None |  type d’authentification. |
| callback | `function` | - |  avec les paramètres ci-dessous :<br><br>\*@param {boolean} isSuccessful la valeur true si les empreintes digitales est possible<br><br>\*code de motif de codes de motif @param {chaîne} pourquoi doigt impression n’est pas possible |

**Renvoie :** `void`

___

<a id="istalkbackenabledasync"></a>

###  <a name="istalkbackenabledasync"></a>isTalkBackEnabledAsync

▸ **isTalkBackEnabledAsync**(rappel : *`function`*) :`void`

Indique si talkback est activé ou non

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*valeur true talkBackEnabled @param {boolean} si talkback est activé. |

**Renvoie :** `void`

___

<a id="logtoreport"></a>

###  <a name="logtoreport"></a>logToReport

▸ **logToReport**(données : *`string`*) :`void`

Les journaux de données pour « Envoyer le rapport »

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| data | `string` |  string |

**Renvoie :**`void`

___

<a id="openattachmentimmersiveview"></a>

###  <a name="openattachmentimmersiveview"></a>openAttachmentImmersiveView

▸ **openAttachmentImmersiveView**(attachmentObj : *[KASAttachment](../classes/kasclient.kasattachment.md)*) :`void`

Ouvrir la pièce jointe en mode immersif.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| attachmentObj | [KASAttachment](../classes/kasclient.kasattachment.md) |   |

**Renvoie :** `void`

___

<a id="openimmersiveviewforattachmentlist"></a>

###  <a name="openimmersiveviewforattachmentlist"></a>openImmersiveViewForAttachmentList

▸ **openImmersiveViewForAttachmentList**(attachmentList : *[] [KASAttachment](../classes/kasclient.kasattachment.md)*, atIndex? : *`number`*) :`void`

Ouvrir la pièce jointe en mode immersif.

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| attachmentList | [KASAttachment](../classes/kasclient.kasattachment.md) [] | - |
| `Default value`atIndex | `number` | 0 |

**Renvoie :** `void`

___

<a id="performauthenticationasync"></a>

###  <a name="performauthenticationasync"></a>performAuthenticationAsync

▸ **performAuthenticationAsync**(authenticationType? : *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, rappel : *`function`*) :`void`

Si le type d’authentification est autorisé, cette API effectue l’authentification et renvoie l’état de réussite/false sinon il renvoie une chaîne d’erreur avec motif pourquoi l’authentification n’est pas possible.

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType.None |  type d’authentification. |
| callback | `function` | - |  avec les paramètres ci-dessous :<br><br>\*@param {boolean} isSuccessful la valeur true si le formulaire n’est pas encore terminée.<br><br>\*codes de motif @param {chaîne} raison code en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="performhttprequest"></a>

###  <a name="performhttprequest"></a>performHTTPRequest

▸ **performHTTPRequest**(url : *`string`*, parametersJSON : *`string`*, rappel : *`function`*) :`void`

effectue une demande http et renvoie la réponse comme indiqué ci-dessous :

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| url | `string` |  url de base à ouvrir |
| parametersJSON | `string` |  jsonstring contenant des paramètres peut être indiquée comme null.<br><br> Si indiqués sous forme de valeur null sera une demande à l’url indiquée ci-dessus. Paramètres inclure l’en-tête de la demande, les paramètres de requête (vide par défaut), demander la méthode (GET par défaut) et le corps de la demande (le corps pour être publiés si la méthode de demande est POST. valeur par défaut vide.) Les clés pour les paramètres sont les suivants :<br><br> « méthode » a) : méthode de demande. exemple : « POST ». la valeur par défaut est « GET ».<br><br> b) « requestBody » : le corps de demande en cas de « POST ». valeur par défaut est vide.<br><br> c) « requestHeaders » : les en-têtes pour être envoyé avec la demande. doit être un json avec<br> clé comme en-tête de la demande et la valeur que la valeur souhaitée. valeur par défaut est vide.<br><br> d.) « queryParameters » : paramètres de requête. sera codé dans l’url. doit être un json avec<br> clé en tant que nom du paramètre et valeur que sa valeur. valeur par défaut est vide.<br><br> e.) « requestResourcePath » : sera ajouté à l’url de base. valeur par défaut est vide. |
| callback | `function` |  rappel avec paramètres ci-dessous :<br><br>\*corps de réponse @param {chaîne} response renvoyé<br><br> Cela peut avoir les deux options de configuration possibles :<br><br> Si la demande a réussi, elle renvoie jsonstring avec clés suivantes :<br><br> a.) « HttpResponseCode » : le code de réponse de la demande.<br><br> b) « HttpResponseHeader » : les en-têtes de réponse HTTP<br><br> c) « HttpResponseBody » : le corps de réponse est renvoyée pour la demande.<br><br> Si une erreur réseau s’est produite il renvoie :<br><br> a.) « HttpErrorCode » : le code d’erreur<br><br> b) « HttpErrorMessage » : le message d’erreur, par exemple. URL incorrecte, ne peut pas se connecter à l’hôte, etc..<br><br>\*erreur @param {chaîne} le cas échéant : Cela inclut le code d’erreur standard défini dans la documentation KASClient. |

**Renvoie :** `void`

___

<a id="printf"></a>

###  <a name="printf"></a>printf

▸ **printf**(principale : *`string`*, … args : * `any`[]*) :`string`

Renvoie une chaîne.

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| principale | `string` |
| `Rest`args | `any`[] |  tableau d’arguments. |

**Renvoie :** `string`

___

<a id="readtalkbackmessage"></a>

###  <a name="readtalkbackmessage"></a>readTalkBackMessage

▸ **readTalkBackMessage**(talkBackMessage : *`string`*) :`void`

Lit le texte si TalkBack/voix hors champ activé

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| talkBackMessage | `string` |

**Renvoie :** `void`

___

<a id="registerhardwarebackpresscallback"></a>

###  <a name="registerhardwarebackpresscallback"></a>registerHardwareBackPressCallback

▸ **registerHardwareBackPressCallback**(callback? : *`function`*) :`void`

Enregistre un rappel à exécuter sur matériel, appuyez sur le bouton précédent (pour Android)

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`rappel | `function` |  null |  méthode à exécuter |

**Renvoie :** `void`

___

<a id="setnativetoolbarproperties"></a>

###  <a name="setnativetoolbarproperties"></a>setNativeToolbarProperties

▸ **setNativeToolbarProperties**(propriétés : *[KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md)*) :`void`

Définit certaines propriétés lors de l’utilisation d’une barre d’outils natif

#### <a name="sample-usage"></a>Exemple d’utilisation

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

**Renvoie :** `void`

___

<a id="setuserstrings"></a>

###  <a name="setuserstrings"></a>setUserStrings

▸ **setUserStrings**(strings? : *`JSON`*) :`void`

**Paramètres :**

| Nom | Type | Valeur par défaut |
| ------ | ------ | ------ |
| `Default value`chaînes | `JSON` |  null |

**Renvoie :** `void`

___

<a id="showattachmentpickerasync"></a>

###  <a name="showattachmentpickerasync"></a>showAttachmentPickerAsync

▸ **showAttachmentPickerAsync**(supportedTypes : *[] [KASAttachmentType](../enums/kasclient.kasattachmenttype.md)*, propriétés : *`JSON`*, rappel : *`function`*) :`void`

Affiche un sélecteur de pièce jointe dans la couche native

#### <a name="sample-usage"></a>Exemple d’utilisation

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
| supportedTypes | [KASAttachmentType](../enums/kasclient.kasattachmenttype.md) [] |  tableau des types de pièce jointe pris en charge pour le sélecteur. |
| propriétés | `JSON` |  propriétés supplémentaires pour configurer le sélecteur |
| callback | `function` |  avec les paramètres ci-dessous<br><br>\*@param {KASAttachment\[\]} selectedAttachments chaîne de pièces jointes sélectionnées<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="showbarcodescannerasync"></a>

###  <a name="showbarcodescannerasync"></a>showBarcodeScannerAsync

▸ **showBarcodeScannerAsync**(rappel : *`function`*) :`void`

Lance l’Analyseur de code-barres et renvoie l’objet analysé

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {chaîne} barcodeInfo peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="showcontactpickerasync"></a>

###  <a name="showcontactpickerasync"></a>showContactPickerAsync

▸ **showContactPickerAsync**(titre : *`string`*, selectedMutableUser : * `string`[]*, selectedImmutableUser : * `string`[]*, isSingleSelection : *`boolean`*, rappel : *`function`*) :`void`

Affiche un sélecteur de contact natif et renvoie un tableau des détails de tous les utilisateurs

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| title | `string` |  du sélecteur de contacts |
| selectedMutableUser | `string`[] |  tableau des ID utilisateur sélectionné |
| selectedImmutableUser | `string`[] |  tableau des ID utilisateur sélectionné fixe |
| isSingleSelection | `boolean` |  seule la sélection dans le sélecteur de contacts |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {KASUser\[\]} selectedUsers (tableau de détails de l’utilisateur) peut être null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void` Tableau des détails de tous les utilisateurs (tableau de JSON)
#### <a name="sample-usage"></a>Exemple d’utilisation
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

▸ **showDurationPickerAsync**(defaultDurationInMinutes : *`number`*, rappel : *`function`*) :`void`

Affiche un sélecteur de durée native avec jour/heure/minute

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| defaultDurationInMinutes | `number` |  la durée par défaut à afficher dans le sélecteur |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*durationInMinutes @param {nombre} sélectionné la durée en minutes<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="showimageimmersiveview"></a>

###  <a name="showimageimmersiveview"></a>showImageImmersiveView

▸ **showImageImmersiveView**(urls? : * `string`[]*, currentImageIndex? : *`number`*) :`void`

Affiche l’Image en mode immersif.

#### <a name="sample-usage"></a>Exemple d’utilisation

```
var urlArray = ["path1", "path2"];
KASClient.App.showImageImmersiveView(urlArray);
```

**Paramètres :**

| Nom | Type | Valeur par défaut | Description |
| ------ | ------ | ------ | ------ |
| `Default value`URL | `string`[] |  [] |  Tableau d’images url : |
| `Default value`currentImageIndex | `number` | 0 |

**Renvoie :** `void`

___

<a id="showimagepickerasync"></a>

###  <a name="showimagepickerasync"></a>showImagePickerAsync

▸ **showImagePickerAsync**(rappel : *`function`*) :`void`

Affiche un sélecteur d’images natif et renvoie le chemin d’accès de l’image sélectionnée

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {chaîne} selectedImagePath peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void` Sélectionné l’emplacement de l’image

___

<a id="showlocationonmap"></a>

###  <a name="showlocationonmap"></a>showLocationOnMap

▸ **showLocationOnMap**(emplacement : *[KASLocation](../classes/kasclient.kaslocation.md)*) :`void`

Indique un emplacement particulier, comme indiqué dans KASLocation

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| location | [KASLocation](../classes/kasclient.kaslocation.md) |   |

**Renvoie :** `void`

___

<a id="shownativeerrormessage"></a>

###  <a name="shownativeerrormessage"></a>showNativeErrorMessage

▸ **showNativeErrorMessage**(message : *`string`*) :`void`

Affiche une alerte native (pour les e/s) ou une alerte (Android) avec le message

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| message | `string` |   |

**Renvoie :** `void`

___

<a id="showplacepickerasync"></a>

###  <a name="showplacepickerasync"></a>showPlacePickerAsync

▸ **showPlacePickerAsync**(rappel : *`function`*) :`void`

Affiche un sélecteur de place natif et renvoie le lieu sélectionné (lt, lg, n)

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {KASLocation} selectedLocation peut être une valeur nulle en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="showprogressbar"></a>

###  <a name="showprogressbar"></a>ShowProgressBar indique

▸ **ShowProgressBar indique**(texte : *`string`*) :`void`

Affiche une barre de progression de l ' écran complète native avec le texte donné

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| text | `string` |   |

**Renvoie :** `void`

___

<a id="showqrcodescannerasync"></a>

###  <a name="showqrcodescannerasync"></a>showQRcodeScannerAsync

▸ **showQRcodeScannerAsync**(rappel : *`function`*) :`void`

Lance l’Analyseur de code QR et renvoie l’objet analysé

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*@param {chaîne} qrCodeInfo peut être une valeur null en cas d’erreur<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="showuserprofileasync"></a>

###  <a name="showuserprofileasync"></a>showUserProfileAsync

▸ **showUserProfileAsync**(userId : *`string`*, isMiniProfile : *`boolean`*, rappel : *`function`*) :`void`

Indique les détails/page de profil d’un utilisateur

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  de l’utilisateur dont le profil doit être affiché |
| isMiniProfile | `boolean` |  s’il faut afficher d’abord Mini profil |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*false la valeur true si l’opération réussit, de réussite @param {boolean} sinon<br><br>\*message d’erreur @param {chaîne} en cas d’erreur, la valeur null dans le cas contraire |

**Renvoie :** `void`

___

<a id="startchatasync"></a>

###  <a name="startchatasync"></a>startChatAsync

▸ **startChatAsync**(userId : *`string`*, rappel : *`function`*) :`void`

Conversation commence avec un utilisateur

**Paramètres :**

| Nom | Type | Description |
| ------ | ------ | ------ |
| userId | `string` |  de l’utilisateur |
| callback | `function` |  avec les paramètres ci-dessous :<br><br>\*réussite @param {boolean}<br><br>\*erreur @param {chaîne} |

**Renvoie :** `void`

___

