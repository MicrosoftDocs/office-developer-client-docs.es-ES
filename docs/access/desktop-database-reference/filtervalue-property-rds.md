---
title: FilterValue (propiedad, RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721951"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="f32c7-102">FilterValue (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="f32c7-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="f32c7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f32c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f32c7-104">Indica el valor mediante el que se van a filtrar registros.</span><span class="sxs-lookup"><span data-stu-id="f32c7-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f32c7-105">Syntax</span></span>

<span data-ttu-id="f32c7-106">*DataControl*. FilterValue = *cadena*</span><span class="sxs-lookup"><span data-stu-id="f32c7-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="f32c7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f32c7-107">Parameters</span></span>

|<span data-ttu-id="f32c7-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f32c7-108">Parameter</span></span>|<span data-ttu-id="f32c7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f32c7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f32c7-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f32c7-110">*DataControl*</span></span> |<span data-ttu-id="f32c7-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f32c7-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="f32c7-112">*String*</span><span class="sxs-lookup"><span data-stu-id="f32c7-112">*String*</span></span> |<span data-ttu-id="f32c7-113">Un valor de **tipo String** que representa un valor de datos con el que se va a filtrar registros (por ejemplo, 'Programmer' o 125).</span><span class="sxs-lookup"><span data-stu-id="f32c7-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="f32c7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f32c7-114">Remarks</span></span>

<span data-ttu-id="f32c7-115">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente.</span><span class="sxs-lookup"><span data-stu-id="f32c7-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="f32c7-116">La función de ordenación ordena los registros por los valores de una columna.</span><span class="sxs-lookup"><span data-stu-id="f32c7-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="f32c7-117">La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="f32c7-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="f32c7-118">El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="f32c7-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="f32c7-119">Los valores nulos dan lugar a un error de falta de coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="f32c7-119">Null values result in a type mismatch error.</span></span>

