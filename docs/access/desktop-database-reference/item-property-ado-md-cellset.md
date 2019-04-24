---
title: Item (propiedad, Cellset de ADO MD)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290870"
---
# <a name="item-property-ado-md-cellset"></a>Item (propiedad, Cellset de ADO MD)

**Se aplica a:** Access 2013, Office 2013

Recupera una celda de un conjunto de celdas utilizando sus coordenadas.

## <a name="syntax"></a>Sintaxis

Establece el conjunto de celdas de la*celda* = **. Elemento (*posiciones*)

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Positions* |Una **matriz** de valores Variant que especifica de forma única una celda. *Positions* puede ser uno de los siguientes:<br/><br/>-Una matriz de números de posición<br/>-Una matriz de nombres de miembros<br/>-La posición ordinal |

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto [Cell](cell-object-ado-md.md) dentro de un objeto [Cellset](cellset-object-ado-md.md). Si la propiedad **Item** no puede encontrar la celda correspondiente al argumento *Positions*, se produce un error.

**Item** es la propiedad predeterminada para el objeto **Cellset**. Los siguientes formatos de sintaxis son intercambiables:

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

El argumento *Positions* especifica la celda que se devuelve. Puede especificar la celda por la posición ordinal o por la posición a lo largo del eje. Cuando se especifica por la posición a lo largo del eje, puede indicar el valor numérico de la posición o los nombres de los miembros de cada posición.

La posición ordinal es un número que identifica inequívocamente una celda dentro del **conjunto de celdas**. Conceptualmente, las celdas se numeran en un **conjunto de celdas** como si el **conjunto de celdas** fuera una matriz de *p* dimensiones, donde *p* es el número de ejes. El tratamiento de las celdas sigue el orden de fila mayor.

Si se pasan nombres de miembros como cadenas al objeto **Item**, los miembros deben especificarse siguiendo el orden creciente de los identificadores de eje numérico. Dentro de un eje, los miembros deben especificarse en orden creciente de las dimensiones anidadas , es decir, primero el miembro de la dimensión exterior y después los miembros de las dimensiones interiores. Cada dimensión debe representarse mediante una cadena distinta, y la lista de cadenas de miembro debe separarse por comas.


> [!NOTE]
> [!NOTA] Puede que el proveedor de datos no permita la recuperación de celdas por nombre de miembro. Vea la documentación de su proveedor para obtener más información.


