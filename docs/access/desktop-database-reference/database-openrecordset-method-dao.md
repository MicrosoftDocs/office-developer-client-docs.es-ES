---
title: Método Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 06/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b13abd7f3f2c856a0f1a1288717d6f8affb81252
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675746"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="98aa7-102">Método Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="98aa7-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="98aa7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98aa7-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="98aa7-104">Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="98aa7-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="98aa7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98aa7-105">Syntax</span></span>

<span data-ttu-id="98aa7-106">*expression*.**OpenRecordset**(_Name_, _Type_, _Options_, _LockEdit_)</span><span class="sxs-lookup"><span data-stu-id="98aa7-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span></span>

<span data-ttu-id="98aa7-107">*expression* Variable que representa un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="98aa7-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="98aa7-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="98aa7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98aa7-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="98aa7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="98aa7-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="98aa7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="98aa7-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="98aa7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="98aa7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="98aa7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98aa7-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="98aa7-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="98aa7-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="98aa7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="98aa7-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="98aa7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="98aa7-p101">Origen de los registros para el nuevo <strong>Recordset</strong>. El origen puede ser un nombre de tabla o de consulta, o una instrucción SQL que devuelve registros. Para los objetos <strong>Recordset</strong> de tipo tabla en las bases de datos del motor de base de datos de Microsoft Access, el origen solo puede ser un nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="98aa7-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98aa7-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="98aa7-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="98aa7-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="98aa7-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="98aa7-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="98aa7-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="98aa7-122">Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</span><span class="sxs-lookup"><span data-stu-id="98aa7-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="98aa7-123"><strong>NOTA</strong>: si abre un <strong>Recordset</strong> en un área de trabajo de Microsoft Access y no especifica un tipo, <strong>OpenRecordset</strong> crea un <strong>Recordset</strong> de tipo tabla, si es posible.</span><span class="sxs-lookup"><span data-stu-id="98aa7-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="98aa7-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="98aa7-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98aa7-125"><em>Opciones</em></span><span class="sxs-lookup"><span data-stu-id="98aa7-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="98aa7-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="98aa7-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="98aa7-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="98aa7-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="98aa7-128">Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifican características del nuevo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="98aa7-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="98aa7-129"><strong>NOTA</strong>: las constantes <strong>dbConsistent</strong> y <strong>dbInconsistent</strong> son mutuamente exclusivas, y usar las dos producirá un error.</span><span class="sxs-lookup"><span data-stu-id="98aa7-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="98aa7-130">Si proporciona un argumento LockEdit cuando Options usa la constante <strong>dbReadOnly</strong> también provoca un error.</span><span class="sxs-lookup"><span data-stu-id="98aa7-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98aa7-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="98aa7-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="98aa7-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="98aa7-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="98aa7-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="98aa7-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="98aa7-134">Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo del <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="98aa7-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="98aa7-135"><strong>NOTA</strong>: puede usar <strong>dbReadOnly</strong> en el argumento Options o en el argumento LockedEdit, pero no en ambos.</span><span class="sxs-lookup"><span data-stu-id="98aa7-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="98aa7-136">Si lo usa para ambos argumentos, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="98aa7-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="98aa7-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98aa7-137">Return value</span></span>

<span data-ttu-id="98aa7-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="98aa7-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="98aa7-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98aa7-139">Remarks</span></span>

<span data-ttu-id="98aa7-p105">En general, si el usuario obtiene este error mientras actualiza un registro, el código debe actualizar el contenido de los campos y recuperar los valores recién modificados. Si el error se produce al eliminar un registro, el código puede mostrar los nuevos datos de registros al usuario y un mensaje en el que se indica que los datos han cambiado recientemente. En ese momento, el código puede pedir una confirmación de que aún se desea eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="98aa7-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="98aa7-143">Debe usar también la constante **dbSeeChanges** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.</span><span class="sxs-lookup"><span data-stu-id="98aa7-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="98aa7-p106">Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **MoveLast** en cuanto se abra el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="98aa7-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="98aa7-146">Cerrar un objeto **Recordset** con el método **[Close](connection-close-method-dao.md)** lo elimina automáticamente de la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="98aa7-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="98aa7-147">Si *origen* hace referencia a una instrucción SQL compuesta por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU., como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), se produce un error cuando intenta abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="98aa7-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="98aa7-148">Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="98aa7-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="98aa7-149">**Vínculo proporcionado por** la comunidad de [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="98aa7-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="98aa7-150">UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="98aa7-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="98aa7-151">Transferencia de datos de Access a Excel</span><span class="sxs-lookup"><span data-stu-id="98aa7-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="98aa7-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98aa7-152">Example</span></span>

<span data-ttu-id="98aa7-153">En el siguiente ejemplo, se muestra cómo abrir un Recordset basado en una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="98aa7-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="98aa7-154">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="98aa7-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="98aa7-155">En el siguiente ejemplo, se muestra cómo abrir un Recordset a partir de una tabla o una consulta.</span><span class="sxs-lookup"><span data-stu-id="98aa7-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="98aa7-156">En el siguiente ejemplo, se muestra cómo abrir un Recordset a partir de una instrucción del Lenguaje de consulta estructurado (SQL).</span><span class="sxs-lookup"><span data-stu-id="98aa7-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="98aa7-157">En el siguiente ejemplo se muestra cómo usar la propiedad Filter para determinar los registros que se incluirán en un Recordset que se abrirá posteriormente.</span><span class="sxs-lookup"><span data-stu-id="98aa7-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



