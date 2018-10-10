---
title: Relation.Attributes Property (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f07435f573d48e94b0f6b2b9f3b5fcfcd043239e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484912"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="13c70-102">Relation.Attributes Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="13c70-102">Relation.Attributes Property (DAO)</span></span>


<span data-ttu-id="13c70-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="13c70-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="13c70-p101">Establece o devuelve un valor que indica una o varias características del objeto **Relation**. **Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="13c70-p101">Sets or returns a value that indicates one or more characteristics of a **Relation** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c70-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13c70-106">Syntax</span></span>

<span data-ttu-id="13c70-107">*expresión* . Atributos</span><span class="sxs-lookup"><span data-stu-id="13c70-107">*expression* .Attributes</span></span>

<span data-ttu-id="13c70-108">*expresión* Variable que representa un objeto **Relation** .</span><span class="sxs-lookup"><span data-stu-id="13c70-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c70-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13c70-109">Remarks</span></span>

<span data-ttu-id="13c70-110">Para un objeto no anexado todavía a una colección, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="13c70-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="13c70-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13c70-111">Example</span></span>

<span data-ttu-id="13c70-112">En este ejemplo, se muestra la propiedad **Attributes** para los objetos **Field**, **Relation** y **TableDef** de la base de datos Northwind.</span><span class="sxs-lookup"><span data-stu-id="13c70-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

