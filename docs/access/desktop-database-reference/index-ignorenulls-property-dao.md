---
title: Propiedad Index.IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6c306f76e34e24abb5065c627d9325b48c3acead
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708862"
---
# <a name="indexignorenulls-property-dao"></a>Propiedad Index.IgnoreNulls (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que indica si los registros con valores Null en sus campos de índice tienen entradas de índice (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . IgnoreNulls

*expresión* Variable que representa un objeto **Index** .

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura para un nuevo objeto **[Index](index-object-dao.md)** que todavía no está anexado a una colección y es de solo lectura para un objeto **Index** existente en una colección **[Indexes](indexes-collection-dao.md)**.

Para acelerar el proceso de búsqueda de registros, puede definir un índice para un campo. Si permite entradas **null** en un campo indizado y espera que muchas de las entradas sean **null**, puede establecer la propiedad **IgnoreNulls** para el objeto **Index** en **True** para reducir la cantidad de espacio de almacenamiento que usa el índice.

El valor de la propiedad **IgnoreNulls** y el valor de la propiedad **[Required](field-required-property-dao.md)** determinan juntos si un registro con un valor de índice **null** tiene una entrada de índice.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si IgnoreNulls es</p></th>
<th><p>Y Required es</p></th>
<th><p>Entonces</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>False</p></td>
<td><p>Se permite un valor nulo en el campo de índice; no se agregó entrada de índice.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>False</p></td>
<td><p>Se permite un valor nulo en el campo de índice; se agregó entrada de índice.</p></td>
</tr>
<tr class="odd">
<td><p>True o False</p></td>
<td><p>True</p></td>
<td><p>No se permite un valor nulo en el campo de índice; no se agregó entrada de índice.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Ejemplo

En este ejemplo se establece la propiedad **IgnoreNulls** de un nuevo objeto **Index** en **True** o **False** a partir de los datos definidos por el usuario y después se demuestra el efecto en un objeto **Recordset** con un registro cuyo campo clave contiene un valor **Null**.

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
