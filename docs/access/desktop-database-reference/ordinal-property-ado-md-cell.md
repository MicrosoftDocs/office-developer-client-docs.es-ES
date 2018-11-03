---
title: Ordinal (propiedad, Cell de ADO MD)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fbbe461390a5f8a068f839bcf41fab5e1ad66ff
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946758"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="23d52-102">Ordinal (propiedad, Cell de ADO MD)</span><span class="sxs-lookup"><span data-stu-id="23d52-102">Ordinal property (ADO MD Cell)</span></span>


<span data-ttu-id="23d52-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23d52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23d52-104">Identifica exclusivamente una celda por su posición dentro de un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="23d52-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="23d52-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="23d52-105">Return values</span></span>

<span data-ttu-id="23d52-106">Devuelve un entero **Long** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="23d52-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="23d52-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23d52-107">Remarks</span></span>

<span data-ttu-id="23d52-p101">El valor ordinal de la celda identifica inequívocamente la celda dentro de un conjunto de celdas. Conceptualmente, las celdas se numeran en un conjunto de celdas como si el conjunto de celdas fuera una matriz de *p* dimensiones, donde *p* es el número de [ejes](axes-collection-ado-md.md). Las celdas se numeran empezando desde cero en orden de fila mayor.</span><span class="sxs-lookup"><span data-stu-id="23d52-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="23d52-111">El valor ordinal de la celda se puede utilizar con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md) para recuperar rápidamente la [celda](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="23d52-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

