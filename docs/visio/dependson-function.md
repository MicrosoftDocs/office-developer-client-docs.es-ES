---
title: DEPENDSON (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crea una dependencia de referencia de celda.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423471"
---
# <a name="dependson-function"></a><span data-ttu-id="774ca-103">Función DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="774ca-103">DEPENDSON Function</span></span>

<span data-ttu-id="774ca-104">Crea una dependencia de referencia de celda.</span><span class="sxs-lookup"><span data-stu-id="774ca-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="774ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="774ca-105">Syntax</span></span>

<span data-ttu-id="774ca-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="774ca-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="774ca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="774ca-107">Parameters</span></span>

|<span data-ttu-id="774ca-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="774ca-108">**Name**</span></span>|<span data-ttu-id="774ca-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="774ca-109">**Required/Optional**</span></span>|<span data-ttu-id="774ca-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="774ca-110">**Data Type**</span></span>|<span data-ttu-id="774ca-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="774ca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="774ca-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="774ca-112">_cellref_</span></span> <br/> |<span data-ttu-id="774ca-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="774ca-113">Required</span></span>  <br/> |<span data-ttu-id="774ca-114">**String**</span><span class="sxs-lookup"><span data-stu-id="774ca-114">**String**</span></span> <br/> |<span data-ttu-id="774ca-115">La primera referencia de celda.</span><span class="sxs-lookup"><span data-stu-id="774ca-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="774ca-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="774ca-116">_cellref2_</span></span> <br/> |<span data-ttu-id="774ca-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="774ca-117">Optional</span></span>  <br/> |<span data-ttu-id="774ca-118">**String**</span><span class="sxs-lookup"><span data-stu-id="774ca-118">**String**</span></span> <br/> |<span data-ttu-id="774ca-119">La segunda referencia de celda.</span><span class="sxs-lookup"><span data-stu-id="774ca-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="774ca-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="774ca-120">Remarks</span></span>

<span data-ttu-id="774ca-p101">Esta función siempre devuelve el valor FALSE. No tiene ningún efecto cuando se utiliza en una celda Action o en una fila Event.</span><span class="sxs-lookup"><span data-stu-id="774ca-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="774ca-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="774ca-123">Example</span></span>

<span data-ttu-id="774ca-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="774ca-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="774ca-125">Abre el bloque de texto de una forma siempre que cambien las celdas PinX o PinY de la forma.</span><span class="sxs-lookup"><span data-stu-id="774ca-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

