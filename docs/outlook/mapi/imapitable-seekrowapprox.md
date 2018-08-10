---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817617"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="3bf6d-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="3bf6d-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="3bf6d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bf6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3bf6d-105">Mueve el cursor a una posición aproximada fraccionaria en la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="3bf6d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bf6d-106">Parameters</span></span>

 <span data-ttu-id="3bf6d-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="3bf6d-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="3bf6d-108">[entrada] Puntero a la numerador de la fracción que representa la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="3bf6d-109">Si el parámetro _ulNumerator_ es cero, se coloca el cursor al principio de la tabla independientemente del valor de denominador.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="3bf6d-110">Si _ulNumerator_ es igual que el parámetro _ulDenominator_ , se coloca el cursor después de la última fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="3bf6d-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="3bf6d-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="3bf6d-112">[entrada] Puntero a como denominador de la fracción que representa la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="3bf6d-113">El parámetro _ulDenominator_ no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bf6d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bf6d-114">Return value</span></span>

<span data-ttu-id="3bf6d-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bf6d-115">S_OK</span></span> 
  
> <span data-ttu-id="3bf6d-116">La operación seek fue correcta.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="3bf6d-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3bf6d-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3bf6d-118">Otra operación está en curso que impide que la fila que busquen la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="3bf6d-119">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bf6d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bf6d-120">Remarks</span></span>

<span data-ttu-id="3bf6d-121">La posición del cursor en una tabla después de una llamada al método **IMAPITable:: SeekRowApprox** es la fracción de forma heurística y puede no ser exacta.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="3bf6d-122">Por ejemplo, ciertos proveedores podrían implementar una tabla en la parte superior un árbol binario, tratando punto intermedio de la tabla como la parte superior del árbol por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="3bf6d-123">Si no se equilibra el árbol, a continuación, el punto medio utilizado podría no ser exactamente la mitad a través de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3bf6d-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3bf6d-124">Notes to callers</span></span>

<span data-ttu-id="3bf6d-125">Llame a **SeekRowApprox** para proporcionar los datos para una implementación de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="3bf6d-126">Por ejemplo, si el usuario coloca el cuadro de desplazamiento 2/3 hacia abajo de la barra de desplazamiento, se puede modelar esa acción llamando a **SeekRowApprox** y pasando un valor fraccionario equivalente mediante _ulNumerator_ y _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="3bf6d-127">La búsqueda de **SeekRowApprox** siempre es absoluta desde el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="3bf6d-128">Para desplazarse hasta el final de la tabla, los valores de _ulNumerator_ y _ulDenominator_ deben ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="3bf6d-129">Usar cualquier combinación de número es adecuado.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="3bf6d-130">Es decir, para buscar a una posición intermedia a través de la tabla, puede especificar 1/2, 10/20 o 50/100.</span><span class="sxs-lookup"><span data-stu-id="3bf6d-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bf6d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bf6d-131">See also</span></span>



[<span data-ttu-id="3bf6d-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bf6d-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

