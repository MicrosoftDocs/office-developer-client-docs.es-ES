---
title: GETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Hace referencia a una celda y no actualiza la fórmula cuando cambia la celda a la que se hace referencia.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424332"
---
# <a name="getref-function"></a><span data-ttu-id="280d0-103">Función GETREF</span><span class="sxs-lookup"><span data-stu-id="280d0-103">GETREF Function</span></span>

<span data-ttu-id="280d0-104">Hace referencia a una celda y no actualiza la fórmula cuando cambia la celda a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="280d0-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="280d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="280d0-105">Syntax</span></span>

<span data-ttu-id="280d0-106">GETREF(\*\* *cellname* \*\* )</span><span class="sxs-lookup"><span data-stu-id="280d0-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="280d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="280d0-107">Parameters</span></span>

|<span data-ttu-id="280d0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="280d0-108">**Name**</span></span>|<span data-ttu-id="280d0-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="280d0-109">**Required/Optional**</span></span>|<span data-ttu-id="280d0-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="280d0-110">**Data Type**</span></span>|<span data-ttu-id="280d0-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="280d0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="280d0-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="280d0-112">_cellname_</span></span> <br/> |<span data-ttu-id="280d0-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="280d0-113">Required</span></span>  <br/> |<span data-ttu-id="280d0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="280d0-114">**String**</span></span> <br/> |<span data-ttu-id="280d0-115">Nombre de la celda a la que se debe obtener una referencia.</span><span class="sxs-lookup"><span data-stu-id="280d0-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="280d0-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="280d0-116">Example</span></span>

<span data-ttu-id="280d0-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="280d0-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="280d0-118">Establece el valor 5,1 en la fórmula de la celda PinX.</span><span class="sxs-lookup"><span data-stu-id="280d0-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

