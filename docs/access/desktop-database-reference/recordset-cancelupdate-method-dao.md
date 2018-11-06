---
title: Recordset.CancelUpdate (método) (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6cb9823cec79a31f8ae26b2518d4368f6eefe2ce
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999081"
---
# <a name="recordsetcancelupdate-method-dao"></a>Recordset.CancelUpdate (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Cancela todas las actualizaciones pendientes para un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . CancelUpdate (***UpdateType***)

*expresión* Variable que representa un objeto **Recordset** .

## <a name="parameters"></a>Parámetros

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
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Establecer en uno de los valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Nota</strong>: los valores de <EM>valores dbUpdateRegular</EM> y <EM>dbUpdateBatch</EM> son válidos sólo si está habilitada la actualización por lotes.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Puede utilizar el método **CancelUpdate** para cancelar todas las operaciones pendientes resultantes de una operación **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)**. Por ejemplo, si un usuario llama al método **Edit** o **AddNew** y aún no se ha invocado el método **Update**, **CancelUpdate** cancela todos los cambios efectuados después de la llamada a **Edit** o **AddNew**.

Compruebe la propiedad **[EditMode](recordset-editmode-property-dao.md)** del objeto **Recordset** para determinar si hay alguna operación pendiente que se pueda cancelar.

> [!NOTE]
> [!NOTA] El método **CancelUpdate** tiene el mismo efecto que desplazarse a otro registro sin usar el método **[Update](recordset-update-method-dao.md)**, con la diferencia de que el registro actual no cambia y algunas propiedades, como **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** no se actualizan.


## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo se utiliza el método **CancelUpdate** con el método **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo se muestra cómo se utiliza el método **CancelUpdate** con el método **Edit**.

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

