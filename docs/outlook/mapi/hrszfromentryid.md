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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817068"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="25cff-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="25cff-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="25cff-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25cff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25cff-105">Codifica un identificador de entrada en una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="25cff-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25cff-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="25cff-106">Header file:</span></span>  <br/> |<span data-ttu-id="25cff-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="25cff-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="25cff-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="25cff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="25cff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="25cff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="25cff-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="25cff-110">Called by:</span></span>  <br/> |<span data-ttu-id="25cff-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="25cff-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="25cff-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25cff-112">Parameters</span></span>

 <span data-ttu-id="25cff-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="25cff-113">_cb_</span></span>
  
> <span data-ttu-id="25cff-114">[entrada] Tamaño, en bytes, del identificador de entrada que señala el parámetro _pentry_ .</span><span class="sxs-lookup"><span data-stu-id="25cff-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="25cff-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="25cff-115">_pentry_</span></span>
  
> <span data-ttu-id="25cff-116">[entrada] Puntero a una estructura [ENTRYID](entryid.md) que contiene el identificador de entrada que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="25cff-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="25cff-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="25cff-117">_psz_</span></span>
  
> <span data-ttu-id="25cff-118">[out] Puntero a la cadena devuelta de ASCII.</span><span class="sxs-lookup"><span data-stu-id="25cff-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25cff-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25cff-119">Return value</span></span>

<span data-ttu-id="25cff-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25cff-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25cff-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25cff-121">Remarks</span></span>

<span data-ttu-id="25cff-122">Las funciones [HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre la cadena y formatos binarios de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="25cff-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="25cff-123">Con MAPI, debe usar las estructuras de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="25cff-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="25cff-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="25cff-124">Notes to callers</span></span>

<span data-ttu-id="25cff-125">La función **HrSzFromEntryID** asigna memoria de la cadena de ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="25cff-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

