---
title: 'Capítulo 4: Edición de datos'
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b954cf8b730a74fb7e630fbafb96c046491c6f46
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701147"
---
# <a name="chapter-4-editing-data"></a>Capítulo 4: Edición de datos

**Se aplica a**: Access 2013, Office 2013

En los dos capítulos anteriores, se explicaba cómo utilizar ADO para conectarse a un origen de datos, ejecutar un comando, obtener los resultados en un objeto **Recordset** y desplazarse dentro del **conjunto de registros**. Este capítulo se centra en la siguiente operación fundamental de ADO: la edición de datos.

En este capítulo, se sigue utilizando el **conjunto de registros** de ejemplo introducido en el capítulo 3 (con un cambio importante). El código siguiente se utiliza para abrir el **conjunto de registros**:

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

El cambio importante en el código consiste en establecer la propiedad **CursorLocation** del objeto **Connection** en **adUseClient** en la función GetNewConnection (que se muestra a continuación), lo que indica el uso de un cursor de cliente. Para obtener más información acerca de las diferencias entre cursores de cliente y de servidor, vea el [Capítulo 8: Cursores y bloqueos](chapter-8-understanding-cursors-and-locks.md).

El valor **adUseClient** de la propiedad **CursorLocation** mueve la ubicación del cursor desde el origen de datos (SQL Server en este caso) a la ubicación del código de cliente (la estación de trabajo de escritorio). Esta configuración obliga a ADO a invocar el Client Cursor Engine para OLE DB en el cliente para crear y administrar el cursor.

Es posible que también haya observado que el parámetro **LockType** del método **Open** se ha cambiado a **adLockBatchOptimistic**. De este modo, el cursor se abre en modo de proceso por lotes (el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente cuando se llama al método **UpdateBatch** ). Los cambios realizados en el **conjunto de registros** no se actualizarán en la base de datos hasta que se llame al método **UpdateBatch**.

Por último, el código de este capítulo utiliza una versión modificada de la función GetNewConnection, que se presentó en el capítulo 2. Esta versión de la función devuelve ahora un cursor de cliente. La función tiene la forma:

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

En este capítulo, se tratan los temas siguientes:

- [Edición de registros existentes](editing-existing-records.md)
- [Determinación de lo que es compatible](determining-what-is-supported.md)
- [Eliminación de registros utilizando el método Delete](deleting-records-using-the-delete-method.md)
- [Alternativas: utilizar instrucciones SQL](alternatives-using-sql-statements.md)
- [Adición de registros (ADO)](adding-records.md)
