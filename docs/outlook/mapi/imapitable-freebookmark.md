---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409457"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="35aff-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="35aff-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="35aff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35aff-105">Libera la memoria asociada a un marcador.</span><span class="sxs-lookup"><span data-stu-id="35aff-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="35aff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35aff-106">Parameters</span></span>

 <span data-ttu-id="35aff-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="35aff-107">_bkPosition_</span></span>
  
> <span data-ttu-id="35aff-108">[entrada] Marcador que se va a liberar, creado llamando al [método IMAPITable::CreateBookmark.](imapitable-createbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="35aff-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35aff-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35aff-109">Return value</span></span>

<span data-ttu-id="35aff-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="35aff-110">S_OK</span></span> 
  
> <span data-ttu-id="35aff-111">El marcador se ha libre correctamente.</span><span class="sxs-lookup"><span data-stu-id="35aff-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="35aff-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="35aff-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="35aff-113">El marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="35aff-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35aff-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35aff-114">Remarks</span></span>

<span data-ttu-id="35aff-115">El **método IMAPITable::FreeBookmark** libera un marcador que ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="35aff-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="35aff-116">El marcador ya no es válido después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="35aff-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="35aff-117">Cada vez que se libera una tabla de la memoria, también se liberan todos los marcadores asociados.</span><span class="sxs-lookup"><span data-stu-id="35aff-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="35aff-118">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="35aff-118">Notes to implementers</span></span>

<span data-ttu-id="35aff-119">Si el autor de la llamada pasa uno de los tres marcadores predefinidos en el parámetro  _bkPosition,_ ignore la solicitud y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="35aff-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35aff-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="35aff-120">See also</span></span>



[<span data-ttu-id="35aff-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="35aff-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="35aff-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35aff-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

