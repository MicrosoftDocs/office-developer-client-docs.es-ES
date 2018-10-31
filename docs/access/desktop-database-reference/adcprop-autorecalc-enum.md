---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b9c1aff21b62eff061a3f68ef3ad56e07e46388d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860087"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="2f7bc-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="2f7bc-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="2f7bc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f7bc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f7bc-104">Especifica cuándo el proveedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) debe volver a calcular las columnas agregadas y calculadas de un objeto Recordset jerárquico.</span><span class="sxs-lookup"><span data-stu-id="2f7bc-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="2f7bc-105">Estas constantes sólo se utilizan con el proveedor **MSDataShape** y la propiedad dinámica "**Auto Recalc**" del **Recordset** , que se hace referencia en el [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) y se explica en el [servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) o la documentación de [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7bc-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f7bc-106">Constante</span><span class="sxs-lookup"><span data-stu-id="2f7bc-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2f7bc-107">Valor</span><span class="sxs-lookup"><span data-stu-id="2f7bc-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2f7bc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f7bc-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f7bc-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="2f7bc-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="2f7bc-110">1</span><span class="sxs-lookup"><span data-stu-id="2f7bc-110">1</span></span></p></td>
<td><p><span data-ttu-id="2f7bc-p101">Valor predeterminado. Vuelve a calcular siempre que el proveedor <strong>MSDataShape</strong> determine que han cambiado los valores de los que dependen las columnas calculadas.</span><span class="sxs-lookup"><span data-stu-id="2f7bc-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f7bc-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="2f7bc-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="2f7bc-114">0</span><span class="sxs-lookup"><span data-stu-id="2f7bc-114">0</span></span></p></td>
<td><p><span data-ttu-id="2f7bc-115">Calcula solo al generar inicialmente el objeto <strong>Recordset</strong> jerárquico.</span><span class="sxs-lookup"><span data-stu-id="2f7bc-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2f7bc-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2f7bc-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2f7bc-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="2f7bc-117">These constants do not have ADO/WFC equivalents.</span></span>

