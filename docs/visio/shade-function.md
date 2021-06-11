---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad por la cantidad (positiva o negativa) especificada en el parámetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326603"
---
# <a name="shade-function"></a><span data-ttu-id="8fd00-103">Función SHADE</span><span class="sxs-lookup"><span data-stu-id="8fd00-103">SHADE Function</span></span>

<span data-ttu-id="8fd00-104">Modifica el color disminuyendo su luminosidad por la cantidad (positiva o negativa) especificada en el _parámetro int._</span><span class="sxs-lookup"><span data-stu-id="8fd00-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8fd00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fd00-105">Syntax</span></span>

<span data-ttu-id="8fd00-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8fd00-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8fd00-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fd00-107">Parameters</span></span>

|<span data-ttu-id="8fd00-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8fd00-108">**Name**</span></span>|<span data-ttu-id="8fd00-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8fd00-109">**Required/Optional**</span></span>|<span data-ttu-id="8fd00-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8fd00-110">**Data Type**</span></span>|<span data-ttu-id="8fd00-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fd00-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8fd00-112">_color_</span><span class="sxs-lookup"><span data-stu-id="8fd00-112">_color_</span></span> <br/> |<span data-ttu-id="8fd00-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8fd00-113">Required</span></span>  <br/> |<span data-ttu-id="8fd00-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="8fd00-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8fd00-115">Índice de color de Microsoft Visio o valor RGB del color.</span><span class="sxs-lookup"><span data-stu-id="8fd00-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="8fd00-116">_int_</span><span class="sxs-lookup"><span data-stu-id="8fd00-116">_int_</span></span> <br/> |<span data-ttu-id="8fd00-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8fd00-117">Required</span></span>  <br/> |<span data-ttu-id="8fd00-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8fd00-118">**Integer**</span></span> <br/> |<span data-ttu-id="8fd00-p101">Cantidad por la que se disminuye la luminosidad del color. Puede ser positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="8fd00-p101">The amount by which to decrease the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8fd00-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fd00-121">Return value</span></span>

 <span data-ttu-id="8fd00-122">**RVA**</span><span class="sxs-lookup"><span data-stu-id="8fd00-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fd00-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8fd00-123">Remarks</span></span>

<span data-ttu-id="8fd00-124">Los límites superior o inferior de luminosidad son 0 y 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8fd00-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="8fd00-125">No hay ningún límite en el tamaño del entero que se puede pasar para el parámetro  _int,_ pero la luminosidad nunca supera estos límites.</span><span class="sxs-lookup"><span data-stu-id="8fd00-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Límites superiores e inferiores de luminosidad](media/image199_ZA10173627.gif)
  

