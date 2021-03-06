---
title: Instrucción TRANSFORM (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: 9abe91d4ce6996a725e246da6922015d15a8bd39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314045"
---
# <a name="transform-statement-microsoft-access-sql"></a>Instrucción TRANSFORM (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea una consulta de tabla de referencias cruzadas.

## <a name="syntax"></a>Sintaxis

TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*valor1*\[, *valor2*\[, …\]\])\]

La instrucción TRANSFORM consta de las siguientes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>aggfunction</em></p></td>
<td><p><a href="sql-aggregate-functions-sql.md">Función de agregado de SQL</a> que opera sobre los datos seleccionados.</p></td>
</tr>
<tr class="even">
<td><p><em>selectstatement</em></p></td>
<td><p>Instrucción <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>pivotfield</em></p></td>
<td><p>Campo o expresión que desea usar para crear encabezados de columna en el conjunto de resultados de la consulta.</p></td>
</tr>
<tr class="even">
<td><p><em>valor1</em>, <em>valor2</em></p></td>
<td><p>Valores fijos que se usan para crear encabezados de columna.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Al resumir datos mediante una consulta de tabla de referencias cruzadas, selecciona valores en campos o expresiones especificados como encabezados de columna para poder ver los datos en un formato más compacto que con una consulta de selección.

TRANSFORM es opcional pero si se incluye, es la primera instrucción de una cadena SQL. Precede a una instrucción SELECT que especifica los campos usados como encabezados de fila y una cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) que especifica el agrupamiento de filas. Opcionalmente, puede incluir otras cláusulas, como [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), que especifican criterios adicionales de selección u ordenación. También puede usar subconsultas o predicados, específicamente los de la cláusula WHERE, en una consulta de tabla de referencias cruzadas.

Los valores devueltos en *campo_dinámico* se usan como encabezados de columna en el conjunto de resultados de la consulta. Por ejemplo, la creación de tablas de las cifras de ventas en el mes de la venta en una consulta de tabla de referencias cruzadas crearía 12 columnas. Puede restringir *campo_dinámico* para crear títulos a partir de los valores fijos (*valor1*, *valor2*) enumerados en la cláusula IN opcional. También puede incluir valores fijos para los que no hay datos para crear columnas adicionales.

## <a name="example"></a>Ejemplo

En este ejemplo, se utiliza la cláusula SQL TRANSFORM para crear una consulta de tabla de referencias cruzadas que muestra el número de pedidos obtenidos por cada empleado en cada trimestre de 1994. La función SQLTRANSFORMOutput es necesaria para ejecutar este procedimiento.

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

En este ejemplo, se utiliza la cláusula SQL TRANSFORM para crear una consulta de tabla de referencias cruzadas más compleja que muestre el importe total en dólares de los pedidos obtenidos por cada empleado en cada trimestre de 1994. La función SQLTRANSFORMOutput es necesaria para ejecutar este procedimiento.

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
