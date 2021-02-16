---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408827"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="3ac66-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="3ac66-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="3ac66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ac66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ac66-105">Crea un marcador en la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3ac66-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="3ac66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ac66-106">Parameters</span></span>

 <span data-ttu-id="3ac66-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="3ac66-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="3ac66-108">[salida] Puntero al valor de marcador de 32 bits devuelto.</span><span class="sxs-lookup"><span data-stu-id="3ac66-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="3ac66-109">Este marcador se puede pasar más adelante en una llamada al método [IMAPITable::SeekRow.](imapitable-seekrow.md)</span><span class="sxs-lookup"><span data-stu-id="3ac66-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ac66-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac66-110">Return value</span></span>

<span data-ttu-id="3ac66-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ac66-111">S_OK</span></span> 
  
> <span data-ttu-id="3ac66-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3ac66-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3ac66-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="3ac66-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="3ac66-114">No se pudo completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3ac66-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ac66-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ac66-115">Remarks</span></span>

<span data-ttu-id="3ac66-116">El **método IMAPITable::CreateBookmark** marca una posición de tabla mediante la creación de un valor denominado marcador.</span><span class="sxs-lookup"><span data-stu-id="3ac66-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="3ac66-117">Se puede usar un marcador para volver a la posición identificada por el marcador.</span><span class="sxs-lookup"><span data-stu-id="3ac66-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="3ac66-118">La posición de marcador está asociada con el objeto en esa fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3ac66-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="3ac66-119">Los marcadores no se admiten en las tablas de datos adjuntos y las implementaciones de tablas de datos adjuntos de **CreateBookmark** devuelven MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="3ac66-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ac66-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="3ac66-120">Notes to implementers</span></span>

<span data-ttu-id="3ac66-121">Debido al gasto de memoria de mantener las posiciones del cursor con marcadores, limite el número de marcadores que puede crear.</span><span class="sxs-lookup"><span data-stu-id="3ac66-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="3ac66-122">Cuando llegue a ese número, devuelva MAPI_E_UNABLE_TO_COMPLETE de todas las llamadas subsiguientes a **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="3ac66-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="3ac66-123">A veces, un marcador apunta a una fila que ya no está en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="3ac66-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="3ac66-124">Si el autor de la llamada usa un marcador de este tipo, mueva el cursor a la siguiente fila visible y deténlo allí.</span><span class="sxs-lookup"><span data-stu-id="3ac66-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="3ac66-125">Cuando el autor de la llamada intenta usar un marcador que apunta a una fila no invisible porque se ha contraído, MAPI_W_POSITION_CHANGED después de mover el marcador.</span><span class="sxs-lookup"><span data-stu-id="3ac66-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="3ac66-126">Puede cambiar la posición del marcador a la siguiente fila visible en este momento o cuando se produzca la con contraer en el método **SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="3ac66-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="3ac66-127">Si mueve el marcador en el momento en que se contrae la fila, debe conservar un poco en el marcador que indica exactamente cuándo se movió el marcador: desde su último uso o si nunca se ha usado desde su creación.</span><span class="sxs-lookup"><span data-stu-id="3ac66-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ac66-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3ac66-128">Notes to callers</span></span>

 <span data-ttu-id="3ac66-129">**CreateBookmark** asigna memoria para el marcador que crea.</span><span class="sxs-lookup"><span data-stu-id="3ac66-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="3ac66-130">Libere los recursos del marcador llamando al [método IMAPITable::FreeBookmark.](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="3ac66-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ac66-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3ac66-131">See also</span></span>



[<span data-ttu-id="3ac66-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="3ac66-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="3ac66-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="3ac66-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="3ac66-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ac66-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

