---
title: TEXTHEIGHT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Devuelve el alto del texto compuesto de una forma donde ninguna línea de texto excede el ancho máximo.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823383"
---
# <a name="textheight-function"></a><span data-ttu-id="5184e-103">Función TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="5184e-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="5184e-104">Devuelve el alto del texto compuesto de una forma donde ninguna línea de texto excede el _ancho máximo_.</span><span class="sxs-lookup"><span data-stu-id="5184e-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5184e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5184e-105">Syntax</span></span>

<span data-ttu-id="5184e-106">TEXTHEIGHT (** *nombreDeForma! TheText* ** ** *[, valor]* **)</span><span class="sxs-lookup"><span data-stu-id="5184e-106">TEXTHEIGHT(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5184e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5184e-107">Parameters</span></span>

|<span data-ttu-id="5184e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5184e-108">**Name**</span></span>|<span data-ttu-id="5184e-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5184e-109">**Required/Optional**</span></span>|<span data-ttu-id="5184e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5184e-110">**Data Type**</span></span>|<span data-ttu-id="5184e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5184e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5184e-112">_nombreDeForma! theText_</span><span class="sxs-lookup"><span data-stu-id="5184e-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="5184e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5184e-113">Required</span></span>  <br/> |<span data-ttu-id="5184e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5184e-114">**String**</span></span> <br/> |<span data-ttu-id="5184e-115">Una referencia a la celda llamada TheText en la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="5184e-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="5184e-116">_¡nombreDeForma!_</span><span class="sxs-lookup"><span data-stu-id="5184e-116">_shapename!_</span></span> <span data-ttu-id="5184e-117">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="5184e-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="5184e-118">_valor_</span><span class="sxs-lookup"><span data-stu-id="5184e-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="5184e-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="5184e-119">Optional</span></span>  <br/> |<span data-ttu-id="5184e-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="5184e-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5184e-121">Ancho máximo del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="5184e-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5184e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5184e-122">Return value</span></span>

<span data-ttu-id="5184e-123">String</span><span class="sxs-lookup"><span data-stu-id="5184e-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5184e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5184e-124">Remarks</span></span>

<span data-ttu-id="5184e-p102">El valor que se devuelve incluye el alto del texto, los espacios que le preceden y le siguen, el espaciado entre líneas del texto y los márgenes superior e inferior del bloque de texto. Esta función se utiliza habitualmente para ajustar el alto de una forma en función del texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="5184e-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="5184e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5184e-127">Example</span></span>

<span data-ttu-id="5184e-128">TEXTHEIGHT(TheText,(Width - 0,5 pda))</span><span class="sxs-lookup"><span data-stu-id="5184e-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="5184e-129">Devuelve el alto del texto cuando se ajusta al ancho de la forma menos 0,5 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="5184e-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

