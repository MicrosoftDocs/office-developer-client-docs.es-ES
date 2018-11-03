---
title: SortDirection (propiedad, RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aef8b658bbe16c7b56c97900edb5a9c6bf1e8a0c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929646"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="f9624-102">SortDirection (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="f9624-102">SortDirection property (RDS)</span></span>


<span data-ttu-id="f9624-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9624-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f9624-104">Indica si un criterio de ordenación es ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="f9624-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9624-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9624-105">Syntax</span></span>

<span data-ttu-id="f9624-106">*DataControl*. SortDirection = *valor*</span><span class="sxs-lookup"><span data-stu-id="f9624-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="f9624-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9624-107">Parameters</span></span>

  - <span data-ttu-id="f9624-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f9624-108">*DataControl*</span></span>

  - <span data-ttu-id="f9624-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f9624-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="f9624-110">*Valor*</span><span class="sxs-lookup"><span data-stu-id="f9624-110">*Value*</span></span>

  - <span data-ttu-id="f9624-p101">Un valor de tipo **Boolean** que, si está establecido en **True**, indica que el orden es ascendente. **False** indica un orden descendente.</span><span class="sxs-lookup"><span data-stu-id="f9624-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9624-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9624-113">Remarks</span></span>

<span data-ttu-id="f9624-p102">Las propiedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método **Reset** ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="f9624-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

