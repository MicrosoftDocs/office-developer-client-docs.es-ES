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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329074"
---
# <a name="evalcell-function"></a><span data-ttu-id="7468c-104">Función EVALCELL</span><span class="sxs-lookup"><span data-stu-id="7468c-104">EVALCELL Function</span></span>

<span data-ttu-id="7468c-105">Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor para pasar a la función personalizada como argumentos (opcional).</span><span class="sxs-lookup"><span data-stu-id="7468c-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="7468c-106">Devuelve el resultado calculado de la función personalizada a partir de los argumentos y valores especificados.</span><span class="sxs-lookup"><span data-stu-id="7468c-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7468c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7468c-107">Syntax</span></span>

<span data-ttu-id="7468c-108">EVALCELL (\* \* *cellRef* \* *, [* \* *arg1Name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="7468c-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7468c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7468c-109">Parameters</span></span>

|<span data-ttu-id="7468c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7468c-110">**Name**</span></span>|<span data-ttu-id="7468c-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7468c-111">**Required/Optional**</span></span>|<span data-ttu-id="7468c-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7468c-112">**Data Type**</span></span>|<span data-ttu-id="7468c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7468c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7468c-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="7468c-114">_cellRef_</span></span> <br/> |<span data-ttu-id="7468c-115">Necesario</span><span class="sxs-lookup"><span data-stu-id="7468c-115">Required</span></span>  <br/> |<span data-ttu-id="7468c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="7468c-116">**String**</span></span> <br/> |<span data-ttu-id="7468c-117">Referencia a una celda que contiene la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="7468c-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="7468c-118">Se permiten referencias entre hojas.</span><span class="sxs-lookup"><span data-stu-id="7468c-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="7468c-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="7468c-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="7468c-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="7468c-120">Optional</span></span>  <br/> |<span data-ttu-id="7468c-121">**String**</span><span class="sxs-lookup"><span data-stu-id="7468c-121">**String**</span></span> <br/> |<span data-ttu-id="7468c-122">Nombre del primer argumento que se va a pasar a la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="7468c-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="7468c-123">Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="7468c-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="7468c-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="7468c-124">_arg1_</span></span> <br/> |<span data-ttu-id="7468c-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="7468c-125">Optional</span></span>  <br/> |<span data-ttu-id="7468c-126">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="7468c-126">**Varies**</span></span> <br/> |<span data-ttu-id="7468c-127">Valor del parámetro _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="7468c-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="7468c-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="7468c-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="7468c-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="7468c-129">Optional</span></span>  <br/> |<span data-ttu-id="7468c-130">**String**</span><span class="sxs-lookup"><span data-stu-id="7468c-130">**String**</span></span> <br/> |<span data-ttu-id="7468c-131">Nombre del segundo argumento que se va a pasar a la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="7468c-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="7468c-132">Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="7468c-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="7468c-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="7468c-133">_arg2_</span></span> <br/> |<span data-ttu-id="7468c-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="7468c-134">Optional</span></span>  <br/> |<span data-ttu-id="7468c-135">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="7468c-135">**Varies**</span></span> <br/> |<span data-ttu-id="7468c-136">Valor del parámetro _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="7468c-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7468c-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7468c-137">Return value</span></span>

<span data-ttu-id="7468c-138">Número</span><span class="sxs-lookup"><span data-stu-id="7468c-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7468c-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7468c-139">Remarks</span></span>

<span data-ttu-id="7468c-140">No es necesario especificar en la celda que realiza la llamada todos los argumentos utilizados por la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="7468c-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7468c-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7468c-141">Example</span></span>

<span data-ttu-id="7468c-142">En el ejemplo siguiente se muestra cómo utilizar la función EVALCELL en combinación con la función ARG para buscar el valor medio en un conjunto de tres valores.</span><span class="sxs-lookup"><span data-stu-id="7468c-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="7468c-143">En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="7468c-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="7468c-144">En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="7468c-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


