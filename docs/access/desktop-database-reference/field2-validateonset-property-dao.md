---
title: Propiedad Field2. ValidateOnSet (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 07612730-8dad-4ef0-b19b-f76845973fc3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844969(v=office.15)
ms:contentKeyID: 48543075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 427903186cce0f2ce3adf7690682a793fb417873
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292646"
---
# <a name="field2validateonset-property-dao"></a><span data-ttu-id="cebcd-102">Propiedad Field2. ValidateOnSet (DAO)</span><span class="sxs-lookup"><span data-stu-id="cebcd-102">Field2.ValidateOnSet property (DAO)</span></span>


<span data-ttu-id="cebcd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cebcd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="cebcd-104">Establece o devuelve un valor que especifica si el valor de un objeto **Field2** se valida inmediatamente cuando se establece la propiedad del objeto **Value** (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cebcd-104">Sets or returns a value that specifies whether or not the value of a **Field2** object is immediately validated when the object's **Value** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cebcd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cebcd-105">Syntax</span></span>

<span data-ttu-id="cebcd-106">*expresión* . ValidateOnSet</span><span class="sxs-lookup"><span data-stu-id="cebcd-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="cebcd-107">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="cebcd-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cebcd-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cebcd-108">Remarks</span></span>

<span data-ttu-id="cebcd-109">Solo los objetos **Field2** en los objetos **Recordset** admiten la propiedad **ValidateOnSet** como de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cebcd-109">Only **Field2** objects in **Recordset** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="cebcd-p101">Puede ser útil establecer la propiedad **ValidateOnSet** en **True** en aquellas situaciones en las que un usuario especifica registros que incluyen importantes datos Memo. Si se espera hasta que aparezca la llamada a **Update** para validar los datos, puede que el tiempo dedicado a escribir extensos datos Memo en la base de datos sea innecesario si los datos no son válidos de ninguna manera porque la regla de validación se ha interrumpido en otro campo.</span><span class="sxs-lookup"><span data-stu-id="cebcd-p101">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data. Waiting until the **Update** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="cebcd-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cebcd-112">Example</span></span>

<span data-ttu-id="cebcd-p102">En este ejemplo se utiliza la propiedad **ValidateOnSet** para demostrar cómo se pueden capturar errores durante la entrada de datos. Se requiere la función ValidateData para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="cebcd-p102">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry. The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new Field object to the Fields 
     ' collection of the Employees table. 
     Set fldDays = _ 
     dbsNorthwind.TableDefs!Employees.CreateField( _ 
     "DaysOfVacation", dbInteger, 2) 
     fldDays.ValidationRule = "BETWEEN 1 AND 20" 
     fldDays.ValidationText = _ 
     "Number must be between 1 and 20!" 
     dbsNorthwind.TableDefs!Employees.Fields.Append fldDays 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     
     Do While True 
     ' Add new record. 
     .AddNew 
     
     ' Get user input for three fields. Verify that the 
     ' data do not violate the validation rules for any 
     ' of the fields. 
     If ValidateData(!FirstName, _ 
     "Enter first name.") = False Then Exit Do 
     If ValidateData(!LastName, _ 
     "Enter last name.") = False Then Exit Do 
     If ValidateData(!DaysOfVacation, _ 
     "Enter days of vacation.") = False Then Exit Do 
     
     .Update 
     .Bookmark = .LastModified 
     Debug.Print !FirstName & " " & !LastName & _ 
     " - " & "DaysOfVacation = " & !DaysOfVacation 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     Exit Do 
     Loop 
     
     ' Cancel AddNew method if any of the validation rules 
     ' were broken. 
     If .EditMode <> dbEditNone Then .CancelUpdate 
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     dbsNorthwind.TableDefs!Employees.Fields.Delete _ 
     fldDays.Name 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function ValidateData(fldTemp As Field2, _ 
     strMessage As String) As Boolean 
     
     Dim strInput As String 
     Dim errLoop As Error 
     
     ValidateData = True 
     ' ValidateOnSet is only read/write for Field objects in 
     ' Recordset objects. 
     fldTemp.ValidateOnSet = True 
     
     Do While True 
     strInput = InputBox(strMessage) 
     If strInput = "" Then Exit Do 
     ' Trap for errors when setting the Field value. 
     On Error GoTo Err_Data 
     If fldTemp.Type = dbInteger Then 
     fldTemp = Val(strInput) 
     Else 
     fldTemp = strInput 
     End If 
     On Error GoTo 0 
     If Not IsNull(fldTemp) Then Exit Do 
     Loop 
     
     If strInput = "" Then ValidateData = False 
     
     Exit Function 
     
    Err_Data: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. The description 
     ' property of the last Error object will be set to 
     ' the ValidationText property of the relevant 
     ' field. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Function
```
