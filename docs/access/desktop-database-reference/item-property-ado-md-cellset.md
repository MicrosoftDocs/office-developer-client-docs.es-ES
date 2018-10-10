---
title: Item (propiedad) (conjunto de celdas de ADO MD)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 017b25b164233cb0e16753874e5b898409b5ac5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484073"
---
# <a name="item-property-ado-md-cellset"></a>Item (propiedad) (conjunto de celdas de ADO MD)

**Se aplica a**: Access 2013 | Office 2013

Recupera una celda de un conjunto de celdas utilizando sus coordenadas.

## <a name="syntax"></a>Sintaxis

Establecer*celda* = *conjunto de celdas*. Elemento (*posiciones*)

## <a name="parameters"></a>Parámetros

- *Positions*

- Una **matriz** **Variant** de valores que especifican inequívocamente una celda. *Positions* puede ser una de las siguientes opciones:
    
  - Una matriz de números de posiciones
    
  - Una matriz de nombres de miembros
    
  - La posición ordinal

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto [Cell](cell-object-ado-md.md) dentro de un objeto [Cellset](cellset-object-ado-md.md). Si la propiedad **Item** no puede encontrar la celda correspondiente al argumento *Positions* , se produce un error.

**Item** es la propiedad predeterminada para el objeto **Cellset**. Los siguientes formatos de sintaxis son intercambiables:

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

El argumento *Positions* especifica la celda que se devuelven. Puede especificar la celda por la posición ordinal o por la posición a lo largo del eje. Cuando se especifica por la posición a lo largo del eje, puede indicar el valor numérico de la posición o los nombres de los miembros de cada posición.

La posición ordinal es un número que identifica inequívocamente una celda dentro del **conjunto de celdas**. Conceptualmente, las celdas se numeran en un **conjunto de celdas** como si el **conjunto de celdas** fuera una matriz de *p* dimensiones, donde *p* es el número de ejes. El tratamiento de las celdas sigue el orden de fila mayor.

Si se pasan nombres de miembros como cadenas al objeto **Item**, los miembros deben especificarse siguiendo el orden creciente de los identificadores de eje numérico. Dentro de un eje, los miembros deben especificarse en orden creciente de las dimensiones anidadas , es decir, primero el miembro de la dimensión exterior y después los miembros de las dimensiones interiores. Cada dimensión debe representarse mediante una cadena distinta, y la lista de cadenas de miembro debe separarse por comas.


> [!NOTE]
> [!NOTA] Puede que el proveedor de datos no permita la recuperación de celdas por nombre de miembro. Vea la documentación de su proveedor para obtener más información.


