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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415659"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="fc4ab-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="fc4ab-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="fc4ab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc4ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc4ab-105">Indica el lugar al que pertenece un mensaje en un subproceso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc4ab-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc4ab-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="fc4ab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fc4ab-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc4ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc4ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc4ab-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc4ab-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="fc4ab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="fc4ab-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fc4ab-112">Parameters</span></span>

 <span data-ttu-id="fc4ab-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="fc4ab-113">_cbParent_</span></span>
  
> <span data-ttu-id="fc4ab-114">a Número de bytes en el índice de conversaciones primario.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="fc4ab-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="fc4ab-115">_lpbParent_</span></span>
  
> <span data-ttu-id="fc4ab-116">a Puntero a los bytes del índice de conversaciones primario.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="fc4ab-117">Puede ser NULL si _cbParent_ es cero.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="fc4ab-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="fc4ab-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="fc4ab-119">contempla Puntero al número de bytes en el nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="fc4ab-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="fc4ab-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="fc4ab-121">contempla Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc4ab-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc4ab-122">Return value</span></span>

<span data-ttu-id="fc4ab-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc4ab-123">S_OK</span></span> 
  
> <span data-ttu-id="fc4ab-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-124">The call succeeded and has returned the expected value or values.</span></span>
    

