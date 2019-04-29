---
title: EVALCELL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor para pasar a la función personalizada como argumentos (opcional). Devuelve el resultado calculado de la función personalizada a partir de los argumentos y valores especificados.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418907"
---
# <a name="evalcell-function"></a><span data-ttu-id="c2991-104">Función EVALCELL</span><span class="sxs-lookup"><span data-stu-id="c2991-104">EVALCELL Function</span></span>

<span data-ttu-id="c2991-105">Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor para pasar a la función personalizada como argumentos (opcional).</span><span class="sxs-lookup"><span data-stu-id="c2991-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="c2991-106">Devuelve el resultado calculado de la función personalizada a partir de los argumentos y valores especificados.</span><span class="sxs-lookup"><span data-stu-id="c2991-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c2991-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2991-107">Syntax</span></span>

<span data-ttu-id="c2991-108">EVALCELL (\* \* *cellRef* \* *, [* \* *arg1Name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="c2991-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c2991-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2991-109">Parameters</span></span>

|<span data-ttu-id="c2991-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c2991-110">**Name**</span></span>|<span data-ttu-id="c2991-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c2991-111">**Required/Optional**</span></span>|<span data-ttu-id="c2991-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c2991-112">**Data Type**</span></span>|<span data-ttu-id="c2991-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2991-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c2991-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="c2991-114">_cellRef_</span></span> <br/> |<span data-ttu-id="c2991-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c2991-115">Required</span></span>  <br/> |<span data-ttu-id="c2991-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c2991-116">**String**</span></span> <br/> |<span data-ttu-id="c2991-117">Referencia a una celda que contiene la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="c2991-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="c2991-118">Se permiten referencias entre hojas.</span><span class="sxs-lookup"><span data-stu-id="c2991-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="c2991-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="c2991-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="c2991-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2991-120">Optional</span></span>  <br/> |<span data-ttu-id="c2991-121">**String**</span><span class="sxs-lookup"><span data-stu-id="c2991-121">**String**</span></span> <br/> |<span data-ttu-id="c2991-122">Nombre del primer argumento que se va a pasar a la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="c2991-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="c2991-123">Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="c2991-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="c2991-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="c2991-124">_arg1_</span></span> <br/> |<span data-ttu-id="c2991-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2991-125">Optional</span></span>  <br/> |<span data-ttu-id="c2991-126">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="c2991-126">**Varies**</span></span> <br/> |<span data-ttu-id="c2991-127">Valor del parámetro _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="c2991-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="c2991-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="c2991-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="c2991-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2991-129">Optional</span></span>  <br/> |<span data-ttu-id="c2991-130">**String**</span><span class="sxs-lookup"><span data-stu-id="c2991-130">**String**</span></span> <br/> |<span data-ttu-id="c2991-131">Nombre del segundo argumento que se va a pasar a la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="c2991-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="c2991-132">Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="c2991-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="c2991-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="c2991-133">_arg2_</span></span> <br/> |<span data-ttu-id="c2991-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2991-134">Optional</span></span>  <br/> |<span data-ttu-id="c2991-135">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="c2991-135">**Varies**</span></span> <br/> |<span data-ttu-id="c2991-136">Valor del parámetro _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="c2991-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c2991-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2991-137">Return value</span></span>

<span data-ttu-id="c2991-138">Número</span><span class="sxs-lookup"><span data-stu-id="c2991-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2991-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2991-139">Remarks</span></span>

<span data-ttu-id="c2991-140">No es necesario especificar en la celda que realiza la llamada todos los argumentos utilizados por la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="c2991-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c2991-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2991-141">Example</span></span>

<span data-ttu-id="c2991-142">En el ejemplo siguiente se muestra cómo utilizar la función EVALCELL en combinación con la función ARG para buscar el valor medio en un conjunto de tres valores.</span><span class="sxs-lookup"><span data-stu-id="c2991-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="c2991-143">En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="c2991-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="c2991-144">En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="c2991-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


