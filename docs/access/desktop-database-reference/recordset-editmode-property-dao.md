---
title: Recordset.EditMode Property (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7445538d1e9aaa27f9cefcd17f085e2e0f26ec23
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871356"
---
# <a name="recordseteditmode-property-dao"></a>Recordset.EditMode Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica el estado de edición del registro actual.

## <a name="syntax"></a>Sintaxis

*expresión* . EditMode

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

El valor devuelto es un tipo de datos **Long** que indica el estado de edición. El valor puede ser una de las constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propiedad **EditMode** es útil cuando se interrumpe un proceso de edición, por ejemplo por un error durante la validación. Puede usar el valor de la propiedad **EditMode** para determinar si debe usar el método **[Update](recordset-update-method-dao.md)** o **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

También puede comprobar si el valor de la propiedad **[LockEdits](recordset-lockedits-property-dao.md)** es **True** y el valor de la propiedad **EditMode** es **dbEditInProgress** con el fin de determinar si la página actual está bloqueada.

## <a name="example"></a>Ejemplo

En este ejemplo, se muestra el valor de la propiedad **EditMode** en diversas condiciones. La función EditModeOutput es necesaria para que se pueda ejecutar este procedimiento.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
