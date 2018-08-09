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
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823193"
---
# <a name="shapetext-function"></a><span data-ttu-id="2a8fa-103">Función SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="2a8fa-103">SHAPETEXT Function</span></span>

<span data-ttu-id="2a8fa-104">Obtiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2a8fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a8fa-105">Syntax</span></span>

<span data-ttu-id="2a8fa-106">SHAPETEXT (** *nombreDeForma! TheText* ** ** *[, marca]* **)</span><span class="sxs-lookup"><span data-stu-id="2a8fa-106">SHAPETEXT (** *shapename!TheText* ** ** *[,flag]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2a8fa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a8fa-107">Parameters</span></span>

|<span data-ttu-id="2a8fa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-108">**Name**</span></span>|<span data-ttu-id="2a8fa-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-109">**Required/Optional**</span></span>|<span data-ttu-id="2a8fa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-110">**Data Type**</span></span>|<span data-ttu-id="2a8fa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2a8fa-112">_¡nombreDeForma! TheText_</span><span class="sxs-lookup"><span data-stu-id="2a8fa-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="2a8fa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2a8fa-113">Required</span></span>  <br/> ||<span data-ttu-id="2a8fa-114">Una referencia a la celda llamada TheText en la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="2a8fa-115">_¡NombreDeForma!_</span><span class="sxs-lookup"><span data-stu-id="2a8fa-115">_Shapename!_</span></span> <span data-ttu-id="2a8fa-116">es el nombre de la forma desde la que desea recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="2a8fa-117">_marca_</span><span class="sxs-lookup"><span data-stu-id="2a8fa-117">_flag_</span></span> <br/> |<span data-ttu-id="2a8fa-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="2a8fa-118">Optional</span></span>  <br/> |<span data-ttu-id="2a8fa-119">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-119">**Numeric**</span></span> <br/> |<span data-ttu-id="2a8fa-p102">Un bit que especifica el formato del texto. La marca predeterminada (0) muestra el texto exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-p102">A bit that specifies the format of the text. The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2a8fa-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a8fa-122">Return value</span></span>

<span data-ttu-id="2a8fa-123">String</span><span class="sxs-lookup"><span data-stu-id="2a8fa-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a8fa-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a8fa-124">Remarks</span></span>

<span data-ttu-id="2a8fa-125">En la función SHAPETEXT, puede usar cualquier combinación de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="2a8fa-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-126">**Flag**</span></span>|<span data-ttu-id="2a8fa-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a8fa-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a8fa-128">0</span><span class="sxs-lookup"><span data-stu-id="2a8fa-128">0</span></span>  <br/> |<span data-ttu-id="2a8fa-129">Mostrar el texto exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-130">1</span><span class="sxs-lookup"><span data-stu-id="2a8fa-130">1</span></span>  <br/> |<span data-ttu-id="2a8fa-131">Incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-132">2</span><span class="sxs-lookup"><span data-stu-id="2a8fa-132">2</span></span>  <br/> |<span data-ttu-id="2a8fa-133">No incluir el texto expandido en los campos.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-134">4</span><span class="sxs-lookup"><span data-stu-id="2a8fa-134">4</span></span>  <br/> |<span data-ttu-id="2a8fa-135">Convertir los tabuladores en un espacio.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-136">8</span><span class="sxs-lookup"><span data-stu-id="2a8fa-136">8</span></span>  <br/> |<span data-ttu-id="2a8fa-137">Convertir los tabuladores en varios espacios.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-138">16</span><span class="sxs-lookup"><span data-stu-id="2a8fa-138">16</span></span>  <br/> |<span data-ttu-id="2a8fa-139">Convertir los retornos de carro y las nuevas líneas en espacios.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-140">32</span><span class="sxs-lookup"><span data-stu-id="2a8fa-140">32</span></span>  <br/> |<span data-ttu-id="2a8fa-141">Convertir las comillas tipográficas en comillas normales.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="2a8fa-142">64</span><span class="sxs-lookup"><span data-stu-id="2a8fa-142">64</span></span>  <br/> |<span data-ttu-id="2a8fa-143">Convertir los espacios en blanco contiguos en un solo espacio.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="2a8fa-144">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a8fa-144">Example 1</span></span>

<span data-ttu-id="2a8fa-145">SHAPETEXT(sheetN!TheText)</span><span class="sxs-lookup"><span data-stu-id="2a8fa-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="2a8fa-146">Devuelve el texto de la forma llamada hojaN exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2a8fa-147">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2a8fa-147">Example 2</span></span>

<span data-ttu-id="2a8fa-148">SHAPETEXT(TheText)</span><span class="sxs-lookup"><span data-stu-id="2a8fa-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="2a8fa-149">Devuelve el texto de la forma actual exactamente como se muestra en la forma.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2a8fa-150">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="2a8fa-150">Example 3</span></span>

<span data-ttu-id="2a8fa-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="2a8fa-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="2a8fa-p103">Devuelve el texto de la forma actual. Además, convierte los espacios en blanco contiguos en un solo espacio (64), los retornos de carro y las nuevas líneas en espacios (16), y los tabuladores en un solo espacio (4). La suma de dichas marcas es 84.</span><span class="sxs-lookup"><span data-stu-id="2a8fa-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

