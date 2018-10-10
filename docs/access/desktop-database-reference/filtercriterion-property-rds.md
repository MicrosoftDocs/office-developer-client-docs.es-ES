---
title: FilterCriterion (propiedad, RDS)
TOCTitle: FilterCriterion Property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b847318c5fe0132fbc53f588b4478b7f37ec4ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486641"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="ae358-102">FilterCriterion (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="ae358-102">FilterCriterion Property (RDS)</span></span>


<span data-ttu-id="ae358-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae358-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ae358-104">Indica el operador de evaluación que se utilizará en el valor de filtro.</span><span class="sxs-lookup"><span data-stu-id="ae358-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae358-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae358-105">Syntax</span></span>

<span data-ttu-id="ae358-106">*DataControl*. FilterCriterion = *cadena*</span><span class="sxs-lookup"><span data-stu-id="ae358-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ae358-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae358-107">Parameters</span></span>

  - <span data-ttu-id="ae358-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ae358-108">*DataControl*</span></span>

  - <span data-ttu-id="ae358-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ae358-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="ae358-110">*String*</span><span class="sxs-lookup"><span data-stu-id="ae358-110">*String*</span></span>

  - <span data-ttu-id="ae358-111">Un valor de tipo **String** que especifica el operador de evaluación de [FilterValue](filtervalue-property-rds.md) a los registros.</span><span class="sxs-lookup"><span data-stu-id="ae358-111">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="ae358-112">Puede ser uno de los siguientes: \<, \<=, \>, \>=, =, o \< \>.</span><span class="sxs-lookup"><span data-stu-id="ae358-112">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae358-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae358-113">Remarks</span></span>

<span data-ttu-id="ae358-p102">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="ae358-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="ae358-118">La "\!=" operador no es válido para **FilterCriterion**; en su lugar, use "\<\>".</span><span class="sxs-lookup"><span data-stu-id="ae358-118">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="ae358-p103">Si se establecen las propiedades de filtrado y ordenación y se llama al método **Reset**, el conjunto de filas primero se filtra y luego se ordena. En un orden ascendente, los valores nulos se encuentran en la parte superior, mientras que en un orden descendente están en la parte inferior (el orden ascendente es el comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="ae358-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

