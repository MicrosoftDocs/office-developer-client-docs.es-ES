---
title: Index.Unique Property (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 877be95d2cd65b020946f125714e0229650d5ec5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871888"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="95186-102">Index.Unique Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="95186-102">Index.Unique Property (DAO)</span></span>

<span data-ttu-id="95186-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95186-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95186-104">Establece o devuelve un valor que indica si un objeto **[Index](index-object-dao.md)** representa un índice (clave) único para una tabla (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="95186-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="95186-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95186-105">Syntax</span></span>

<span data-ttu-id="95186-106">*expresión* . Único</span><span class="sxs-lookup"><span data-stu-id="95186-106">*expression* .Unique</span></span>

<span data-ttu-id="95186-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="95186-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95186-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95186-108">Remarks</span></span>

<span data-ttu-id="95186-109">El valor de esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección; a partir de ese momento, es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="95186-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="95186-p101">Un índice único consta de uno o varios campos que organizan de forma lógica todos los registros de una tabla según un orden único predefinido. Si el índice consta de un campo, los valores de dicho campo deben ser únicos en toda la tabla. Si el índice consta de varios campos, cada campo puede contener valores duplicados, pero cada combinación de valores de todos los campos indizados deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="95186-p101">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order. If the index consists of one field, values in that field must be unique for the entire table. If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="95186-p102">Si las propiedades **Unique** y **[Primary](index-primary-property-dao.md)** de un objeto **Index** se establecen en **True**, el índice es único y principal: identifica de forma única todos los registros de la tabla en un orden lógico predefinido. Si la propiedad **Primary** se establece en **False**, el índice es un índice secundario. Los índices secundarios (ya sean o no clave) organizan de forma lógica los registros según un orden predefinido y no actúan como identificadores de los registros de la tabla.</span><span class="sxs-lookup"><span data-stu-id="95186-p102">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order. If the **Primary** property is set to **False**, the index is a secondary index. Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="95186-116">No tiene que crear índices para las tablas pero, en tablas grandes sin indizar, el acceso a un registro concreto puede durar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="95186-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span></P>
> <LI>
> <P><span data-ttu-id="95186-117">Los registros recuperados de tablas sin índices se devuelven sin seguir una secuencia concreta.</span><span class="sxs-lookup"><span data-stu-id="95186-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="95186-118">La propiedad <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> de cada objeto <STRONG><A href="field-object-dao.md">Field</A></STRONG> del objeto <STRONG>Index</STRONG> determina el orden de los registros y, por lo tanto, determina las técnicas de acceso que se utilizan para ese objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="95186-118">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that <STRONG>Index</STRONG> object.</span></span></P>
> <LI>
> <P><span data-ttu-id="95186-119">Un índice único ayuda a optimizar la búsqueda de registros.</span><span class="sxs-lookup"><span data-stu-id="95186-119">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="95186-120">Los índices no afectan al orden físico de una tabla base; solo afectan a cómo el objeto <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> de tipo tabla obtiene acceso a los registros cuando se elige un índice concreto o cuando el motor de base de datos de Microsoft Access crea objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="95186-120">Indexes don't affect the physical order of a base table indexes affect only how the records are accessed by the table-type <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> object when a particular index is chosen or when the Microsoft Access database engine creates <STRONG>Recordset</STRONG> objects.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="95186-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95186-121">Example</span></span>

<span data-ttu-id="95186-p103">En este ejemplo, la propiedad **Unique** de un objeto **Index** nuevo se establece en **True**, y se anexa el objeto Index a la colección **Indexes** de la tabla Employees. A continuación, se enumera la colección **Indexes** del objeto **TableDef** y la colección **Properties** de cada objeto **Index**. El nuevo objeto **Index** sólo permitirá un registro con una combinación concreta de Country, LastName y FirstName en el objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="95186-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
