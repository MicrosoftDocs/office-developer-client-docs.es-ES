---
title: Propiedad Field2. AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3125a5669ea8aa016d8554be0357572d56c08ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292912"
---
# <a name="field2allowzerolength-property-dao"></a>Propiedad Field2. AllowZeroLength (DAO)


**Se aplica a:** Access 2013, Office 2013


Establece o devuelve un valor que indica si una cadena de longitud cero ("") es válida para la propiedad **[Value](field-value-property-dao.md)** del objeto **Field2** con un tipo de datos Text o Memo (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Longitud

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Comentarios

Para un objeto que aún no se haya anexado a la colección **Fields**, esta propiedad es de lectura y escritura.

Una vez que se haya anexado a una colección **Fields**, la disponibilidad de la propiedad **AllowZeroLength** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la colección Fields pertenece a</p></th>
<th><p>Disponibilidad de AllowZeroLength</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>
						Objeto <strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>Relation</strong></p></td>
<td><p>No está admitido</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>TableDef</strong></p></td>
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>


Puede usar esta propiedad junto con la propiedad **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** o **[ValidationRule](field-validationrule-property-dao.md)** para validar un valor de un campo.

## <a name="example"></a>Ejemplo

En este ejemplo, la propiedad **AllowZeroLength** permite al usuario establecer el valor de un objeto **Field2** en una cadena vacía. En esta situación, el usuario puede distinguir entre un registro en el que no se conocen los datos y un registro en el que los datos no son aplicables.

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
