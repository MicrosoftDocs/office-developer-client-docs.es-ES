---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410108"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="74923-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="74923-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="74923-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74923-105">Devuelve una lista de columnas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="74923-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="74923-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="74923-106">Parameters</span></span>

 <span data-ttu-id="74923-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74923-107">_ulFlags_</span></span>
  
> <span data-ttu-id="74923-108">[in] Máscara de bits de marcas que indica qué conjunto de columnas se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="74923-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="74923-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="74923-109">The following flag can be set:</span></span>
    
<span data-ttu-id="74923-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="74923-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="74923-111">La tabla debe devolver todas las columnas disponibles.</span><span class="sxs-lookup"><span data-stu-id="74923-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="74923-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="74923-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="74923-113">[salida] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad del conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="74923-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="74923-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74923-114">Return value</span></span>

<span data-ttu-id="74923-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="74923-115">S_OK</span></span> 
  
> <span data-ttu-id="74923-116">El conjunto de columnas se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="74923-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="74923-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="74923-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="74923-118">Hay otra operación en curso que impide que se inicie la operación de recuperación del conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="74923-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="74923-119">Debe permitirse completar la operación en curso o detenerse.</span><span class="sxs-lookup"><span data-stu-id="74923-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74923-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74923-120">Remarks</span></span>

<span data-ttu-id="74923-121">Se **puede llamar al método IMAPITable::QueryColumns** para recuperar:</span><span class="sxs-lookup"><span data-stu-id="74923-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="74923-122">Conjunto de columnas predeterminado para una tabla.</span><span class="sxs-lookup"><span data-stu-id="74923-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="74923-123">El conjunto de columnas actual de una tabla, tal como se establece mediante una llamada al método [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="74923-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="74923-124">Conjunto de columnas completo para una tabla, las columnas que están disponibles, pero no necesariamente parte del conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="74923-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="74923-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="74923-125">Notes to callers</span></span>

<span data-ttu-id="74923-126">Si no establece la marca TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** devuelve el conjunto de columnas predeterminado o actual de una tabla, en función de si la tabla se ha visto afectada por una llamada a **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="74923-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="74923-127">**SetColumns** cambia el orden y la selección de columnas en el conjunto de columnas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="74923-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="74923-128">Si establece la marca TBL_ALL_COLUMNS, **QueryColumns** devuelve todas las columnas que pueden estar en el conjunto de columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="74923-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="74923-129">Libera la memoria de la matriz de etiquetas de propiedad a la que apunta el parámetro _lpPropTagArray_ llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="74923-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="74923-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="74923-130">MFCMAPI reference</span></span>

<span data-ttu-id="74923-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="74923-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74923-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="74923-132">**File**</span></span>|<span data-ttu-id="74923-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="74923-133">**Function**</span></span>|<span data-ttu-id="74923-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="74923-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74923-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="74923-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="74923-136">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="74923-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="74923-137">MFCMAPI usa el **método IMAPITable::QueryColumns** para recuperar el conjunto de columnas actual de una tabla para que el usuario pueda editarlo.</span><span class="sxs-lookup"><span data-stu-id="74923-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74923-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="74923-138">See also</span></span>



[<span data-ttu-id="74923-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="74923-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="74923-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="74923-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="74923-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="74923-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="74923-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74923-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="74923-143">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="74923-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

