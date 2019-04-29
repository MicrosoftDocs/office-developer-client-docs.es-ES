---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413048"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="2021b-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="2021b-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="2021b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2021b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2021b-105">Mueve el cursor a una posición específica de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="2021b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2021b-106">Parameters</span></span>

 <span data-ttu-id="2021b-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="2021b-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="2021b-108">a Marcador que identifica la posición inicial de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2021b-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="2021b-109">Un marcador se puede crear con el método [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="2021b-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="2021b-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="2021b-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="2021b-111">Inicia la operación de búsqueda desde el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="2021b-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="2021b-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="2021b-113">Inicia la operación de búsqueda desde la fila de la tabla donde se encuentra el cursor.</span><span class="sxs-lookup"><span data-stu-id="2021b-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="2021b-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="2021b-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="2021b-115">Inicia la operación de búsqueda a partir del final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="2021b-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="2021b-116">_lRowCount_</span></span>
  
> <span data-ttu-id="2021b-117">a Recuento con signo del número de filas que se va a mover, a partir del marcador identificado por el parámetro _bkOrigin_ .</span><span class="sxs-lookup"><span data-stu-id="2021b-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="2021b-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="2021b-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="2021b-119">contempla Si _lRowCount_ es un puntero válido en la entrada, _lplRowsSought_ apunta al número de filas que se procesaron en la operación de búsqueda, cuyo signo indica la dirección de la búsqueda, hacia delante o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="2021b-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="2021b-120">Si _lRowCount_ es negativo, _lplRowsSought_ es negativo.</span><span class="sxs-lookup"><span data-stu-id="2021b-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2021b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2021b-121">Return value</span></span>

<span data-ttu-id="2021b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="2021b-122">S_OK</span></span> 
  
> <span data-ttu-id="2021b-123">La operación de búsqueda se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2021b-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="2021b-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="2021b-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="2021b-125">Hay otra operación en curso que evita que la operación de búsqueda de filas se inicie.</span><span class="sxs-lookup"><span data-stu-id="2021b-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="2021b-126">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="2021b-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="2021b-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="2021b-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="2021b-128">El marcador especificado en el parámetro _bkOrigin_ no es válido porque se quitó o porque está más allá de la última fila solicitada.</span><span class="sxs-lookup"><span data-stu-id="2021b-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="2021b-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="2021b-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="2021b-130">La llamada se realizó correctamente, pero el marcador especificado en el parámetro _bkOrigin_ ya no se establece en la misma fila que tenía cuando se usó por última vez.</span><span class="sxs-lookup"><span data-stu-id="2021b-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="2021b-131">Si no se ha utilizado el marcador, deja de estar en la misma posición que cuando se creó.</span><span class="sxs-lookup"><span data-stu-id="2021b-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="2021b-132">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="2021b-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2021b-133">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="2021b-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2021b-134">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2021b-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2021b-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2021b-135">Remarks</span></span>

<span data-ttu-id="2021b-136">El método **IMAPITable:: SeekRow** establece una nueva posición de BOOKMARK_CURRENT para el cursor.</span><span class="sxs-lookup"><span data-stu-id="2021b-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="2021b-137">El parámetro _lRowCount_ indica el número de filas que se mueve el cursor, así como la dirección del movimiento.</span><span class="sxs-lookup"><span data-stu-id="2021b-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="2021b-138">Si la posición resultante está más allá de la última fila de la tabla, el cursor se coloca detrás de la última fila.</span><span class="sxs-lookup"><span data-stu-id="2021b-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="2021b-139">Si la posición resultante se encuentra antes de la primera fila de la tabla, el cursor se coloca al principio de la primera fila.</span><span class="sxs-lookup"><span data-stu-id="2021b-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2021b-140">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2021b-140">Notes to implementers</span></span>

<span data-ttu-id="2021b-141">Si la fila a la que apunta _bkOrigin_ ya no existe en la tabla y no puede establecer una nueva posición para el marcador, devuelva MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="2021b-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="2021b-142">Si la fila a la que apunta _bkOrigin_ ya no existe y puede establecer una nueva posición para el marcador, devuelva MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="2021b-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="2021b-143">Todavía se puede usar un marcador que apunte a una fila contraída de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="2021b-144">Si el autor de la llamada intenta mover el cursor a dicho marcador, mueva el cursor a la siguiente fila visible y devuelva MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="2021b-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="2021b-145">Puede mover los marcadores de los puestos contraídos fuera de la vista, ya sea en el momento de su uso o en el momento en que se contrae la fila.</span><span class="sxs-lookup"><span data-stu-id="2021b-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="2021b-146">Si un marcador se mueve en el momento en que se contrae la fila, mantenga un bit en el marcador que indique si el marcador se ha movido desde el último uso o, si nunca se ha usado, desde su creación.</span><span class="sxs-lookup"><span data-stu-id="2021b-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2021b-147">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2021b-147">Notes to callers</span></span>

<span data-ttu-id="2021b-148">Para indicar un movimiento hacia atrás para **SeekRow**, pase un valor negativo en _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="2021b-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="2021b-149">Para buscar el principio de la tabla, pase cero en _lRowCount_ y el valor BOOKMARK_BEGINNING en _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="2021b-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="2021b-150">Si hay muchas filas en la tabla, la operación **SeekRow** puede ser lenta.</span><span class="sxs-lookup"><span data-stu-id="2021b-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="2021b-151">El rendimiento también puede verse afectado si requiere que se devuelva un recuento de filas en el contenido del parámetro _lplRowsSought_ .</span><span class="sxs-lookup"><span data-stu-id="2021b-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="2021b-152">**SeekRow** devuelve el número de filas en las que se busca, positivo o negativo, en la variable a la que apunta _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="2021b-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="2021b-153">En operaciones ordinarias, debe devolver el mismo valor para _lplRowsSought_ como se pasó para _lRowCount_, a menos que la búsqueda haya alcanzado el principio o el final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="2021b-154">No establezca _lRowCount_ en un número mayor que 50.</span><span class="sxs-lookup"><span data-stu-id="2021b-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="2021b-155">Para buscar un número mayor de filas, use el método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) .</span><span class="sxs-lookup"><span data-stu-id="2021b-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2021b-156">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2021b-156">MFCMAPI reference</span></span>

<span data-ttu-id="2021b-157">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2021b-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2021b-158">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2021b-158">**File**</span></span>|<span data-ttu-id="2021b-159">**Función**</span><span class="sxs-lookup"><span data-stu-id="2021b-159">**Function**</span></span>|<span data-ttu-id="2021b-160">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2021b-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2021b-161">MAPIProcessor. cpp</span><span class="sxs-lookup"><span data-stu-id="2021b-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="2021b-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="2021b-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="2021b-163">MFCMAPI usa el método **IMAPITable:: SeekRow** para localizar el principio de la tabla antes de procesarla.</span><span class="sxs-lookup"><span data-stu-id="2021b-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2021b-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="2021b-164">See also</span></span>



[<span data-ttu-id="2021b-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="2021b-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="2021b-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="2021b-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="2021b-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2021b-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="2021b-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="2021b-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="2021b-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2021b-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="2021b-170">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2021b-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

