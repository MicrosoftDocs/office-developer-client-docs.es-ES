---
title: Recordset.Seek (método) (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: db2c90d42feacee58af9eea30a2d99439cb4ddaf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708896"
---
# <a name="recordsetseek-method-dao"></a><span data-ttu-id="63557-102">Recordset.Seek (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="63557-102">Recordset.Seek method (DAO)</span></span>

<span data-ttu-id="63557-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63557-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63557-104">Busca el registro en un objeto **Recordset** de tipo tabla indizada que satisface los criterios especificados para el índice activo y hace de este registro el registro activo (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="63557-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="63557-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63557-105">Syntax</span></span>

<span data-ttu-id="63557-106">*expresión* . Seek (***comparación***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="63557-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="63557-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="63557-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="63557-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63557-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63557-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="63557-109">Name</span></span></p></th>
<th><p><span data-ttu-id="63557-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="63557-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="63557-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63557-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="63557-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="63557-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63557-113"><em>Comparison</em></span><span class="sxs-lookup"><span data-stu-id="63557-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="63557-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="63557-114">Required</span></span></p></td>
<td><p><span data-ttu-id="63557-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="63557-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="63557-116">Una de las siguientes expresiones de cadena: &lt;, &lt;=, =, &gt;=, o &gt;.</span><span class="sxs-lookup"><span data-stu-id="63557-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63557-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="63557-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="63557-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="63557-118">Required</span></span></p></td>
<td><p><span data-ttu-id="63557-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63557-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63557-120">Uno o más valores correspondientes a campos en el índice actual del objeto <strong>Recordset</strong>, según lo especificado por su configuración de propiedad <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="63557-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="63557-121">Puede utilizar hasta 13 argumentos key.</span><span class="sxs-lookup"><span data-stu-id="63557-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63557-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63557-122">Remarks</span></span>

<span data-ttu-id="63557-p102">Debe establecer el índice activo con la propiedad **Index** antes de utilizar **Seek**. Si el índice identifica un campo clave no único, **Seek** localiza el primer registro que satisface los criterios.</span><span class="sxs-lookup"><span data-stu-id="63557-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="63557-125">El método **Seek** busca en los campos clave especificados y localiza el primer registro que satisface los criterios indicados por comparison y key1.</span><span class="sxs-lookup"><span data-stu-id="63557-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="63557-126">Una vez encontrado, hace del registro el registro activo y establece la propiedad **NoMatch** en **False**.</span><span class="sxs-lookup"><span data-stu-id="63557-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="63557-127">Si el método **Seek** no consigue encontrar coincidencias, la propiedad **NoMatch** se establece en **True** y el registro activo es indefinido.</span><span class="sxs-lookup"><span data-stu-id="63557-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="63557-128">Si comparison es igual (=), mayor o igual (\>=), o mayor que (\>), **Seek** comienza al principio del índice y busca hacia delante.</span><span class="sxs-lookup"><span data-stu-id="63557-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="63557-129">Si comparison es menor que (\<) o menor o igual (\<=), **Seek** comienza por el final del índice y busca hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="63557-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="63557-130">No obstante, si hay entradas de índice duplicadas al final del éste, **Seek** comienza en una entrada arbitraria entre las duplicadas y busca hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="63557-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="63557-131">Debe especificar valores para todos los campos definidos en el índice.</span><span class="sxs-lookup"><span data-stu-id="63557-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="63557-132">Si utiliza **Seek** con un índice de varias columnas y no especifica un valor de comparación para cada campo del índice, no puede utilizar el operador igual (=) en la comparación.</span><span class="sxs-lookup"><span data-stu-id="63557-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="63557-133">Que es debido a que algunos de los campos de criterios (key2, key3 etc.) se establece en Null, lo que probablemente no coincidirá manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63557-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="63557-134">Por lo tanto, el operador igual funcionará correctamente sólo si tiene un registro que es todo **null** excepto la clave que está buscando.</span><span class="sxs-lookup"><span data-stu-id="63557-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="63557-135">Se recomienda que utilice la mayor o igual (\>=) operador en su lugar.</span><span class="sxs-lookup"><span data-stu-id="63557-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="63557-136">El argumento key1 debe ser del mismo tipo de datos de campo que el campo correspondiente en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="63557-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="63557-137">Por ejemplo, si el índice actual hace referencia a un campo de número (por ejemplo, el identificador de empleado), key1 debe ser un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="63557-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="63557-138">De forma similar, si el índice actual hace referencia a un campo de texto (como apellido), key1 debe ser una cadena.</span><span class="sxs-lookup"><span data-stu-id="63557-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="63557-139">No es necesario que haya un registro activo cuando se utiliza **Seek**.</span><span class="sxs-lookup"><span data-stu-id="63557-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="63557-140">Puede utilizar la colección **[Indexes](indexes-collection-dao.md)** para enumerar los índices existentes.</span><span class="sxs-lookup"><span data-stu-id="63557-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="63557-p107">Para localizar un registro en un objeto **Recordset** de tipo dynaset o snapshot que cumpla una condición específica que no está cubierta por los índices existentes, use los métodos **[Find](recordset-findfirst-method-dao.md)**. Para incluir todos los registros, no solo los que cumplen una condición específica, use los métodos **[Move](recordset-movefirst-method-dao.md)** para desplazarse de un registro a otro.</span><span class="sxs-lookup"><span data-stu-id="63557-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="63557-p108">No puede usar el método **Seek** en una tabla vinculada porque no puede abrir tablas vinculadas como objetos **Recordset** de tipo tabla. No obstante, si usa el método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir directamente una base de datos (que no sea ODBC) ISAM instalable, puede usar **Seek** en las tablas de esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="63557-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="63557-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63557-145">Example</span></span>

<span data-ttu-id="63557-146">En este ejemplo se demuestra el método **Seek** al permitir al usuario buscar un producto basándose en un número de identificador.</span><span class="sxs-lookup"><span data-stu-id="63557-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="63557-p109">En este ejemplo se utiliza la propiedad **NoMatch** para determinar si **Seek** y **FindFirst** han tenido un resultado correcto y, en caso contrario, proporcionar información adecuada. Se necesitan los procedimientos SeekMatch y FindMatch para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="63557-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="63557-149">El siguiente ejemplo muestra cómo usar el método Seek para encontrar un registro en una tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="63557-149">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="63557-150">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="63557-150">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
