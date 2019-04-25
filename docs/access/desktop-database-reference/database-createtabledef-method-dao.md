---
title: Método Database.CreateTableDef (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c986f0a96c14dac8a9ee4f3c7fded5a049fa451e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294949"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="ffde0-102">Método Database.CreateTableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="ffde0-102">Database.CreateTableDef method (DAO)</span></span>

<span data-ttu-id="ffde0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffde0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ffde0-104">Crea un nuevo objeto **[TableDef](tabledef-object-dao.md)** (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ffde0-104">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only). .</span></span> <span data-ttu-id="ffde0-105">.</span><span class="sxs-lookup"><span data-stu-id="ffde0-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="ffde0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffde0-106">Syntax</span></span>

<span data-ttu-id="ffde0-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="ffde0-107">offexpression.CreateTableDef(\*\*\*\*Name\*\*\*\*, ***Attributes***, ***SourceTableName, \*\*\*\*\*\*Connect***)</span></span>

<span data-ttu-id="ffde0-108">*expression* Variable que representa un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-108">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffde0-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="ffde0-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ffde0-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="ffde0-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ffde0-111">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="ffde0-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ffde0-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ffde0-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="ffde0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffde0-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffde0-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ffde0-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ffde0-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="ffde0-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="ffde0-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ffde0-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ffde0-117"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffde0-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="ffde0-118">Vea el tema relativo a la propiedad <strong><a href="tabledef-name-property-dao.md">Name</a></strong> para obtener información sobre los nombres de <strong>TableDef</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="ffde0-118">See the <a href="tabledef-name-property-dao.md"><strong>Name</strong></a> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffde0-119"><em>Atributos</em></span><span class="sxs-lookup"><span data-stu-id="ffde0-119"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="ffde0-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="ffde0-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ffde0-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ffde0-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ffde0-122">Una constante o una combinación de constantes que indica una o varias de las características del nuevo objeto <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffde0-122">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="ffde0-123">Vea el tema relativo a la propiedad <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ffde0-123">See the <a href="tabledef-attributes-property-dao.md"><strong>Attributes</strong></a> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffde0-124"><em>SourceTableName</em></span><span class="sxs-lookup"><span data-stu-id="ffde0-124"><em>SourceTableName property</em></span></span></p></td>
<td><p><span data-ttu-id="ffde0-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="ffde0-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="ffde0-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ffde0-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ffde0-127"><strong>Variant</strong> (subtipo <strong>String</strong>) que contiene el nombre de una tabla en una base de datos externa que es el origen de los datos.</span><span class="sxs-lookup"><span data-stu-id="ffde0-127">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data.</span></span> <span data-ttu-id="ffde0-128">La cadena de origen se convierte en el valor de la propiedad <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> del nuevo objeto <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffde0-128">The source string becomes the <a href="tabledef-sourcetablename-property-dao.md"><strong>SourceTableName</strong></a> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffde0-129"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="ffde0-129"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="ffde0-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="ffde0-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="ffde0-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ffde0-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ffde0-132"><strong>Variant</strong> (subtipo <strong>String</strong>) que contiene información sobre el origen de una base de datos abierta, una base de datos utilizada en una consulta de paso o una tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="ffde0-132">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table.</span></span> <span data-ttu-id="ffde0-133">Vea el tema relativo a la propiedad <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> para obtener más información sobre las cadenas de conexión válidas.</span><span class="sxs-lookup"><span data-stu-id="ffde0-133">See the <a href="tabledef-connect-property-dao.md"><strong>Connect</strong></a> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ffde0-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffde0-134">Return value</span></span>

<span data-ttu-id="ffde0-135">TableDef</span><span class="sxs-lookup"><span data-stu-id="ffde0-135">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="ffde0-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffde0-136">Remarks</span></span>

<span data-ttu-id="ffde0-p106">Si omite uno o varios de los argumentos opcionales cuando utiliza el método **CreateTableDef**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunas pero no todas sus propiedades. Vea los temas correspondientes a cada propiedad para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="ffde0-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="ffde0-140">Si name hace referencia a un objeto que ya es un miembro de la colección, o especifica una propiedad no válida en el objeto **TableDef** o **[Field](field-object-dao.md)** que va a agregar, se produce un error en tiempo de ejecución al utilizar el método **[Append](tabledefs-append-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-140">If  name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or [**Field**](tabledefs-append-method-dao.md) object you're appending, a run-time error occurs when you use the **Append** method.</span></span> <span data-ttu-id="ffde0-141">Asimismo, no puede agregar un objeto **TableDef** a la colección **TableDefs** hasta que defina al menos un objeto **Field** para el objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-141">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="ffde0-142">Para quitar un objeto **TableDef** de la colección **[TableDefs](tabledefs-collection-dao.md)**, utilice el método **[Delete](tabledefs-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="ffde0-142">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="ffde0-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffde0-143">Example</span></span>

<span data-ttu-id="ffde0-144">En este ejemplo se crea un nuevo objeto **TableDef** en la base de datos Northwind.</span><span class="sxs-lookup"><span data-stu-id="ffde0-144">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ffde0-p108">En este ejemplo se utilizan los métodos **CreateTableDef** y **FillCache**, y las propiedades **CacheSize**, **CacheStart** y **SourceTableName** para enumerar los registros de una tabla vinculada dos veces. A continuación, se enumeran los registros dos veces con una caché de 50 registros. En este ejemplo se muestran luego las estadísticas de rendimiento para las ejecuciones almacenadas y no almacenadas en caché a través de la tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="ffde0-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
