---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411557"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="75d1c-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="75d1c-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="75d1c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75d1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75d1c-105">Codifica un identificador de entrada en una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="75d1c-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75d1c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="75d1c-106">Header file:</span></span>  <br/> |<span data-ttu-id="75d1c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="75d1c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="75d1c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="75d1c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="75d1c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="75d1c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="75d1c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="75d1c-110">Called by:</span></span>  <br/> |<span data-ttu-id="75d1c-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="75d1c-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="75d1c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="75d1c-112">Parameters</span></span>

 <span data-ttu-id="75d1c-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="75d1c-113">_cb_</span></span>
  
> <span data-ttu-id="75d1c-114">[in] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro pentry._</span><span class="sxs-lookup"><span data-stu-id="75d1c-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="75d1c-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="75d1c-115">_pentry_</span></span>
  
> <span data-ttu-id="75d1c-116">[in] Puntero a una [estructura ENTRYID](entryid.md) que contiene el identificador de entrada que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="75d1c-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="75d1c-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="75d1c-117">_psz_</span></span>
  
> <span data-ttu-id="75d1c-118">[salida] Puntero a la cadena ASCII devuelta.</span><span class="sxs-lookup"><span data-stu-id="75d1c-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75d1c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75d1c-119">Return value</span></span>

<span data-ttu-id="75d1c-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75d1c-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75d1c-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75d1c-121">Remarks</span></span>

<span data-ttu-id="75d1c-122">Las [funciones HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre la cadena y los formatos binarios de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="75d1c-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="75d1c-123">Con MAPI, debe usar estructuras con datos binarios.</span><span class="sxs-lookup"><span data-stu-id="75d1c-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="75d1c-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="75d1c-124">Notes to callers</span></span>

<span data-ttu-id="75d1c-125">La **función HrSzFromEntryID** asigna memoria a la cadena ASCII mediante la [función MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="75d1c-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

