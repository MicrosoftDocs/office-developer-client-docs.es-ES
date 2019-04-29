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
description: Devuelve el ancho del texto compuesto en una forma.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422036"
---
# <a name="textwidth-function"></a><span data-ttu-id="4fa15-103">Función TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="4fa15-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="4fa15-104">Devuelve el ancho del texto compuesto en una forma.</span><span class="sxs-lookup"><span data-stu-id="4fa15-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4fa15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fa15-105">Syntax</span></span>

<span data-ttu-id="4fa15-106">TEXTWIDTH (\* \* *nombredeforma! TheText* \* \* \* \* *[, MaximumWidth]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4fa15-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4fa15-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fa15-107">Parameters</span></span>

|<span data-ttu-id="4fa15-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4fa15-108">**Name**</span></span>|<span data-ttu-id="4fa15-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4fa15-109">**Required/Optional**</span></span>|<span data-ttu-id="4fa15-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4fa15-110">**Data Type**</span></span>|<span data-ttu-id="4fa15-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fa15-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4fa15-112">_nombredeforma! TheText_</span><span class="sxs-lookup"><span data-stu-id="4fa15-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="4fa15-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4fa15-113">Required</span></span>  <br/> |<span data-ttu-id="4fa15-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4fa15-114">**String**</span></span> <br/> |<span data-ttu-id="4fa15-115">Una referencia a la celda llamada TheText de la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="4fa15-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="4fa15-116">_nombredeforma!_</span><span class="sxs-lookup"><span data-stu-id="4fa15-116">_shapename!_</span></span> <span data-ttu-id="4fa15-117">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="4fa15-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="4fa15-118">_MaximumWidth_</span><span class="sxs-lookup"><span data-stu-id="4fa15-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="4fa15-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="4fa15-119">Optional</span></span>  <br/> |<span data-ttu-id="4fa15-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4fa15-120">**Numeric**</span></span> <br/> |<span data-ttu-id="4fa15-121">Ancho máximo del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="4fa15-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4fa15-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fa15-122">Return value</span></span>

<span data-ttu-id="4fa15-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fa15-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fa15-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fa15-124">Remarks</span></span>

<span data-ttu-id="4fa15-125">La función TEXTWIDTH se utiliza habitualmente para ajustar el ancho de una forma en función del texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="4fa15-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="4fa15-126">Si _sheetn!_</span><span class="sxs-lookup"><span data-stu-id="4fa15-126">If  _sheetN!_</span></span> <span data-ttu-id="4fa15-127">se omite, la forma predeterminada es la forma actual.</span><span class="sxs-lookup"><span data-stu-id="4fa15-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="4fa15-128">Si se especifica _MaximumWidth_ , el resultado es la mayor línea de texto que cabe en _MaximumWidth_.</span><span class="sxs-lookup"><span data-stu-id="4fa15-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="4fa15-129">Si se omite _MaximumWidth_ , el resultado es el ancho total del texto.</span><span class="sxs-lookup"><span data-stu-id="4fa15-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4fa15-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4fa15-130">Example</span></span>

<span data-ttu-id="4fa15-131">TEXTWIDTH (TheText)</span><span class="sxs-lookup"><span data-stu-id="4fa15-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="4fa15-132">Devuelve la longitud total del texto que hay dentro de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="4fa15-132">Returns the total length of the text in the current shape.</span></span> 
  

