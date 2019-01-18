---
title: Instrucción SELECT (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: 962e425c2c69511b6d7770fb03e954588249cf2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718787"
---
# <a name="select-statement-microsoft-access-sql"></a>Instrucción SELECT (Microsoft Access SQL)

**Se aplica a:** Access 2013 | Office 2013

Indica al motor de base de datos de Microsoft Access que devuelva información de la base de datos como un conjunto de registros.

## <a name="syntax"></a>Sintaxis

Seleccione \[ *predicado* \] { \*  |  *tabla*.\*  |  \[ *tabla*. \] *campo1* \[AS *alias1* \] \[, \[ *tabla*. \] *field2* \[AS *alias2* \] \[,... \] \]} FROM *expresióndetabla* \[,... \] \[IN *basededatosexterna* \] \[donde... \]\[GROUP BY … \]\[HAVING … \]\[ORDER BY... \]\[Con OWNERACCESS OPTION\]

La instrucción SELECT consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>predicado</em></p></td>
<td><p>Uno de los siguientes predicados: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW o TOP</a>. El predicado se usa para restringir el número de registros devueltos. Si no se especifica ninguno, el valor predeterminado es ALL.  </p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Especifica que se seleccionen todos los campos de la tabla o tablas especificadas.</p></td>
</tr>
<tr class="odd">
<td><p><em>tabla</em></p></td>
<td><p>Nombre de la tabla que contiene los campos en los que se seleccionan registros.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nombres de los campos que contienen los datos que desea recuperar. Si incluye varios campos, éstos se recuperan en el orden enumerado.</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>, <em>alias2</em></p></td>
<td><p>Nombres que se usarán como encabezados de columna en lugar de los nombres de columna originales en <em>tabla</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>expresiónDeTabla</em></p></td>
<td><p>Nombre de la tabla o tablas que contienen los datos que desea recuperar.</p></td>
</tr>
<tr class="odd">
<td><p><em>baseDeDatosExterna</em></p></td>
<td><p>El nombre de la base de datos que contiene las tablas de <em>expresióndetabla</em> si no se encuentran en la base de datos actual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Para realizar esta operación, el motor de base de datos de Microsoft Jet busca en la tabla o tablas especificadas, extrae las columnas elegidas, selecciona las filas que cumplen con el criterio y ordena o agrupa las filas resultantes en el orden especificado.

Las instrucciones SELECT no modifican los datos de la base de datos.

SELECT suele ser la primera palabra de una instrucción SQL. La mayoría de las instrucciones SQL son instrucciones SELECT o [SELECT…INTO](select-into-statement-microsoft-access-sql.md).

La sintaxis mínima de una instrucción SELECT es la siguiente:

SELECT *campos* FROM *tabla*

Puede usar un asterisco (\*) para seleccionar todos los campos de una tabla. En el siguiente ejemplo, se seleccionan todos los campos de la tabla Employees:

```sql
SELECT * FROM Employees;
```

Si un nombre de campo está incluido en más de una tabla en la cláusula FROM, debe ir precedido por el nombre de la tabla y el operador **.** (punto). En el siguiente ejemplo, el campo Department se encuentra la tabla Employees y la tabla Supervisors. La instrucción SQL selecciona los departamentos de la tabla Employees y los nombres de los supervisores de la tabla Supervisors:

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

Cuando se crea un objeto **Recordset**, el motor de base de datos Microsoft Jet usa el nombre de campo de la tabla como el nombre de objeto **Field** en el objeto **Recordset**. Si desea un nombre de campo diferente o no hay un nombre implícito en la expresión usada para generar el campo, use la palabra reservada AS. En el siguiente ejemplo, se usa el título Birth para nombrar el objeto **Field** devuelto en el objeto **Recordset** resultante:

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

Si se usan funciones de agregado o consultas que devuelven nombres de objeto **Field** ambiguos o duplicados, debe usar la cláusula AS para proporcionar un nombre alternativo para el objeto **Field**. En el siguiente ejemplo, se usa el título HeadCount para nombrar el objeto **Field** devuelto en el objeto **Recordset** resultante:

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Puede usar las demás cláusulas de una instrucción SELECT para restringir y organizar los datos devueltos. Para obtener más información, vea el tema de Ayuda acerca de la cláusula que utilice.

**Vínculos proporcionados por** la comunidad de [UtterAccess](https://www.utteraccess.com). UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.

- [Formateador de SQL a VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Ver registros en un intervalo definido](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Ejemplo

En algunos de los ejemplos siguientes, se supone la existencia de un campo hipotético Salary en una tabla Employees. Tenga en cuenta que este campo no existe realmente en la tabla Employees (Empleados) de la base de datos Northwind (Neptuno).

En este ejemplo, se crea un objeto **Recordset** de tipo Dynaset basado en una instrucción SQL que selecciona los campos Apellidos y Nombre de todos los registros de la tabla Empleados. Llama al procedimiento EnumFields, que imprime el contenido de un objeto **Recordset** en la ventana **Depuración**.

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<br/>

En este ejemplo, se cuenta el número de registros que tienen una entrada en el campo PostalCode y asigna al campo devuelto el nombre Tally.

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<br/>

En este ejemplo, se muestra el número de empleados y los salarios medio y máximo.

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Se pasa un objeto **Recordset** al procedimiento **Sub** EnumFields desde el procedimiento que realiza la llamada. Después, el procedimiento da formato a los campos de **Recordset** y los imprime en la ventana **Depuración**. La variable es el ancho del campo impreso deseado. Algunos campos pueden estar truncados.

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




