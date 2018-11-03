---
title: Propiedad Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd214058b0b478c45b719798dc0b858bfd29b43
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928106"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="80a38-102">Propiedad Recordset.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="80a38-102">Recordset.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="80a38-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80a38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80a38-104">Configura o devuelve el número de registros con respecto al registro actual de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="80a38-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80a38-105">Syntax</span></span>

<span data-ttu-id="80a38-106">*expresión* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="80a38-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="80a38-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="80a38-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a38-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80a38-108">Remarks</span></span>

<span data-ttu-id="80a38-p101">Puede usar la propiedad **AbsolutePosition** para colocar el puntero del registro actual en un registro específico en función de su posición ordinal en un objeto **Recordset** de tipo Dynaset o instantánea. También puede determinar el número de registro actual comprobando el valor de la propiedad **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="80a38-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="80a38-p102">Puesto que el valor de la propiedad **AbsolutePosition** está basado en cero (el valor 0 hace referencia al primer registro del objeto **Recordset**), no se puede establecer en un valor mayor o igual que el número de registros rellenados; si se hace, se produce un error capturable. Puede determinar el número de registros rellenados en el objeto **Recordset** comprobando el valor de la propiedad **RecordCount**. El valor máximo admisible para la propiedad **AbsolutePosition** es el valor de la propiedad **RecordCount** menos 1.</span><span class="sxs-lookup"><span data-stu-id="80a38-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="80a38-114">Si no hay ningún registro actual, como cuando no hay ningún registro en el objeto **Recordset** , **AbsolutePosition** devuelve – 1.</span><span class="sxs-lookup"><span data-stu-id="80a38-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="80a38-115">Si se elimina el registro actual, el valor de la propiedad **AbsolutePosition** no se define y se produce un error si se hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="80a38-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="80a38-116">Los registros nuevos se agregan al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="80a38-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="80a38-p104">No debe usarse esta propiedad como un número de registro suplente. Los marcadores siguen siendo la forma recomendada de conservar una posición determinada y volver a ella, y son la única forma de colocar el registro actual en todos los tipos de objetos **Recordset**. En particular, la posición de un registro cambia cuando se eliminan uno o varios registros que le preceden. Tampoco hay garantía de que un registro tendrá la misma posición absoluta si se vuelve a crear el objeto **Recordset**, ya que el orden de los registros individuales en un objeto **Recordset** no está garantizado a menos que se cree con una instrucción SQL que use una cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="80a38-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="80a38-p105">Si se establece la propiedad **AbsolutePosition** en un valor mayor que cero en un objeto **Recordset** recién abierto pero sin rellenar, se produce un error capturable. Primero debe rellenarse el objeto **Recordset** con el método **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="80a38-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error. Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="80a38-123">La propiedad **AbsolutePosition** no está disponible en objetos **Recordset** de tipo forward – only, o en los objetos **Recordset** abiertos desde consultas de paso a través con bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="80a38-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="80a38-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80a38-124">Example</span></span>

<span data-ttu-id="80a38-125">En este ejemplo, se usa la propiedad **AbsolutePosition** para realizar un seguimiento del progreso de un bucle que enumera todos los registros de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="80a38-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
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
