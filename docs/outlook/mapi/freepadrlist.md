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
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576550"
---
# <a name="freepadrlist"></a><span data-ttu-id="b25a7-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="b25a7-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="b25a7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b25a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b25a7-105">Destruye una estructura de [ADRLIST](adrlist.md) y libera memoria asociada, incluida la memoria asignada para todas las matrices de miembros y estructuras.</span><span class="sxs-lookup"><span data-stu-id="b25a7-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b25a7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b25a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b25a7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b25a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b25a7-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b25a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b25a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b25a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b25a7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b25a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="b25a7-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b25a7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="b25a7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b25a7-112">Parameters</span></span>

 <span data-ttu-id="b25a7-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="b25a7-113">_padrlist_</span></span>
  
> <span data-ttu-id="b25a7-114">[entrada] Puntero a la estructura **ADRLIST** que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="b25a7-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b25a7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b25a7-115">Return value</span></span>

<span data-ttu-id="b25a7-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b25a7-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b25a7-117">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b25a7-117">Notes to callers</span></span>

<span data-ttu-id="b25a7-118">Como parte de su implementación de **FreePadrlist**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura **ADRLIST** antes de liberar la estructura completa.</span><span class="sxs-lookup"><span data-stu-id="b25a7-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="b25a7-119">Por lo tanto, deben haber seguido las reglas de asignación para la estructura [ADRLIST](adrlist.md) a todas las entradas de este tipo, con un individuo [MAPIAllocateBuffer](mapiallocatebuffer.md) de llamada para cada matriz de miembros y estructura.</span><span class="sxs-lookup"><span data-stu-id="b25a7-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="b25a7-120">Para obtener más información sobre la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b25a7-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b25a7-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b25a7-121">MFCMAPI reference</span></span>

<span data-ttu-id="b25a7-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b25a7-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b25a7-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b25a7-123">**File**</span></span>|<span data-ttu-id="b25a7-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="b25a7-124">**Function**</span></span>|<span data-ttu-id="b25a7-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b25a7-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b25a7-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b25a7-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b25a7-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="b25a7-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="b25a7-128">MFCMAPI usa el método **FreePadrlist** para liberar una estructura de ADRLIST que se creó para agregar una dirección de uso único a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b25a7-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b25a7-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b25a7-129">See also</span></span>



[<span data-ttu-id="b25a7-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b25a7-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

