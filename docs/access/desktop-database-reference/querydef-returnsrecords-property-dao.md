---
title: Propiedad QueryDef. ReturnsRecords (DAO)
TOCTitle: ReturnsRecords Property
ms:assetid: 3d1e538b-4d60-588f-4a20-89f1e2b434e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192701(v=office.15)
ms:contentKeyID: 48544334
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053005
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7d2202aa506750cd0a0d2a84eea5c507c3bb1147
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303342"
---
# <a name="querydefreturnsrecords-property-dao"></a><span data-ttu-id="786a1-102">Propiedad QueryDef. ReturnsRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="786a1-102">QueryDef.ReturnsRecords property (DAO)</span></span>

<span data-ttu-id="786a1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="786a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="786a1-104">Establece o devuelve un valor que indica si una consulta de paso a través SQL a una base de datos externa devuelve registros (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="786a1-104">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="786a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="786a1-105">Syntax</span></span>

<span data-ttu-id="786a1-106">*expresión* . ReturnsRecords</span><span class="sxs-lookup"><span data-stu-id="786a1-106">*expression* .ReturnsRecords</span></span>

<span data-ttu-id="786a1-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="786a1-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="786a1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="786a1-108">Remarks</span></span>

<span data-ttu-id="786a1-p101">No todas las consultas de paso a través SQL a bases de datos externas devuelven registros. Por ejemplo, una instrucción UPDATE SQL actualiza registros sin devolver registros, mientras que una instrucción SELECT SQL sí devuelve registros. Si la consulta devuelve registros, establezca la propiedad **ReturnsRecords** en **True**; si no devuelve registros, establezca la propiedad **ReturnsRecords** en **False**.</span><span class="sxs-lookup"><span data-stu-id="786a1-p101">Not all SQL pass-through queries to external databases return records. For example, an SQL UPDATE statement updates records without returning records, while an SQL SELECT statement does return records. If the query returns records, set the **ReturnsRecords** property to **True**; if the query doesn't return records, set the **ReturnsRecords** property to **False**.</span></span>

> [!NOTE]
> <span data-ttu-id="786a1-112">[!NOTA] Debe establecer la propiedad **[Connect](querydef-connect-property-dao.md)** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="786a1-112">You must set the **[Connect](querydef-connect-property-dao.md)** property before you set the **ReturnsRecords** property.</span></span>

## <a name="example"></a><span data-ttu-id="786a1-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="786a1-113">Example</span></span>

<span data-ttu-id="786a1-p102">En este ejemplo se utilizan las propiedades **Connect** y **ReturnsRecords** para seleccionar los cinco títulos de libros más vendidos de una base de datos de Microsoft SQL Server según los volúmenes de ventas de un año hasta la fecha. En el caso de una coincidencia exacta en los volúmenes de ventas, en el ejemplo se aumenta el tamaño de la lista que muestra los resultados de la consulta y se imprime un mensaje que explica lo ocurrido.</span><span class="sxs-lookup"><span data-stu-id="786a1-p102">This example uses the **Connect** and **ReturnsRecords** properties to select the top five book titles from a Microsoft SQL Server database based on year-to-date sales amounts. In the event of an exact match in sales amounts, the example increases the size of the list displaying the results of the query and prints a message explaining why this occurred.</span></span>

```vb 
Sub ClientServerX1() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTopFive As Recordset 
 Dim strMessage As String 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("AllTitles") 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles " & _ 
 "ORDER BY ytd_sales DESC" 
 qdfPassThrough.ReturnsRecords = True 
 
 ' Create a temporary QueryDef object to retrieve 
 ' data from the pass-through query. 
 Set qdfLocal = dbsCurrent.CreateQueryDef("") 
 qdfLocal.SQL = "SELECT TOP 5 title FROM AllTitles" 
 
 Set rstTopFive = qdfLocal.OpenRecordset() 
 
 ' Display results of queries. 
 With rstTopFive 
 strMessage = _ 
 "Our top 5 best-selling books are:" & vbCr 
 
 Do While Not .EOF 
 strMessage = strMessage & " " & !Title & _ 
 vbCr 
 .MoveNext 
 Loop 
 
 If .RecordCount > 5 Then 
 strMessage = strMessage & _ 
 "(There was a tie, resulting in " & _ 
 vbCr & .RecordCount & _ 
 " books in the list.)" 
 End If 
 
 MsgBox strMessage 
 .Close 
 End With 
 
 ' Delete new pass-through query because this is a 
 ' demonstration. 
 dbsCurrent.QueryDefs.Delete "AllTitles" 
 dbsCurrent.Close 
 
```

<br/>

<span data-ttu-id="786a1-116">En este ejemplo se usan la propiedad **ReturnsRecords** y la propiedad personalizada **LogMessages**para crear una consulta de paso a través que devolverá datos y los mensajes generados por el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="786a1-116">This example uses the **ReturnsRecords** property and the custom **LogMessages** property to create a pass-through query that will return data and any messages generated by the remote server.</span></span>

```vb 
Sub LogMessagesX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsCurrent As Database 
 Dim qdfTemp As QueryDef 
 Dim prpNew As Property 
 Dim rstTemp As Recordset 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 Set dbsCurrent = wrkAcc.OpenDatabase("DB1.mdb") 
 
 ' Create a QueryDef that will log any messages from the 
 ' server in temporary tables. 
 Set qdfTemp = dbsCurrent.CreateQueryDef("NewQueryDef") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfTemp.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfTemp.SQL = "SELECT * FROM stores" 
 qdfTemp.ReturnsRecords = True 
 Set prpNew = qdfTemp.CreateProperty("LogMessages", _ 
 dbBoolean, True) 
 qdfTemp.Properties.Append prpNew 
 
 ' Execute query and display results. 
 Set rstTemp = qdfTemp.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfTemp.Name 
 dbsCurrent.Close 
 wrkAcc.Close 
 
End Sub 
 
```

