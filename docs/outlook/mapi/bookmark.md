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
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816660"
---
# <a name="bookmark"></a><span data-ttu-id="07681-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="07681-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="07681-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07681-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07681-105">Define los datos de marcadores de recordar una posición en una tabla.</span><span class="sxs-lookup"><span data-stu-id="07681-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07681-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="07681-106">Header file:</span></span>  <br/> |<span data-ttu-id="07681-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07681-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="07681-108">Métodos relacionados:</span><span class="sxs-lookup"><span data-stu-id="07681-108">Related methods:</span></span>  <br/> |<span data-ttu-id="07681-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="07681-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="07681-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07681-110">Remarks</span></span>

<span data-ttu-id="07681-111">MAPI define tres marcadores, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="07681-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="07681-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="07681-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="07681-113">Recuerda la posición inicial de la tabla.</span><span class="sxs-lookup"><span data-stu-id="07681-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="07681-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="07681-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="07681-115">Recuerda la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="07681-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="07681-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="07681-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="07681-117">Recuerda la posición final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="07681-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="07681-118">Los clientes pueden crear otros marcadores para recordar otras posiciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="07681-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="07681-119">Marcadores son válidos sólo cuando la tabla está abierta.</span><span class="sxs-lookup"><span data-stu-id="07681-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="07681-120">Los clientes deben liberar todos los marcadores que se hayan creado antes de cerrar la tabla asociada.</span><span class="sxs-lookup"><span data-stu-id="07681-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07681-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="07681-121">See also</span></span>



[<span data-ttu-id="07681-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="07681-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="07681-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="07681-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="07681-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="07681-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="07681-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="07681-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="07681-126">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="07681-126">MAPI Data Types</span></span>](mapi-data-types.md)

