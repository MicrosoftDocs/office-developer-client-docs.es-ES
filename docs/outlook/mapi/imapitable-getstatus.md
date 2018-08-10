---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817603"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="225c3-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="225c3-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="225c3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="225c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="225c3-105">Devuelve el estado y el tipo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="225c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="225c3-106">Parameters</span></span>

 <span data-ttu-id="225c3-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="225c3-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="225c3-108">[out] Puntero a un valor que indica el estado de la tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="225c3-109">Puede devolver uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="225c3-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="225c3-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="225c3-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="225c3-111">No hay ninguna operación está en curso.</span><span class="sxs-lookup"><span data-stu-id="225c3-111">No operations are in progress.</span></span>
    
<span data-ttu-id="225c3-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="225c3-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="225c3-113">El contenido de la tabla expectantly ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="225c3-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="225c3-114">No se devuelve este valor de estado para que los cambios que resultan de las operaciones de ordenación o restricción.</span><span class="sxs-lookup"><span data-stu-id="225c3-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="225c3-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="225c3-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="225c3-116">Se ha producido un error durante una operación [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="225c3-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="225c3-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="225c3-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="225c3-118">Una operación **IMAPITable:: Restrict** está en curso.</span><span class="sxs-lookup"><span data-stu-id="225c3-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="225c3-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="225c3-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="225c3-120">Se ha producido un error durante una operación de [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="225c3-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="225c3-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="225c3-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="225c3-122">Una operación **IMAPITable::SetColumns** está en curso.</span><span class="sxs-lookup"><span data-stu-id="225c3-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="225c3-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="225c3-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="225c3-124">Se ha producido un error durante una operación de [SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="225c3-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="225c3-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="225c3-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="225c3-126">Una operación de **SortTable** está en curso.</span><span class="sxs-lookup"><span data-stu-id="225c3-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="225c3-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="225c3-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="225c3-128">[out] Puntero a un valor que indica el tipo de tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="225c3-129">Puede devolver uno de los siguientes tipos de tres tabla:</span><span class="sxs-lookup"><span data-stu-id="225c3-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="225c3-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="225c3-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="225c3-131">Contenido de la tabla es dinámico; pueden cambiar las filas y los valores de columna como los cambios de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="225c3-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="225c3-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="225c3-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="225c3-133">Se corrigen las filas dentro de la tabla, pero los valores de las columnas dentro de estas filas son dinámicos y pueden cambiar como los cambios de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="225c3-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="225c3-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="225c3-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="225c3-135">En la tabla es estática, y su contenido no cambian cuando cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="225c3-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="225c3-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="225c3-136">Return value</span></span>

<span data-ttu-id="225c3-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="225c3-137">S_OK</span></span> 
  
> <span data-ttu-id="225c3-138">Estado de la tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="225c3-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="225c3-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="225c3-139">Remarks</span></span>

<span data-ttu-id="225c3-140">El método **IMAPTable::GetStatus** recupera información sobre el tipo y el estado actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="225c3-141">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="225c3-141">Notes to callers</span></span>

<span data-ttu-id="225c3-142">Puede usar **GetStatus** junto con los otros tres métodos de **IMAPITable** para supervisar el estado de las operaciones y determinar el efecto en la tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="225c3-143">Llamada **GetStatus** después de realizar una de las llamadas de **IMAPITable** siguientes:</span><span class="sxs-lookup"><span data-stu-id="225c3-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="225c3-144">[IMAPITable:: Restrict](imapitable-restrict.md) para establecer una restricción.</span><span class="sxs-lookup"><span data-stu-id="225c3-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="225c3-145">[SortTable](imapitable-sorttable.md) para establecer un criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="225c3-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="225c3-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir un conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="225c3-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="225c3-147">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="225c3-147">MFCMAPI reference</span></span>

<span data-ttu-id="225c3-148">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="225c3-149">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="225c3-149">**File**</span></span>|<span data-ttu-id="225c3-150">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="225c3-150">**Function**</span></span>|<span data-ttu-id="225c3-151">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="225c3-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="225c3-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="225c3-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="225c3-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="225c3-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="225c3-154">MFCMAPI usa el método **IMAPITable::GetStatus** para informar del estado de una tabla.</span><span class="sxs-lookup"><span data-stu-id="225c3-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="225c3-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="225c3-155">See also</span></span>



[<span data-ttu-id="225c3-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="225c3-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="225c3-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="225c3-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="225c3-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="225c3-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="225c3-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="225c3-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="225c3-160">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="225c3-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
