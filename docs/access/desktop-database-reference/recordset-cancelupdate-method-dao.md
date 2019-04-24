---
title: Método Recordset. CancelUpdate (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300682"
---
# <a name="recordsetcancelupdate-method-dao"></a>Método Recordset. CancelUpdate (DAO)

**Se aplica a:** Access 2013, Office 2013

Cancela cualquier actualización pendiente para un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . CancelUpdate (***UpdateType***)

*expresión* Variable que representa un objeto **Recordset** .

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
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Se establece en uno de los valores de <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Nota</strong>: los valores <EM>dbUpdateRegular</EM> y <EM>dbUpdateBatch</EM> solo son válidos si la actualización por lotes está habilitada.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede utilizar el método **CancelUpdate** para cancelar cualquier actualización pendiente resultante de una operación **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)**. Por ejemplo, si un usuario abre el método **Edit** o **AddNew** y no ha abierto aún el método **Update**, **CancelUpdate** cancela cualquier cambio realizado después de abrir **Edit** o **AddNew**.

Compruebe la propiedad **[EditMode](recordset-editmode-property-dao.md)** de **Recordset** para determinar si hay alguna operación pendiente que se puede cancelar.

> [!NOTE]
> [!NOTA] Utilizar el método **CancelUpdate** tiene el mismo efecto que desplazarse a otro registro sin utilizar el método **[Update](recordset-update-method-dao.md)**, excepto que el registro activo no cambia y varias propiedades, como **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** no se actualizan.


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

