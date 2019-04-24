---
title: Propiedad Field2. DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845a2e0c7ffa5d54d73c4fcec1a6c785468d734e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292835"
---
# <a name="field2defaultvalue-property-dao"></a>Propiedad Field2. DefaultValue (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el valor predeterminado de un objeto **Field2**. Para un objeto **Field2** no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . (

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos **String** que puede contener un máximo de 255 caracteres. Puede ser texto o una expresión. Si el valor de la propiedad es una expresión, no puede contener funciones definidas por el usuario, no puede agregar funciones SQL del motor de base de datos de Microsoft Access, ni tener referencias a consultas, formularios u otros objetos **Field2**.

> [!NOTE]
> [!NOTA] También puede establecer la propiedad **DefaultValue** de un objeto **Field2** en un objeto **TableDef** para un valor especial denominado "GenUniqueID( )". Esto provoca que se asigne un número aleatorio a este campo siempre que se agregue o se cree un nuevo registro, de ese modo se asigna cada registro a un identificador único. La propiedad **Type** del campo debe ser **Long**.

La disponibilidad de la propiedad **DefaultValue** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la colección Fields pertenece a</p></th>
<th><p>Entonces DefaultValue</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto Index</p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p>Objeto QueryDef</p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p>Objeto Recordset</p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p>Objeto Relation</p></td>
<td><p>No está admitido</p></td>
</tr>
<tr class="odd">
<td><p>Objeto TableDef</p></td>
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>


Cuando se crea un nuevo registro, el valor de la propiedad **DefaultValue** se incluye automáticamente como el valor para el campo. Puede cambiar el valor del campo al establecer su propiedad en **Value**.

La propiedad **DefaultValue** no se aplica a los campos **AutoNumber** y **Long Binary**.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza la propiedad **DefaultValue** para advertir al usuario de un valor normal del campo mientras se le piden datos de entrada. Además, se demuestra cómo los registros nuevos se rellenarán utilizando **DefaultValue** en ausencia de cualquier otra entrada. Se requiere la función DefaultPrompt para que pueda ejecutarse este procedimiento.

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
