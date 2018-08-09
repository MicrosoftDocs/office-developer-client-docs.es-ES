---
title: TEXTWIDTH, función (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Devuelve el ancho del texto compuesto de una forma.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823381"
---
# <a name="textwidth-function"></a><span data-ttu-id="dc7aa-103">Función TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="dc7aa-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="dc7aa-104">Devuelve el ancho del texto compuesto de una forma.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc7aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc7aa-105">Syntax</span></span>

<span data-ttu-id="dc7aa-106">TEXTWIDTH (** *nombreDeForma! TheText* ** ** *[, valor]* **)</span><span class="sxs-lookup"><span data-stu-id="dc7aa-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc7aa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc7aa-107">Parameters</span></span>

|<span data-ttu-id="dc7aa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-108">**Name**</span></span>|<span data-ttu-id="dc7aa-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-109">**Required/Optional**</span></span>|<span data-ttu-id="dc7aa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-110">**Data Type**</span></span>|<span data-ttu-id="dc7aa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc7aa-112">_nombreDeForma! theText_</span><span class="sxs-lookup"><span data-stu-id="dc7aa-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="dc7aa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dc7aa-113">Required</span></span>  <br/> |<span data-ttu-id="dc7aa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-114">**String**</span></span> <br/> |<span data-ttu-id="dc7aa-115">Una referencia a la celda llamada TheText en la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="dc7aa-116">_¡nombreDeForma!_</span><span class="sxs-lookup"><span data-stu-id="dc7aa-116">_shapename!_</span></span> <span data-ttu-id="dc7aa-117">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="dc7aa-118">_valor_</span><span class="sxs-lookup"><span data-stu-id="dc7aa-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="dc7aa-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="dc7aa-119">Optional</span></span>  <br/> |<span data-ttu-id="dc7aa-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-120">**Numeric**</span></span> <br/> |<span data-ttu-id="dc7aa-121">Ancho máximo del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc7aa-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7aa-122">Return value</span></span>

<span data-ttu-id="dc7aa-123">String</span><span class="sxs-lookup"><span data-stu-id="dc7aa-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc7aa-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc7aa-124">Remarks</span></span>

<span data-ttu-id="dc7aa-125">La función TEXTWIDTH se utiliza habitualmente para ajustar el ancho de una forma en función del texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="dc7aa-126">Si _hojaN!_</span><span class="sxs-lookup"><span data-stu-id="dc7aa-126">If  _sheetN!_</span></span> <span data-ttu-id="dc7aa-127">es se omite, la forma predeterminada es la forma actual.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="dc7aa-128">Si se especifica _anchoMáximo_ , el resultado es la línea más larga de texto que cabe dentro de _anchoMáximo_.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="dc7aa-129">Si se omite el _valor_ , el resultado es el ancho total del texto.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="dc7aa-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc7aa-130">Example</span></span>

<span data-ttu-id="dc7aa-131">TheText</span><span class="sxs-lookup"><span data-stu-id="dc7aa-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="dc7aa-132">Devuelve la longitud total del texto que hay dentro de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-132">Returns the total length of the text in the current shape.</span></span> 
  

