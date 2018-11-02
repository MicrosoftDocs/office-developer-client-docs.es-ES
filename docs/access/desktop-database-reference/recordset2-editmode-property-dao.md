---
title: Propiedad Recordset2.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0279ce7e55ad560225b99ac3c6f81d89d75ca635
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930416"
---
# <a name="recordset2editmode-property-dao"></a>Propiedad Recordset2.EditMode (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica el estado de edición del registro actual.

## <a name="syntax"></a>Sintaxis

*expresión* . EditMode

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

El valor devuelto es un tipo de datos **Long** que indica el estado de edición. El valor puede ser una de las constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propiedad **EditMode** es útil cuando se interrumpe un proceso de edición, por ejemplo por un error durante la validación. Puede usar el valor de la propiedad **EditMode** para determinar si debe usar el método **[Update](recordset2-update-method-dao.md)** o **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

También puede comprobar si el valor de la propiedad **[LockEdits](recordset2-lockedits-property-dao.md)** es **True** y el valor de la propiedad **EditMode** es **dbEditInProgress** con el fin de determinar si la página actual está bloqueada.

## <a name="example"></a>Ejemplo

En este ejemplo, se muestra el valor de la propiedad **EditMode** en diversas condiciones. La función EditModeOutput es necesaria para que se pueda ejecutar este procedimiento.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
