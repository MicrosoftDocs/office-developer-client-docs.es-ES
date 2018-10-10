---
title: Index.DistinctCount Property (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2028334a2fc1d63262d9f109cb6f76c624b64e3a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485534"
---
# <a name="indexdistinctcount-property-dao"></a>Index.DistinctCount Property (DAO)

**Se aplica a**: Access 2013 | Office 2013

Devuelve un valor que indica el número de valores únicos del objeto **[Index](index-object-dao.md)** que se incluyen en la tabla asociada (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . DistinctCount

*expresión* Variable que representa un objeto **Index** .

## <a name="remarks"></a>Observaciones

Compruebe la propiedad **DistinctCount** para determinar el número de valores únicos, o claves, de un índice. Una clave se cuenta sólo una vez, aunque haya varias repeticiones de dicho valor si el índice permite valores duplicados. Esta información es útil en aplicaciones que intentan optimizar el acceso a los datos evaluando la información del índice. El número de valores únicos se conoce también como la cardinalidad de un objeto **Index**.

La propiedad **DistinctCount** no reflejará siempre el número real de claves en un momento determinado. Por ejemplo, un cambio causado por una transacción revertida no se reflejará inmediatamente en la propiedad **DistinctCount**. También es posible que el valor de la propiedad **DistinctCount** no refleje la eliminación de registros con claves únicas. El número será preciso inmediatamente después de usar el método **[CreateIndex](tabledef-createindex-method-dao.md)**.

## <a name="example"></a>Ejemplo

En este ejemplo, se usa la propiedad **DistinctCount** para mostrar cómo se puede determinar el número de valores únicos de un objeto **Index**. Sin embargo, este valor sólo es preciso inmediatamente después de crear el objeto **Index**. Seguirá siendo preciso si ninguna clave cambia o si se agregan claves nuevas y no se elimina ninguna clave antigua; de lo contrario, no será confiable. Si se ejecuta este procedimiento varias veces, puede ver el efecto sobre los valores de la propiedad **DistinctCount** de los objetos Index existentes.

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
