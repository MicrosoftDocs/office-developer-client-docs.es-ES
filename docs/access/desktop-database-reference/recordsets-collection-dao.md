---
title: Recordsets Collection (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8779a0a7ff8b298c8773d661deb525ab5aa3c04
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485972"
---
# <a name="recordsets-collection-dao"></a>Recordsets Collection (DAO)

**Se aplica a**: Access 2013 | Office 2013

Una colección **Recordsets** contiene todos los objetos **Recordset** abiertos en un objeto **Connection** o **Database**.

## <a name="remarks"></a>Observaciones

Cuando se utilizan objetos de DAO, los datos se tratan casi siempre mediante objetos **Recordset**.

Un objeto **Recordset** nuevo se agrega automáticamente a la colección **Recordsets** cuando se abre el objeto **Recordset** y se quita automáticamente cuando se cierra.

Se pueden crear tantas variables del objeto **Recordset** como sean necesarias. Diferentes objetos **Recordset** pueden tener acceso a las mismas tablas, consultas y campos sin entrar en conflicto.

Para hacer referencia a un objeto **Recordset** de una colección por su número ordinal o por su valor de la propiedad **Name**, use uno de los siguientes formatos de sintaxis:

- **Recordsets** (0)

- **Conjuntos de registros** ("nombre")

- **Conjuntos de registros**\!\[nombre\]

> [!NOTE]
> [!NOTA] Se puede abrir un objeto **Recordset** desde el mismo origen de datos o base de datos más de una vez, con lo que se crean nombres duplicados en la colección **Recordsets**. Debe asignar los objetos **Recordset** a variables de objeto y hacer referencia a ellos por el nombre de la variable.

## <a name="example"></a>Ejemplo

A continuación se ofrece una demostración de objetos **Recordset** y la colección **Recordsets**. En este ejemplo, se abren cuatro tipos diferentes de objetos **Recordsets**, se enumera la colección Recordsets del objeto **Database** actual y se enumera la colección **Properties** de cada objeto **Recordset**.

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
