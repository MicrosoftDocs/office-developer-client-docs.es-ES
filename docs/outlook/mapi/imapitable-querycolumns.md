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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817598"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="d22a9-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="d22a9-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="d22a9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d22a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d22a9-105">Devuelve una lista de columnas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="d22a9-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="d22a9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d22a9-106">Parameters</span></span>

 <span data-ttu-id="d22a9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d22a9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d22a9-108">[entrada] Máscara de bits de marcadores que indica qué columna establece que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="d22a9-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="d22a9-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d22a9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d22a9-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="d22a9-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="d22a9-111">La tabla debe devolver todas las columnas disponibles.</span><span class="sxs-lookup"><span data-stu-id="d22a9-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="d22a9-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d22a9-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d22a9-113">[out] Establece el puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad para la columna.</span><span class="sxs-lookup"><span data-stu-id="d22a9-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d22a9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d22a9-114">Return value</span></span>

<span data-ttu-id="d22a9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d22a9-115">S_OK</span></span> 
  
> <span data-ttu-id="d22a9-116">El conjunto de columnas se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d22a9-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="d22a9-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d22a9-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d22a9-118">Otra operación se establece en curso que impide que la columna de operación de recuperación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d22a9-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="d22a9-119">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="d22a9-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d22a9-120">Notas</span><span class="sxs-lookup"><span data-stu-id="d22a9-120">Remarks</span></span>

<span data-ttu-id="d22a9-121">El método **IMAPITable::QueryColumns** se puede llamar para recuperar:</span><span class="sxs-lookup"><span data-stu-id="d22a9-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="d22a9-122">La columna predeterminado establecido para una tabla.</span><span class="sxs-lookup"><span data-stu-id="d22a9-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="d22a9-123">La columna actual establecido para una tabla, según lo establecido por una llamada al método [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="d22a9-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="d22a9-124">La columna completa establecido para una tabla, las columnas que están disponibles, pero no necesariamente parte del conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="d22a9-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d22a9-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d22a9-125">Notes to callers</span></span>

<span data-ttu-id="d22a9-126">Si no se establece la marca TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** devuelve una tabla predeterminada o conjunto de columna actual, dependiendo de si la tabla se ha visto afectada por una llamada a **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="d22a9-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="d22a9-127">**SetColumns** cambia el orden y la selección de columnas en el conjunto de columnas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="d22a9-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="d22a9-128">Si se establece la marca TBL_ALL_COLUMNS, **QueryColumns** devuelve todas las columnas que son capaces de actuar en el conjunto de columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d22a9-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="d22a9-129">Libere la memoria para la matriz de etiqueta de propiedad que apunta el parámetro _lpPropTagArray_ mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d22a9-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d22a9-130">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d22a9-130">MFCMAPI reference</span></span>

<span data-ttu-id="d22a9-131">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d22a9-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d22a9-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d22a9-132">**File**</span></span>|<span data-ttu-id="d22a9-133">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="d22a9-133">**Function**</span></span>|<span data-ttu-id="d22a9-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d22a9-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d22a9-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d22a9-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d22a9-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="d22a9-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="d22a9-137">MFCMAPI usa el método **IMAPITable::QueryColumns** para recuperar la columna actual establecido para una tabla para que el usuario pueda modificarlo.</span><span class="sxs-lookup"><span data-stu-id="d22a9-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d22a9-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="d22a9-138">See also</span></span>



[<span data-ttu-id="d22a9-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d22a9-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="d22a9-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d22a9-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d22a9-141">Elemento SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d22a9-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d22a9-142">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d22a9-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d22a9-143">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d22a9-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

