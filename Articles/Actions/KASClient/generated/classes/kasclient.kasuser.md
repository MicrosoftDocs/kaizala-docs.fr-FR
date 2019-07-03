[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)

# <a name="class-kasuser"></a>Classe: KASUser

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
* [pictureUrl](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

ID d’utilisateur unique

___
<a id="name"></a>

###  <a name="name"></a>name

**● nom**: *`string`* = ""

Nom de l’utilisateur («vous» pour l’utilisateur actuel)

___
<a id="originalname"></a>

###  <a name="originalname"></a>originalName

**● originalName**: *`string`* = ""

N’envisagez pas «vous»

___
<a id="phonenumber"></a>

###  <a name="phonenumber"></a>phoneNumber

**● phoneNumber**: *`string`* = ""

Numéro de téléphone de l’utilisateur

___
<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a>pictureBGColor

**● pictureBGColor**: *`string`* = ""

Si le PictureUrl n’est pas là, nous devons utiliser les initiales des utilisateurs comme profil pic, sous deux membres

___
<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a>pictureInitials

**● pictureInitials**: *`string`* = ""

___
<a id="pictureurl"></a>

###  <a name="pictureurl"></a>pictureUrl

**● pictureUrl**: *`string`* = ""

URL de l’image de profil de l’utilisateur

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`JSON`*): [KASUser](kasclient.kasuser.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie:** [KASUser](kasclient.kasuser.md)

___

