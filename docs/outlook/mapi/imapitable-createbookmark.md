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
ms.openlocfilehash: 5e9135a52c15c18b70116aaf52e1ee63af413673
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563852"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="bf8e4-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="bf8e4-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="bf8e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf8e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf8e4-105">Crea un marcador en la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="bf8e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf8e4-106">Parameters</span></span>

 <span data-ttu-id="bf8e4-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="bf8e4-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="bf8e4-108">[out] Puntero al valor devuelto de 32 bits de marcador.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="bf8e4-109">Más adelante se puede pasar este marcador en una llamada al método [IMAPITable::SeekRow](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bf8e4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf8e4-110">Return value</span></span>

<span data-ttu-id="bf8e4-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf8e4-111">S_OK</span></span> 
  
> <span data-ttu-id="bf8e4-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bf8e4-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="bf8e4-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="bf8e4-114">No se pudo completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf8e4-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf8e4-115">Remarks</span></span>

<span data-ttu-id="bf8e4-116">El método **IMAPITable::CreateBookmark** marca una posición de tabla mediante la creación de un valor de un marcador.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="bf8e4-117">Un marcador se puede utilizar para volver a la posición identificada por el marcador.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="bf8e4-118">El marcador de posición está asociada con el objeto en esa fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="bf8e4-119">En las tablas de datos adjuntos no se admiten los marcadores y las implementaciones de la tabla de datos adjuntos de **CreateBookmark** devuelven MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bf8e4-120">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="bf8e4-120">Notes to implementers</span></span>

<span data-ttu-id="bf8e4-121">Debido a los gastos de memoria del mantenimiento de las posiciones de cursor con marcadores, limitar el número de marcadores que se pueden crear.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="bf8e4-122">Cuando llegue a ese número, devolver MAPI_E_UNABLE_TO_COMPLETE de todas las llamadas subsiguientes a **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="bf8e4-123">En ocasiones, un marcador apunta a una fila que ya no está en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="bf8e4-124">Si un autor de la llamada usa como un marcador, mueva el cursor a la siguiente fila visible y detenga no existe.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="bf8e4-125">Cuando el autor de la llamada intenta utilizar un marcador que señala a una fila no visible debido a que se ha contraído, devolver MAPI_W_POSITION_CHANGED después de mover el marcador.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="bf8e4-126">Puede cambiar la posición del marcador en la siguiente fila visible en este momento, o cuando la contracción se produce en el método **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="bf8e4-127">Si mueve el marcador en el momento de la fila está contraída, debe conservar un poco en el marcador que indica exactamente cuándo se ha movido el marcador: debido a que su última utilizar o si nunca se ha usado desde su creación.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bf8e4-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bf8e4-128">Notes to callers</span></span>

 <span data-ttu-id="bf8e4-129">**CreateBookmark** asigna memoria para el marcador que se creen.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="bf8e4-130">Liberar los recursos para el marcador llamando al método [IMAPITable::FreeBookmark](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf8e4-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bf8e4-131">See also</span></span>



[<span data-ttu-id="bf8e4-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="bf8e4-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="bf8e4-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="bf8e4-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="bf8e4-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf8e4-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

