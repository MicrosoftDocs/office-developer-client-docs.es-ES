---
title: TONE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823429"
---
# <a name="tone-function"></a><span data-ttu-id="53d04-103">TONE (función)</span><span class="sxs-lookup"><span data-stu-id="53d04-103">TONE Function</span></span>

<span data-ttu-id="53d04-104">Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="53d04-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53d04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53d04-105">Syntax</span></span>

<span data-ttu-id="53d04-106">TONO (** *color* **, ** *int* **)</span><span class="sxs-lookup"><span data-stu-id="53d04-106">TONE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="53d04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53d04-107">Parameters</span></span>

|<span data-ttu-id="53d04-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="53d04-108">**Name**</span></span>|<span data-ttu-id="53d04-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="53d04-109">**Required/Optional**</span></span>|<span data-ttu-id="53d04-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="53d04-110">**Data Type**</span></span>|<span data-ttu-id="53d04-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53d04-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53d04-112">_color_</span><span class="sxs-lookup"><span data-stu-id="53d04-112">_color_</span></span> <br/> |<span data-ttu-id="53d04-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53d04-113">Required</span></span>  <br/> |<span data-ttu-id="53d04-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="53d04-114">**Numeric**</span></span> <br/> |<span data-ttu-id="53d04-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="53d04-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="53d04-116">_int_</span><span class="sxs-lookup"><span data-stu-id="53d04-116">_int_</span></span> <br/> |<span data-ttu-id="53d04-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53d04-117">Required</span></span>  <br/> |<span data-ttu-id="53d04-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="53d04-118">**Integer**</span></span> <br/> |<span data-ttu-id="53d04-p101">Cantidad por la que se reduce la saturación del color. Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="53d04-p101">The amount by which to decrease the saturation of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="53d04-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d04-121">Return value</span></span>

 <span data-ttu-id="53d04-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="53d04-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53d04-123">Notas</span><span class="sxs-lookup"><span data-stu-id="53d04-123">Remarks</span></span>

<span data-ttu-id="53d04-124">Los límites superiores e inferiores de saturación son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="53d04-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="53d04-125">No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la saturación nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="53d04-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

