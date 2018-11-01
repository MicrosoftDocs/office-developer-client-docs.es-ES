---
title: Declaración PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS Declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 24212ce3a29c0e30fae1dad7566ef93815f8a03f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876782"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="ce109-102">Declaración PARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ce109-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="ce109-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce109-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce109-104">Declara el nombre y tipo de datos de cada parámetro de una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce109-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce109-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce109-105">Syntax</span></span>

<span data-ttu-id="ce109-106">PARAMETERS *nombre tipodedatos* \[, *nombre tipodedatos* \[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="ce109-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="ce109-107">La instrucción PARAMETERS consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ce109-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce109-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce109-108">Part</span></span></p></th>
<th><p><span data-ttu-id="ce109-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce109-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce109-110"><em>nombre</em></span><span class="sxs-lookup"><span data-stu-id="ce109-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="ce109-111">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="ce109-111">The name of the parameter.</span></span> <span data-ttu-id="ce109-112">Se asigna a la propiedad <strong>Name</strong> del objeto <strong>Parameter</strong> y se usa para identificar este parámetro en la colección <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce109-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="ce109-113">Puede usar <em>nombre</em> como una cadena que se muestra en un cuadro de diálogo mientras la aplicación ejecuta la consulta.</span><span class="sxs-lookup"><span data-stu-id="ce109-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="ce109-114">Use corchetes ([ ]) para incluir el texto que contenga espacios o signos de puntuación.</span><span class="sxs-lookup"><span data-stu-id="ce109-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="ce109-115">Por ejemplo, [precio bajo] y [empezar informe con qué month?] son argumentos válidos de <em>nombre</em> .</span><span class="sxs-lookup"><span data-stu-id="ce109-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce109-116"><em>tipoDeDatos</em></span><span class="sxs-lookup"><span data-stu-id="ce109-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="ce109-117">Uno de los principales <a href="sql-data-types.md">tipos de datos de Microsoft Access SQL</a> o sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="ce109-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ce109-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce109-118">Remarks</span></span>

<span data-ttu-id="ce109-p102">Para consultas que se ejecuten habitualmente, puede usar una declaración PARAMETERS para crear una consulta de parámetros. Una consulta de parámetros puede ayudar a automatizar el proceso de cambio de los criterios de la consulta. Con una consulta de parámetros, deberán proporcionarse los parámetros en el código cada vez que se ejecute la consulta.</span><span class="sxs-lookup"><span data-stu-id="ce109-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="ce109-122">La declaración PARAMETERS es opcional pero si se incluye, va delante de cualquier otra instrucción, incluida la instrucción [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ce109-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="ce109-p103">Si la declaración incluye varios parámetros, sepárelos mediante comas. En el siguiente ejemplo, se incluyen dos parámetros:</span><span class="sxs-lookup"><span data-stu-id="ce109-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="ce109-125">Puede usar *nombre* pero no *tipoDeDatos* en una cláusula [donde](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) o [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="ce109-125">You can use *name* but not *datatype* in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause.</span></span> <span data-ttu-id="ce109-126">En el siguiente ejemplo, se espera que se proporcionen dos parámetros y, después, se aplican los criterios a los registros de la tabla Orders:</span><span class="sxs-lookup"><span data-stu-id="ce109-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="ce109-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce109-127">Example</span></span>

<span data-ttu-id="ce109-128">Este ejemplo requiere que el usuario proporcione un puesto y lo use como criterios para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ce109-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="ce109-129">Este ejemplo llama al procedimiento EnumFields, que encontrará en el ejemplo de [instrucción SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ce109-129">This example calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
