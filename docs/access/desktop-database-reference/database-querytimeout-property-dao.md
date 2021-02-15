---
title: Propiedad Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294742"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="4ee9f-102">Propiedad Database.QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ee9f-102">Database.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="4ee9f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ee9f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4ee9f-104">Establece o devuelve un valor que especifica el número de segundos que se deben esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ee9f-105">Syntax</span></span>

<span data-ttu-id="4ee9f-106">*expresión* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="4ee9f-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="4ee9f-107">*expression* Variable que representa un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee9f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ee9f-108">Remarks</span></span>

<span data-ttu-id="4ee9f-109">El valor predeterminado es 60.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-109">The default value is 60.</span></span>

<span data-ttu-id="4ee9f-p101">Cuando se utiliza una base de datos ODBC, como Microsoft SQL Server, pueden producirse retrasos debido al tráfico de la red o al uso intensivo del servidor ODBC. En lugar de esperar indefinidamente, se puede especificar cuánto tiempo se desea esperar.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="4ee9f-p102">Cuando se utiliza **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, especifica un valor global para todas las consultas asociadas con la base de datos. Puede invalidar este valor para una consulta específica estableciendo la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** en particular.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="4ee9f-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ee9f-114">Example</span></span>

<span data-ttu-id="4ee9f-115">En este ejemplo se utilizan las propiedades **ODBCTimeout** y **QueryTimeout** para mostrar cómo el valor **QueryTimeout** en un objeto **Database** establece el valor **ODBCTimeout** predeterminado en cualquier objeto **QueryDef** creado desde un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

