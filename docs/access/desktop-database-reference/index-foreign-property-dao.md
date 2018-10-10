---
title: Index.Foreign Property (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 410629c3e5ebec47dd8acefd852379ee74568832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485060"
---
# <a name="indexforeign-property-dao"></a>Index.Foreign Property (DAO)

**Se aplica a**: Access 2013 | Office 2013

Devuelve un valor que indica si un objeto **[Index](index-object-dao.md)** representa una clave externa en una tabla (solo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Externa

*expresión* Variable que representa un objeto **Index** .

## <a name="remarks"></a>Observaciones

El valor devuelto es un tipo de datos **Boolean** que devuelve **True** si el objeto **Index** representa una clave externa.

Una clave externa consiste en uno o más campos en una tabla externa que identifica únicamente todas las filas en una tabla principal.

El motor de base de datos Microsoft Access crea un objeto **Index** para la tabla externa y establece la propiedad **Foreign** cuando usted crea una relación que fuerza la integridad referencial.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo la propiedad **Foreign** puede indicar los objetos **Index** en **TableDef** que son índices de claves externas. Esos índices se crean mediante un motor de base de datos Microsoft Access cuando se crea un objeto **Relation**. El nombre predeterminado para los índices de claves externas es el nombre de la tabla principal más el nombre de la tabla externa. Se requiere la función ForeignOutput para que pueda ejecutarse este procedimiento.

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
