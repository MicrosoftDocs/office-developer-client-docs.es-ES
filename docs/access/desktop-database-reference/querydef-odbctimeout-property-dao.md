---
title: QueryDef.ODBCTimeout Property (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dcb15511f3052366eb3d322c26cdd31d72c9beab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486440"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="5c299-102">QueryDef.ODBCTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c299-102">QueryDef.ODBCTimeout Property (DAO)</span></span>


<span data-ttu-id="5c299-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c299-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c299-104">Indica el número de segundos que hay que esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta **[QueryDef](querydef-object-dao.md)** en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="5c299-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c299-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c299-105">Syntax</span></span>

<span data-ttu-id="5c299-106">*expresión* . ODBCTimeout</span><span class="sxs-lookup"><span data-stu-id="5c299-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="5c299-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="5c299-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c299-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c299-108">Remarks</span></span>

<span data-ttu-id="5c299-p101">Cuando la propiedad **ODBCTimeout** está establecida en -1, el tiempo de espera establece el valor actual de la propiedad **[QueryTimeout](database-querytimeout-property-dao.md)** del objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)** que contiene **QueryDef**. Cuando la propiedad **ODBCTimeout** está establecida en 0, no se produce un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="5c299-p101">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**. When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="5c299-p102">Cuando esté utilizando una base de datos ODBC como, por ejemplo Microsoft SQL Server, pueden producirse demoras debido al tráfico en la red o a una sobrecarga en el servidor ODBC. En vez de esperar indefinidamente, puede especificar el tiempo de espera antes de que se devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="5c299-p102">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="5c299-113">Al establecer la propiedad **ODBCTimeout** de un objeto **QueryDef** se anula el valor especificado por la propiedad **QueryTimeout** del objeto **Connection** o **Database** que contiene **QueryDef**, pero únicamente para ese objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="5c299-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="5c299-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c299-114">Example</span></span>

<span data-ttu-id="5c299-115">En este ejemplo se utilizan las propiedades **ODBCTimeout** y **QueryTimeout** para mostrar cómo el valor **QueryTimeout** en un objeto **Database** establece el valor **ODBCTimeout** predeterminado en cualquier objeto **QueryDef** creado desde un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="5c299-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

