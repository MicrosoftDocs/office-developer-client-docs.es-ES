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
localization_priority: Normal
ms.openlocfilehash: d4043a442bec8c5ce421d85de6256eb9c5cb353f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716750"
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
