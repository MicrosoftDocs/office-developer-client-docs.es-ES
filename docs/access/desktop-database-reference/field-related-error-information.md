---
title: Información de errores relacionados con campos
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292975"
---
# <a name="field-related-error-information"></a><span data-ttu-id="6e9b4-102">Información de errores relacionados con campos</span><span class="sxs-lookup"><span data-stu-id="6e9b4-102">Field-related error information</span></span>


<span data-ttu-id="6e9b4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e9b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e9b4-p101">Si un error está relacionado directamente con un campo (por ejemplo, si faltan datos o si no son del tipo correcto para el campo), puede recuperar más información sobre la causa del problema examinando la propiedad **Status** del objeto **Field**. Esta propiedad se ha mejorado para que proporcione información específica sobre el problema. Así pues, por ejemplo, si una llamada a **UpdateBatch** falla, la causa del problema se puede determinar examinando la propiedad **Status** de los **campos** en cada uno de los registros afectados. La propiedad contendrá uno de los valores de la constante **FieldStatusEnum**. La tabla siguiente incluye los valores que son especialmente interesantes cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-p101">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property. This property has been enhanced to provide specific information about the problem. So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records. The property will contain one of the values in the **FieldStatusEnum** constant. The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e9b4-109">Constante</span><span class="sxs-lookup"><span data-stu-id="6e9b4-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e9b4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6e9b4-110">Value</span></span></p></th>
<th><p><span data-ttu-id="6e9b4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e9b4-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e9b4-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-113">2 </span><span class="sxs-lookup"><span data-stu-id="6e9b4-113">2</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-114">Indica que el campo no se puede recuperar ni almacenar sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9b4-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-116">6 </span><span class="sxs-lookup"><span data-stu-id="6e9b4-116">6</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-117">Indica que los datos devueltos por el proveedor desbordaron el tipo de datos del campo.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9b4-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-119">13 </span><span class="sxs-lookup"><span data-stu-id="6e9b4-119">13</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-120">Indica que se utilizó el valor predeterminado del campo al configurar datos.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9b4-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-122">15 </span><span class="sxs-lookup"><span data-stu-id="6e9b4-122">15</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-p102">Indica que este campo se omitió cuando se establecieron valores de datos en el origen. El proveedor no estableció ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-p102">Indicates that this field was skipped when setting data values in the source. No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9b4-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-126">10  </span><span class="sxs-lookup"><span data-stu-id="6e9b4-126">10</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-127">Indica que el campo no se puede modificar porque es una entidad calculada o derivada.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9b4-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-129">3 </span><span class="sxs-lookup"><span data-stu-id="6e9b4-129">3</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-130">Indica que el proveedor devolvió un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9b4-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="6e9b4-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="6e9b4-132">22</span><span class="sxs-lookup"><span data-stu-id="6e9b4-132">22</span></span></p></td>
<td><p><span data-ttu-id="6e9b4-133">Indica que el proveedor no puede obtener suficiente espacio de almacenamiento para completar una operación de movimiento o de copia.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

