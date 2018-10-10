---
title: Containers Collection (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b87aaf5eec856b17372627b0b298e36fa322ea5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486660"
---
# <a name="containers-collection-dao"></a><span data-ttu-id="e072d-102">Containers Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="e072d-102">Containers Collection (DAO)</span></span>

<span data-ttu-id="e072d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e072d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e072d-104">Una colección **Containers** contiene todos los objetos de **contenedor** que se definen en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e072d-104">A **Containers** collection contains all of the **Container** objects that are defined in a database.</span></span>

## <a name="remarks"></a><span data-ttu-id="e072d-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e072d-105">Remarks</span></span>

<span data-ttu-id="e072d-106">Cada objeto **Database** tiene una colección **Containers** que consta de objetos **Container** integrados.</span><span class="sxs-lookup"><span data-stu-id="e072d-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="e072d-107">Algunos de estos objetos **Container** están definidos por el motor de base de datos de Microsoft Access mientras que otros pueden estar definidos por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e072d-107">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span>

## <a name="example"></a><span data-ttu-id="e072d-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e072d-108">Example</span></span>

<span data-ttu-id="e072d-109">En este ejemplo se enumera la colección **Containers** de la base de datos Northwind y la colección **Properties** de cada objeto **Container** de la colección.</span><span class="sxs-lookup"><span data-stu-id="e072d-109">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

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
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
