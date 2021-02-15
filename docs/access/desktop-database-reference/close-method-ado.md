---
title: 'Close (método): ActiveX data objects (ADO)'
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296314"
---
# <a name="close-method-ado"></a>Método Close (ADO)


**Se aplica a:** Access 2013, Office 2013

Cierra un objeto abierto y cualquier objeto dependiente.

## <a name="syntax"></a>Sintaxis

*object*.Close

## <a name="remarks"></a>Comentarios

Use el método **Close** para cerrar un objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) o [Stream](stream-object-ado.md) para liberar recursos del sistema asociado. Cerrar un objeto no lo quita de la memoria; puede cambiar su configuración de propiedad y abrirlo más tarde. Para eliminar completamente un objeto de la memoria, establezca la variable de objeto en *Nothing* (en Visual Basic) después de cerrar el objeto.

**Connection**

El uso del método **Close** para cerrar un objeto **Connection** también cierra cualquier objeto **Recordset** activo asociado con la conexión. Un objeto [Command](command-object-ado.md) asociado con el objeto **Connection** que está cerrando continuará, pero no se asociará con un objeto **Connection**; es decir, su propiedad [ActiveConnection](activeconnection-property-ado.md) se establecerá en **Nothing**. Además, la colección **Parameters** del objeto [Command](parameters-collection-ado.md) no tendrá ningún parámetro definido por el proveedor.

Luego puede llamar al método [Open](open-method-ado-connection.md) para restablecer la conexión al mismo o a otro origen de datos. Mientras que el objeto **Connection** está cerrado, llamar a cualquier método que requiere una conexión abierta al origen de datos genera un error.

Cerrar un objeto **Connection** mientras hay objetos **Recordset** abiertos en la conexión revierte cualquier cambio pendiente en todos los objetos **Recordset**. Cerrar explícitamente un objeto **Connection** (llamar al método **Close** ) mientras una transacción está en progreso genera un error. Si un objeto **Connection** se va de alcance mientras una transacción está en progreso, ADO automáticamente revierte la transacción.

**Recordset, Record, Stream**

El uso del método **Close** para cerrar un objeto **Recordset**, **Record** o **Stream** libera los datos asociados y cualquier acceso exclusivo que pudo haber tenido a los datos a través de este objeto particular. Puede luego llamar al método [Open](open-method-ado-recordset.md) para volver a abrir el objeto con los mismos atributos, o modificados.

Mientras un objeto **Recordset** está cerrado, llamar a cualquier método que requiera un cursor activo genera un error.

Si una modificación está en progreso en modo de actualización inmediata, llamar al método **Close** genera un error; en cambio, llame al método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md) primero. Si cierra el objeto **Recordset** en modo de actualización por lotes, se pierden todos los cambios desde la última llamada [UpdateBatch](updatebatch-method-ado.md).

Si usa el método [Clone](clone-method-ado.md) para crear copias de un objeto **Recordset** abierto, cerrar el original o el clon no afecta cualquier otra copia.

