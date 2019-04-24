---
title: Propiedad Recordset. EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307654"
---
# <a name="recordseteditmode-property-dao"></a>Propiedad Recordset. EditMode (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve un valor que indica el estado de edición para el registro actual.

## <a name="syntax"></a>Sintaxis

*expresión* . EditMode

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

El valor devuelto es de tipo **Long** que indica el estado de edición. El valor puede ser una de las constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propiedad **EditMode** es útil cuando se interrumpe un proceso de edición, por ejemplo, por un error durante la validación. Puede utilizar el valor de la propiedad **EditMode** para determinar si debería utilizar el método **[Update](recordset-update-method-dao.md)** o **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

También puede comprobar si el valor de la propiedad **[LockEdits](recordset-lockedits-property-dao.md)** es **True** y el valor de la propiedad **EditMode** es **dbEditInProgress** para determinar si la página actual está bloqueada.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra el valor de la propiedad **EditMode** en diversas condiciones. Se requiere la función EditModeOutput para que pueda ejecutarse este procedimiento.

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
