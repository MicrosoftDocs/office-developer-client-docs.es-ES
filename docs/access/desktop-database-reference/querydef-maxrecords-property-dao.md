---
title: Propiedad QueryDef.MaxRecords (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5893dd0c6538a1812dc9b19aede2b9114899d68c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927131"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="65ea8-102">Propiedad QueryDef.MaxRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="65ea8-102">QueryDef.MaxRecords property (DAO)</span></span>


<span data-ttu-id="65ea8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65ea8-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="65ea8-104">Establece o devuelve el número máximo de registros que se devuelven desde una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="65ea8-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ea8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65ea8-105">Syntax</span></span>

<span data-ttu-id="65ea8-106">*expresión* . Número máximo de registros</span><span class="sxs-lookup"><span data-stu-id="65ea8-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="65ea8-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="65ea8-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ea8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65ea8-108">Remarks</span></span>

<span data-ttu-id="65ea8-109">El valor predeterminado es 0, lo que indica que no hay límite en el número de registros devueltos.</span><span class="sxs-lookup"><span data-stu-id="65ea8-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="65ea8-p101">Una vez que el número de filas especificado por **MaxRecords** se devuelve a la aplicación del usuario en un **[Recordset](recordset-object-dao.md)**, el procesador de consultas dejará de devolver registros adicionales incluso si hay más registros cualificados para su inclusión en **Recordset**. Esta propiedad es útil en situaciones donde los recursos de cliente limitados prohíben la administración de grandes cantidades de registros.</span><span class="sxs-lookup"><span data-stu-id="65ea8-p101">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**. This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>


> [!NOTE]
> <P><span data-ttu-id="65ea8-112">[!NOTA] La propiedad <STRONG>MaxRecords</STRONG> sólo se puede usar con un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="65ea8-112">The <STRONG>MaxRecords</STRONG> property can only be used with an ODBC data source.</span></span></P>



## <a name="example"></a><span data-ttu-id="65ea8-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65ea8-113">Example</span></span>

<span data-ttu-id="65ea8-114">En este ejemplo se utiliza la propiedad **MaxRecords** para establecer un límite sobre el número de registros que devuelve una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="65ea8-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

