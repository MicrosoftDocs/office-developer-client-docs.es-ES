---
title: FilterValue (propiedad, RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39152be2c53dc0de9bc1bcb21fee505fcb9106dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484503"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="ec2d8-102">FilterValue (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="ec2d8-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="ec2d8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec2d8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ec2d8-104">Indica el valor mediante el que se van a filtrar registros.</span><span class="sxs-lookup"><span data-stu-id="ec2d8-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec2d8-105">Syntax</span></span>

<span data-ttu-id="ec2d8-106">*DataControl*. FilterValue = *cadena*</span><span class="sxs-lookup"><span data-stu-id="ec2d8-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ec2d8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec2d8-107">Parameters</span></span>

  - <span data-ttu-id="ec2d8-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ec2d8-108">*DataControl*</span></span>

  - <span data-ttu-id="ec2d8-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ec2d8-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="ec2d8-110">*String*</span><span class="sxs-lookup"><span data-stu-id="ec2d8-110">*String*</span></span>

  - <span data-ttu-id="ec2d8-111">Un valor de **tipo String** que representa un valor de datos con el que se va a filtrar registros (por ejemplo, 'Programmer' o 125).</span><span class="sxs-lookup"><span data-stu-id="ec2d8-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2d8-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec2d8-112">Remarks</span></span>

<span data-ttu-id="ec2d8-p101">Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="ec2d8-p101">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="ec2d8-117">Los valores nulos dan lugar a un error de falta de coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="ec2d8-117">Null values result in a type mismatch error.</span></span>

