---
title: Propiedad Recordset2.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6adf3e5ec2ec36163d4818411a1abc07e940b209
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922688"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="924b8-102">Propiedad Recordset2.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="924b8-102">Recordset2.AbsolutePosition property (DAO)</span></span>


<span data-ttu-id="924b8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="924b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="924b8-104">Establece o devuelve el número de registro relativo del registro actual de un objeto **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="924b8-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="924b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="924b8-105">Syntax</span></span>

<span data-ttu-id="924b8-106">*expresión* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="924b8-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="924b8-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="924b8-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="924b8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="924b8-108">Remarks</span></span>

<span data-ttu-id="924b8-p101">Puede usar la propiedad **AbsolutePosition** para colocar el puntero del registro actual en un registro específico basado en su posición ordinal en un objeto **Recordset2** de tipo Dynaset o Snapshot. Puede también determinar el número del registro actual comprobando del valor de la propiedad **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="924b8-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="924b8-p102">Como el valor de la propiedad **AbsolutePosition** se basa en cero (es decir, un valor de 0 hace referencia al primer registro en el objeto **Recordset2**), no puede establecerlo en un valor mayor o igual al número de registros rellenados; si lo hace se producirá un error capturable. Puede determinar el número de registros rellenados en el objeto **Recordset2** comprobando el valor de la propiedad **RecordCount**. El valor máximo permitido para la propiedad **AbsolutePosition** es el valor de la propiedad **RecordCount** menos 1.</span><span class="sxs-lookup"><span data-stu-id="924b8-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="924b8-114">Si no hay ningún registro actual, como cuando no hay ningún registro en el objeto **Recordset2** , **AbsolutePosition** devuelve – 1.</span><span class="sxs-lookup"><span data-stu-id="924b8-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="924b8-115">Si se elimina el registro actual, el valor de la propiedad **AbsolutePosition** no se define y se produce un error si se hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="924b8-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="924b8-116">Los registros nuevos se agregan al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="924b8-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="924b8-p104">No debería usar esta propiedad como un número de registro suplente. Los marcadores son todavía el método recomendado para retener cierta posición y volver a ella, y son la única manera de colocar el registro actual a través de todos los tipos de objetos **Recordset2**. En particular, la posición de un registro cambia cuando se eliminan uno o más registros anteriores. Además, no se tiene la certeza de que un registro tenga exactamente la misma posición si el objeto **Recordset2** se vuelve a crear porque no se garantiza el orden de los registros individuales en un objeto **Recordset** a no ser que se cree con una instrucción SQL mediante el uso de una cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="924b8-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="924b8-p105">Al establecer la propiedad <STRONG>AbsolutePosition</STRONG> en un valor mayor que cero en un objeto <STRONG>Recordset2</STRONG> recién abierto pero sin rellenar, se provoca un error capturable. Primero, rellene el objeto <STRONG>Recordset2</STRONG> mediante el método <STRONG>MoveLast</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="924b8-p105">Setting the <STRONG>AbsolutePosition</STRONG> property to a value greater than zero on a newly opened but unpopulated <STRONG>Recordset2</STRONG> object causes a trappable error. Populate the <STRONG>Recordset2</STRONG> object first with the <STRONG>MoveLast</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="924b8-123">La propiedad <STRONG>AbsolutePosition</STRONG> no está disponible en los objetos <STRONG>Recordset2</STRONG> tipo forward – only, o en los objetos <STRONG>Recordset2</STRONG> abiertos desde consultas de paso a través con bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="924b8-123">The <STRONG>AbsolutePosition</STRONG> property isn't available on forward–only–type <STRONG>Recordset2</STRONG> objects, or on <STRONG>Recordset2</STRONG> objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="924b8-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="924b8-124">Example</span></span>

<span data-ttu-id="924b8-125">En este ejemplo se usa la propiedad **AbsolutePosition** para realizar un seguimiento del proceso de un bucle que enumera todos los registros de un objeto **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="924b8-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
