[](../README.md) > [KASClient](../modules/kasclient.md) > [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)

# <a name="class-kasactionlocalcacheprop"></a>Classe: KASActionLocalCacheProp

## <a name="hierarchy"></a>Hierarchy

**KASActionLocalCacheProp**

## <a name="index"></a>Index

### <a name="properties"></a>Propriétés

* [cacheScope](kasclient.kasactionlocalcacheprop.md#cachescope)
* [cacheVisibility](kasclient.kasactionlocalcacheprop.md#cachevisibility)
* [key](kasclient.kasactionlocalcacheprop.md#key)
* [value](kasclient.kasactionlocalcacheprop.md#value)
### <a name="methods"></a>Méthodes

* [toJSON](kasclient.kasactionlocalcacheprop.md#tojson)
* [fromJSON](kasclient.kasactionlocalcacheprop.md#fromjson)

---

## <a name="properties"></a>Propriétés

<a id="cachescope"></a>

###  <a name="cachescope"></a>cacheScope

**● cacheScope**: *[cacheScope](../enums/kasclient.cachescope.md)* = cacheScope. global

cacheScope indique que les données seront stockées au niveau global ou converastion.

___
<a id="cachevisibility"></a>

###  <a name="cachevisibility"></a>cacheVisibility

**● cacheVisibility**: *[cacheVisibility](../enums/kasclient.cachevisibility.md)* = cacheVisibility. app

cacheVisibility indique que les données visibles par d’autres applications ou non.

___
<a id="key"></a>

###  <a name="key"></a>clé

**● clé**: *`string`* = ""

clé de la valeur stockée dans le cache

___
<a id="value"></a>

###  <a name="value"></a>value

**● valeur**: *`string`* = ""

___

## <a name="methods"></a>Méthodes

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **toJSON**():`JSON`

**Renvoie:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(objet: *`JSON`*): [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)

**Paramètres :**

| Nom | Type |
| ------ | ------ |
| objet | `JSON` |

**Renvoie:** [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)

___

