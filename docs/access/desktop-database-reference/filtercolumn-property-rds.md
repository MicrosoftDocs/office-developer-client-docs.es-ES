---
title: Propiedad FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292443"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="b7beb-102">Propiedad FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="b7beb-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="b7beb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7beb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7beb-104">Indica la columna en la que evaluar los criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="b7beb-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7beb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7beb-105">Syntax</span></span>

<span data-ttu-id="b7beb-106">*DataControl*. FilterColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="b7beb-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="b7beb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7beb-107">Parameters</span></span>

|<span data-ttu-id="b7beb-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b7beb-108">Parameter</span></span>|<span data-ttu-id="b7beb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7beb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b7beb-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b7beb-110">*DataControl*</span></span> |<span data-ttu-id="b7beb-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b7beb-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="b7beb-112">*String*</span><span class="sxs-lookup"><span data-stu-id="b7beb-112">*String*</span></span> |<span data-ttu-id="b7beb-p101">Un valor de tipo **String** que especifica la columna en la que evaluar los criterios de filtro. Los criterios de filtro se especifican en la propiedad [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b7beb-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b7beb-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7beb-115">Remarks</span></span>

<span data-ttu-id="b7beb-116">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y **FilterColumn** proporcionan funciones de ordenación y filtrado en la memoria caché del cliente.</span><span class="sxs-lookup"><span data-stu-id="b7beb-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="b7beb-117">La función de ordenación ordena los registros por los valores de una columna.</span><span class="sxs-lookup"><span data-stu-id="b7beb-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="b7beb-118">La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b7beb-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="b7beb-119">El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="b7beb-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

