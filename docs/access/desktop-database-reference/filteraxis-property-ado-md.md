---
title: FilterAxis (propiedad, ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603059"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="edbbf-102">FilterAxis (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="edbbf-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="edbbf-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="edbbf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="edbbf-104">Indica información de filtro acerca del conjunto de celdas activo.</span><span class="sxs-lookup"><span data-stu-id="edbbf-104">Indicates filter information about the current cellset.</span></span>

<span data-ttu-id="edbbf-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="edbbf-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="edbbf-106">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="edbbf-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="edbbf-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="edbbf-107">Return values</span></span>
>>>>>>> <span data-ttu-id="edbbf-108">master</span><span class="sxs-lookup"><span data-stu-id="edbbf-108">master</span></span>

<span data-ttu-id="edbbf-109">Devuelve un objeto [Axis](axis-object-ado-md.md) y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="edbbf-109">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbbf-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edbbf-110">Remarks</span></span>

<span data-ttu-id="edbbf-p101">Utilice la propiedad **FilterAxis** para devolver información acerca de las dimensiones que se utilizaron para distribuir los datos en sectores. La propiedad [DimensionCount](dimensioncount-property-ado-md.md) del **eje** devuelve el número de dimensiones del rebanador. Este eje normalmente tiene sólo una fila.</span><span class="sxs-lookup"><span data-stu-id="edbbf-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="edbbf-114">El **eje** que devuelve [FilterAxis](filteraxis-property-ado-md.md) no está contenido en la colección [Axes](axes-collection-ado-md.md) correspondiente a un objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="edbbf-114">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

