---
title: Colección Containers (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be25a2f8b5d6da7b569858d758b3fb541cf9be51
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920441"
---
# <a name="containers-collection-dao"></a>Colección Containers (DAO)

**Se aplica a**: Access 2013, Office 2013

Una colección **Containers** contiene todos los objetos de **contenedor** que se definen en una base de datos.

## <a name="remarks"></a>Observaciones

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
