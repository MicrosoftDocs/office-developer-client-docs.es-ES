---
title: Documents Collection (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ed91166c8a244c20848069ecfd936a25c10accd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878167"
---
# <a name="documents-collection-dao"></a><span data-ttu-id="dfa28-102">Documents Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="dfa28-102">Documents Collection (DAO)</span></span>


<span data-ttu-id="dfa28-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfa28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfa28-104">Una colección **Documents** contiene todos los objetos **Document** de un tipo de objeto específico (sólo bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dfa28-104">A **Documents** collection contains all of the **Document** objects for a specific type of object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa28-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfa28-105">Remarks</span></span>

<span data-ttu-id="dfa28-106">Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**.</span><span class="sxs-lookup"><span data-stu-id="dfa28-106">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span>

<span data-ttu-id="dfa28-107">Para hacer referencia a un objeto **Document** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfa28-107">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="dfa28-108">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="dfa28-108">**Documents**(0)</span></span>

  - <span data-ttu-id="dfa28-109">**Documentos** ("*nombre*")</span><span class="sxs-lookup"><span data-stu-id="dfa28-109">**Documents**("*name*")</span></span>

  - <span data-ttu-id="dfa28-110">**Documentos**\!\[*nombre*\]</span><span class="sxs-lookup"><span data-stu-id="dfa28-110">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="dfa28-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfa28-111">Example</span></span>

<span data-ttu-id="dfa28-112">En este ejemplo se enumera la colección **Documents** del contenedor Tables y, a continuación, se enumera la colección **Properties** del primer objeto **Document** de la colección.</span><span class="sxs-lookup"><span data-stu-id="dfa28-112">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

