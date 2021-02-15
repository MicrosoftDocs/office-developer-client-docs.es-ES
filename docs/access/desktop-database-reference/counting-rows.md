---
title: Recuento de filas (referencia de base de datos de escritorio de Access)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2388978185ac29149f7f15150ccfdbc559cc910f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295418"
---
# <a name="counting-rows"></a>Recuento de filas


**Se aplica a:** Access 2013, Office 2013

La propiedad **RecordCount** devuelve un valor **Long** que indica el número de registros del **Recordset**. Use la propiedad **RecordCount** para determinar cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o tipo de cursor no admite **RecordCount**. La lectura de la propiedad **RecordCount** de un **Recordset** cerrado causa un error.

La propiedad **RecordCount** depende de las capacidades del proveedor y del tipo de cursor. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves, y -1 o el recuento real para un cursor dinámico, en función del origen de datos.

El **Recordset** de ejemplo presentado en [Examinar datos](chapter-3-examining-data.md) devolverá –1 porque se abrió un cursor de sólo avance. Para usar la propiedad **RecordCount**, debería abrir el **Recordset** con un cursor más complejo (estático o conjunto de claves).

En algunos casos, puede que el proveedor o el cursor no puedan proporcionar el valor de **RecordCount** sin obtener primero todos los registros desde el origen de datos. Para forzar este tipo de búsqueda, llame al método **MoveLast** de **Recordset** antes de llamar a **RecordCount**

Si reemplazara la línea de código que llama al método **Open** de **Recordset** por lo siguiente:

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

podría utilizar la propiedad **RecordCount**, ya que los cursores estáticos del [Proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md) admiten **RecordCount**. Por ejemplo, el código siguiente imprimirá el número de registros devueltos por el comando a la ventana de depuración, suponiendo que el cursor admita la propiedad **RecordCount**:

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

A partir de este momento, se supone que se utilizan estas opciones más eficaces (pero más costosas) de tipo de cursor y bloqueo.

