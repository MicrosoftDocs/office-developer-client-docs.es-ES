---
title: Método Recordset2.Move (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307269"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="6cad5-102">Método Recordset2.Move (DAO)</span><span class="sxs-lookup"><span data-stu-id="6cad5-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="6cad5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cad5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cad5-104">Mueve la posición del registro actual de un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6cad5-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cad5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cad5-105">Syntax</span></span>

<span data-ttu-id="6cad5-106">*expresión* .Move(***Columnas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="6cad5-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="6cad5-107">*expresión* Variable que representa un objeto **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="6cad5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cad5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cad5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cad5-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="6cad5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6cad5-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="6cad5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6cad5-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6cad5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6cad5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cad5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cad5-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="6cad5-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="6cad5-114">Necesario</span><span class="sxs-lookup"><span data-stu-id="6cad5-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6cad5-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="6cad5-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="6cad5-p101">El número de filas en que se mueve la posición. Si rows es superior a 0, la posición se desplaza hacia delante (hacia el final del archivo). Si rows es inferior a 0, la posición se desplaza hacia atrás (hacia el principio del archivo).</span><span class="sxs-lookup"><span data-stu-id="6cad5-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cad5-119"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="6cad5-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="6cad5-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="6cad5-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="6cad5-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6cad5-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6cad5-p102">Valor que identifica un marcador. Si especifica startbookmark, el desplazamiento se inicia en relación con este marcador. De lo contrario, el desplazamiento comienza en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="6cad5-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6cad5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cad5-125">Remarks</span></span>

<span data-ttu-id="6cad5-p103">Si usa **Move** para colocar el puntero del registro actual delante del primer registro, el puntero del registro actual se mueve al principio del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[BOF](recordset2-bof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia atrás produce un error.</span><span class="sxs-lookup"><span data-stu-id="6cad5-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="6cad5-p104">Si usa **Move** para colocar el puntero del registro actual detrás del último registro, la posición del puntero del registro actual se mueve al final del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[EOF](recordset2-eof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia delante produce un error.</span><span class="sxs-lookup"><span data-stu-id="6cad5-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="6cad5-130">Si la propiedad **BOF** o **EOF** es **True** e intenta usar el método **Move** sin un marcador válido, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6cad5-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="6cad5-p105">Cuando use **Move** en un objeto **Recordset** de tipo de solo avance, el argumento rows debe ser un entero positivo y no se permiten marcadores. Esto significa que el movimiento solo puede ser hacia delante.</span><span class="sxs-lookup"><span data-stu-id="6cad5-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span>
> - <span data-ttu-id="6cad5-133">Para que el registro primero, último, siguiente o anterior de un objeto **Recordset** sea el registro actual, use el método **MoveFirst**, **MoveLast**, **MoveNext** o **MovePrevious**.</span><span class="sxs-lookup"><span data-stu-id="6cad5-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="6cad5-p106">El uso de **Move** con un número de filas igual a 0 es una manera fácil de recuperar los datos subyacentes para el registro actual. Esto es útil si quiere asegurarse de que el registro actual tiene los datos más recientes de las tablas base. Asimismo, cancela cualquier llamada **[Edit](recordset2-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)** pendiente.</span><span class="sxs-lookup"><span data-stu-id="6cad5-p106">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="6cad5-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6cad5-137">Example</span></span>

<span data-ttu-id="6cad5-138">En este ejemplo se usa el método **Move** para ubicar el puntero de registros en función de los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6cad5-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
