---
title: Propiedad Recordset.Restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 26d9d215c35e9a768a663d41ecc40f49bee4dfdb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920861"
---
# <a name="recordsetrestartable-property-dao"></a><span data-ttu-id="46c12-102">Propiedad Recordset.Restartable (DAO)</span><span class="sxs-lookup"><span data-stu-id="46c12-102">Recordset.Restartable property (DAO)</span></span>


<span data-ttu-id="46c12-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46c12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46c12-104">Devuelve un valor que indica si un objeto **[Recordset](recordset-object-dao.md)** admite el método **[Requery](recordset-requery-method-dao.md)**, método que vuelve a ejecutar la consulta en la que se basa el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="46c12-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c12-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46c12-105">Syntax</span></span>

<span data-ttu-id="46c12-106">*expresión* . Restartable</span><span class="sxs-lookup"><span data-stu-id="46c12-106">*expression* .Restartable</span></span>

<span data-ttu-id="46c12-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="46c12-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46c12-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46c12-108">Remarks</span></span>

<span data-ttu-id="46c12-109">Los objetos **Recordset** de tipo Table siempre devuelven **False**.</span><span class="sxs-lookup"><span data-stu-id="46c12-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="46c12-p101">Compruebe la propiedad **Restartable** antes de usar el método **Requery** en un objeto **Recordset**. Si la propiedad **Restartable** del objeto está establecida en **False**, utilice el método **[OpenRecordset](connection-openrecordset-method-dao.md)** en el objeto base **[QueryDef](querydef-object-dao.md)** para volver a ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="46c12-p101">Check the **Restartable** property before using the **Requery** method on a **Recordset** object. If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="46c12-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46c12-112">Example</span></span>

<span data-ttu-id="46c12-113">En este ejemplo se muestra la propiedad **Restartable** con distintos objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="46c12-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
