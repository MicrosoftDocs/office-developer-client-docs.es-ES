---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 942639a4c87cfe325b9ec8326e2eb392458fa8b3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863695"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="a5f16-102">ADCPROP\_UPDATECRITERIA\_ENUM</span><span class="sxs-lookup"><span data-stu-id="a5f16-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="a5f16-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5f16-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5f16-104">Especifica qué campos se pueden usar para detectar conflictos durante una actualización optimista de una fila del origen de datos con un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5f16-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="a5f16-105">Use estas constantes con la propiedad dinámica "**Update Criteria**" del objeto **Recordset**, que aparece en el [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) y se explica en la documentación del [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="a5f16-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f16-106">Constante</span><span class="sxs-lookup"><span data-stu-id="a5f16-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="a5f16-107">Valor</span><span class="sxs-lookup"><span data-stu-id="a5f16-107">Value</span></span></p></th>
<th><p><span data-ttu-id="a5f16-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5f16-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-110">1</span><span class="sxs-lookup"><span data-stu-id="a5f16-110">1</span></span></p></td>
<td><p><span data-ttu-id="a5f16-111">Detecta conflictos si se ha cambiado cualquier columna de la fila del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="a5f16-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-113">0</span><span class="sxs-lookup"><span data-stu-id="a5f16-113">0</span></span></p></td>
<td><p><span data-ttu-id="a5f16-114">Detecta conflictos si se ha cambiado la columna de clave de la fila del origen de datos; es decir, se ha eliminado la fila.</span><span class="sxs-lookup"><span data-stu-id="a5f16-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-116">3</span><span class="sxs-lookup"><span data-stu-id="a5f16-116">3</span></span></p></td>
<td><p><span data-ttu-id="a5f16-117">Detecta conflictos si la marca de tiempo de la fila del origen de datos ha cambiado; es decir, se ha tenido acceso a la fila después de obtenerse el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5f16-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-119">2</span><span class="sxs-lookup"><span data-stu-id="a5f16-119">2</span></span></p></td>
<td><p><span data-ttu-id="a5f16-120">Detecta conflictos si se han cambiado columnas de la fila del origen de datos correspondientes a campos actualizados del objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5f16-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a5f16-121">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a5f16-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="a5f16-122">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a5f16-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f16-123">Constante</span><span class="sxs-lookup"><span data-stu-id="a5f16-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="a5f16-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="a5f16-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="a5f16-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="a5f16-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

