---
title: FORMAT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Devuelve el resultado de expresión como una cadena con formato de acuerdo con el valor de formatoDeImagen.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822198"
---
# <a name="format-function"></a><span data-ttu-id="85d62-103">Función FORMAT</span><span class="sxs-lookup"><span data-stu-id="85d62-103">FORMAT Function</span></span>

<span data-ttu-id="85d62-104">Devuelve el resultado de _expresión_ como una cadena con formato de acuerdo con el _valor de formatoDeImagen_.</span><span class="sxs-lookup"><span data-stu-id="85d62-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="85d62-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85d62-105">Syntax</span></span>

<span data-ttu-id="85d62-106">FORMATO (** *expresión* **, "** *formatoDeImagen* **")</span><span class="sxs-lookup"><span data-stu-id="85d62-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="85d62-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85d62-107">Parameters</span></span>

|<span data-ttu-id="85d62-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="85d62-108">**Name**</span></span>|<span data-ttu-id="85d62-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="85d62-109">**Required/Optional**</span></span>|<span data-ttu-id="85d62-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="85d62-110">**Data Type**</span></span>|<span data-ttu-id="85d62-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85d62-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="85d62-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="85d62-112">_expression_</span></span> <br/> |<span data-ttu-id="85d62-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="85d62-113">Required</span></span>  <br/> |<span data-ttu-id="85d62-114">**String**</span><span class="sxs-lookup"><span data-stu-id="85d62-114">**String**</span></span> <br/> |<span data-ttu-id="85d62-115">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.</span><span class="sxs-lookup"><span data-stu-id="85d62-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="85d62-116">_formatoDeImagen_</span><span class="sxs-lookup"><span data-stu-id="85d62-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="85d62-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="85d62-117">Required</span></span>  <br/> |<span data-ttu-id="85d62-118">**String**</span><span class="sxs-lookup"><span data-stu-id="85d62-118">**String**</span></span> <br/> |<span data-ttu-id="85d62-119">La imagen de formato usada para dar formato a la cadena.</span><span class="sxs-lookup"><span data-stu-id="85d62-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="85d62-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85d62-120">Return value</span></span>

<span data-ttu-id="85d62-121">String</span><span class="sxs-lookup"><span data-stu-id="85d62-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85d62-122">Notas</span><span class="sxs-lookup"><span data-stu-id="85d62-122">Remarks</span></span>

<span data-ttu-id="85d62-123">El tipo de la expresión y el tipo especificado en el formato de imagen controlan el comportamiento de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="85d62-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="85d62-124">El _valor de formatoDeImagen_ debe ser adecuado para el tipo de expresión.</span><span class="sxs-lookup"><span data-stu-id="85d62-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="85d62-125">Para obtener más información acerca de cómo especificar imágenes de formato, vea [acerca de las imágenes de formato](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="85d62-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="85d62-126">Devuelve un error si el resultado de la _expresión_ y el tipo esperado en _formatoDeImagen_ son distintos, o si hay errores de sintaxis en _formatoDeImagen_.</span><span class="sxs-lookup"><span data-stu-id="85d62-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="85d62-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="85d62-127">Example 1</span></span>

<span data-ttu-id="85d62-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="85d62-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="85d62-129">Devuelve "0,250 cm".</span><span class="sxs-lookup"><span data-stu-id="85d62-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="85d62-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="85d62-130">Example 2</span></span>

<span data-ttu-id="85d62-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="85d62-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="85d62-132">Devuelve "0,25 CM".</span><span class="sxs-lookup"><span data-stu-id="85d62-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="85d62-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="85d62-133">Example 3</span></span>

<span data-ttu-id="85d62-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="85d62-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="85d62-135">Devuelve "0,3 cm".</span><span class="sxs-lookup"><span data-stu-id="85d62-135">Returns "0.3 cm."</span></span>
  

