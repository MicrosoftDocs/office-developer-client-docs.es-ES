---
title: GETVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822226"
---
# <a name="getval-function"></a><span data-ttu-id="be235-103">Función GETVAL</span><span class="sxs-lookup"><span data-stu-id="be235-103">GETVAL Function</span></span>

<span data-ttu-id="be235-104">Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="be235-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="be235-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be235-105">Syntax</span></span>

<span data-ttu-id="be235-106">GETVAL (** *nombreDeCelda* **)</span><span class="sxs-lookup"><span data-stu-id="be235-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="be235-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be235-107">Parameters</span></span>

|<span data-ttu-id="be235-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="be235-108">**Name**</span></span>|<span data-ttu-id="be235-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="be235-109">**Required/Optional**</span></span>|<span data-ttu-id="be235-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="be235-110">**Data Type**</span></span>|<span data-ttu-id="be235-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be235-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="be235-112">_nombreDeCelda_</span><span class="sxs-lookup"><span data-stu-id="be235-112">_cellname_</span></span> <br/> |<span data-ttu-id="be235-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="be235-113">Required</span></span>  <br/> |<span data-ttu-id="be235-114">**String**</span><span class="sxs-lookup"><span data-stu-id="be235-114">**String**</span></span> <br/> |<span data-ttu-id="be235-115">El nombre de la celda de la cual obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="be235-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="be235-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be235-116">Example</span></span>

<span data-ttu-id="be235-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="be235-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="be235-118">Devuelve la suma de los valores de las celdas PinX, PinY y Width.</span><span class="sxs-lookup"><span data-stu-id="be235-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

