---
title: Propiedad TableDef.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abdb0d07f2293a53fccaf0d628c301750027acc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716163"
---
# <a name="tabledefattributes-property-dao"></a><span data-ttu-id="57067-102">Propiedad TableDef.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="57067-102">TableDef.Attributes property (DAO)</span></span>


<span data-ttu-id="57067-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57067-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="57067-p101">Establece o devuelve un valor que indica una o más características de un objeto **TableDef**. **Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="57067-p101">Sets or returns a value that indicates one or more characteristics of a **TableDef** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="57067-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57067-106">Syntax</span></span>

<span data-ttu-id="57067-107">*expresión* . Atributos</span><span class="sxs-lookup"><span data-stu-id="57067-107">*expression* .Attributes</span></span>

<span data-ttu-id="57067-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="57067-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="57067-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57067-109">Remarks</span></span>

<span data-ttu-id="57067-110">Para un objeto no anexado todavía a una colección, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="57067-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="57067-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="57067-111">Example</span></span>

<span data-ttu-id="57067-112">En este ejemplo, se muestra la propiedad **Attributes** para los objetos **Field**, **Relation** y **TableDef** de la base de datos Northwind.</span><span class="sxs-lookup"><span data-stu-id="57067-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

