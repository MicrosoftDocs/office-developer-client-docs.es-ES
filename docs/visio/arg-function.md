---
title: ARG (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica un argumento que la celda que realiza la llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que realiza la llamada no pasa un valor para el argumento. Devuelve el valor especificado por la celda que realiza la llamada y el parámetro argName correspondiente.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293488"
---
# <a name="arg-function"></a><span data-ttu-id="83e3d-104">Función ARG</span><span class="sxs-lookup"><span data-stu-id="83e3d-104">ARG Function</span></span>

<span data-ttu-id="83e3d-105">Especifica un argumento que la celda que realiza la llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que realiza la llamada no pasa un valor para el argumento.</span><span class="sxs-lookup"><span data-stu-id="83e3d-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="83e3d-106">Devuelve el valor especificado por la celda que realiza la llamada y el parámetro argName correspondiente.</span><span class="sxs-lookup"><span data-stu-id="83e3d-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="83e3d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83e3d-107">Syntax</span></span>

<span data-ttu-id="83e3d-108">ARG (***argName***, [ ***DefaultValue*** ])</span><span class="sxs-lookup"><span data-stu-id="83e3d-108">ARG(***argName***,[ ***defaultValue*** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="83e3d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83e3d-109">Parameters</span></span>

|<span data-ttu-id="83e3d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="83e3d-110">**Name**</span></span>|<span data-ttu-id="83e3d-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="83e3d-111">**Required/Optional**</span></span>|<span data-ttu-id="83e3d-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="83e3d-112">**Data Type**</span></span>|<span data-ttu-id="83e3d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83e3d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83e3d-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="83e3d-114">_argName_</span></span> <br/> |<span data-ttu-id="83e3d-115">Necesario</span><span class="sxs-lookup"><span data-stu-id="83e3d-115">Required</span></span>  <br/> |<span data-ttu-id="83e3d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="83e3d-116">**String**</span></span> <br/> |<span data-ttu-id="83e3d-117">Nombre de un argumento que la celda que realiza la llamada puede pasar a la función</span><span class="sxs-lookup"><span data-stu-id="83e3d-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="83e3d-118">_Valor predeterminado_</span><span class="sxs-lookup"><span data-stu-id="83e3d-118">_default Value_</span></span> <br/> |<span data-ttu-id="83e3d-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="83e3d-119">Optional</span></span>  <br/> |<span data-ttu-id="83e3d-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="83e3d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="83e3d-121">El valor devuelto por ARG si la celda que realiza la llamada no pasa un valor para el parámetro  _argName_ .</span><span class="sxs-lookup"><span data-stu-id="83e3d-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83e3d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83e3d-122">Remarks</span></span>

<span data-ttu-id="83e3d-p103">Como programador de formas, puede crear funciones personalizadas colocando una expresión en una celda y llamando a esa expresión desde una o varias celdas. Esta expresión puede incluir cadenas literales y funciones y referencias a celdas de ShapeSheet. Esta expresión también puede incluir argumentos específicos que pasa la celda que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="83e3d-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="83e3d-126">La celda que realiza la llamada especifica la celda que contiene la función personalizada, así como los argumentos que desea pasar a la función.</span><span class="sxs-lookup"><span data-stu-id="83e3d-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="83e3d-127">La celda que contiene la expresión se evalúa y se devuelve el resultado a la celda que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="83e3d-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="83e3d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83e3d-128">Example</span></span>

<span data-ttu-id="83e3d-129">En el ejemplo siguiente se muestra cómo utilizar la función ARG en combinación con la función EVALCELL para buscar el valor medio en un conjunto de tres valores.</span><span class="sxs-lookup"><span data-stu-id="83e3d-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="83e3d-130">En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="83e3d-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="83e3d-131">En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:</span><span class="sxs-lookup"><span data-stu-id="83e3d-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


