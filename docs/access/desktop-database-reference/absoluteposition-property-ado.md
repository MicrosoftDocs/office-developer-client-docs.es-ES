---
title: Propiedad AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281980"
---
# <a name="absoluteposition-property-ado"></a>Propiedad AbsolutePosition (ADO)

**Se aplica a:** Access 2013, Office 2013

Indica la posición ordinal del registro actual de un objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de registros del objeto **Recordset** ([RecordCount](recordcount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Comentarios

Para establecer la **propiedad AbsolutePosition,** ADO requiere que el proveedor OLE DB que está usando implemente la interfaz IRowsetLocate.

Al obtener acceso a la propiedad **AbsolutePosition** de un objeto **Recordset** que se ha abierto con un cursor de sólo avance o un cursor dinámico, se genera el error **adErrFeatureNotAvailable**. Con otros tipos de cursor, se devolverá la posición correcta, siempre y cuando el proveedor admita la interfaz IRowsetScroll. Si el proveedor no admite la interfaz *IRowsetScroll*, el valor de la propiedad se establece en **adPosUnknown**. Vea la documentación de su proveedor para determinar si admite *IRowsetScroll*.

Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset** o para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.

Al igual que la propiedad [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Se puede obtener el número total de registros del objeto **Recordset** mediante la propiedad [RecordCount](recordcount-property-ado.md).

Al establecer la propiedad **AbsolutePosition,** incluso si se encuentra en un registro de la memoria caché actual, ADO vuelve a cargar la memoria caché con un nuevo grupo de registros a partir del registro especificado. La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.


> [!NOTE]
> [!NOTA] No es aconsejable usar la propiedad **AbsolutePosition** como número de registro suplente. La posición de un registro determinado cambia cuando se elimina un registro anterior. Tampoco hay ninguna garantía de que un registro determinado tendrá la misma **AbsolutePosition** si el objeto **Recordset** se vuelve a consultar o se vuelve a abrir. Los marcadores siguen siendo la forma recomendada de conservar y volver a una posición determinada, y son la única forma de colocarse en todos los tipos de **objetos Recordset.**


