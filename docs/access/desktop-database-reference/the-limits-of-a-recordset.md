---
title: Los límites de un conjunto de registros
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314116"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="9c1df-102">Límites de un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="9c1df-102">Limits of a Recordset</span></span>


<span data-ttu-id="9c1df-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c1df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c1df-p101">Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se han sobrepasado los límites de un objeto **Recordset** al moverse de un registro a otro. Considere **BOF** y **EOF** como registros "fantasma" situados al principio y al final del **conjunto de registros**. Trabajando con el **conjunto de registros** de ejemplo de [Examinar datos](chapter-3-examining-data.md), ahora tendría este aspecto:</span><span class="sxs-lookup"><span data-stu-id="9c1df-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c1df-107">Cuyo</span><span class="sxs-lookup"><span data-stu-id="9c1df-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="9c1df-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="9c1df-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="9c1df-109">UnitPrice</span><span class="sxs-lookup"><span data-stu-id="9c1df-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c1df-110">BOF</span><span class="sxs-lookup"><span data-stu-id="9c1df-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c1df-111">0,7</span><span class="sxs-lookup"><span data-stu-id="9c1df-111">7</span></span></p></td>
<td><p><span data-ttu-id="9c1df-112">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="9c1df-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="9c1df-113">30,0000</span><span class="sxs-lookup"><span data-stu-id="9c1df-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c1df-114">apartado</span><span class="sxs-lookup"><span data-stu-id="9c1df-114">14</span></span></p></td>
<td><p><span data-ttu-id="9c1df-115">Judías</span><span class="sxs-lookup"><span data-stu-id="9c1df-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="9c1df-116">23,2500</span><span class="sxs-lookup"><span data-stu-id="9c1df-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c1df-117">28</span><span class="sxs-lookup"><span data-stu-id="9c1df-117">28</span></span></p></td>
<td><p><span data-ttu-id="9c1df-118">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="9c1df-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="9c1df-119">45,6000</span><span class="sxs-lookup"><span data-stu-id="9c1df-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c1df-120">51</span><span class="sxs-lookup"><span data-stu-id="9c1df-120">51</span></span></p></td>
<td><p><span data-ttu-id="9c1df-121">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="9c1df-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="9c1df-122">53,0000</span><span class="sxs-lookup"><span data-stu-id="9c1df-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c1df-123">74</span><span class="sxs-lookup"><span data-stu-id="9c1df-123">74</span></span></p></td>
<td><p><span data-ttu-id="9c1df-124">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="9c1df-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="9c1df-125">10,0000</span><span class="sxs-lookup"><span data-stu-id="9c1df-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c1df-126">EOF</span><span class="sxs-lookup"><span data-stu-id="9c1df-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c1df-127">La propiedad **BOF** devuelve **True** (-1) si la posición de registro actual se sitúa delante del primer registro y devuelve **False** (0) si la posición de registro actual se sitúa en el primer registro o después del mismo.</span><span class="sxs-lookup"><span data-stu-id="9c1df-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="9c1df-128">La propiedad **EOF** devuelve **True** si la posición del registro activo es posterior al último registro y **False** si la posición del registro activo está en el último registro o antes de él.</span><span class="sxs-lookup"><span data-stu-id="9c1df-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="9c1df-129">Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro activo, como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c1df-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="9c1df-130">Si se abre un objeto **Recordset** que no contiene ningún registro, las propiedades **BOF** y **EOF** se establecen en **True** y el valor de la propiedad **RecordCount** del objeto **Recordset** dependerá del tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="9c1df-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="9c1df-131">se devolverá-1 para cursores dinámicos (**CursorType** = **adOpenDynamic**) y 0 se devolverá para otros cursores.</span><span class="sxs-lookup"><span data-stu-id="9c1df-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="9c1df-132">Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el activo y las propiedades **BOF** y **EOF** son **False**.</span><span class="sxs-lookup"><span data-stu-id="9c1df-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="9c1df-p103">Si se elimina el último registro que queda en el objeto **Recordset**, el cursor queda en un estado indeterminado. Las propiedades **BOF** y **EOF** pueden permanecer en **False** hasta que se intente ajustar la posición del registro activo, dependiendo del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9c1df-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

