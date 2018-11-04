---
title: FilterValue (propiedad, RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de54097c7992583851bbbd7b04c40f10fbca76e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949484"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="3eb8d-102">FilterValue (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="3eb8d-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="3eb8d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3eb8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3eb8d-104">Indica el valor mediante el que se van a filtrar registros.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3eb8d-105">Syntax</span></span>

<span data-ttu-id="3eb8d-106">*DataControl*. FilterValue = *cadena*</span><span class="sxs-lookup"><span data-stu-id="3eb8d-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3eb8d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3eb8d-107">Parameters</span></span>

|<span data-ttu-id="3eb8d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3eb8d-108">Parameter</span></span>|<span data-ttu-id="3eb8d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eb8d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3eb8d-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3eb8d-110">*DataControl*</span></span> |<span data-ttu-id="3eb8d-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3eb8d-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="3eb8d-112">*String*</span><span class="sxs-lookup"><span data-stu-id="3eb8d-112">*String*</span></span> |<span data-ttu-id="3eb8d-113">Un valor de **tipo String** que representa un valor de datos con el que se va a filtrar registros (por ejemplo, 'Programmer' o 125).</span><span class="sxs-lookup"><span data-stu-id="3eb8d-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="3eb8d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3eb8d-114">Remarks</span></span>

<span data-ttu-id="3eb8d-115">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="3eb8d-116">La función de ordenación ordena los registros por los valores de una columna.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="3eb8d-117">La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="3eb8d-118">El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="3eb8d-119">Los valores nulos dan lugar a un error de falta de coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="3eb8d-119">Null values result in a type mismatch error.</span></span>

