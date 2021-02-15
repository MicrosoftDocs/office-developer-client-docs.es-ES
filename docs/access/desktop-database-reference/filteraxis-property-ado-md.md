---
title: FilterAxis (propiedad, ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292457"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="6f405-102">FilterAxis (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6f405-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="6f405-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f405-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f405-104">Indica información de filtro acerca del conjunto de celdas activo.</span><span class="sxs-lookup"><span data-stu-id="6f405-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="6f405-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6f405-105">Return values</span></span>

<span data-ttu-id="6f405-106">Devuelve un objeto [Axis](axis-object-ado-md.md) y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6f405-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f405-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f405-107">Remarks</span></span>

<span data-ttu-id="6f405-p101">Utilice la propiedad **FilterAxis** para devolver información acerca de las dimensiones que se utilizaron para distribuir los datos en sectores. La propiedad [DimensionCount](dimensioncount-property-ado-md.md) del **eje** devuelve el número de dimensiones del rebanador. Este eje normalmente tiene sólo una fila.</span><span class="sxs-lookup"><span data-stu-id="6f405-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="6f405-111">El **eje** que devuelve [FilterAxis](filteraxis-property-ado-md.md) no está contenido en la colección [Axes](axes-collection-ado-md.md) correspondiente a un objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="6f405-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

