---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816825"
---
# <a name="flatentrylist"></a><span data-ttu-id="9e7fd-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="9e7fd-103">FLATENTRYLIST</span></span>

<span data-ttu-id="9e7fd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e7fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e7fd-105">Contiene una matriz de estructuras [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e7fd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9e7fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e7fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e7fd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9e7fd-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="9e7fd-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9e7fd-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="9e7fd-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="9e7fd-110">Members</span><span class="sxs-lookup"><span data-stu-id="9e7fd-110">Members</span></span>

<span data-ttu-id="9e7fd-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="9e7fd-111">**cEntries**</span></span>
  
> <span data-ttu-id="9e7fd-112">Recuento de las estructuras **FLATENTRY** en la matriz descritos por el miembro **abEntries** .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="9e7fd-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="9e7fd-113">**cbEntries**</span></span>
  
> <span data-ttu-id="9e7fd-114">Número de bytes de la matriz descritos por **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="9e7fd-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="9e7fd-115">**abEntries**</span></span>
  
> <span data-ttu-id="9e7fd-116">Matriz de bytes que contiene una o más estructuras **FLATENTRY** , organizado de un extremo a extremo.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e7fd-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e7fd-117">Remarks</span></span>

<span data-ttu-id="9e7fd-118">En la matriz **abEntries** , cada estructura **FLATENTRY** se alinea en un límite alineado con naturalidad.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="9e7fd-119">Bytes adicionales se incluyen como relleno para realizar la alineación natural seguro entre los dos estructuras **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="9e7fd-120">La primera estructura **FLATENTRY** en la matriz siempre se alinea correctamente debido a que el desplazamiento del miembro **abEntries** es 8.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="9e7fd-121">Para calcular el desplazamiento de la estructura siguiente, utilice el tamaño de la primera entrada que se redondea hacia arriba hasta el próximo múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="9e7fd-122">Utilice la macro [CbFLATENTRY](cbflatentry.md) para calcular el tamaño de una estructura **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="9e7fd-123">Por ejemplo, la segunda estructura **FLATENTRY** se inicia en una posición de desplazamiento que consta del desplazamiento de la primera entrada y la longitud de la primera entrada redondeada a los siguientes cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="9e7fd-124">La longitud de la primera entrada es la longitud de su miembro **cb** más la longitud de su miembro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="9e7fd-125">El ejemplo de código siguiente indica cómo calcular los desplazamientos en una estructura **FLATENTRYLIST** .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="9e7fd-126">Se supone que _lpFlatEntry_ es un puntero a la primera estructura de la lista.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="9e7fd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e7fd-127">See also</span></span>

- [<span data-ttu-id="9e7fd-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="9e7fd-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="9e7fd-129">Propiedad canónica PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="9e7fd-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="9e7fd-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9e7fd-130">MAPI Structures</span></span>](mapi-structures.md)

