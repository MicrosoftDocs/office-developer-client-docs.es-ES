---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816879"
---
# <a name="freeprows"></a><span data-ttu-id="730a2-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="730a2-103">FreeProws</span></span>

  
  
<span data-ttu-id="730a2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="730a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="730a2-105">Destruye una estructura [SRowSet](srowset.md) y libera memoria asociada, incluida la memoria asignada para todas las matrices de miembros y estructuras.</span><span class="sxs-lookup"><span data-stu-id="730a2-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="730a2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="730a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="730a2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="730a2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="730a2-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="730a2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="730a2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="730a2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="730a2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="730a2-110">Called by:</span></span>  <br/> |<span data-ttu-id="730a2-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="730a2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="730a2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="730a2-112">Parameters</span></span>

 <span data-ttu-id="730a2-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="730a2-113">_prows_</span></span>
  
> <span data-ttu-id="730a2-114">[entrada] Puntero a la estructura **SRowSet** que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="730a2-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="730a2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="730a2-115">Return value</span></span>

<span data-ttu-id="730a2-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="730a2-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="730a2-117">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="730a2-117">Notes to callers</span></span>

<span data-ttu-id="730a2-118">Como parte de su implementación de **FreeProws**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura de **SRowSet** antes de liberar la estructura completa.</span><span class="sxs-lookup"><span data-stu-id="730a2-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="730a2-119">Por lo tanto, todas las entradas de esas deben haber seguido las reglas de asignación para la estructura de [SRowSet](srowset.md) , con un individuo [MAPIAllocateBuffer](mapiallocatebuffer.md) de llamada para cada matriz de miembros y estructura.</span><span class="sxs-lookup"><span data-stu-id="730a2-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="730a2-120">Para obtener más información sobre la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="730a2-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="730a2-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="730a2-121">MFCMAPI reference</span></span>

<span data-ttu-id="730a2-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="730a2-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="730a2-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="730a2-123">**File**</span></span>|<span data-ttu-id="730a2-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="730a2-124">**Function**</span></span>|<span data-ttu-id="730a2-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="730a2-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="730a2-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="730a2-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="730a2-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="730a2-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="730a2-128">MFCMAPI usa el método **FreeProws** para liberar una estructura SRowSet que contiene las filas de la tabla que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="730a2-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="730a2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="730a2-129">See also</span></span>



[<span data-ttu-id="730a2-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="730a2-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

