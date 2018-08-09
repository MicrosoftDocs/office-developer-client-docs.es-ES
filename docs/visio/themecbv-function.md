---
title: Función THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Devuelve un valor RGB o un número entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como un argumento ha sido modificado por el valor especificado de tinta o sombreado almacenado en la configuración de degradado del tema activo.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823403"
---
# <a name="themecbv-function"></a><span data-ttu-id="a536a-103">Función THEMECBV</span><span class="sxs-lookup"><span data-stu-id="a536a-103">THEMECBV Function</span></span>

<span data-ttu-id="a536a-104">Devuelve un valor RGB o un número entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como un argumento ha sido modificado por el valor especificado de tinta o sombreado almacenado en la configuración de degradado del tema activo.</span><span class="sxs-lookup"><span data-stu-id="a536a-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="a536a-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="a536a-105">Version Information</span></span>

<span data-ttu-id="a536a-106">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="a536a-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a536a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a536a-107">Syntax</span></span>

 <span data-ttu-id="a536a-108">**THEMECBV** ( _color_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="a536a-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="a536a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a536a-109">Parameters</span></span>

|<span data-ttu-id="a536a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a536a-110">**Name**</span></span>|<span data-ttu-id="a536a-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a536a-111">**Required/Optional**</span></span>|<span data-ttu-id="a536a-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a536a-112">**Data Type**</span></span>|<span data-ttu-id="a536a-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a536a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a536a-114">_color_</span><span class="sxs-lookup"><span data-stu-id="a536a-114">_color_</span></span> <br/> |<span data-ttu-id="a536a-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a536a-115">Required</span></span>  <br/> |<span data-ttu-id="a536a-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="a536a-116">**Number**</span></span> <br/> |<span data-ttu-id="a536a-117">Un número que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="a536a-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="a536a-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="a536a-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="a536a-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a536a-119">Required</span></span>  <br/> |<span data-ttu-id="a536a-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="a536a-120">**Number**</span></span> <br/> |<span data-ttu-id="a536a-121">El punto de degradado (tinta o sombreado) almacenado en la configuración de degradado del tema activo que se debe aplicar al color.</span><span class="sxs-lookup"><span data-stu-id="a536a-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="a536a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a536a-122">Return value</span></span>

 <span data-ttu-id="a536a-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="a536a-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a536a-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a536a-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="a536a-125">La función THEMECBV no modifica el color que se pasa como un argumento si la QuickStyle que se asigna a la forma no tiene un degradado.</span><span class="sxs-lookup"><span data-stu-id="a536a-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="a536a-126">La configuración de degradado en un tema es una serie de puntos de degradado numeradas que correspondan a una "iluminado" (tint) o "oscurecimiento" (tono).</span><span class="sxs-lookup"><span data-stu-id="a536a-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="a536a-127">Estos tonos y tintas se aplican a un color base para crear un efecto de color de degradado.</span><span class="sxs-lookup"><span data-stu-id="a536a-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="a536a-128">La función **THEMECBV** toma una entrada de color y da como resultado el color después de que se ha modificado por la tinta o sombreado del delimitador de degradado especificada.</span><span class="sxs-lookup"><span data-stu-id="a536a-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="a536a-129">Los matices y gradaciones proceden de la definición del tema, si el estilo rápido actual contiene un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="a536a-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="a536a-130">Si no especifica el estilo rápido activo un relleno degradado o la forma se establece en Sin tema, esta fórmula devuelve simplemente el color que se pasó para el primer argumento.</span><span class="sxs-lookup"><span data-stu-id="a536a-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a536a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a536a-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="a536a-132">Devuelve el color creado mediante la aplicación de la tinta o sombreado en el punto de degradado quinto del degradado para el color especificado en la celda **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="a536a-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="a536a-133">Devuelve un tono o matiz de rojo creada aplicando el segundo punto de degradado a un color base de rojo.</span><span class="sxs-lookup"><span data-stu-id="a536a-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

