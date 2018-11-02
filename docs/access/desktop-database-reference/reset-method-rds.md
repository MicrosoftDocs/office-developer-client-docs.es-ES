---
title: Método Reset (RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e336a7ddf4db6e927c185b33a4138ab8dd5d5e9a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925971"
---
# <a name="reset-method-rds"></a><span data-ttu-id="f280b-102">Reset (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="f280b-102">Reset method (RDS)</span></span>


<span data-ttu-id="f280b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f280b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f280b-104">Ordena o filtra un objeto **Recordset** de cliente según las propiedades de ordenación y filtro especificadas.</span><span class="sxs-lookup"><span data-stu-id="f280b-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f280b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f280b-105">Syntax</span></span>

<span data-ttu-id="f280b-106">*DataControl*. Reset (*valor*)</span><span class="sxs-lookup"><span data-stu-id="f280b-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f280b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f280b-107">Parameters</span></span>

  - <span data-ttu-id="f280b-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f280b-108">*DataControl*</span></span>

  - <span data-ttu-id="f280b-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f280b-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="f280b-110">*value*</span><span class="sxs-lookup"><span data-stu-id="f280b-110">*value*</span></span>

  - <span data-ttu-id="f280b-p101">Es opcional. Valor de tipo **Boolean** que es **True** (valor predeterminado) si se desea filtrar el conjunto de filas "filtrado" actual. El valor **False** indica que se va a filtrar el conjunto de filas original y que se quitan todas las opciones de filtro anteriores.</span><span class="sxs-lookup"><span data-stu-id="f280b-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>

## <a name="remarks"></a><span data-ttu-id="f280b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f280b-114">Remarks</span></span>

<span data-ttu-id="f280b-p102">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente. La funcionalidad de ordenación permite ordenar los registros por los valores de una columna. La funcionalidad de filtro permite mostrar un subconjunto de registros basándose en criterios de búsqueda, si bien el objeto [Recordset](recordset-object-ado.md) completo se mantiene en la caché. El método **Reset** ejecutará los criterios y reemplazará el actual objeto **Recordset** con un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="f280b-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="f280b-p103">Si se realizaron cambios en los datos originales que aún no se enviaron, el método **Reset** genera un error. Use primero el método [SubmitChanges](submitchanges-method-rds.md) para guardar los cambios en un objeto **Recordset** de lectura y escritura y, a continuación, use el método **Reset** para ordenar o filtrar los registros.</span><span class="sxs-lookup"><span data-stu-id="f280b-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="f280b-121">Si desea realizar más de un filtro en el conjunto de filas, puede utilizar el opcional argumento *booleano* con el método **Reset** .</span><span class="sxs-lookup"><span data-stu-id="f280b-121">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="f280b-122">En el ejemplo siguiente se muestra cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="f280b-122">The following example shows how to do this:</span></span>

