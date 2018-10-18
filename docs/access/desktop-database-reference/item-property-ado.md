---
<<<<<<< Título HEAD: elemento (propiedad) (ADO) TOCTitle: elemento (propiedad) (ADO) === título: Item (propiedad, ADO) TOCTitle: Item (propiedad, ADO)
>>>>>>> Master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: ms.date 48545767: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="item-property-ado"></a>Item (propiedad, ADO)
=======
# <a name="item-property-ado"></a>Elemento (propiedad, ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indica un miembro específico de una colección, por nombre o número ordinal.

## <a name="syntax"></a>Sintaxis

*Objeto*de conjunto de = *colección*. Item (Index)

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve una referencia de objeto.

## <a name="parameters"></a>Parámetros

- *Index*

- Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto específico de una colección. Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error. Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.

**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:

```vb
    collection.Item (Index)
    collection (Index)
```
