---
title: TINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica el color aumentando su luminosidad por la cantidad (positiva o negativa) especificada en el parámetro int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406580"
---
# <a name="tint-function"></a><span data-ttu-id="c868d-103">Función TINT</span><span class="sxs-lookup"><span data-stu-id="c868d-103">TINT Function</span></span>

<span data-ttu-id="c868d-104">Modifica el color aumentando su luminosidad por la cantidad (positiva o negativa) especificada en el parámetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="c868d-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c868d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c868d-105">Syntax</span></span>

<span data-ttu-id="c868d-106">MATIZ (\* \* *color* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c868d-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c868d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c868d-107">Parameters</span></span>

|<span data-ttu-id="c868d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c868d-108">**Name**</span></span>|<span data-ttu-id="c868d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c868d-109">**Required/Optional**</span></span>|<span data-ttu-id="c868d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c868d-110">**Data Type**</span></span>|<span data-ttu-id="c868d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c868d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c868d-112">_color_</span><span class="sxs-lookup"><span data-stu-id="c868d-112">_color_</span></span> <br/> |<span data-ttu-id="c868d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c868d-113">Required</span></span>  <br/> |<span data-ttu-id="c868d-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="c868d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c868d-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="c868d-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="c868d-116">_int_</span><span class="sxs-lookup"><span data-stu-id="c868d-116">_int_</span></span> <br/> |<span data-ttu-id="c868d-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c868d-117">Required</span></span>  <br/> |<span data-ttu-id="c868d-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c868d-118">**Integer**</span></span> <br/> |<span data-ttu-id="c868d-119">Cantidad por la que se aumenta la luminosidad del color.</span><span class="sxs-lookup"><span data-stu-id="c868d-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="c868d-120">Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="c868d-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c868d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c868d-121">Return value</span></span>

 <span data-ttu-id="c868d-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="c868d-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c868d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c868d-123">Remarks</span></span>

<span data-ttu-id="c868d-124">Los límites superior o inferior de luminosidad son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c868d-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="c868d-125">No hay ningún límite en el tamaño del número entero que puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="c868d-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

