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
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412152"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="d54d7-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="d54d7-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="d54d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d54d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d54d7-105">Mueve el cursor a una posición fraccional aproximada en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="d54d7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d54d7-106">Parameters</span></span>

 <span data-ttu-id="d54d7-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="d54d7-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="d54d7-108">a Puntero al numerador de la fracción que representa la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="d54d7-109">Si el parámetro _ulNumerator_ es cero, el cursor se coloca al principio de la tabla independientemente del valor del denominador.</span><span class="sxs-lookup"><span data-stu-id="d54d7-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="d54d7-110">Si _ulNumerator_ es igual al parámetro _ulDenominator_ , el cursor se coloca detrás de la última fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="d54d7-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="d54d7-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="d54d7-112">a Puntero al denominador de la fracción que representa la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="d54d7-113">El parámetro _ulDenominator_ no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="d54d7-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d54d7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d54d7-114">Return value</span></span>

<span data-ttu-id="d54d7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d54d7-115">S_OK</span></span> 
  
> <span data-ttu-id="d54d7-116">La operación de búsqueda se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d54d7-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="d54d7-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d54d7-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d54d7-118">Hay otra operación en curso que evita que la operación de búsqueda de filas se inicie.</span><span class="sxs-lookup"><span data-stu-id="d54d7-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="d54d7-119">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="d54d7-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d54d7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d54d7-120">Remarks</span></span>

<span data-ttu-id="d54d7-121">La posición del cursor en una tabla después de una llamada al método **IMAPITable:: SeekRowApprox** es heurísticamente la fracción y podría no ser exacta.</span><span class="sxs-lookup"><span data-stu-id="d54d7-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="d54d7-122">Por ejemplo, algunos proveedores pueden implementar una tabla sobre un árbol binario, tratando la mitad central de la tabla como la parte superior del árbol por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d54d7-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="d54d7-123">Si no se equilibra el árbol, es posible que el punto medio utilizado no sea exactamente la mitad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d54d7-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d54d7-124">Notes to callers</span></span>

<span data-ttu-id="d54d7-125">Llamar a **SeekRowApprox** para proporcionar los datos para la implementación de una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d54d7-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="d54d7-126">Por ejemplo, si el usuario coloca el cuadro de desplazamiento 2/3 hacia abajo en la barra de desplazamiento, puede modelar esa acción llamando a **SeekRowApprox** y pasando un valor fraccionario equivalente mediante _ulNumerator_ y _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="d54d7-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="d54d7-127">La búsqueda de **SeekRowApprox** siempre es absoluta desde el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d54d7-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="d54d7-128">Para ir al final de la tabla, los valores de _ulNumerator_ y _ulDenominator_ deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="d54d7-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="d54d7-129">Use cualquier esquema de números adecuado.</span><span class="sxs-lookup"><span data-stu-id="d54d7-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="d54d7-130">Es decir, para buscar una posición a mitad de la tabla, puede especificar 1/2, 10/20 o 50/100.</span><span class="sxs-lookup"><span data-stu-id="d54d7-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d54d7-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="d54d7-131">See also</span></span>



[<span data-ttu-id="d54d7-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d54d7-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

