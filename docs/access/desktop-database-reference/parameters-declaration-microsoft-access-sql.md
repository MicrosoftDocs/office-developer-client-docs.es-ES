---
title: Declaración PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: d78a6c043e99af1ca50ca798b94088400fd09f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287870"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>Declaración PARAMETERS (Microsoft Access SQL)


**Se aplica a:** Access 2013, Office 2013

Declara el nombre y tipo de datos de cada parámetro de una consulta de parámetros.

## <a name="syntax"></a>Sintaxis

PARAMETERS *nombre tipoDeDatos*\[, *nombre tipoDeDatos*\[, ...\]\]

La instrucción PARAMETERS consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>name</em></p></td>
<td><p>Nombre del parámetro. Se asigna a la propiedad <strong>Name</strong> del objeto <strong>Parameter</strong> y se usa para identificar este parámetro en la colección <strong>Parameters</strong>. Puede usar <em>nombre</em> como una cadena que se muestre en un cuadro de diálogo mientras la aplicación ejecuta la consulta. Use corchetes ([ ]) para incluir el texto que contenga espacios o signos de puntuación. Por ejemplo, [Precio inferior] y [¿Con qué mes debe comenzar el informe?] son argumentos <em>nombre</em> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>tipo_datos</em></p></td>
<td><p>Uno de los principales <a href="sql-data-types.md">tipos de datos de Microsoft Access SQL</a> o sus sinónimos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Para consultas que se ejecuten habitualmente, puede usar una declaración PARAMETERS para crear una consulta de parámetros. Una consulta de parámetros puede ayudar a automatizar el proceso de cambio de los criterios de la consulta. Con una consulta de parámetros, deberán proporcionarse los parámetros en el código cada vez que se ejecute la consulta.

La declaración PARAMETERS es opcional pero si se incluye, va delante de cualquier otra instrucción, incluida la instrucción [SELECT](select-statement-microsoft-access-sql.md).

Si la declaración incluye varios parámetros, sepárelos mediante comas. En el siguiente ejemplo, se incluyen dos parámetros:

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

Puede usar *nombre* pero no *tipoDeDatos* en una cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) o [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql). En el siguiente ejemplo, se espera que se proporcionen dos parámetros y, después, se aplican los criterios a los registros de la tabla Orders:

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Ejemplo

Este ejemplo requiere que el usuario proporcione un puesto y lo use como criterio para la búsqueda.

Se llama al procedimiento EnumFields, que se incluye en el ejemplo de la [instrucción SELECT](select-statement-microsoft-access-sql.md).

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
