---
title: Propiedad Index.Primary (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: da0d28a5599dadc9432b38ab6155e53e884e4838
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291757"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="6228d-102">Propiedad Index.Primary (DAO)</span><span class="sxs-lookup"><span data-stu-id="6228d-102">Index.Primary property (DAO)</span></span>

<span data-ttu-id="6228d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6228d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6228d-104">Establece o devuelve un valor que indica si un objeto **[Index](index-object-dao.md)** representa un índice de clave principal en una tabla (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6228d-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6228d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6228d-105">Syntax</span></span>

<span data-ttu-id="6228d-106">*expresión* . Principal</span><span class="sxs-lookup"><span data-stu-id="6228d-106">*expression* .Primary</span></span>

<span data-ttu-id="6228d-107">*expresión* Variable que representa un **objeto Index.**</span><span class="sxs-lookup"><span data-stu-id="6228d-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6228d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6228d-108">Remarks</span></span>

<span data-ttu-id="6228d-p101">El valor de la propiedad **Primary** es de lectura y escritura para un nuevo objeto **Index** que todavía no está anexado a una colección y es de sólo lectura para un objeto **Index** existente en una colección **[Indexes](indexes-collection-dao.md)**. Si el objeto **Index** está anexado al objeto **[TableDef](tabledef-object-dao.md)** pero el objeto **TableDef** no está anexado a la colección **[TableDefs](tabledefs-collection-dao.md)**, la propiedad **Index** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6228d-p101">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection. If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="6228d-p102">Un índice de clave principal consiste en uno o varios campos que identifican de manera única todos los registros de una tabla según un orden predefinido. Como el campo de índice debe ser único, la propiedad **[Unique](index-unique-property-dao.md)** del objeto **Index** está establecida en **True**. Si el índice de clave principal se compone de varios campos, cada campo puede contener valores duplicados, pero cada combinación de valores de todos los campos indizados debe ser única. Un índice de clave principal se compone de una clave para la tabla y generalmente contiene los mismos campos que la clave principal.</span><span class="sxs-lookup"><span data-stu-id="6228d-p102">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**. If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique. A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>

> [!NOTE]
> <span data-ttu-id="6228d-p103">[!NOTA] No tiene que crear índices para las tablas, pero el proceso para tener acceso a un registro concreto en tablas grandes sin indizar puede durar mucho tiempo. La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** en el objeto **Index** determina el orden de los registros y, como consecuencia, se determinan las técnicas de acceso que hay que usar para ese índice. Al crear una nueva tabla en su base de datos, es recomendable crear un índice para uno o más campos que identifique cada registro de forma única y después establecer la propiedad **Primary** del objeto **Index** en **True**.</span><span class="sxs-lookup"><span data-stu-id="6228d-p103">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time. The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index. When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the **Primary** property of the **Index** object to **True**.</span></span>

<span data-ttu-id="6228d-118">Cuando se establece una clave principal en una tabla, la clave principal se define automáticamente como el índice de clave principal de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="6228d-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="6228d-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6228d-119">Example</span></span>

<span data-ttu-id="6228d-p104">En este ejemplo se utiliza la propiedad **Primary** para designar un nuevo **Index** en un nuevo **TableDef** como el **Index** principal para esa tabla. Observe que al establecer la propiedad **Primary** en **True** automáticamente se establecen las propiedades **Unique** y **Required** también en **True**.</span><span class="sxs-lookup"><span data-stu-id="6228d-p104">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table. Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
