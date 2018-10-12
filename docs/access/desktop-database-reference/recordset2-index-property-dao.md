---
title: Recordset2.Index Property (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad875f1aba667924d5e00dc9990fd09b6826947d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485422"
---
# <a name="recordset2index-property-dao"></a><span data-ttu-id="848a5-102">Recordset2.Index Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="848a5-102">Recordset2.Index Property (DAO)</span></span>


<span data-ttu-id="848a5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="848a5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="848a5-104">Establece o devuelve un valor que indica el nombre del objeto actual **[Index](index-object-dao.md)** en un objeto de tipo de tabla **[Recordset](recordset-object-dao.md)** (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="848a5-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="848a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="848a5-105">Syntax</span></span>

<span data-ttu-id="848a5-106">*expresión* . Índice</span><span class="sxs-lookup"><span data-stu-id="848a5-106">*expression* .Index</span></span>

<span data-ttu-id="848a5-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="848a5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="848a5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="848a5-108">Remarks</span></span>

<span data-ttu-id="848a5-p101">Los registros en tablas base no se almacenan en ningún un orden determinado. El valor de la propiedad **Index** cambia el orden de los registros que se devuelven desde la base de datos; esto no afecta al orden en el que se almacenaron los registros.</span><span class="sxs-lookup"><span data-stu-id="848a5-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="848a5-p102">El objeto específico **Index** debe estar ya definido. Si establece la propiedad **Index** en un objeto **Index** que no existe o si la propiedad **Index** no está establecida cuando utiliza el método **[Seek](recordset2-seek-method-dao.md)**, se produce un error capturable.</span><span class="sxs-lookup"><span data-stu-id="848a5-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="848a5-113">Examine la colección **Indexes** de un objeto **TableDef** para determinar los objetos **Index** que están disponibles para objetos de tipo tabla **Recordset** creados desde ese objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="848a5-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="848a5-114">Puede crear un índice nuevo para la tabla mediante la creación de un nuevo objeto **Index**, al establecer sus propiedades, al anexarlo a la colección **Indexes** de un objeto base **TableDef** y después al volver a abrir el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="848a5-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="848a5-115">Los registros devueltos desde un objeto **Recordset** de tipo de tabla pueden ordenarse sólo por los índices definidos por el objeto base **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="848a5-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="848a5-116">Para ordenar los registros en cualquier otro orden, puede abrir un dynaset, instantánea u objeto **Recordset** de tipo forward – only mediante el uso de una instrucción SQL con una cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="848a5-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="848a5-p104">No tiene que crear índices para tablas. Con grandes tablas sin índice, puede que tarde mucho tiempo en tener acceso a un registro específico o en crear un objeto <STRONG>Recordset</STRONG>. Por otra parte, al crear demasiados índices se ralentiza el actualizar, anexar y eliminar operaciones debido a que todos los índices se actualizan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="848a5-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a <STRONG>Recordset</STRONG> object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span></P>
> <LI>
> <P><span data-ttu-id="848a5-120">Los registros leídos desde tablas sin índices no se devuelven en secuencias concretas.</span><span class="sxs-lookup"><span data-stu-id="848a5-120">Records read from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="848a5-121">La propiedad <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> de cada objeto <STRONG><A href="field-object-dao.md">Field</A></STRONG> en el objeto <STRONG>Index</STRONG> determina el orden de los registros y, como consecuencia, se determinan las técnicas de acceso que hay que usar para ese índice.</span><span class="sxs-lookup"><span data-stu-id="848a5-121">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that index.</span></span></P>
> <LI>
> <P><span data-ttu-id="848a5-122">Un índice único ayuda a optimizar la búsqueda de registros.</span><span class="sxs-lookup"><span data-stu-id="848a5-122">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="848a5-123">Los índices no afectan al orden físico de los índices de tablas base, solo afectan a cómo se tiene acceso a los registros mediante el objeto <STRONG>Recordset</STRONG> de tipo de tabla cuando se elige un índice concreto o cuando se abre <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="848a5-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type <STRONG>Recordset</STRONG> object when a particular index is chosen or when <STRONG>Recordset</STRONG> is opened.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="848a5-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="848a5-124">Example</span></span>

<span data-ttu-id="848a5-125">Este ejemplo usa la propiedad **Index** para establecer diferentes órdenes de registro para un tipo de tabla **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="848a5-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="848a5-126">En este ejemplo se muestra el método **Seek** al permitir que el usuario busque un producto basado en un número de Id.</span><span class="sxs-lookup"><span data-stu-id="848a5-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
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