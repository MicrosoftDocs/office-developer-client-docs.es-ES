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
# <a name="recordset2move-method-dao"></a>Método Recordset2.Move (DAO)

**Se aplica a:** Access 2013, Office 2013

Mueve la posición del registro actual de un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* .Move(***Columnas***, ***StartBookmark***)

*expresión* Variable que representa un **objeto Recordset2.**

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>El número de filas en que se mueve la posición. Si rows es superior a 0, la posición se desplaza hacia delante (hacia el final del archivo). Si rows es inferior a 0, la posición se desplaza hacia atrás (hacia el principio del archivo).</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Valor que identifica un marcador. Si especifica startbookmark, el desplazamiento se inicia en relación con este marcador. De lo contrario, el desplazamiento comienza en el registro activo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Si usa **Move** para colocar el puntero del registro actual delante del primer registro, el puntero del registro actual se mueve al principio del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[BOF](recordset2-bof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia atrás produce un error.

Si usa **Move** para colocar el puntero del registro actual detrás del último registro, la posición del puntero del registro actual se mueve al final del archivo. Si el objeto **Recordset** no contiene ningún registro y su propiedad **[EOF](recordset2-eof-property-dao.md)** es **True**, el uso de este método para un movimiento hacia delante produce un error.

Si la propiedad **BOF** o **EOF** es **True** e intenta usar el método **Move** sin un marcador válido, se produce un error en tiempo de ejecución.

> [!NOTE]
> - Cuando use **Move** en un objeto **Recordset** de tipo de solo avance, el argumento rows debe ser un entero positivo y no se permiten marcadores. Esto significa que el movimiento solo puede ser hacia delante.
> - Para que el registro primero, último, siguiente o anterior de un objeto **Recordset** sea el registro actual, use el método **MoveFirst**, **MoveLast**, **MoveNext** o **MovePrevious**.
> - El uso de **Move** con un número de filas igual a 0 es una manera fácil de recuperar los datos subyacentes para el registro actual. Esto es útil si quiere asegurarse de que el registro actual tiene los datos más recientes de las tablas base. Asimismo, cancela cualquier llamada **[Edit](recordset2-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)** pendiente.


## <a name="example"></a>Ejemplo

En este ejemplo se usa el método **Move** para ubicar el puntero de registros en función de los datos proporcionados por el usuario.

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
