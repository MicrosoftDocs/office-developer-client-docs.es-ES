---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437731"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="fb2d2-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="fb2d2-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="fb2d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb2d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb2d2-105">Vuelve a crear un identificador de entrada a partir de su codificación ASCII.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb2d2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fb2d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb2d2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fb2d2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fb2d2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fb2d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fb2d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fb2d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fb2d2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fb2d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="fb2d2-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="fb2d2-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="fb2d2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb2d2-112">Parameters</span></span>

 <span data-ttu-id="fb2d2-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="fb2d2-113">_sz_</span></span>
  
> <span data-ttu-id="fb2d2-114">[entrada] Puntero a la cadena ASCII desde la que se va a crear un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="fb2d2-115">_indeste_</span><span class="sxs-lookup"><span data-stu-id="fb2d2-115">_pcb_</span></span>
  
> <span data-ttu-id="fb2d2-116">[salida] Puntero al tamaño, en bytes, del identificador de entrada al que apunta el _parámetro ppentry._</span><span class="sxs-lookup"><span data-stu-id="fb2d2-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="fb2d2-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="fb2d2-117">_ppentry_</span></span>
  
> <span data-ttu-id="fb2d2-118">[salida] Puntero a un puntero a la estructura [ENTRYID](entryid.md) devuelta que contiene el nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb2d2-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb2d2-119">Return value</span></span>

<span data-ttu-id="fb2d2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb2d2-120">S_OK</span></span>
  
> <span data-ttu-id="fb2d2-121">La recreación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-121">The recreation was successful.</span></span>
    
<span data-ttu-id="fb2d2-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fb2d2-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="fb2d2-123">El identificador de entrada no era válido.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb2d2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb2d2-124">Remarks</span></span>

<span data-ttu-id="fb2d2-125">Las **funciones HrEntryIDFromSz** y [HrSzFromEntryID](hrszfromentryid.md) proporcionan conversión entre la cadena y los formatos binarios de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb2d2-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fb2d2-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="fb2d2-126">Notes to callers</span></span>

<span data-ttu-id="fb2d2-127">La **función HrEntryIDFromSz** asigna memoria para la cadena ASCII mediante la [función MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="fb2d2-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

