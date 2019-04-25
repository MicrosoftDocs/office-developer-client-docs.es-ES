---
title: Propiedad Recordset.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 630efdc4da5a9064f9dd9055e3ceabc0283d6d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307584"
---
# <a name="recordsetsort-property-dao"></a>Propiedad Recordset.Sort (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el criterio de ordenación para los registros de un objeto **[Recordset](recordset-object-dao.md)** (solo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expression* .Sort

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Puede usar la propiedad **Sort** con objetos **Recordset** de tipo Dynaset y Snapshot.

Cuando se configura esta propiedad para un objeto, se produce la ordenación cada vez que se crea un objeto **Recordset** a partir de ese objeto. El valor de la propiedad **Sort** invalida el criterio de ordenación especificado para un objeto **[QueryDef](querydef-object-dao.md)**.

El criterio de ordenación predeterminado es ascendente (de A a Z o de 0 a 100).

La propiedad **Sort** no se aplica a objetos **Recordset** de tipo tabla o de tipo de solo avance. Para ordenar un objeto **Recordset** de tipo tabla, use la propiedad **[Index](recordset-index-property-dao.md)**.

> [!NOTE]
> En muchos casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya los criterios de ordenación.

## <a name="example"></a>Ejemplo

En este ejemplo se cambia el valor de la propiedad **Sort** y se crea un nuevo objeto **Recordset** para demostrar el uso de dicha propiedad. Para que este procedimiento se ejecute se necesita la función SortOutput.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

Cuando se conocen los datos que quieren seleccionar, suele ser más eficaz crear un objeto **Recordset** con una instrucción SQL. En este ejemplo se muestra cómo se puede crear un objeto **Recordset** y obtener los mismos resultados que en el ejemplo anterior.

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
