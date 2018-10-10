---
title: Ordinal (propiedad, posición de ADO MD)
TOCTitle: Ordinal Property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e953c038947073d3cdeb971e705c80f63d12a15b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483981"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="6a5b5-102">Ordinal (propiedad, posición de ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6a5b5-102">Ordinal Property (ADO MD Position)</span></span>


<span data-ttu-id="6a5b5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a5b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a5b5-104">Identifica exclusivamente una posición a lo largo de un eje.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="6a5b5-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6a5b5-105">Return Values</span></span>

<span data-ttu-id="6a5b5-106">Devuelve un entero **Long** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5b5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a5b5-107">Remarks</span></span>

<span data-ttu-id="6a5b5-108">El **Ordinal** de un objeto [Position](position-object-ado-md.md) corresponde al índice del objeto **Position** dentro de la colección [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="6a5b5-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="6a5b5-109">Una celda se puede recuperar rápidamente utilizando el **Ordinal** de la **posición** a lo largo de cada eje con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="6a5b5-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

