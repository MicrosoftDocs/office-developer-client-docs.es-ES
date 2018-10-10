---
title: Propiedad Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb3d73cc236821d56e2151d80cf0e0aba241b8c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484431"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="1730f-102">Propiedad Recordset.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="1730f-102">Recordset.RecordCount Property (DAO)</span></span>


<span data-ttu-id="1730f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1730f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1730f-p101">Devuelve el número de registros a los que se tuvo acceso en un objeto **[Recordset](recordset-object-dao.md)**, o el número total de registros en un objeto **Recordset** u objeto **[TableDef](tabledef-object-dao.md)** tipo tabla. **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1730f-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1730f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1730f-107">Syntax</span></span>

<span data-ttu-id="1730f-108">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="1730f-108">*expression* .RecordCount</span></span>

<span data-ttu-id="1730f-109">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1730f-109">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1730f-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1730f-110">Remarks</span></span>

<span data-ttu-id="1730f-111">Use la propiedad **RecordCount** para saber a cuántos registros se tuvo acceso en un objeto **Recordset** o **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="1730f-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="1730f-112">La propiedad **RecordCount** no indica cuántos registros se están contenidos en un dynaset, instantánea u objeto **Recordset** de tipo forward – only hasta que todos los registros se ha tenido acceso.</span><span class="sxs-lookup"><span data-stu-id="1730f-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="1730f-113">Una vez que se tuvo acceso al último registro, la propiedad **RecordCount** indica el número total de registros sin eliminar en el objeto **Recordset** o **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="1730f-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="1730f-114">Para obligar el acceso al último registro, use el método **[MoveLast](recordset-movelast-method-dao.md)** en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1730f-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="1730f-115">También puede usar una función **Count** de SQL para determinar el número aproximado de registros que devolverá su consulta.</span><span class="sxs-lookup"><span data-stu-id="1730f-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1730f-p103">[!NOTA] El uso del método <STRONG>MoveLast</STRONG> para rellenar un <STRONG>Recordset</STRONG> recién abierto afecta negativamente al rendimiento. A menos que sea necesario tener un <STRONG>RecordCount</STRONG> preciso tan pronto como se abra un <STRONG>Recordset</STRONG>, es preferible esperar hasta que se rellene el <STRONG>Recordset</STRONG> con otras partes del código antes de comprobar la propiedad <STRONG>RecordCount</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1730f-p103">Using the <STRONG>MoveLast</STRONG> method to populate a newly opened <STRONG>Recordset</STRONG> negatively impacts performance. Unless it is necessary to have an accurate <STRONG>RecordCount</STRONG> as soon as you open a <STRONG>Recordset</STRONG>, it's better to wait until you populate the <STRONG>Recordset</STRONG> with other portions of code before checking the <STRONG>RecordCount</STRONG> property.</span></span></P>



<span data-ttu-id="1730f-p104">Como su aplicación elimina registros en un objeto **Recordset** de tipo Dynaset, el valor de la propiedad **RecordCount** se reduce. Sin embargo, los registros eliminados por otros usuarios no los refleja la propiedad **RecordCount** hasta que el registro actual se coloca en un registro eliminado. Si ejecuta una transacción que afecta al valor de la propiedad **RecordCount** y posteriormente deshace la transacción, la propiedad **RecordCount** no reflejará el número real de los registros restantes.</span><span class="sxs-lookup"><span data-stu-id="1730f-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="1730f-121">La propiedad **RecordCount** de un objeto **Recordset** de tipo snapshot o forward – only no se ve afectada por los cambios en las tablas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="1730f-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="1730f-122">Un objeto **Recordset** o **TableDef** sin registros tiene un valor 0 para la propiedad **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="1730f-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="1730f-123">Al usar el método **[Requery](recordset-requery-method-dao.md)** en un objeto **Recordset**, se restablece la propiedad **RecordCount** de la misma manera que si se volviera a ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="1730f-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="1730f-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1730f-124">Example</span></span>

<span data-ttu-id="1730f-125">En este ejemplo se muestra la propiedad **RecordCount** con distintos tipos de **Recordsets** antes y después de que estos se rellenaran.</span><span class="sxs-lookup"><span data-stu-id="1730f-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```