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
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817592"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="6e0f1-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="6e0f1-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="6e0f1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e0f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e0f1-105">Libera la memoria asociada con un marcador.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="6e0f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e0f1-106">Parameters</span></span>

 <span data-ttu-id="6e0f1-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="6e0f1-107">_bkPosition_</span></span>
  
> <span data-ttu-id="6e0f1-108">[entrada] El marcador que se va a liberar, creado al llamar al método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0f1-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6e0f1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e0f1-109">Return value</span></span>

<span data-ttu-id="6e0f1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e0f1-110">S_OK</span></span> 
  
> <span data-ttu-id="6e0f1-111">El marcador correctamente se libera.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="6e0f1-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="6e0f1-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="6e0f1-113">El marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e0f1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e0f1-114">Remarks</span></span>

<span data-ttu-id="6e0f1-115">El método **IMAPITable::FreeBookmark** libera un marcador que ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="6e0f1-116">El marcador ya no es válido después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="6e0f1-117">Siempre que se publique una tabla de la memoria, todos sus marcadores asociados también se liberan.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6e0f1-118">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="6e0f1-118">Notes to implementers</span></span>

<span data-ttu-id="6e0f1-119">Si el autor de la llamada pasa a uno de los tres marcadores predefinidos en el parámetro _bkPosition_ , omitir la solicitud y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="6e0f1-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e0f1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e0f1-120">See also</span></span>



[<span data-ttu-id="6e0f1-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="6e0f1-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="6e0f1-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e0f1-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

