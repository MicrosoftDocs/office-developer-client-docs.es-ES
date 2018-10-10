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
# <a name="indexforeign-property-dao"></a><span data-ttu-id="79898-102">Index.Foreign Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="79898-102">Index.Foreign Property (DAO)</span></span>

<span data-ttu-id="79898-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="79898-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="79898-p101">Devuelve un valor que indica si un objeto **[Index](index-object-dao.md)** representa una clave externa en una tabla (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="79898-p101">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="79898-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79898-106">Syntax</span></span>

<span data-ttu-id="79898-107">*expresión* . Externa</span><span class="sxs-lookup"><span data-stu-id="79898-107">*expression* .Foreign</span></span>

<span data-ttu-id="79898-108">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="79898-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="79898-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79898-109">Remarks</span></span>

<span data-ttu-id="79898-110">El valor devuelto es un tipo de datos **Boolean** que devuelve **True** si el objeto **Index** representa una clave externa.</span><span class="sxs-lookup"><span data-stu-id="79898-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="79898-111">Una clave externa consiste en uno o más campos en una tabla externa que identifica únicamente todas las filas en una tabla principal.</span><span class="sxs-lookup"><span data-stu-id="79898-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="79898-112">El motor de base de datos Microsoft Access crea un objeto **Index** para la tabla externa y establece la propiedad **Foreign** cuando usted crea una relación que fuerza la integridad referencial.</span><span class="sxs-lookup"><span data-stu-id="79898-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="79898-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79898-113">Example</span></span>

<span data-ttu-id="79898-p102">En este ejemplo se muestra cómo la propiedad **Foreign** puede indicar los objetos **Index** en **TableDef** que son índices de claves externas. Esos índices se crean mediante un motor de base de datos Microsoft Access cuando se crea un objeto **Relation**. El nombre predeterminado para los índices de claves externas es el nombre de la tabla principal más el nombre de la tabla externa. Se requiere la función ForeignOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="79898-p102">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.</span></span>

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