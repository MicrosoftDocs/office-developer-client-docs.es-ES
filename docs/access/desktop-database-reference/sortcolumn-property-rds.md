---
title: SortColumn (propiedad, RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61d31ba6044448d2b2534d6affa6157765e9cbc7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949638"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="bf219-102">SortColumn (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="bf219-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="bf219-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf219-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf219-104">Indica la columna por la que se van a ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="bf219-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf219-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf219-105">Syntax</span></span>

<span data-ttu-id="bf219-106">*DataControl*. SortColumn = *cadena*</span><span class="sxs-lookup"><span data-stu-id="bf219-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="bf219-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf219-107">Parameters</span></span>

|<span data-ttu-id="bf219-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bf219-108">Parameter</span></span>|<span data-ttu-id="bf219-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf219-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bf219-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="bf219-110">*DataControl*</span></span> |<span data-ttu-id="bf219-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="bf219-112">*String*</span><span class="sxs-lookup"><span data-stu-id="bf219-112">*String*</span></span> |<span data-ttu-id="bf219-113">Un valor de tipo **String** que representa el nombre o el alias de la columna mediante la que se ordenan los registros.</span><span class="sxs-lookup"><span data-stu-id="bf219-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bf219-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf219-114">Remarks</span></span>

<span data-ttu-id="bf219-p101">Las propiedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="bf219-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="bf219-119">Para ordenar un objeto **Recordset**, en primer lugar se deben guardar los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="bf219-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="bf219-120">Si se usa **RDS.DataControl**, se puede usar el método [SubmitChanges](submitchanges-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="bf219-121">Por ejemplo, si su **RDS. DataControl** es denomina ADC1, el código será ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="bf219-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="bf219-122">Si se usa un objeto **Recordset** ADO, es posible usar su método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="bf219-123">**UpdateBatch** es el método recomendado para los objetos **Recordset** creados con el método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="bf219-124">Por ejemplo, el código podría ser myRS.UpdateBatch o.</span><span class="sxs-lookup"><span data-stu-id="bf219-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="bf219-125">Si se usa un objeto **Recordset** ADO, es posible usar su método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="bf219-126">**UpdateBatch** es el método recomendado para los objetos **Recordset** creados con el método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bf219-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="bf219-127">Por ejemplo, el código podría ser myRS.UpdateBatch o ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="bf219-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

