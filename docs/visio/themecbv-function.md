---
title: Función THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) pasado como argumento ha sido modificado por el valor de tono o tono especificado almacenado en la configuración de degradado del tema activo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429141"
---
# <a name="themecbv-function"></a><span data-ttu-id="53ecc-103">Función THEMECBV</span><span class="sxs-lookup"><span data-stu-id="53ecc-103">THEMECBV Function</span></span>

<span data-ttu-id="53ecc-104">Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) pasado como argumento ha sido modificado por el valor de tono o tono especificado almacenado en la configuración de degradado del tema activo.</span><span class="sxs-lookup"><span data-stu-id="53ecc-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="53ecc-105">Información de versiones</span><span class="sxs-lookup"><span data-stu-id="53ecc-105">Version Information</span></span>

<span data-ttu-id="53ecc-106">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="53ecc-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53ecc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53ecc-107">Syntax</span></span>

 <span data-ttu-id="53ecc-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="53ecc-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="53ecc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53ecc-109">Parameters</span></span>

|<span data-ttu-id="53ecc-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="53ecc-110">**Name**</span></span>|<span data-ttu-id="53ecc-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="53ecc-111">**Required/Optional**</span></span>|<span data-ttu-id="53ecc-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="53ecc-112">**Data Type**</span></span>|<span data-ttu-id="53ecc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53ecc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53ecc-114">_color_</span><span class="sxs-lookup"><span data-stu-id="53ecc-114">_color_</span></span> <br/> |<span data-ttu-id="53ecc-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53ecc-115">Required</span></span>  <br/> |<span data-ttu-id="53ecc-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="53ecc-116">**Number**</span></span> <br/> |<span data-ttu-id="53ecc-117">Número que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="53ecc-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="53ecc-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="53ecc-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="53ecc-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53ecc-119">Required</span></span>  <br/> |<span data-ttu-id="53ecc-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="53ecc-120">**Number**</span></span> <br/> |<span data-ttu-id="53ecc-121">El punto de degradado (tono o sombra) almacenado en la configuración de degradado del tema activo que se aplicará al color.</span><span class="sxs-lookup"><span data-stu-id="53ecc-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="53ecc-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53ecc-122">Return value</span></span>

 <span data-ttu-id="53ecc-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="53ecc-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53ecc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53ecc-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="53ecc-125">La función THEMECBV no hace nada con el color pasado como argumento si el QuickStyle asignado a la forma no tiene un degradado.</span><span class="sxs-lookup"><span data-stu-id="53ecc-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="53ecc-126">La configuración de degradado de un tema es una serie de delimitadores de degradado numerados que corresponden a una "iluminación" (tono) o "oscurecido" (sombra).</span><span class="sxs-lookup"><span data-stu-id="53ecc-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="53ecc-127">Estos tonos y tonos se aplican a un color base para crear un efecto de color degradado.</span><span class="sxs-lookup"><span data-stu-id="53ecc-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="53ecc-128">La **función THEMECBV** toma una entrada de color y genera el color después de que haya sido modificado por el tono o la sombra del delimitador de degradado especificado.</span><span class="sxs-lookup"><span data-stu-id="53ecc-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="53ecc-129">Los tonos y sombras provienen de la definición del tema, si el estilo rápido actual contiene un relleno degradado.</span><span class="sxs-lookup"><span data-stu-id="53ecc-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="53ecc-130">Si el estilo rápido activo no especifica un relleno degradado o la forma está establecida en Sin tema, esta fórmula simplemente devuelve el color que se pasó para el primer argumento.</span><span class="sxs-lookup"><span data-stu-id="53ecc-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="53ecc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53ecc-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="53ecc-132">Devuelve el color creado aplicando el tono o la sombra del quinto punto de degradado del degradado al color especificado en la celda **FillForegnd.**</span><span class="sxs-lookup"><span data-stu-id="53ecc-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="53ecc-133">Devuelve una sombra o tono de rojo creado aplicando el segundo punto de degradado a un color base de rojo.</span><span class="sxs-lookup"><span data-stu-id="53ecc-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

