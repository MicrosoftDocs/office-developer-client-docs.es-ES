---
title: AbsolutePosition (propiedad, ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486270"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica la posición ordinal del registro actual de un objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de registros del objeto **Recordset** ([RecordCount](recordcount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Comentarios

Para establecer la propiedad **AbsolutePosition**, ADO requiere que el proveedor OLE DB utilizado implemente la interfaz IRowsetLocate.

Al obtener acceso a la propiedad **AbsolutePosition** de un objeto **Recordset** que se ha abierto con un cursor de sólo avance o un cursor dinámico, se genera el error **adErrFeatureNotAvailable**. Con otros tipos de cursor, se devolverá la posición correcta, siempre y cuando el proveedor admita la interfaz IRowsetScroll. Si el proveedor no admite la interfaz *IRowsetScroll*, el valor de la propiedad se establece en **adPosUnknown**. Vea la documentación de su proveedor para determinar si admite *IRowsetScroll*.

Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset** o para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.

Al igual que la propiedad [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Se puede obtener el número total de registros del objeto **Recordset** mediante la propiedad [RecordCount](recordcount-property-ado.md).

Cuando establece la propiedad **AbsolutePosition**, incluso estableciéndola en un registro de la caché actual, ADO vuelve a cargar la caché con un nuevo grupo de registros empezando por el registro especificado. La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.


> [!NOTE]
> <P>[!NOTA] La propiedad <STRONG>AbsolutePosition</STRONG> no debe utilizarse como un número de registro suplente. La posición de un registro determinado cambia al eliminar un registro anterior. Tampoco hay ninguna garantía de que un registro determinado tenga el mismo valor de <STRONG>AbsolutePosition</STRONG> si se vuelve a consultar o a abrir el objeto <STRONG>Recordset</STRONG>. Se recomienda usar marcadores para mantener y volver a una posición determinada. Además, son la única forma de establecer el posicionamiento en todos los tipos de objetos <STRONG>Recordset</STRONG>.</P>


