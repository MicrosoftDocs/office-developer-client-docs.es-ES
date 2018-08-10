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
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823005"
---
# <a name="rept-function"></a><span data-ttu-id="eaea5-103">Función REPT</span><span class="sxs-lookup"><span data-stu-id="eaea5-103">REPT Function</span></span>

<span data-ttu-id="eaea5-104">Repite el texto un número determinado de veces.</span><span class="sxs-lookup"><span data-stu-id="eaea5-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eaea5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eaea5-105">Syntax</span></span>

<span data-ttu-id="eaea5-106">REPT (** *texto* **, ** *veces* **)</span><span class="sxs-lookup"><span data-stu-id="eaea5-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eaea5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eaea5-107">Parameters</span></span>

|<span data-ttu-id="eaea5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="eaea5-108">**Name**</span></span>|<span data-ttu-id="eaea5-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="eaea5-109">**Required/Optional**</span></span>|<span data-ttu-id="eaea5-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="eaea5-110">**Data Type**</span></span>|<span data-ttu-id="eaea5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eaea5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eaea5-112">_text_</span><span class="sxs-lookup"><span data-stu-id="eaea5-112">_text_</span></span> <br/> |<span data-ttu-id="eaea5-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="eaea5-113">Required</span></span>  <br/> |<span data-ttu-id="eaea5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="eaea5-114">**String**</span></span> <br/> | <span data-ttu-id="eaea5-115">El texto que se desea repetir.</span><span class="sxs-lookup"><span data-stu-id="eaea5-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="eaea5-116">_número de veces_</span><span class="sxs-lookup"><span data-stu-id="eaea5-116">_number_times_</span></span> <br/> |<span data-ttu-id="eaea5-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="eaea5-117">Required</span></span>  <br/> |<span data-ttu-id="eaea5-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="eaea5-118">**Number**</span></span> <br/> |<span data-ttu-id="eaea5-119">Número positivo que indica las veces que debe aparecer el texto.</span><span class="sxs-lookup"><span data-stu-id="eaea5-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaea5-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaea5-120">Remarks</span></span>

<span data-ttu-id="eaea5-121">Si *veces* es:</span><span class="sxs-lookup"><span data-stu-id="eaea5-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="eaea5-122">cero (0), REPT devuelve "" (ningún texto).</span><span class="sxs-lookup"><span data-stu-id="eaea5-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="eaea5-123">Un número no entero, se redondea a la baja.</span><span class="sxs-lookup"><span data-stu-id="eaea5-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="eaea5-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eaea5-124">Example</span></span>

<span data-ttu-id="eaea5-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="eaea5-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="eaea5-126">Devuelve \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="eaea5-126">Returns \*\*\*\*\*.</span></span> 
  
