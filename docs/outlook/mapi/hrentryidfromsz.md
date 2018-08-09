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
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817051"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="e31bc-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="e31bc-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="e31bc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e31bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e31bc-105">Vuelve a crear un identificador de entrada de su codificación de ASCII.</span><span class="sxs-lookup"><span data-stu-id="e31bc-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e31bc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e31bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="e31bc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e31bc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e31bc-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e31bc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e31bc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e31bc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e31bc-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e31bc-110">Called by:</span></span>  <br/> |<span data-ttu-id="e31bc-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="e31bc-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="e31bc-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e31bc-112">Parameters</span></span>

 <span data-ttu-id="e31bc-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="e31bc-113">_sz_</span></span>
  
> <span data-ttu-id="e31bc-114">[entrada] Puntero a la cadena de ASCII desde el que se va a crear un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e31bc-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="e31bc-115">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="e31bc-115">_pcb_</span></span>
  
> <span data-ttu-id="e31bc-116">[out] Puntero al tamaño, en bytes, del identificador de entrada indicada por el parámetro _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="e31bc-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="e31bc-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="e31bc-117">_ppentry_</span></span>
  
> <span data-ttu-id="e31bc-118">[out] Puntero a un puntero a la estructura [ENTRYID](entryid.md) devuelto que contiene el nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e31bc-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e31bc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e31bc-119">Return value</span></span>

<span data-ttu-id="e31bc-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e31bc-120">S_OK</span></span>
  
> <span data-ttu-id="e31bc-121">La recreación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="e31bc-121">The recreation was successful.</span></span>
    
<span data-ttu-id="e31bc-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e31bc-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="e31bc-123">El identificador de entrada no es válido.</span><span class="sxs-lookup"><span data-stu-id="e31bc-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e31bc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e31bc-124">Remarks</span></span>

<span data-ttu-id="e31bc-125">Las funciones **HrEntryIDFromSz** y [HrSzFromEntryID](hrszfromentryid.md) proporcionan conversión entre la cadena y formatos binarios de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="e31bc-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e31bc-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e31bc-126">Notes to callers</span></span>

<span data-ttu-id="e31bc-127">La función **HrEntryIDFromSz** asigna memoria de la cadena de ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e31bc-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

