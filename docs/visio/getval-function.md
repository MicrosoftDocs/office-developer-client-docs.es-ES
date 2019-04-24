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
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327317"
---
# <a name="getval-function"></a><span data-ttu-id="799ea-103">Función GETVAL</span><span class="sxs-lookup"><span data-stu-id="799ea-103">GETVAL Function</span></span>

<span data-ttu-id="799ea-104">Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="799ea-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="799ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="799ea-105">Syntax</span></span>

<span data-ttu-id="799ea-106">GETVAL (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="799ea-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="799ea-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="799ea-107">Parameters</span></span>

|<span data-ttu-id="799ea-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="799ea-108">**Name**</span></span>|<span data-ttu-id="799ea-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="799ea-109">**Required/Optional**</span></span>|<span data-ttu-id="799ea-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="799ea-110">**Data Type**</span></span>|<span data-ttu-id="799ea-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="799ea-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="799ea-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="799ea-112">_cellname_</span></span> <br/> |<span data-ttu-id="799ea-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="799ea-113">Required</span></span>  <br/> |<span data-ttu-id="799ea-114">**String**</span><span class="sxs-lookup"><span data-stu-id="799ea-114">**String**</span></span> <br/> |<span data-ttu-id="799ea-115">El nombre de la celda de la cual obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="799ea-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="799ea-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="799ea-116">Example</span></span>

<span data-ttu-id="799ea-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="799ea-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="799ea-118">Devuelve la suma de los valores de las celdas PinX, PinY y Width.</span><span class="sxs-lookup"><span data-stu-id="799ea-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

