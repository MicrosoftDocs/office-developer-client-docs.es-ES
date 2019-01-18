---
title: MoveFirst, MoveLast, MoveNext y MovePrevious (métodos, ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cb6ea7f82ac37460d7f2a4dd998ae7435c04230
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704129"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a>MoveFirst, MoveLast, MoveNext y MovePrevious (métodos, ADO)


**Se aplica a**: Access 2013, Office 2013

Se desplaza al registro primero, último, siguiente o anterior en el objeto [Recordset](recordset-object-ado.md) especificado y convierte ese registro en el registro actual.

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. { Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="remarks"></a>Comentarios

Utilice el método **MoveFirst** para mover la posición de registro actual al primer registro del objeto **Recordset**.

Utilice el método **MoveLast** para mover la posición de registro actual al último registro del objeto **Recordset**. El objeto **Recordset** debe admitir marcadores o movimientos de cursor hacia atrás; en caso contrario, la llamada a este método generará un error.

Si se llama a **MoveFirst** o **MoveLast** cuando el objeto **Recordset** está vacío (el valor de **BOF** y de **EOF** es True), se generará un error.

Utilice el método **MoveNext** para avanzar un registro la posición de registro actual (hacia el final del objeto **Recordset**). Si el último registro es el registro actual y se llama al método **MoveNext**, ADO establece el registro actual en la posición situada detrás del último registro del objeto **Recordset** ([EOF](bof-eof-properties-ado.md) es **True**). Si el valor de la propiedad **EOF** ya es **True**, cualquier intento de avanzar genera un error.

En casos en los que se filtra u ordena el **conjunto de registros** y se cambian los datos del registro activo, es posible que también cambie la posición. En tales casos la **MoveNext** método funciona normalmente, pero debe tener en cuenta que la posición se encuentra uno que se ha movido registro con respecto a la nueva posición, no respecto a la antigua. Por ejemplo, cambiando los datos en el registro actual, de modo que el registro se desplaza hasta el final del **objeto Recordset,** ordenada significa que la llamada a **MoveNext** provocará que ADO si se establece el registro actual en la posición después del último registro en el ** Conjunto de registros** (**EOF** = **es True**).

Use el método **MovePrevious** para retroceder un registro la posición de registro actual (hacia el principio del objeto **Recordset**). El objeto **Recordset** debe admitir marcadores o movimientos de cursor hacia atrás; en caso contrario, la llamada al método generará un error. Si el primer registro es el registro actual y se llama al método **MovePrevious**, ADO establece el registro actual en la posición situada delante del primer registro del objeto **Recordset** (el valor de [BOF](bof-eof-properties-ado.md) es **True**). Cualquier intento de retroceder cuando el valor de **BOF** ya es **True** genera un error. Si el objeto **Recordset** no admite marcadores o movimientos de cursor hacia atrás, el método **MovePrevious** generará un error.

Si el objeto **Recordset** es de solo avance y desea poder realizar desplazamientos tanto hacia adelante como hacia atrás, podrá usar la propiedad [CacheSize](cachesize-property-ado.md) para crear una memoria caché de registros que admita movimientos de cursor hacia atrás mediante el método [Move](move-method-ado.md). Dado que los registros almacenados en caché se cargan en la memoria, deberá evitar almacenar en caché un número excesivo de registros. Puede llamar al método **MoveFirst** en un objeto **Recordset** de solo avance; si lo hace, puede que el proveedor vuelva a ejecutar el comando que generó el objeto **Recordset**.

