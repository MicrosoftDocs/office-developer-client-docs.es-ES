---
title: TONE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica el color disminuyendo su saturación por la cantidad especificada en el parámetro int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434378"
---
# <a name="tone-function"></a><span data-ttu-id="ea182-103">Función TONE</span><span class="sxs-lookup"><span data-stu-id="ea182-103">TONE Function</span></span>

<span data-ttu-id="ea182-104">Modifica el color disminuyendo su saturación por la cantidad especificada en el _parámetro int._</span><span class="sxs-lookup"><span data-stu-id="ea182-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ea182-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea182-105">Syntax</span></span>

<span data-ttu-id="ea182-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ea182-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea182-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea182-107">Parameters</span></span>

|<span data-ttu-id="ea182-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea182-108">**Name**</span></span>|<span data-ttu-id="ea182-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ea182-109">**Required/Optional**</span></span>|<span data-ttu-id="ea182-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ea182-110">**Data Type**</span></span>|<span data-ttu-id="ea182-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea182-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea182-112">_color_</span><span class="sxs-lookup"><span data-stu-id="ea182-112">_color_</span></span> <br/> |<span data-ttu-id="ea182-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ea182-113">Required</span></span>  <br/> |<span data-ttu-id="ea182-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="ea182-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ea182-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="ea182-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="ea182-116">_int_</span><span class="sxs-lookup"><span data-stu-id="ea182-116">_int_</span></span> <br/> |<span data-ttu-id="ea182-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ea182-117">Required</span></span>  <br/> |<span data-ttu-id="ea182-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="ea182-118">**Integer**</span></span> <br/> |<span data-ttu-id="ea182-119">Cantidad por la que se reduce la saturación del color.</span><span class="sxs-lookup"><span data-stu-id="ea182-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="ea182-120">Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="ea182-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ea182-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea182-121">Return value</span></span>

 <span data-ttu-id="ea182-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="ea182-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea182-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea182-123">Remarks</span></span>

<span data-ttu-id="ea182-124">Los límites superior o inferior de saturación son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ea182-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="ea182-125">No hay ningún límite en el tamaño del entero que puedes pasar para el parámetro  _int,_ pero la saturación nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="ea182-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

