---
title: 'Capítulo 4: Modificar datos'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c5364a7b9e70c4627a7f5b4e6708542e2c8516f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485078"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="0cd43-102">Capítulo 4: Modificar datos</span><span class="sxs-lookup"><span data-stu-id="0cd43-102">Chapter 4: Editing Data</span></span>


<span data-ttu-id="0cd43-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cd43-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cd43-p101">En los dos capítulos anteriores, se explicaba cómo utilizar ADO para conectarse a un origen de datos, ejecutar un comando, obtener los resultados en un objeto **Recordset** y desplazarse dentro del **conjunto de registros**. Este capítulo se centra en la siguiente operación fundamental de ADO: la edición de datos.</span><span class="sxs-lookup"><span data-stu-id="0cd43-p101">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**. This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="0cd43-p102">En este capítulo, se sigue utilizando el **conjunto de registros** de ejemplo introducido en el capítulo 3 (con un cambio importante). El código siguiente se utiliza para abrir el **conjunto de registros**:</span><span class="sxs-lookup"><span data-stu-id="0cd43-p102">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change. The following code is used to open the **Recordset**:</span></span>

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

<span data-ttu-id="0cd43-p103">El cambio importante en el código consiste en establecer la propiedad **CursorLocation** del objeto **Connection** en **adUseClient** en la función GetNewConnection (que se muestra a continuación), lo que indica el uso de un cursor de cliente. Para obtener más información acerca de las diferencias entre cursores de cliente y de servidor, vea el [Capítulo 8: Cursores y bloqueos](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="0cd43-p103">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor. For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="0cd43-p104">El valor **adUseClient** de la propiedad **CursorLocation** mueve la ubicación del cursor desde el origen de datos (SQL Server en este caso) a la ubicación del código de cliente (la estación de trabajo de escritorio). Esta configuración obliga a ADO a invocar el Client Cursor Engine para OLE DB en el cliente para crear y administrar el cursor.</span><span class="sxs-lookup"><span data-stu-id="0cd43-p104">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation). This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="0cd43-p105">Es posible que también haya observado que el parámetro **LockType** del método **Open** se ha cambiado a **adLockBatchOptimistic**. De este modo, el cursor se abre en modo de proceso por lotes (el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente cuando se llama al método **UpdateBatch** ). Los cambios realizados en el **conjunto de registros** no se actualizarán en la base de datos hasta que se llame al método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="0cd43-p105">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**. This opens the cursor in batch mode. (The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="0cd43-p106">Por último, el código de este capítulo utiliza una versión modificada de la función GetNewConnection, que se presentó en el capítulo 2. Esta versión de la función devuelve ahora un cursor de cliente. La función tiene la forma:</span><span class="sxs-lookup"><span data-stu-id="0cd43-p106">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2. This version of the function now returns a client-side cursor. The function looks like this:</span></span>

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

