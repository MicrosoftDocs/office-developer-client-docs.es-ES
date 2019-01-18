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
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="8a658-102">Instrucción SELECT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8a658-102">SELECT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8a658-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a658-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="8a658-104">Indica al motor de base de datos de Microsoft Access que devuelva información de la base de datos como un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="8a658-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a658-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a658-105">Syntax</span></span>

<span data-ttu-id="8a658-106">Seleccione \[ *predicado* \] { \*  |  *tabla*.\*  |  \[ *tabla*. \] *campo1* \[AS *alias1* \] \[, \[ *tabla*. \] *field2* \[AS *alias2* \] \[,... \] \]} FROM *expresióndetabla* \[,... \] \[IN *basededatosexterna* \] \[donde...</span><span class="sxs-lookup"><span data-stu-id="8a658-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="8a658-107">\]\[GROUP BY …</span><span class="sxs-lookup"><span data-stu-id="8a658-107">\] \[GROUP BY…</span></span> <span data-ttu-id="8a658-108">\]\[HAVING …</span><span class="sxs-lookup"><span data-stu-id="8a658-108">\] \[HAVING…</span></span> <span data-ttu-id="8a658-109">\]\[ORDER BY...</span><span class="sxs-lookup"><span data-stu-id="8a658-109">\] \[ORDER BY…</span></span> <span data-ttu-id="8a658-110">\]\[Con OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="8a658-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="8a658-111">La instrucción SELECT consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8a658-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a658-112">Parte</span><span class="sxs-lookup"><span data-stu-id="8a658-112">Part</span></span></p></th>
<th><p><span data-ttu-id="8a658-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a658-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a658-114"><em>predicado</em></span><span class="sxs-lookup"><span data-stu-id="8a658-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-p102">Uno de los siguientes predicados: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW o TOP</a>. El predicado se usa para restringir el número de registros devueltos. Si no se especifica ninguno, el valor predeterminado es ALL.  </span><span class="sxs-lookup"><span data-stu-id="8a658-p102">One of the following predicates: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="8a658-118">Especifica que se seleccionen todos los campos de la tabla o tablas especificadas.</span><span class="sxs-lookup"><span data-stu-id="8a658-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a658-119"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="8a658-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-120">Nombre de la tabla que contiene los campos en los que se seleccionan registros.</span><span class="sxs-lookup"><span data-stu-id="8a658-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a658-121"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="8a658-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-p103">Nombres de los campos que contienen los datos que desea recuperar. Si incluye varios campos, éstos se recuperan en el orden enumerado.</span><span class="sxs-lookup"><span data-stu-id="8a658-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a658-124"><em>alias1</em>, <em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="8a658-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-125">Nombres que se usarán como encabezados de columna en lugar de los nombres de columna originales en <em>tabla</em>.</span><span class="sxs-lookup"><span data-stu-id="8a658-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a658-126"><em>expresiónDeTabla</em></span><span class="sxs-lookup"><span data-stu-id="8a658-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-127">Nombre de la tabla o tablas que contienen los datos que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="8a658-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a658-128"><em>baseDeDatosExterna</em></span><span class="sxs-lookup"><span data-stu-id="8a658-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="8a658-129">El nombre de la base de datos que contiene las tablas de <em>expresióndetabla</em> si no se encuentran en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="8a658-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8a658-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a658-130">Remarks</span></span>

<span data-ttu-id="8a658-131">Para realizar esta operación, el motor de base de datos de Microsoft Jet busca en la tabla o tablas especificadas, extrae las columnas elegidas, selecciona las filas que cumplen con el criterio y ordena o agrupa las filas resultantes en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="8a658-131">To perform this operation, the Microsoft Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="8a658-132">Las instrucciones SELECT no modifican los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a658-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="8a658-p104">SELECT suele ser la primera palabra de una instrucción SQL. La mayoría de las instrucciones SQL son instrucciones SELECT o [SELECT…INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="8a658-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="8a658-135">La sintaxis mínima de una instrucción SELECT es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8a658-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="8a658-136">SELECT *campos* FROM *tabla*</span><span class="sxs-lookup"><span data-stu-id="8a658-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="8a658-p105">Puede usar un asterisco (\*) para seleccionar todos los campos de una tabla. En el siguiente ejemplo, se seleccionan todos los campos de la tabla Employees:</span><span class="sxs-lookup"><span data-stu-id="8a658-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="8a658-p106">Si un nombre de campo está incluido en más de una tabla en la cláusula FROM, debe ir precedido por el nombre de la tabla y el operador **.** (punto). En el siguiente ejemplo, el campo Department se encuentra la tabla Employees y la tabla Supervisors. La instrucción SQL selecciona los departamentos de la tabla Employees y los nombres de los supervisores de la tabla Supervisors:</span><span class="sxs-lookup"><span data-stu-id="8a658-p106">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.** (dot) operator. In the following example, the Department field is in both the Employees table and the Supervisors table. The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="8a658-p107">Cuando se crea un objeto **Recordset**, el motor de base de datos Microsoft Jet usa el nombre de campo de la tabla como el nombre de objeto **Field** en el objeto **Recordset**. Si desea un nombre de campo diferente o no hay un nombre implícito en la expresión usada para generar el campo, use la palabra reservada AS. En el siguiente ejemplo, se usa el título Birth para nombrar el objeto **Field** devuelto en el objeto **Recordset** resultante:</span><span class="sxs-lookup"><span data-stu-id="8a658-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="8a658-p108">Si se usan funciones de agregado o consultas que devuelven nombres de objeto **Field** ambiguos o duplicados, debe usar la cláusula AS para proporcionar un nombre alternativo para el objeto **Field**. En el siguiente ejemplo, se usa el título HeadCount para nombrar el objeto **Field** devuelto en el objeto **Recordset** resultante:</span><span class="sxs-lookup"><span data-stu-id="8a658-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="8a658-p109">Puede usar las demás cláusulas de una instrucción SELECT para restringir y organizar los datos devueltos. Para obtener más información, vea el tema de Ayuda acerca de la cláusula que utilice.</span><span class="sxs-lookup"><span data-stu-id="8a658-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="8a658-150">**Vínculos proporcionados por** la comunidad de [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="8a658-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="8a658-151">UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8a658-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="8a658-152">Formateador de SQL a VBA</span><span class="sxs-lookup"><span data-stu-id="8a658-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="8a658-153">Ver registros en un intervalo definido</span><span class="sxs-lookup"><span data-stu-id="8a658-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="8a658-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a658-154">Example</span></span>

<span data-ttu-id="8a658-p111">En algunos de los ejemplos siguientes, se supone la existencia de un campo hipotético Salary en una tabla Employees. Tenga en cuenta que este campo no existe realmente en la tabla Employees (Empleados) de la base de datos Northwind (Neptuno).</span><span class="sxs-lookup"><span data-stu-id="8a658-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="8a658-p112">En este ejemplo, se crea un objeto **Recordset** de tipo Dynaset basado en una instrucción SQL que selecciona los campos Apellidos y Nombre de todos los registros de la tabla Empleados. Llama al procedimiento EnumFields, que imprime el contenido de un objeto **Recordset** en la ventana **Depuración**.</span><span class="sxs-lookup"><span data-stu-id="8a658-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

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

<span data-ttu-id="8a658-159">En este ejemplo, se cuenta el número de registros que tienen una entrada en el campo PostalCode y asigna al campo devuelto el nombre Tally.</span><span class="sxs-lookup"><span data-stu-id="8a658-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

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

<span data-ttu-id="8a658-160">En este ejemplo, se muestra el número de empleados y los salarios medio y máximo.</span><span class="sxs-lookup"><span data-stu-id="8a658-160">This example shows the number of employees and the average and maximum salaries.</span></span>

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

<span data-ttu-id="8a658-p113">Se pasa un objeto **Recordset** al procedimiento **Sub** EnumFields desde el procedimiento que realiza la llamada. Después, el procedimiento da formato a los campos de **Recordset** y los imprime en la ventana **Depuración**. La variable es el ancho del campo impreso deseado. Algunos campos pueden estar truncados.</span><span class="sxs-lookup"><span data-stu-id="8a658-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

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




