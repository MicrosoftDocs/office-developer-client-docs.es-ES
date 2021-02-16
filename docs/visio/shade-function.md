---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad en la cantidad (positiva o negativa) especificada en el parámetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326603"
---
# <a name="shade-function"></a><span data-ttu-id="6e8c6-103">Función SHADE</span><span class="sxs-lookup"><span data-stu-id="6e8c6-103">SHADE Function</span></span>

<span data-ttu-id="6e8c6-104">Modifica el color disminuyendo su luminosidad en la cantidad (positiva o negativa) especificada en el _parámetro int._</span><span class="sxs-lookup"><span data-stu-id="6e8c6-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6e8c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e8c6-105">Syntax</span></span>

<span data-ttu-id="6e8c6-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6e8c6-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e8c6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e8c6-107">Parameters</span></span>

|<span data-ttu-id="6e8c6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-108">**Name**</span></span>|<span data-ttu-id="6e8c6-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-109">**Required/Optional**</span></span>|<span data-ttu-id="6e8c6-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-110">**Data Type**</span></span>|<span data-ttu-id="6e8c6-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e8c6-112">_color_</span><span class="sxs-lookup"><span data-stu-id="6e8c6-112">_color_</span></span> <br/> |<span data-ttu-id="6e8c6-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e8c6-113">Required</span></span>  <br/> |<span data-ttu-id="6e8c6-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-114">**Numeric**</span></span> <br/> |<span data-ttu-id="6e8c6-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="6e8c6-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="6e8c6-116">_int_</span><span class="sxs-lookup"><span data-stu-id="6e8c6-116">_int_</span></span> <br/> |<span data-ttu-id="6e8c6-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e8c6-117">Required</span></span>  <br/> |<span data-ttu-id="6e8c6-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-118">**Integer**</span></span> <br/> |<span data-ttu-id="6e8c6-119">Cantidad por la que se disminuye la luminosidad del color.</span><span class="sxs-lookup"><span data-stu-id="6e8c6-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="6e8c6-120">Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="6e8c6-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6e8c6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e8c6-121">Return value</span></span>

 <span data-ttu-id="6e8c6-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="6e8c6-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e8c6-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e8c6-123">Remarks</span></span>

<span data-ttu-id="6e8c6-124">Los límites superior o inferior de luminosidad son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6e8c6-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="6e8c6-125">No hay ningún límite en el tamaño del entero que puedes pasar para el parámetro  _int,_ pero la luminosidad nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="6e8c6-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Límites superiores e inferiores de luminosidad](media/image199_ZA10173627.gif)
  

