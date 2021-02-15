---
title: Colección Containers (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c874a1555fa6a6f5f948275176c57b5fb1c48bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295607"
---
# <a name="containers-collection-dao"></a>Colección Containers (DAO)

**Se aplica a:** Access 2013, Office 2013

Una **colección Containers** contiene todos los objetos **Container** que se definen en una base de datos.

## <a name="remarks"></a>Comentarios

Cada objeto **Database** tiene una colección **Containers** que consta de objetos **Container** integrados. Algunos de estos objetos **Container** están definidos por el motor de base de datos de Microsoft Access mientras que otros pueden estar definidos por otras aplicaciones.

## <a name="example"></a>Ejemplo

En este ejemplo se enumera la colección **Containers** de la base de datos Northwind y la colección **Properties** de cada objeto **Container** de la colección.

```vb
    Sub ContainerObjectX()
    
       Dim dbsNorthwind As Database
       Dim ctrLoop As Container
       Dim prpLoop As Property
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
    
          ' Enumerate Containers collection.
          For Each ctrLoop In .Containers
             Debug.Print "Properties of " & ctrLoop.Name _
                & " container"
    
             ' Enumerate Properties collection of each
             ' Container object.
             For Each prpLoop In ctrLoop.Properties
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
