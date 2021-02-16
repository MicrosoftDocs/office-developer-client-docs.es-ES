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
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413860"
---
# <a name="flatentrylist"></a><span data-ttu-id="d613e-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="d613e-103">FLATENTRYLIST</span></span>

<span data-ttu-id="d613e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d613e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d613e-105">Contiene una matriz de [estructuras FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="d613e-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d613e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d613e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d613e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d613e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d613e-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="d613e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="d613e-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="d613e-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="d613e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d613e-110">Members</span></span>

<span data-ttu-id="d613e-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="d613e-111">**cEntries**</span></span>
  
> <span data-ttu-id="d613e-112">Número de **estructuras FLATENTRY** en la matriz descrita por el **miembro abEntries.**</span><span class="sxs-lookup"><span data-stu-id="d613e-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="d613e-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="d613e-113">**cbEntries**</span></span>
  
> <span data-ttu-id="d613e-114">Número de bytes de la matriz descrita por **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="d613e-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="d613e-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="d613e-115">**abEntries**</span></span>
  
> <span data-ttu-id="d613e-116">Matriz de bytes que contiene una o más **estructuras FLATENTRY,** organizadas de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="d613e-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d613e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d613e-117">Remarks</span></span>

<span data-ttu-id="d613e-118">En la **matriz abEntries,** cada **estructura FLATENTRY** se alinea en un límite alineado de forma natural.</span><span class="sxs-lookup"><span data-stu-id="d613e-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="d613e-119">Se incluyen bytes adicionales como relleno para garantizar la alineación natural entre cualquiera de las dos **estructuras FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="d613e-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="d613e-120">La primera **estructura FLATENTRY** de la matriz siempre se alinea correctamente porque el desplazamiento del miembro **abEntries** es 8.</span><span class="sxs-lookup"><span data-stu-id="d613e-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="d613e-121">Para calcular el desplazamiento de la siguiente estructura, use el tamaño de la primera entrada redondeada al múltiplo siguiente de 4.</span><span class="sxs-lookup"><span data-stu-id="d613e-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="d613e-122">Utilice la [macro CbFLATENTRY](cbflatentry.md) para calcular el tamaño de una **estructura FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="d613e-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="d613e-123">Por ejemplo, la segunda estructura **FLATENTRY** comienza con un desplazamiento que consiste en el desplazamiento de la primera entrada más la longitud de la primera entrada redondeada a los cuatro bytes siguientes.</span><span class="sxs-lookup"><span data-stu-id="d613e-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="d613e-124">La longitud de la primera entrada es la longitud de su **miembro cb** más la longitud de su **miembro abEntry.**</span><span class="sxs-lookup"><span data-stu-id="d613e-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="d613e-125">En el ejemplo de código siguiente se indica cómo calcular los desplazamientos en una **estructura FLATENTRYLIST.**</span><span class="sxs-lookup"><span data-stu-id="d613e-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="d613e-126">Supongamos que  _lpFlatEntry_ es un puntero a la primera estructura de la lista.</span><span class="sxs-lookup"><span data-stu-id="d613e-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="d613e-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d613e-127">See also</span></span>

- [<span data-ttu-id="d613e-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="d613e-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="d613e-129">Propiedad canónica PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="d613e-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="d613e-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d613e-130">MAPI Structures</span></span>](mapi-structures.md)

