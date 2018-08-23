---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594484"
---
# <a name="bookmark"></a><span data-ttu-id="94286-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="94286-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="94286-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94286-105">Define los datos de marcadores de recordar una posición en una tabla.</span><span class="sxs-lookup"><span data-stu-id="94286-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94286-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="94286-106">Header file:</span></span>  <br/> |<span data-ttu-id="94286-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94286-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="94286-108">Métodos relacionados:</span><span class="sxs-lookup"><span data-stu-id="94286-108">Related methods:</span></span>  <br/> |<span data-ttu-id="94286-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="94286-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="94286-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94286-110">Remarks</span></span>

<span data-ttu-id="94286-111">MAPI define tres marcadores, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="94286-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="94286-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="94286-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="94286-113">Recuerda la posición inicial de la tabla.</span><span class="sxs-lookup"><span data-stu-id="94286-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="94286-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="94286-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="94286-115">Recuerda la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="94286-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="94286-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="94286-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="94286-117">Recuerda la posición final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="94286-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="94286-118">Los clientes pueden crear otros marcadores para recordar otras posiciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="94286-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="94286-119">Marcadores son válidos sólo cuando la tabla está abierta.</span><span class="sxs-lookup"><span data-stu-id="94286-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="94286-120">Los clientes deben liberar todos los marcadores que se hayan creado antes de cerrar la tabla asociada.</span><span class="sxs-lookup"><span data-stu-id="94286-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94286-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="94286-121">See also</span></span>



[<span data-ttu-id="94286-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="94286-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="94286-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="94286-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="94286-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="94286-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="94286-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="94286-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="94286-126">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="94286-126">MAPI Data Types</span></span>](mapi-data-types.md)

