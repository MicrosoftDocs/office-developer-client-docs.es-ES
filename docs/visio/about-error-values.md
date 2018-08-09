---
title: Valores de error
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Los valores de error se muestran en las celdas que contienen fórmulas incorrectas.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821483"
---
# <a name="about-error-values"></a><span data-ttu-id="051f3-103">Información sobre los valores de error</span><span class="sxs-lookup"><span data-stu-id="051f3-103">About Error Values</span></span>

<span data-ttu-id="051f3-104">Los valores de error se muestran en las celdas que contienen fórmulas incorrectas.</span><span class="sxs-lookup"><span data-stu-id="051f3-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="051f3-p101">Si una fórmula hace referencia a una celda que contiene un valor de error, también mostrará un valor de error. Puede utilizar las funciones ISERR, ISERRNA, ISERROR o ISERRVALUE para buscar valores de error.</span><span class="sxs-lookup"><span data-stu-id="051f3-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="051f3-107">**Valores de error**</span><span class="sxs-lookup"><span data-stu-id="051f3-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="051f3-108">**Si en la celda aparece**</span><span class="sxs-lookup"><span data-stu-id="051f3-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="051f3-109">**La fórmula contiene**</span><span class="sxs-lookup"><span data-stu-id="051f3-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="051f3-110">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="051f3-110">**Example**</span></span> <br/> |
| <span data-ttu-id="051f3-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="051f3-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="051f3-112">
                División entre cero
</span><span class="sxs-lookup"><span data-stu-id="051f3-112">Division by 0</span></span>  <br/> |<span data-ttu-id="051f3-113">10/0</span><span class="sxs-lookup"><span data-stu-id="051f3-113">10/0</span></span>  <br/> |
| <span data-ttu-id="051f3-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="051f3-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="051f3-115">
                
                
                Argumento u operando de tipo no válido
</span><span class="sxs-lookup"><span data-stu-id="051f3-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="051f3-116">
                
                
                5 + "Casa"
</span><span class="sxs-lookup"><span data-stu-id="051f3-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="051f3-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="051f3-117">#REF!</span></span>  <br/> | <span data-ttu-id="051f3-118">
                
                
                Referencia a una celda que no existe
</span><span class="sxs-lookup"><span data-stu-id="051f3-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="051f3-119">
                
                
                Una celda hace referencia a otra que ya no existe
</span><span class="sxs-lookup"><span data-stu-id="051f3-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="051f3-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="051f3-120">#NUM!</span></span>  <br/> | <span data-ttu-id="051f3-121">
                
                
                Número no válido
</span><span class="sxs-lookup"><span data-stu-id="051f3-121">An invalid number</span></span>  <br/> | <span data-ttu-id="051f3-122">
                
                
                Raíz cuadrada de un número negativo
</span><span class="sxs-lookup"><span data-stu-id="051f3-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="051f3-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="051f3-123">#N/A!</span></span>  <br/> | <span data-ttu-id="051f3-124">No es un valor disponible</span><span class="sxs-lookup"><span data-stu-id="051f3-124">Not an available value</span></span>  <br/> | <span data-ttu-id="051f3-125">
                
                
                Función NA( )
</span><span class="sxs-lookup"><span data-stu-id="051f3-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="051f3-126">¡#DIM!</span><span class="sxs-lookup"><span data-stu-id="051f3-126">#DIM!</span></span>  <br/> | <span data-ttu-id="051f3-127">Valor dimensional que excede el intervalo de la dimensión (exponentes válidos son enteros -128 \<= n \<= 127)</span><span class="sxs-lookup"><span data-stu-id="051f3-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="051f3-128">Valor dimensional utilizado en una operación no válida
</span><span class="sxs-lookup"><span data-stu-id="051f3-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="051f3-129">1pda ^ 100 \* 1pda ^ 100 (el resultado es 1pda ^ 200, que está fuera del intervalo de dimensión)</span><span class="sxs-lookup"><span data-stu-id="051f3-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="051f3-130">5,2cm^1,5 (exponente no entero)
</span><span class="sxs-lookup"><span data-stu-id="051f3-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

