---
title: FilterColumn (propiedad, RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459fc61dbb8c8b1eecffdea3d2c5d2f105b9212a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484180"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="3c355-102">FilterColumn (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="3c355-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="3c355-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c355-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3c355-104">Indica la columna en la que evaluar los criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="3c355-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c355-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c355-105">Syntax</span></span>

<span data-ttu-id="3c355-106">*DataControl*. FilterColumn = *cadena*</span><span class="sxs-lookup"><span data-stu-id="3c355-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3c355-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c355-107">Parameters</span></span>

  - <span data-ttu-id="3c355-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3c355-108">*DataControl*</span></span>

  - <span data-ttu-id="3c355-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3c355-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="3c355-110">*String*</span><span class="sxs-lookup"><span data-stu-id="3c355-110">*String*</span></span>

  - <span data-ttu-id="3c355-p101">Un valor de tipo **String** que especifica la columna en la que evaluar los criterios de filtro. Los criterios de filtro se especifican en la propiedad [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3c355-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c355-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c355-113">Remarks</span></span>

<span data-ttu-id="3c355-p102">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y **FilterColumn** proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="3c355-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

