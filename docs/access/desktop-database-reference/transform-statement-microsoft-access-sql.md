---
title: TRANSFORMACIÓN de instrucción (Microsoft Access SQL)
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 16b88f2cf441802c6246425d5bb7bb2efb71a679
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861221"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="0ac16-102">TRANSFORMACIÓN de instrucción (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0ac16-102">TRANSFORM statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="0ac16-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ac16-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0ac16-104">Crea una consulta de tabla de referencias cruzadas.</span><span class="sxs-lookup"><span data-stu-id="0ac16-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ac16-105">Syntax</span></span>

<span data-ttu-id="0ac16-106">TRANSFORM *funcióndeagregadoinstrucciónselect* PIVOT *pivotfield* \[IN (*valor1*\[, *valor2*\[,... \]\])\]</span><span class="sxs-lookup"><span data-stu-id="0ac16-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="0ac16-107">La instrucción TRANSFORM consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ac16-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ac16-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ac16-108">Part</span></span></p></th>
<th><p><span data-ttu-id="0ac16-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ac16-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ac16-110"><em>funciónDeAgregado</em></span><span class="sxs-lookup"><span data-stu-id="0ac16-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="0ac16-111"><a href="sql-aggregate-functions-sql.md">Función de agregado de SQL</a> que opera sobre los datos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="0ac16-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac16-112"><em>instrucciónSelect</em></span><span class="sxs-lookup"><span data-stu-id="0ac16-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="0ac16-113">Instrucción <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="0ac16-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac16-114"><em>campoDeTablaDinámica</em></span><span class="sxs-lookup"><span data-stu-id="0ac16-114"><em>pivotfield</em></span></span></p></td>
<td><p><span data-ttu-id="0ac16-115">Campo o expresión que desea usar para crear encabezados de columna en el conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="0ac16-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac16-116"><em>valor1</em>, <em>valor2</em></span><span class="sxs-lookup"><span data-stu-id="0ac16-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="0ac16-117">Valores fijos que se usan para crear encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="0ac16-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="0ac16-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ac16-118">Remarks</span></span>

<span data-ttu-id="0ac16-119">Al resumir datos mediante una consulta de tabla de referencias cruzadas, selecciona valores en campos o expresiones especificados como encabezados de columna para poder ver los datos en un formato más compacto que con una consulta de selección.</span><span class="sxs-lookup"><span data-stu-id="0ac16-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="0ac16-p101">TRANSFORM es opcional pero si se incluye, es la primera instrucción de una cadena SQL. Precede a una instrucción SELECT que especifica los campos usados como encabezados de fila y una cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) que especifica el agrupamiento de filas. Opcionalmente, puede incluir otras cláusulas, como [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), que especifican criterios adicionales de selección u ordenación. También puede usar subconsultas o predicados, específicamente los de la cláusula WHERE, en una consulta de tabla de referencias cruzadas.</span><span class="sxs-lookup"><span data-stu-id="0ac16-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="0ac16-p102">Los valores devueltos en *campoDeTablaDinámica* se usan como encabezados de columna en el conjunto de resultados de la consulta. Por ejemplo, si se crea un campo de tabla dinámica con las cifras de ventas por el mes de la venta en una consulta de tabla de referencias cruzadas, se generarían 12 columnas. Puede restringir *campoDeTablaDinámica* para crear encabezados a partir de los valores fijos (*valor1*, *valor2*) enumerados en la cláusula IN opcional. También puede incluir valores fijos para los que no existen datos para crear columnas adicionales.</span><span class="sxs-lookup"><span data-stu-id="0ac16-p102">The values returned in *pivotfield* are used as column headings in the query's result set. For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns. You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause. You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="0ac16-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ac16-128">Example</span></span>

<span data-ttu-id="0ac16-p103">En este ejemplo, se utiliza la cláusula SQL TRANSFORM para crear una consulta de tabla de referencias cruzadas que muestra el número de pedidos obtenidos por cada empleado en cada trimestre de 1994. La función SQLTRANSFORMOutput es necesaria para ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0ac16-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="0ac16-p104">En este ejemplo, se utiliza la cláusula SQL TRANSFORM para crear una consulta de tabla de referencias cruzadas más compleja que muestre el importe total en dólares de los pedidos obtenidos por cada empleado en cada trimestre de 1994. La función SQLTRANSFORMOutput es necesaria para ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0ac16-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```
