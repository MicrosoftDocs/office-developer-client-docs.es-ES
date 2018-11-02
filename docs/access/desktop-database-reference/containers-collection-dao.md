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
# <a name="containers-collection-dao"></a><span data-ttu-id="7f7b7-102">Colección Containers (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f7b7-102">Containers collection (DAO)</span></span>

<span data-ttu-id="7f7b7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f7b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f7b7-104">Una colección **Containers** contiene todos los objetos de **contenedor** que se definen en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="7f7b7-104">A **Containers** collection contains all of the **Container** objects that are defined in a database.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f7b7-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f7b7-105">Remarks</span></span>

<span data-ttu-id="7f7b7-106">Cada objeto **Database** tiene una colección **Containers** que consta de objetos **Container** integrados.</span><span class="sxs-lookup"><span data-stu-id="7f7b7-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="7f7b7-107">Algunos de estos objetos **Container** están definidos por el motor de base de datos de Microsoft Access mientras que otros pueden estar definidos por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7f7b7-107">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span>

## <a name="example"></a><span data-ttu-id="7f7b7-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f7b7-108">Example</span></span>

<span data-ttu-id="7f7b7-109">En este ejemplo se enumera la colección **Containers** de la base de datos Northwind y la colección **Properties** de cada objeto **Container** de la colección.</span><span class="sxs-lookup"><span data-stu-id="7f7b7-109">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

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
