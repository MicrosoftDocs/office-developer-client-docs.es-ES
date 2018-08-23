---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594155"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="2fe56-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="2fe56-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="2fe56-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fe56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fe56-105">Indica que en un subproceso del mensaje de un mensaje pertenece.</span><span class="sxs-lookup"><span data-stu-id="2fe56-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fe56-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2fe56-106">Header file:</span></span>  <br/> |<span data-ttu-id="2fe56-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2fe56-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2fe56-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="2fe56-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2fe56-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe56-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2fe56-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2fe56-110">Called by:</span></span>  <br/> |<span data-ttu-id="2fe56-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2fe56-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="2fe56-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fe56-112">Parameters</span></span>

 <span data-ttu-id="2fe56-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="2fe56-113">_cbParent_</span></span>
  
> <span data-ttu-id="2fe56-114">[entrada] Recuento de bytes en el índice de conversación primario.</span><span class="sxs-lookup"><span data-stu-id="2fe56-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="2fe56-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="2fe56-115">_lpbParent_</span></span>
  
> <span data-ttu-id="2fe56-116">[entrada] Puntero a bytes en el índice de conversación primario.</span><span class="sxs-lookup"><span data-stu-id="2fe56-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="2fe56-117">Esto puede ser NULL si _cbParent_ es cero.</span><span class="sxs-lookup"><span data-stu-id="2fe56-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="2fe56-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="2fe56-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="2fe56-119">[out] Puntero para el número de bytes en el nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="2fe56-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="2fe56-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="2fe56-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="2fe56-121">[out] Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="2fe56-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2fe56-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fe56-122">Return value</span></span>

<span data-ttu-id="2fe56-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fe56-123">S_OK</span></span> 
  
> <span data-ttu-id="2fe56-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="2fe56-124">The call succeeded and has returned the expected value or values.</span></span>
    

