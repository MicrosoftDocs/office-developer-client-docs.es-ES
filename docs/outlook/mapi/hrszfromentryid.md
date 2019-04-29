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
# <a name="hrszfromentryid"></a><span data-ttu-id="a4bdd-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="a4bdd-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="a4bdd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4bdd-105">Codifica un identificador de entrada en una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4bdd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a4bdd-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4bdd-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a4bdd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a4bdd-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a4bdd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4bdd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4bdd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4bdd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a4bdd-110">Called by:</span></span>  <br/> |<span data-ttu-id="a4bdd-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="a4bdd-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="a4bdd-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a4bdd-112">Parameters</span></span>

 <span data-ttu-id="a4bdd-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="a4bdd-113">_cb_</span></span>
  
> <span data-ttu-id="a4bdd-114">a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _pentry_ .</span><span class="sxs-lookup"><span data-stu-id="a4bdd-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="a4bdd-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="a4bdd-115">_pentry_</span></span>
  
> <span data-ttu-id="a4bdd-116">a Puntero a una estructura [EntryID](entryid.md) que contiene el identificador de entrada que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="a4bdd-117">_PSZ_</span><span class="sxs-lookup"><span data-stu-id="a4bdd-117">_psz_</span></span>
  
> <span data-ttu-id="a4bdd-118">contempla Puntero a la cadena ASCII devuelta.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4bdd-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4bdd-119">Return value</span></span>

<span data-ttu-id="a4bdd-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4bdd-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4bdd-121">Remarks</span></span>

<span data-ttu-id="a4bdd-122">Las funciones [HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre los formatos binarios y de cadena de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="a4bdd-123">Con MAPI, debe usar estructuras con datos binarios.</span><span class="sxs-lookup"><span data-stu-id="a4bdd-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4bdd-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a4bdd-124">Notes to callers</span></span>

<span data-ttu-id="a4bdd-125">La función **HrSzFromEntryID** asigna memoria para la cadena ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a4bdd-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

