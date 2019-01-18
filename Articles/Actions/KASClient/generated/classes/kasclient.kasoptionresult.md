---
ms.openlocfilehash: c52e672a7e3356171388692054fcd1dc3cee5365
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727908"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)

# <a name="class-kasoptionresult"></a>Classe : KASOptionResult

## <a name="hierarchy"></a>Hierarchy

**KASOptionResult**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [Id_option](kasclient.kasoptionresult.md#optionid)
* [optionTitle](kasclient.kasoptionresult.md#optiontitle)
* [responderToResponseCount](kasclient.kasoptionresult.md#respondertoresponsecount)
* [totalResponsesCount](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a>Méthodes

* [fromJSON](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="optionid"></a>

###  <a name="optionid"></a>Id_option

**● Id_option**: *`number`* = 0

Index de l’option

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a>optionTitle

**● optionTitle**: *`string`* = « »

Titre de l’option

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a>responderToResponseCount

**● responderToResponseCount**:*`object`*

Un mappage de l’ID d’utilisateur par rapport à leur nombre de réponse Dictionary<UserId : chaîne, ResponseCount : number>
#### <a name="type-declaration"></a>Déclaration de type

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a>totalResponsesCount

**● totalResponsesCount**: *`number`* = 0

Combien choisi cette option

___

## <a name="methods"></a>Méthodes

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet : *`any`*) : [KASOptionResult](kasclient.kasoptionresult.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `any` |

**Renvoie :** [KASOptionResult](kasclient.kasoptionresult.md)

___

