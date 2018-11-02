---
title: Propiedad Index.DistinctCount (DAO)
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
ms.openlocfilehash: 62c8681baebf0c1959fcb86df91d61387070adc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923647"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="5cb38-102">Propiedad Index.DistinctCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cb38-102">Index.DistinctCount property (DAO)</span></span>

<span data-ttu-id="5cb38-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cb38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cb38-104">Devuelve un valor que indica el número de valores únicos del objeto **[Index](index-object-dao.md)** que se incluyen en la tabla asociada (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5cb38-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cb38-105">Syntax</span></span>

<span data-ttu-id="5cb38-106">*expresión* . DistinctCount</span><span class="sxs-lookup"><span data-stu-id="5cb38-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="5cb38-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="5cb38-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb38-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cb38-108">Remarks</span></span>

<span data-ttu-id="5cb38-p101">Compruebe la propiedad **DistinctCount** para determinar el número de valores únicos, o claves, de un índice. Una clave se cuenta sólo una vez, aunque haya varias repeticiones de dicho valor si el índice permite valores duplicados. Esta información es útil en aplicaciones que intentan optimizar el acceso a los datos evaluando la información del índice. El número de valores únicos se conoce también como la cardinalidad de un objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="5cb38-p101">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index. Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values. This information is useful in applications that attempt to optimize data access by evaluating index information. The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="5cb38-p102">La propiedad **DistinctCount** no reflejará siempre el número real de claves en un momento determinado. Por ejemplo, un cambio causado por una transacción revertida no se reflejará inmediatamente en la propiedad **DistinctCount**. También es posible que el valor de la propiedad **DistinctCount** no refleje la eliminación de registros con claves únicas. El número será preciso inmediatamente después de usar el método **[CreateIndex](tabledef-createindex-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="5cb38-p102">The **DistinctCount** property won't always reflect the actual number of keys at a particular time. For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property. The **DistinctCount** property value also may not reflect the deletion of records with unique keys. The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="5cb38-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cb38-117">Example</span></span>

<span data-ttu-id="5cb38-p103">En este ejemplo, se usa la propiedad **DistinctCount** para mostrar cómo se puede determinar el número de valores únicos de un objeto **Index**. Sin embargo, este valor sólo es preciso inmediatamente después de crear el objeto **Index**. Seguirá siendo preciso si ninguna clave cambia o si se agregan claves nuevas y no se elimina ninguna clave antigua; de lo contrario, no será confiable. Si se ejecuta este procedimiento varias veces, puede ver el efecto sobre los valores de la propiedad **DistinctCount** de los objetos Index existentes.</span><span class="sxs-lookup"><span data-stu-id="5cb38-p103">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
