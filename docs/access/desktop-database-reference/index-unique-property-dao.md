---
title: Propiedad index. Unique (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291695"
---
# <a name="indexunique-property-dao"></a>Propiedad index. Unique (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica si un objeto **[Index](index-object-dao.md)** representa un índice (clave) único para una tabla (únicamente áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Singular

*expresión* Variable que representa un objeto **index** .

## <a name="remarks"></a>Comentarios

El valor de esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección; a partir de ese momento, es de sólo lectura.

Un índice único consta de uno o varios campos que organizan de forma lógica todos los registros de una tabla según un orden único predefinido. Si el índice consta de un campo, los valores de dicho campo deben ser únicos en toda la tabla. Si el índice consta de varios campos, cada campo puede contener valores duplicados, pero cada combinación de valores de todos los campos indizados deben ser únicos.

Si las propiedades **Unique** y **[Primary](index-primary-property-dao.md)** de un objeto **Index** se establecen en **True**, el índice es único y principal: identifica de forma única todos los registros de la tabla en un orden lógico predefinido. Si la propiedad **Primary** se establece en **False**, el índice es un índice secundario. Los índices secundarios (ya sean o no clave) organizan de forma lógica los registros según un orden predefinido y no actúan como identificadores de los registros de la tabla.

> [!NOTE]
> - No tiene que crear índices para las tablas pero, en tablas grandes sin indizar, el acceso a un registro concreto puede durar mucho tiempo.
> - Los registros recuperados de tablas sin índices se devuelven sin seguir una secuencia concreta.
> - La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** del objeto **Index** determina el orden de los registros y, por lo tanto, determina las técnicas de acceso que se utilizan para ese objeto **Index**.
> - Un índice único ayuda a optimizar la búsqueda de registros.
> - Los índices no afectan al orden físico de una tabla base; los índices afectan solo a cómo se obtiene acceso a los registros mediante el objeto **[Recordset](recordset-object-dao.md)** de tipo de tabla cuando se elige un índice en particular o cuando el motor de base de datos de Microsoft Access crea objetos **Recordset** .

## <a name="example"></a>Ejemplo

En este ejemplo, la propiedad **Unique** de un objeto **Index** nuevo se establece en **True**, y se anexa el objeto Index a la colección **Indexes** de la tabla Employees. A continuación, se enumera la colección **Indexes** del objeto **TableDef** y la colección **Properties** de cada objeto **Index**. El nuevo objeto **Index** sólo permitirá un registro con una combinación concreta de Country, LastName y FirstName en el objeto **TableDef**.

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
