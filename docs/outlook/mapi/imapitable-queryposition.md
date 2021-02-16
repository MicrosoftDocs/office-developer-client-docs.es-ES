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
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415666"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="0f003-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="0f003-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="0f003-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f003-105">Recupera la posición de fila de tabla actual del cursor, basándose en un valor fraccionrio.</span><span class="sxs-lookup"><span data-stu-id="0f003-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="0f003-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f003-106">Parameters</span></span>

 <span data-ttu-id="0f003-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="0f003-107">_lpulRow_</span></span>
  
> <span data-ttu-id="0f003-108">[salida] Puntero al número de la fila actual.</span><span class="sxs-lookup"><span data-stu-id="0f003-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="0f003-109">El número de fila es de base cero; la primera fila de la tabla es cero.</span><span class="sxs-lookup"><span data-stu-id="0f003-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="0f003-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="0f003-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="0f003-111">[salida] Puntero al numerador de la fracción que identifica la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0f003-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="0f003-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="0f003-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="0f003-113">[salida] Puntero al denominador de la fracción que identifica la posición de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0f003-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="0f003-114">El  _parámetro lpulDenominator_ no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="0f003-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0f003-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f003-115">Return value</span></span>

<span data-ttu-id="0f003-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f003-116">S_OK</span></span> 
  
> <span data-ttu-id="0f003-117">El método devuelve valores válidos  _en lpulRow_,  _lpulNumerator_ y  _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="0f003-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f003-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f003-118">Remarks</span></span>

<span data-ttu-id="0f003-119">El **método IMAPITable::QueryPosition** determina la posición de fila actual y devuelve el número de la fila actual y un valor fraccionario que indica su posición relativa al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0f003-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="0f003-120">MAPI define la fila actual como la siguiente fila que se leerá.</span><span class="sxs-lookup"><span data-stu-id="0f003-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0f003-121">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="0f003-121">Notes to implementers</span></span>

<span data-ttu-id="0f003-122">No es necesario devolver el número exacto de filas de la tabla para el parámetro  _lpulDenominator;_ puede ser una aproximación.</span><span class="sxs-lookup"><span data-stu-id="0f003-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="0f003-123">Si no puede determinar la fila actual, devuelva un valor de 0xFFFFFFFF  _en lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="0f003-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f003-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0f003-124">Notes to callers</span></span>

<span data-ttu-id="0f003-125">Puede usar **QueryPosition para** colocar un cuadro de desplazamiento en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0f003-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="0f003-126">Por ejemplo, en una tabla que contiene 100 filas, si **QueryPosition** devuelve un valor de 75 en el parámetro  _lpulNumerator,_ 100 en el parámetro  _lpulDenominator_ y 75 en el parámetro  _lpulRow,_ puede colocar el cuadro de desplazamiento 3/4 del camino a través de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0f003-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="0f003-127">No confíe en que el valor de  _lpulDenominator_ sea el número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0f003-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="0f003-128">**QueryPosition** no siempre puede identificar la fila exacta en la que está situado el cursor.</span><span class="sxs-lookup"><span data-stu-id="0f003-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="0f003-129">Una llamada a **QueryPosition puede** implicar grandes cantidades de memoria, especialmente para tablas categorizadas grandes.</span><span class="sxs-lookup"><span data-stu-id="0f003-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="0f003-130">Si el  _parámetro lpulRow_ se establece en 0xFFFFFFFF, se requiere demasiada memoria para **que QueryPosition** determine la fila actual.</span><span class="sxs-lookup"><span data-stu-id="0f003-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="0f003-131">Llame al [método IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) para colocar la tabla en la fila identificada por los parámetros _lpulNumerator_ e _lpulDenominator._</span><span class="sxs-lookup"><span data-stu-id="0f003-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="0f003-132">Sin embargo, no siempre **esperes que SeekRowApprox** establezca como la posición actual la misma fila **que QueryPosition** tendría si la memoria no hubiera sido un factor.</span><span class="sxs-lookup"><span data-stu-id="0f003-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f003-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0f003-133">See also</span></span>



[<span data-ttu-id="0f003-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="0f003-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="0f003-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f003-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

