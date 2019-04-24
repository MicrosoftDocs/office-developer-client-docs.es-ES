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
description: Devuelve el resultado de la expresión como una cadena con formato de acuerdo con formatodeimagen.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339896"
---
# <a name="format-function"></a><span data-ttu-id="f6d5f-103">Función FORMAT</span><span class="sxs-lookup"><span data-stu-id="f6d5f-103">FORMAT Function</span></span>

<span data-ttu-id="f6d5f-104">Devuelve el resultado de la _expresión_ como una cadena con formato de acuerdo con _formatodeimagen_.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f6d5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6d5f-105">Syntax</span></span>

<span data-ttu-id="f6d5f-106">Format (\* \* *expresión* \* *, "* \* *formatodeimagen* \* \*")</span><span class="sxs-lookup"><span data-stu-id="f6d5f-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f6d5f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6d5f-107">Parameters</span></span>

|<span data-ttu-id="f6d5f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-108">**Name**</span></span>|<span data-ttu-id="f6d5f-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-109">**Required/Optional**</span></span>|<span data-ttu-id="f6d5f-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-110">**Data Type**</span></span>|<span data-ttu-id="f6d5f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f6d5f-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="f6d5f-112">_expression_</span></span> <br/> |<span data-ttu-id="f6d5f-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f6d5f-113">Required</span></span>  <br/> |<span data-ttu-id="f6d5f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-114">**String**</span></span> <br/> |<span data-ttu-id="f6d5f-115">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="f6d5f-116">_formatodeimagen_</span><span class="sxs-lookup"><span data-stu-id="f6d5f-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="f6d5f-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f6d5f-117">Required</span></span>  <br/> |<span data-ttu-id="f6d5f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f6d5f-118">**String**</span></span> <br/> |<span data-ttu-id="f6d5f-119">La imagen de formato usada para dar formato a la cadena.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f6d5f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6d5f-120">Return value</span></span>

<span data-ttu-id="f6d5f-121">String</span><span class="sxs-lookup"><span data-stu-id="f6d5f-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6d5f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6d5f-122">Remarks</span></span>

<span data-ttu-id="f6d5f-123">El tipo de la expresión y el especificado en el formato de imagen controlan el comportamiento de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="f6d5f-124">_Formatodeimagen_ debe ser adecuado para el tipo de expresión.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="f6d5f-125">Para obtener más información acerca de cómo especificar imágenes de formato, vea [acerca de las imágenes de formato](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="f6d5f-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="f6d5f-126">Devuelve un error si el resultado de la _expresión_ y el tipo esperado en _formatodeimagen_ son de diferente tipo o si hay errores de sintaxis en _formatodeimagen_.</span><span class="sxs-lookup"><span data-stu-id="f6d5f-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="f6d5f-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6d5f-127">Example 1</span></span>

<span data-ttu-id="f6d5f-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="f6d5f-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="f6d5f-129">Devuelve "0,250 cm".</span><span class="sxs-lookup"><span data-stu-id="f6d5f-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f6d5f-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="f6d5f-130">Example 2</span></span>

<span data-ttu-id="f6d5f-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="f6d5f-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="f6d5f-132">Devuelve "0,25 CM".</span><span class="sxs-lookup"><span data-stu-id="f6d5f-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f6d5f-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="f6d5f-133">Example 3</span></span>

<span data-ttu-id="f6d5f-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="f6d5f-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="f6d5f-135">Devuelve "0,3 cm".</span><span class="sxs-lookup"><span data-stu-id="f6d5f-135">Returns "0.3 cm."</span></span>
  

