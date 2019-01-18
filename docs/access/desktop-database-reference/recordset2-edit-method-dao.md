---
title: Recordset2.Edit (método) (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707748"
---
# <a name="recordset2edit-method-dao"></a>Recordset2.Edit (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Copia el registro actual de un objeto **[Recordset](recordset-object-dao.md)** actualizable en el búfer de copias para su posterior modificación.

## <a name="syntax"></a>Sintaxis

*expresión* . Editar

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Después de usar el método **Edit**, los cambios efectuados en los campos del registro actual se copian en el búfer de copias. Tras realizar los cambios necesarios en el registro, use el método **[Update](recordset2-update-method-dao.md)** para guardar los cambios.

El registro actual sigue siendo el registro actual después de usar **Edit**.

> [!NOTE]
> [!NOTA] Si edita un registro y realiza cualquier operación que mueva a otro registro pero sin usar primero **Update**, los cambios se pierden sin advertencia. Además, si cierra recordset o termina el procedimiento que declara el **objeto Recordset** o el objeto primario de **[base de datos](database-object-dao.md)** o **[conexión](connection-object-dao.md)** , el registro editado se descarta sin advertencia.

El uso de **Edit** produce un error si:

- No hay ningún registro actual.

- El objeto **Connection**, **Database** o **Recordset** se abre como de solo lectura.

- No hay campos actualizables en el registro.

- El objeto **Database** o **Recordset** se abrió para uso exclusivo de otro usuario (solo en áreas de trabajo de Microsoft Access).

- Otro usuario ha bloqueado la página que contiene el registro (área de trabajo de Microsoft Access).

En un área de trabajo de Microsoft Access, cuando el valor de la propiedad [**LockEdits**](recordset2-lockedits-property-dao.md) del objeto **Recordset** es **True** (bloqueo pesimista) en un entorno multiusuario, el registro permanece bloqueado desde que se usa **Edit** hasta que finaliza la actualización. Si el valor de la propiedad **LockEdits** es **False** (bloqueo optimista), el registro se bloquea y se compara con el registro previo a la modificación antes de actualizarse en la base de datos. Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error en tiempo de ejecución si usa **OpenRecordset** sin especificar **dbSeeChanges**. De manera predeterminada, las bases de datos de ODBC e ISAM instalable conectadas al motor de base de datos de Microsoft Access usan siempre el bloqueo optimista.

> [!NOTE]
> [!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** o **Edit** en un área de trabajo de Microsoft Access.

## <a name="example"></a>Ejemplo

En este ejemplo se usa el método **Edit** para reemplazar los datos actuales por el nombre especificado. Se necesita el procedimiento EditName para que se pueda ejecutar este procedimiento.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
