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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820585"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="98307-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="98307-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="98307-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98307-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98307-105">Indica que en un subproceso del mensaje de un mensaje pertenece.</span><span class="sxs-lookup"><span data-stu-id="98307-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98307-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="98307-106">Header file:</span></span>  <br/> |<span data-ttu-id="98307-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="98307-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98307-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="98307-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98307-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98307-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98307-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="98307-110">Called by:</span></span>  <br/> |<span data-ttu-id="98307-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="98307-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="98307-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98307-112">Parameters</span></span>

 <span data-ttu-id="98307-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="98307-113">_cbParent_</span></span>
  
> <span data-ttu-id="98307-114">[entrada] Recuento de bytes en el índice de conversación primario.</span><span class="sxs-lookup"><span data-stu-id="98307-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="98307-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="98307-115">_lpbParent_</span></span>
  
> <span data-ttu-id="98307-116">[entrada] Puntero a bytes en el índice de conversación primario.</span><span class="sxs-lookup"><span data-stu-id="98307-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="98307-117">Esto puede ser NULL si _cbParent_ es cero.</span><span class="sxs-lookup"><span data-stu-id="98307-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="98307-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="98307-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="98307-119">[out] Puntero para el número de bytes en el nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="98307-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="98307-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="98307-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="98307-121">[out] Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="98307-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98307-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98307-122">Return value</span></span>

<span data-ttu-id="98307-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="98307-123">S_OK</span></span> 
  
> <span data-ttu-id="98307-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="98307-124">The call succeeded and has returned the expected value or values.</span></span>
    

