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
description: Devuelve el alto del texto compuesto en una forma donde ninguna línea de texto supere MaximumWidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427412"
---
# <a name="textheight-function"></a><span data-ttu-id="406f8-103">Función TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="406f8-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="406f8-104">Devuelve el alto del texto compuesto en una forma donde ninguna línea de texto supere _MaximumWidth_.</span><span class="sxs-lookup"><span data-stu-id="406f8-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="406f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="406f8-105">Syntax</span></span>

<span data-ttu-id="406f8-106">TEXTHEIGHT (\* \* *nombredeforma! TheText* \* \* \* \* *[, MaximumWidth]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="406f8-106">TEXTHEIGHT(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="406f8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="406f8-107">Parameters</span></span>

|<span data-ttu-id="406f8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="406f8-108">**Name**</span></span>|<span data-ttu-id="406f8-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="406f8-109">**Required/Optional**</span></span>|<span data-ttu-id="406f8-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="406f8-110">**Data Type**</span></span>|<span data-ttu-id="406f8-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="406f8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="406f8-112">_nombredeforma! TheText_</span><span class="sxs-lookup"><span data-stu-id="406f8-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="406f8-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="406f8-113">Required</span></span>  <br/> |<span data-ttu-id="406f8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="406f8-114">**String**</span></span> <br/> |<span data-ttu-id="406f8-115">Una referencia a la celda llamada TheText de la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="406f8-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="406f8-116">_nombredeforma!_</span><span class="sxs-lookup"><span data-stu-id="406f8-116">_shapename!_</span></span> <span data-ttu-id="406f8-117">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="406f8-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="406f8-118">_MaximumWidth_</span><span class="sxs-lookup"><span data-stu-id="406f8-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="406f8-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="406f8-119">Optional</span></span>  <br/> |<span data-ttu-id="406f8-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="406f8-120">**Numeric**</span></span> <br/> |<span data-ttu-id="406f8-121">Ancho máximo del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="406f8-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="406f8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="406f8-122">Return value</span></span>

<span data-ttu-id="406f8-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="406f8-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="406f8-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="406f8-124">Remarks</span></span>

<span data-ttu-id="406f8-p102">El valor que se devuelve incluye el alto del texto, los espacios que le preceden y le siguen, el espaciado entre líneas del texto y los márgenes superior e inferior del bloque de texto. Esta función se utiliza habitualmente para ajustar el alto de una forma en función del texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="406f8-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="406f8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="406f8-127">Example</span></span>

<span data-ttu-id="406f8-128">TEXTHEIGHT(TheText,(Width - 0,5 pda))</span><span class="sxs-lookup"><span data-stu-id="406f8-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="406f8-129">Devuelve el alto del texto cuando se ajusta al ancho de la forma menos 0,5 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="406f8-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

