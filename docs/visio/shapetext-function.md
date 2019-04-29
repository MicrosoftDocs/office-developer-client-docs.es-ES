---
title: SHAPETEXT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtiene el texto de una forma.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419348"
---
# <a name="shapetext-function"></a><span data-ttu-id="6baf1-103">Función SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="6baf1-103">SHAPETEXT Function</span></span>

<span data-ttu-id="6baf1-104">Obtiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="6baf1-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6baf1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6baf1-105">Syntax</span></span>

<span data-ttu-id="6baf1-106">SHAPETEXT (\* \* *nombredeforma! Text* \* \* \* \* *[, Flag]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6baf1-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6baf1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6baf1-107">Parameters</span></span>

|<span data-ttu-id="6baf1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6baf1-108">**Name**</span></span>|<span data-ttu-id="6baf1-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6baf1-109">**Required/Optional**</span></span>|<span data-ttu-id="6baf1-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6baf1-110">**Data Type**</span></span>|<span data-ttu-id="6baf1-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6baf1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6baf1-112">_nombredeforma! TheText_</span><span class="sxs-lookup"><span data-stu-id="6baf1-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="6baf1-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6baf1-113">Required</span></span>  <br/> ||<span data-ttu-id="6baf1-114">Una referencia a la celda llamada TheText de la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="6baf1-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="6baf1-115">_Nombredeforma!_</span><span class="sxs-lookup"><span data-stu-id="6baf1-115">_Shapename!_</span></span> <span data-ttu-id="6baf1-116">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="6baf1-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="6baf1-117">_flag_</span><span class="sxs-lookup"><span data-stu-id="6baf1-117">_flag_</span></span> <br/> |<span data-ttu-id="6baf1-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="6baf1-118">Optional</span></span>  <br/> |<span data-ttu-id="6baf1-119">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="6baf1-119">**Numeric**</span></span> <br/> |<span data-ttu-id="6baf1-120">Un bit que especifica el formato del texto.</span><span class="sxs-lookup"><span data-stu-id="6baf1-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="6baf1-121">La marca predeterminada (0) muestra el texto exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="6baf1-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6baf1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6baf1-122">Return value</span></span>

<span data-ttu-id="6baf1-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="6baf1-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6baf1-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6baf1-124">Remarks</span></span>

<span data-ttu-id="6baf1-125">En la función SHAPETEXT, puede usar cualquier combinación de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="6baf1-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="6baf1-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="6baf1-126">**Flag**</span></span>|<span data-ttu-id="6baf1-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6baf1-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6baf1-128">comprendi</span><span class="sxs-lookup"><span data-stu-id="6baf1-128">0</span></span>  <br/> |<span data-ttu-id="6baf1-129">Mostrar el texto exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="6baf1-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="6baf1-130">1</span><span class="sxs-lookup"><span data-stu-id="6baf1-130">1</span></span>  <br/> |<span data-ttu-id="6baf1-131">Incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="6baf1-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="6baf1-132">segundo</span><span class="sxs-lookup"><span data-stu-id="6baf1-132">2</span></span>  <br/> |<span data-ttu-id="6baf1-133">No incluir el texto expandido en los campos.</span><span class="sxs-lookup"><span data-stu-id="6baf1-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="6baf1-134">4 </span><span class="sxs-lookup"><span data-stu-id="6baf1-134">4</span></span>  <br/> |<span data-ttu-id="6baf1-135">Convertir los tabuladores en un espacio.</span><span class="sxs-lookup"><span data-stu-id="6baf1-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="6baf1-136">8 </span><span class="sxs-lookup"><span data-stu-id="6baf1-136">8</span></span>  <br/> |<span data-ttu-id="6baf1-137">Convertir los tabuladores en varios espacios.</span><span class="sxs-lookup"><span data-stu-id="6baf1-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="6baf1-138">16 </span><span class="sxs-lookup"><span data-stu-id="6baf1-138">16</span></span>  <br/> |<span data-ttu-id="6baf1-139">Convertir los retornos de carro y las nuevas líneas en espacios.</span><span class="sxs-lookup"><span data-stu-id="6baf1-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="6baf1-140">32</span><span class="sxs-lookup"><span data-stu-id="6baf1-140">32</span></span>  <br/> |<span data-ttu-id="6baf1-141">Convertir las comillas tipográficas en comillas normales.</span><span class="sxs-lookup"><span data-stu-id="6baf1-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="6baf1-142">64</span><span class="sxs-lookup"><span data-stu-id="6baf1-142">64</span></span>  <br/> |<span data-ttu-id="6baf1-143">Convertir los espacios en blanco contiguos en un solo espacio.</span><span class="sxs-lookup"><span data-stu-id="6baf1-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="6baf1-144">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6baf1-144">Example 1</span></span>

<span data-ttu-id="6baf1-145">SHAPETEXT (hoja de texto)</span><span class="sxs-lookup"><span data-stu-id="6baf1-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="6baf1-146">Devuelve el texto de la forma llamada hojaN exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="6baf1-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6baf1-147">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="6baf1-147">Example 2</span></span>

<span data-ttu-id="6baf1-148">SHAPETEXT (TheText)</span><span class="sxs-lookup"><span data-stu-id="6baf1-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="6baf1-149">Devuelve el texto de la forma actual exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="6baf1-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6baf1-150">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="6baf1-150">Example 3</span></span>

<span data-ttu-id="6baf1-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="6baf1-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="6baf1-p103">Devuelve el texto de la forma actual. Además, convierte los espacios en blanco contiguos en un solo espacio (64), los retornos de carro y las nuevas líneas en espacios (16), y los tabuladores en un solo espacio (4). La suma de dichas marcas es 84.</span><span class="sxs-lookup"><span data-stu-id="6baf1-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

