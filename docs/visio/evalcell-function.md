---
title: EVALCELL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor que se pase a la función personalizada como argumentos (opcional). Devuelve el resultado de la función personalizada dados los argumentos especificados y los valores calculado.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822073"
---
# <a name="evalcell-function"></a><span data-ttu-id="70fc5-104">EVALCELL (función)</span><span class="sxs-lookup"><span data-stu-id="70fc5-104">EVALCELL Function</span></span>

<span data-ttu-id="70fc5-105">Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor que se pase a la función personalizada como argumentos (opcional).</span><span class="sxs-lookup"><span data-stu-id="70fc5-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="70fc5-106">Devuelve el resultado de la función personalizada dados los argumentos especificados y los valores calculado.</span><span class="sxs-lookup"><span data-stu-id="70fc5-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="70fc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70fc5-107">Syntax</span></span>

<span data-ttu-id="70fc5-108">EVALCELL (** *cellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **], …)</span><span class="sxs-lookup"><span data-stu-id="70fc5-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="70fc5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70fc5-109">Parameters</span></span>

|<span data-ttu-id="70fc5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="70fc5-110">**Name**</span></span>|<span data-ttu-id="70fc5-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="70fc5-111">**Required/Optional**</span></span>|<span data-ttu-id="70fc5-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="70fc5-112">**Data Type**</span></span>|<span data-ttu-id="70fc5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70fc5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="70fc5-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="70fc5-114">_cellRef_</span></span> <br/> |<span data-ttu-id="70fc5-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="70fc5-115">Required</span></span>  <br/> |<span data-ttu-id="70fc5-116">**String**</span><span class="sxs-lookup"><span data-stu-id="70fc5-116">**String**</span></span> <br/> |<span data-ttu-id="70fc5-117">Una referencia a la celda que contiene la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="70fc5-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="70fc5-118">Se permiten referencias entre hojas.</span><span class="sxs-lookup"><span data-stu-id="70fc5-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="70fc5-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="70fc5-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="70fc5-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="70fc5-120">Optional</span></span>  <br/> |<span data-ttu-id="70fc5-121">**String**</span><span class="sxs-lookup"><span data-stu-id="70fc5-121">**String**</span></span> <br/> |<span data-ttu-id="70fc5-p104">Nombre del primer argumento que se va a pasar a la función personalizada. Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="70fc5-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="70fc5-124">_Arg1_</span><span class="sxs-lookup"><span data-stu-id="70fc5-124">_arg1_</span></span> <br/> |<span data-ttu-id="70fc5-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="70fc5-125">Optional</span></span>  <br/> |<span data-ttu-id="70fc5-126">**Varía**</span><span class="sxs-lookup"><span data-stu-id="70fc5-126">**Varies**</span></span> <br/> |<span data-ttu-id="70fc5-127">Valor del parámetro _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="70fc5-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="70fc5-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="70fc5-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="70fc5-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="70fc5-129">Optional</span></span>  <br/> |<span data-ttu-id="70fc5-130">**String**</span><span class="sxs-lookup"><span data-stu-id="70fc5-130">**String**</span></span> <br/> |<span data-ttu-id="70fc5-131">El nombre del segundo argumento que se pasan a la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="70fc5-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="70fc5-132">Se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="70fc5-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="70fc5-133">_Arg2_</span><span class="sxs-lookup"><span data-stu-id="70fc5-133">_arg2_</span></span> <br/> |<span data-ttu-id="70fc5-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="70fc5-134">Optional</span></span>  <br/> |<span data-ttu-id="70fc5-135">**Varía**</span><span class="sxs-lookup"><span data-stu-id="70fc5-135">**Varies**</span></span> <br/> |<span data-ttu-id="70fc5-136">Valor del parámetro _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="70fc5-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="70fc5-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70fc5-137">Return value</span></span>

<span data-ttu-id="70fc5-138">Number</span><span class="sxs-lookup"><span data-stu-id="70fc5-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70fc5-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70fc5-139">Remarks</span></span>

<span data-ttu-id="70fc5-140">No es necesario especificar en la celda que realiza la llamada todos los argumentos utilizados por la función personalizada.</span><span class="sxs-lookup"><span data-stu-id="70fc5-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="70fc5-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70fc5-141">Example</span></span>

<span data-ttu-id="70fc5-142">En el ejemplo siguiente se muestra cómo utilizar la función EVALCELL en combinación con la función ARG para buscar el valor medio en un conjunto de tres valores.</span><span class="sxs-lookup"><span data-stu-id="70fc5-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="70fc5-143">En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="70fc5-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="70fc5-144">En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="70fc5-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


