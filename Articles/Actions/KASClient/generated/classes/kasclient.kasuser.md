---
ms.openlocfilehash: 20daed268b67eea07a8185c84086587dcf1f1aeb
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727942"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)

# <a name="class-kasuser"></a>Classe : KASUser

## <a name="hierarchy"></a>Hierarchy

**KASUser**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [id](kasclient.kasuser.md#id)
* [name](kasclient.kasuser.md#name)
* [originalName](kasclient.kasuser.md#originalname)
* [phoneNumber](kasclient.kasuser.md#phonenumber)
* [pictureBGColor](kasclient.kasuser.md#picturebgcolor)
* [pictureInitials](kasclient.kasuser.md#pictureinitials)
* [URL de la photo](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="id"></a>

###  <a name="id"></a>id

**Id ●**: *`string`* = « »

Id d’utilisateur unique

___

<a id="name"></a>

###  <a name="name"></a>name

**Nom ●**: *`string`* = « »

Nom de l’utilisateur (« vous » pour l’utilisateur actuel)

___

<a id="originalname"></a>

###  <a name="originalname"></a>originalName

**● originalName**: *`string`* = « »

Ne pas considérer « Vous »

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a>phoneNumber

**● phoneNumber**: *`string`* = « »

Numéro de téléphone de l’utilisateur

___

<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a>pictureBGColor

**● pictureBGColor**: *`string`* = « »

En cas de l’URL de la photo n’est pas visible, nous devons utiliser les initiales en tant que le pic de profil, sous deux membres qui sont des utilisateurs

___

<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a>pictureInitials

**● pictureInitials**: *`string`* = « »

___

<a id="pictureurl"></a>

###  <a name="pictureurl"></a>URL de la photo

**● pictureUrl**: *`string`* = « »

Url d’image de profil de l’utilisateur

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`JSON`*) : [KASUser](kasclient.kasuser.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie :** [KASUser](kasclient.kasuser.md)

___

