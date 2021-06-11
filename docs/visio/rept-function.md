---
title: REPT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Repite el texto un número determinado de veces.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412082"
---
# <a name="rept-function"></a><span data-ttu-id="c595f-103">Función REPT</span><span class="sxs-lookup"><span data-stu-id="c595f-103">REPT Function</span></span>

<span data-ttu-id="c595f-104">Repite el texto un número determinado de veces.</span><span class="sxs-lookup"><span data-stu-id="c595f-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c595f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c595f-105">Syntax</span></span>

<span data-ttu-id="c595f-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c595f-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c595f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c595f-107">Parameters</span></span>

|<span data-ttu-id="c595f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c595f-108">**Name**</span></span>|<span data-ttu-id="c595f-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c595f-109">**Required/Optional**</span></span>|<span data-ttu-id="c595f-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c595f-110">**Data Type**</span></span>|<span data-ttu-id="c595f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c595f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c595f-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c595f-112">_text_</span></span> <br/> |<span data-ttu-id="c595f-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c595f-113">Required</span></span>  <br/> |<span data-ttu-id="c595f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c595f-114">**String**</span></span> <br/> | <span data-ttu-id="c595f-115">El texto que se desea repetir.</span><span class="sxs-lookup"><span data-stu-id="c595f-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="c595f-116">_number_times_</span><span class="sxs-lookup"><span data-stu-id="c595f-116">_number_times_</span></span> <br/> |<span data-ttu-id="c595f-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c595f-117">Required</span></span>  <br/> |<span data-ttu-id="c595f-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c595f-118">**Number**</span></span> <br/> |<span data-ttu-id="c595f-119">Número positivo que indica las veces que debe aparecer el texto.</span><span class="sxs-lookup"><span data-stu-id="c595f-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c595f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c595f-120">Remarks</span></span>

<span data-ttu-id="c595f-121">Si  *number_times*  es:</span><span class="sxs-lookup"><span data-stu-id="c595f-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="c595f-122">cero (0), REPT devuelve "" (ningún texto).</span><span class="sxs-lookup"><span data-stu-id="c595f-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="c595f-123">Un número no entero, se redondea a la baja.</span><span class="sxs-lookup"><span data-stu-id="c595f-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="c595f-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c595f-124">Example</span></span>

<span data-ttu-id="c595f-125">REPT (" \* ", 5)</span><span class="sxs-lookup"><span data-stu-id="c595f-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="c595f-126">Devuelve \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c595f-126">Returns \*\*\*\*\*.</span></span> 
  

