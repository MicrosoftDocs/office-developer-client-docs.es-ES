---
title: Propiedad Recordset.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c111193f7cfb90eb593788381e839839f29ba784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926447"
---
# <a name="recordseteditmode-property-dao"></a><span data-ttu-id="1d882-102">Propiedad Recordset.EditMode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1d882-102">Recordset.EditMode property (DAO)</span></span>


<span data-ttu-id="1d882-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d882-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d882-104">Devuelve un valor que indica el estado de edición del registro actual.</span><span class="sxs-lookup"><span data-stu-id="1d882-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d882-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d882-105">Syntax</span></span>

<span data-ttu-id="1d882-106">*expresión* . EditMode</span><span class="sxs-lookup"><span data-stu-id="1d882-106">*expression* .EditMode</span></span>

<span data-ttu-id="1d882-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1d882-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d882-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d882-108">Remarks</span></span>

<span data-ttu-id="1d882-p101">El valor devuelto es un tipo de datos **Long** que indica el estado de edición. El valor puede ser una de las constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1d882-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="1d882-p102">La propiedad **EditMode** es útil cuando se interrumpe un proceso de edición, por ejemplo por un error durante la validación. Puede usar el valor de la propiedad **EditMode** para determinar si debe usar el método **[Update](recordset-update-method-dao.md)** o **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1d882-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset-update-method-dao.md)** or **[CancelUpdate](recordset-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="1d882-113">También puede comprobar si el valor de la propiedad **[LockEdits](recordset-lockedits-property-dao.md)** es **True** y el valor de la propiedad **EditMode** es **dbEditInProgress** con el fin de determinar si la página actual está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1d882-113">You can also check to see if the **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="1d882-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d882-114">Example</span></span>

<span data-ttu-id="1d882-p103">En este ejemplo, se muestra el valor de la propiedad **EditMode** en diversas condiciones. La función EditModeOutput es necesaria para que se pueda ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="1d882-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

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
