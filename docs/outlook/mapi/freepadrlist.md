---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408645"
---
# <a name="freepadrlist"></a><span data-ttu-id="d8ab6-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="d8ab6-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="d8ab6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8ab6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8ab6-105">Destruye una estructura [ADRLIST](adrlist.md) y libera la memoria asociada, incluida la memoria asignada para todas las matrices y estructuras de miembros.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8ab6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8ab6-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8ab6-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d8ab6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d8ab6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d8ab6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8ab6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8ab6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8ab6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d8ab6-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8ab6-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d8ab6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="d8ab6-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8ab6-112">Parameters</span></span>

 <span data-ttu-id="d8ab6-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="d8ab6-113">_padrlist_</span></span>
  
> <span data-ttu-id="d8ab6-114">a Puntero a la estructura **ADRLIST** que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8ab6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8ab6-115">Return value</span></span>

<span data-ttu-id="d8ab6-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d8ab6-117">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d8ab6-117">Notes to callers</span></span>

<span data-ttu-id="d8ab6-118">Como parte de su implementación de **FreePadrlist**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura **ADRLIST** antes de liberar la estructura completa.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="d8ab6-119">Por lo tanto, todas estas entradas deben haber seguido las reglas de asignación para la estructura [ADRLIST](adrlist.md) , usando una llamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz y estructura de miembros.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="d8ab6-120">Para obtener más información acerca de la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d8ab6-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d8ab6-121">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d8ab6-121">MFCMAPI reference</span></span>

<span data-ttu-id="d8ab6-122">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d8ab6-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d8ab6-123">**File**</span></span>|<span data-ttu-id="d8ab6-124">**Función**</span><span class="sxs-lookup"><span data-stu-id="d8ab6-124">**Function**</span></span>|<span data-ttu-id="d8ab6-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d8ab6-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8ab6-126">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="d8ab6-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d8ab6-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="d8ab6-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="d8ab6-128">MFCMAPI usa el método **FreePadrlist** para liberar una estructura ADRLIST que se ha creado para agregar una dirección de un solo uso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d8ab6-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8ab6-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8ab6-129">See also</span></span>



[<span data-ttu-id="d8ab6-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d8ab6-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

