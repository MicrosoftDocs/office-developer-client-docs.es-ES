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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351327"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="92d66-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="92d66-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="92d66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92d66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92d66-105">Indica el lugar al que pertenece un mensaje en un subproceso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="92d66-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92d66-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="92d66-106">Header file:</span></span>  <br/> |<span data-ttu-id="92d66-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="92d66-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="92d66-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="92d66-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92d66-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92d66-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92d66-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="92d66-110">Called by:</span></span>  <br/> |<span data-ttu-id="92d66-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="92d66-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="92d66-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="92d66-112">Parameters</span></span>

 <span data-ttu-id="92d66-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="92d66-113">_cbParent_</span></span>
  
> <span data-ttu-id="92d66-114">a Número de bytes en el índice de conversaciones primario.</span><span class="sxs-lookup"><span data-stu-id="92d66-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="92d66-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="92d66-115">_lpbParent_</span></span>
  
> <span data-ttu-id="92d66-116">a Puntero a los bytes del índice de conversaciones primario.</span><span class="sxs-lookup"><span data-stu-id="92d66-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="92d66-117">Puede ser NULL si _cbParent_ es cero.</span><span class="sxs-lookup"><span data-stu-id="92d66-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="92d66-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="92d66-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="92d66-119">contempla Puntero al número de bytes en el nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="92d66-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="92d66-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="92d66-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="92d66-121">contempla Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="92d66-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92d66-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92d66-122">Return value</span></span>

<span data-ttu-id="92d66-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="92d66-123">S_OK</span></span> 
  
> <span data-ttu-id="92d66-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="92d66-124">The call succeeded and has returned the expected value or values.</span></span>
    

