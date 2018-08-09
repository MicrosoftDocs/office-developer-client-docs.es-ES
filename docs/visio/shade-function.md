---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro int.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823133"
---
# <a name="shade-function"></a><span data-ttu-id="13dc6-103">Función SHADE</span><span class="sxs-lookup"><span data-stu-id="13dc6-103">SHADE Function</span></span>

<span data-ttu-id="13dc6-104">Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="13dc6-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13dc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13dc6-105">Syntax</span></span>

<span data-ttu-id="13dc6-106">TONO (** *color* **, ** *int* **)</span><span class="sxs-lookup"><span data-stu-id="13dc6-106">SHADE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="13dc6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13dc6-107">Parameters</span></span>

|<span data-ttu-id="13dc6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="13dc6-108">**Name**</span></span>|<span data-ttu-id="13dc6-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="13dc6-109">**Required/Optional**</span></span>|<span data-ttu-id="13dc6-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="13dc6-110">**Data Type**</span></span>|<span data-ttu-id="13dc6-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13dc6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="13dc6-112">_color_</span><span class="sxs-lookup"><span data-stu-id="13dc6-112">_color_</span></span> <br/> |<span data-ttu-id="13dc6-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="13dc6-113">Required</span></span>  <br/> |<span data-ttu-id="13dc6-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="13dc6-114">**Numeric**</span></span> <br/> |<span data-ttu-id="13dc6-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="13dc6-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="13dc6-116">_int_</span><span class="sxs-lookup"><span data-stu-id="13dc6-116">_int_</span></span> <br/> |<span data-ttu-id="13dc6-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="13dc6-117">Required</span></span>  <br/> |<span data-ttu-id="13dc6-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="13dc6-118">**Integer**</span></span> <br/> |<span data-ttu-id="13dc6-p101">Cantidad por la que se disminuye la luminosidad del color. Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="13dc6-p101">The amount by which to decrease the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="13dc6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13dc6-121">Return value</span></span>

 <span data-ttu-id="13dc6-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="13dc6-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13dc6-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13dc6-123">Remarks</span></span>

<span data-ttu-id="13dc6-124">Los límites superiores e inferiores de luminosidad son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="13dc6-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="13dc6-125">No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="13dc6-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![](media/image199_ZA10173627.gif)
  

