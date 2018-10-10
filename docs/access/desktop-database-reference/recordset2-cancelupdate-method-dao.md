---
title: Recordset2.CancelUpdate Method (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d22f37dbc26c1742f6042d612210135bf8662bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486780"
---
# <a name="recordset2cancelupdate-method-dao"></a>Recordset2.CancelUpdate Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Cancela todas las actualizaciones pendientes para un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . CancelUpdate (***UpdateType***)

*expresión* Variable que representa un objeto **Recordset2** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UpdateType</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Establecer en uno de los valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p>

> [!NOTE]
> <P>Los valores de <EM>valores dbUpdateRegular</EM> y <EM>dbUpdateBatch</EM> son válidos sólo si está habilitada la actualización por lotes.</P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Puede utilizar el método **CancelUpdate** para cancelar todas las operaciones pendientes resultantes de una operación **[Edit](recordset2-edit-method-dao.md)** o **[AddNew](recordset2-addnew-method-dao.md)**. Por ejemplo, si un usuario llama al método **Edit** o **AddNew** y aún no se ha invocado el método **Update**, **CancelUpdate** cancela todos los cambios efectuados después de la llamada a **Edit** o **AddNew**.

Compruebe la propiedad **[EditMode](recordset2-editmode-property-dao.md)** del objeto **Recordset** para determinar si hay alguna operación pendiente que se pueda cancelar.


> [!NOTE]
> <P>[!NOTA] El método <STRONG>CancelUpdate</STRONG> tiene el mismo efecto que desplazarse a otro registro sin usar el método <STRONG><A href="recordset2-update-method-dao.md">Update</A></STRONG>, con la diferencia de que el registro actual no cambia y algunas propiedades, como <STRONG><A href="recordset2-bof-property-dao.md">BOF</A></STRONG> y <STRONG><A href="recordset2-eof-property-dao.md">EOF</A></STRONG> no se actualizan.</P>



## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo se utiliza el método **CancelUpdate** con el método **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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

