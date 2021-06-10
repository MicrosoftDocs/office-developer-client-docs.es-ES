---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280525"
---
# <a name="adcprop_autorecalc_enum"></a><span data-ttu-id="223ca-102">ADCPROP \_ AUTORECALC \_ ENUM</span><span class="sxs-lookup"><span data-stu-id="223ca-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="223ca-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="223ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="223ca-104">Especifica cuándo el proveedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) debe volver a calcular las columnas agregadas y calculadas de un objeto Recordset jerárquico.</span><span class="sxs-lookup"><span data-stu-id="223ca-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="223ca-105">Estas constantes solo se usan con el proveedor **MSDataShape** y la propiedad dinámica **Recordset** "**Auto Recalc**", a la que se hace referencia en el Índice de propiedades dinámicas de [ADO](ado-dynamic-property-index.md) y se documenta en la documentación del Servicio [de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) de Microsoft para OLE DB o del Servicio de forma de datos de [Microsoft para OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)</span><span class="sxs-lookup"><span data-stu-id="223ca-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="223ca-106">Constante</span><span class="sxs-lookup"><span data-stu-id="223ca-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="223ca-107">Valor</span><span class="sxs-lookup"><span data-stu-id="223ca-107">Value</span></span></p></th>
<th><p><span data-ttu-id="223ca-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="223ca-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="223ca-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="223ca-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="223ca-110">1</span><span class="sxs-lookup"><span data-stu-id="223ca-110">1</span></span></p></td>
<td><p><span data-ttu-id="223ca-p101">Valor predeterminado. Vuelve a calcular siempre que el proveedor <strong>MSDataShape</strong> determine que han cambiado los valores de los que dependen las columnas calculadas.</span><span class="sxs-lookup"><span data-stu-id="223ca-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223ca-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="223ca-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="223ca-114">0</span><span class="sxs-lookup"><span data-stu-id="223ca-114">0</span></span></p></td>
<td><p><span data-ttu-id="223ca-115">Calcula solo al generar inicialmente el objeto <strong>Recordset</strong> jerárquico.</span><span class="sxs-lookup"><span data-stu-id="223ca-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="223ca-116">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="223ca-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="223ca-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="223ca-117">These constants do not have ADO/WFC equivalents.</span></span>

