---
title: SortDirection (propiedad, RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 256e6a878e9c3f382bcd65b9138df7a440bf118c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486083"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="c29f9-102">SortDirection (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="c29f9-102">SortDirection Property (RDS)</span></span>


<span data-ttu-id="c29f9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c29f9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="c29f9-104">Indica si un criterio de ordenación es ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="c29f9-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c29f9-105">Syntax</span></span>

<span data-ttu-id="c29f9-106">*DataControl*. SortDirection = *valor*</span><span class="sxs-lookup"><span data-stu-id="c29f9-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="c29f9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c29f9-107">Parameters</span></span>

  - <span data-ttu-id="c29f9-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c29f9-108">*DataControl*</span></span>

  - <span data-ttu-id="c29f9-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="c29f9-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="c29f9-110">*Valor*</span><span class="sxs-lookup"><span data-stu-id="c29f9-110">*Value*</span></span>

  - <span data-ttu-id="c29f9-p101">Un valor de tipo **Boolean** que, si está establecido en **True**, indica que el orden es ascendente. **False** indica un orden descendente.</span><span class="sxs-lookup"><span data-stu-id="c29f9-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="c29f9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c29f9-113">Remarks</span></span>

<span data-ttu-id="c29f9-p102">Las propiedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método **Reset** ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="c29f9-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

