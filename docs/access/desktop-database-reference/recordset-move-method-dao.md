---
title: Recordset.Move Method (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 23de94392fb2d9f1b0106c39f21a8872783b6d7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485744"
---
# <a name="recordsetmove-method-dao"></a><span data-ttu-id="c88c8-102">Recordset.Move Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c88c8-102">Recordset.Move Method (DAO)</span></span>


<span data-ttu-id="c88c8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c88c8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c88c8-104">Mueve la posición del registro activo de un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c88c8-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c88c8-105">Syntax</span></span>

<span data-ttu-id="c88c8-106">*expresión* . Move (***filas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="c88c8-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="c88c8-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c88c8-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c88c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c88c8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c88c8-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="c88c8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c88c8-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="c88c8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c88c8-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c88c8-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c88c8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c88c8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c88c8-113">Filas</span><span class="sxs-lookup"><span data-stu-id="c88c8-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="c88c8-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c88c8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c88c8-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="c88c8-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="c88c8-p101">El número de filas en que se mueve la posición. Si rows es superior a 0, la posición se desplaza hacia delante (hacia el final del archivo). Si rows es inferior a 0, la posición se desplaza hacia atrás (hacia el principio del archivo).</span><span class="sxs-lookup"><span data-stu-id="c88c8-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88c8-119">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="c88c8-119">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="c88c8-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="c88c8-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="c88c8-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c88c8-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c88c8-p102">Valor que identifica un marcador. Si especifica startbookmark, el desplazamiento se inicia en relación con este marcador. De lo contrario, el desplazamiento comienza en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="c88c8-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c88c8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c88c8-125">Remarks</span></span>

<span data-ttu-id="c88c8-p103">Si usa **Move** para colocar el puntero del registro actual delante del primer registro, el puntero del registro actual se mueve al principio del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[BOF](recordset-bof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia delante produce un error.</span><span class="sxs-lookup"><span data-stu-id="c88c8-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="c88c8-p104">Si usa **Move** para colocar el puntero del registro actual detrás del primer registro, la posición del puntero del último registro actual se mueve al final del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[EOF](recordset-eof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia atrás produce un error.</span><span class="sxs-lookup"><span data-stu-id="c88c8-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="c88c8-130">Si la propiedad **BOF** o **EOF** es **True** e intenta utilizar el método **Move** sin un marcador válido, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c88c8-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="c88c8-p105">Cuando use <STRONG>Move</STRONG> en un objeto <STRONG>Recordset</STRONG> de tipo de solo avance, el argumento rows debe ser un entero positivo y no se permiten marcadores. Esto significa que el movimiento solo puede ser hacia delante.</span><span class="sxs-lookup"><span data-stu-id="c88c8-p105">When you use <STRONG>Move</STRONG> on a forward-only-type <STRONG>Recordset</STRONG> object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span></P>
> <LI>
> <P><span data-ttu-id="c88c8-133">Para que el registro primero, último, siguiente o anterior de un objeto <STRONG>Recordset</STRONG> sea el registro activo, use el método <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG> o <STRONG>MovePrevious</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c88c8-133">To make the first, last, next, or previous record in a <STRONG>Recordset</STRONG> the current record, use either the <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>, or <STRONG>MovePrevious</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="c88c8-p106">El uso de <STRONG>Move</STRONG> con un número de filas igual a 0 es una manera fácil de recuperar los datos subyacentes para el registro activo. Esto es útil si desea asegurarse de que el registro activo tiene los datos más recientes de las tablas base. Asimismo, cancela cualquier llamada <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> o <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> pendiente.</span><span class="sxs-lookup"><span data-stu-id="c88c8-p106">Using <STRONG>Move</STRONG> with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> calls.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="c88c8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c88c8-137">Example</span></span>

<span data-ttu-id="c88c8-138">En este ejemplo se utiliza el método **Move** para ubicar el puntero de registros, basándose en los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c88c8-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
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
