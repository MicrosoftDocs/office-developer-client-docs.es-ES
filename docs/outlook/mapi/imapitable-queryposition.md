---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c3c66b9e54f0776a8afd6b4638d36dec3393dda8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817595"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="82d0c-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="82d0c-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="82d0c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82d0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82d0c-105">Recupera la posición de fila de tabla actual del cursor, basándose en un valor decimal.</span><span class="sxs-lookup"><span data-stu-id="82d0c-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="82d0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82d0c-106">Parameters</span></span>

 <span data-ttu-id="82d0c-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="82d0c-107">_lpulRow_</span></span>
  
> <span data-ttu-id="82d0c-108">[out] Puntero al número de la fila actual.</span><span class="sxs-lookup"><span data-stu-id="82d0c-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="82d0c-109">El número de fila es de base cero; la primera fila en la tabla es cero.</span><span class="sxs-lookup"><span data-stu-id="82d0c-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="82d0c-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="82d0c-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="82d0c-111">[out] Puntero al numerador de la fracción que identifica la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d0c-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="82d0c-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="82d0c-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="82d0c-113">[out] Puntero al denominador de la fracción que identifica la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d0c-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="82d0c-114">El parámetro _lpulDenominator_ no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="82d0c-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82d0c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82d0c-115">Return value</span></span>

<span data-ttu-id="82d0c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="82d0c-116">S_OK</span></span> 
  
> <span data-ttu-id="82d0c-117">El método devuelve los valores válidos en _lpulRow_, _lpulNumerator_y _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="82d0c-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82d0c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82d0c-118">Remarks</span></span>

<span data-ttu-id="82d0c-119">El método **IMAPITable::QueryPosition** determina la posición de la fila actual y devuelve el número de la fila actual y un valor decimal que indica su posición relativa al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d0c-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="82d0c-120">MAPI define la fila actual como la siguiente fila se leerá.</span><span class="sxs-lookup"><span data-stu-id="82d0c-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="82d0c-121">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="82d0c-121">Notes to implementers</span></span>

<span data-ttu-id="82d0c-122">No es necesario devolver el número exacto de filas en la tabla para el parámetro _lpulDenominator_ ; puede ser una aproximación.</span><span class="sxs-lookup"><span data-stu-id="82d0c-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="82d0c-123">Si no puede determinar la fila actual, devolverá un valor de 0xFFFFFFFF en _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="82d0c-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="82d0c-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="82d0c-124">Notes to callers</span></span>

<span data-ttu-id="82d0c-125">Puede usar **QueryPosition** para colocar un cuadro de desplazamiento en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="82d0c-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="82d0c-126">Por ejemplo, en una tabla que contiene 100 filas, si **QueryPosition** devuelve un valor de 75 en el parámetro _lpulNumerator_ , 100 en el parámetro _lpulDenominator_ y 75 en el parámetro _lpulRow_ , se puede colocar el cuadro de desplazamiento 3/4 de la forma a través de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="82d0c-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="82d0c-127">No confíe en el valor de _lpulDenominator_ es el número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d0c-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="82d0c-128">**QueryPosition** no siempre puede identificar la fila exacta que se coloca el cursor en.</span><span class="sxs-lookup"><span data-stu-id="82d0c-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="82d0c-129">Una llamada a **QueryPosition** podría implicar grandes cantidades de memoria, especialmente para grandes tablas ordenadas por categorías.</span><span class="sxs-lookup"><span data-stu-id="82d0c-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="82d0c-130">Si el parámetro _lpulRow_ se establece en 0xFFFFFFFF, demasiada memoria era necesaria para **QueryPosition** determinar la fila actual.</span><span class="sxs-lookup"><span data-stu-id="82d0c-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="82d0c-131">Llame al método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) para colocar la tabla a la fila identificada por los parámetros _lpulNumerator_ y _lpulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="82d0c-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="82d0c-132">Sin embargo, no siempre se puede esperar **SeekRowApprox** para establecer que la posición actual de la misma fila **que QueryPosition** tendría si memoria si no se hubiese un factor.</span><span class="sxs-lookup"><span data-stu-id="82d0c-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82d0c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="82d0c-133">See also</span></span>



[<span data-ttu-id="82d0c-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="82d0c-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="82d0c-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82d0c-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

