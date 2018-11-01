---
title: Los límites de un conjunto de registros
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 953e6c030c8ca4155b17603c03921e97fe3748e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887288"
---
# <a name="the-limits-of-a-recordset"></a><span data-ttu-id="f09f2-102">Los límites de un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="f09f2-102">The Limits of a Recordset</span></span>


<span data-ttu-id="f09f2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f09f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f09f2-p101">Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se han sobrepasado los límites de un objeto **Recordset** al moverse de un registro a otro. Considere **BOF** y **EOF** como registros "fantasma" situados al principio y al final del **conjunto de registros**. Trabajando con el **conjunto de registros** de ejemplo de [Examinar datos](chapter-3-examining-data.md), ahora tendría este aspecto:</span><span class="sxs-lookup"><span data-stu-id="f09f2-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f09f2-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="f09f2-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="f09f2-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="f09f2-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="f09f2-109">UnitPrice (PrecioUnitario)</span><span class="sxs-lookup"><span data-stu-id="f09f2-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f09f2-110">BOF</span><span class="sxs-lookup"><span data-stu-id="f09f2-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f09f2-111">7</span><span class="sxs-lookup"><span data-stu-id="f09f2-111">7</span></span></p></td>
<td><p><span data-ttu-id="f09f2-112">Peras secas orgánicas del tío Bob</span><span class="sxs-lookup"><span data-stu-id="f09f2-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="f09f2-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="f09f2-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f09f2-114">14</span><span class="sxs-lookup"><span data-stu-id="f09f2-114">14</span></span></p></td>
<td><p><span data-ttu-id="f09f2-115">Cuajada de judías</span><span class="sxs-lookup"><span data-stu-id="f09f2-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="f09f2-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="f09f2-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f09f2-117">28</span><span class="sxs-lookup"><span data-stu-id="f09f2-117">28</span></span></p></td>
<td><p><span data-ttu-id="f09f2-118">Col fermentada Rössle</span><span class="sxs-lookup"><span data-stu-id="f09f2-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="f09f2-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="f09f2-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f09f2-120">51</span><span class="sxs-lookup"><span data-stu-id="f09f2-120">51</span></span></p></td>
<td><p><span data-ttu-id="f09f2-121">Manzanas secas Manjimup</span><span class="sxs-lookup"><span data-stu-id="f09f2-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="f09f2-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="f09f2-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f09f2-123">74</span><span class="sxs-lookup"><span data-stu-id="f09f2-123">74</span></span></p></td>
<td><p><span data-ttu-id="f09f2-124">Queso de soja Longlife</span><span class="sxs-lookup"><span data-stu-id="f09f2-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="f09f2-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="f09f2-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f09f2-126">EOF</span><span class="sxs-lookup"><span data-stu-id="f09f2-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f09f2-127">La propiedad **BOF** devuelve **True** (-1) si la posición del registro activo es anterior al primer registro y **False** (0) si la posición del registro activo está en el primer registro o después de él.</span><span class="sxs-lookup"><span data-stu-id="f09f2-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="f09f2-128">La propiedad **EOF** devuelve **True** si la posición del registro activo es posterior al último registro y **False** si la posición del registro activo está en el último registro o antes de él.</span><span class="sxs-lookup"><span data-stu-id="f09f2-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="f09f2-129">Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro activo, como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="f09f2-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="f09f2-130">Si se abre un objeto **Recordset** que no contiene ningún registro, las propiedades **BOF** y **EOF** se establecen en **True** y el valor de la propiedad **RecordCount** del objeto **Recordset** dependerá del tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="f09f2-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="f09f2-131">para los cursores dinámicos, se devolverá -1 (**CursorType** = **adOpenDynamic**) y, para otros cursores, se devolverá 0.</span><span class="sxs-lookup"><span data-stu-id="f09f2-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="f09f2-132">Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el activo y las propiedades **BOF** y **EOF** son **False**.</span><span class="sxs-lookup"><span data-stu-id="f09f2-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="f09f2-p103">Si se elimina el último registro que queda en el objeto **Recordset**, el cursor queda en un estado indeterminado. Las propiedades **BOF** y **EOF** pueden permanecer en **False** hasta que se intente ajustar la posición del registro activo, dependiendo del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f09f2-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

