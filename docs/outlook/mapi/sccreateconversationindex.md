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
# <a name="sccreateconversationindex"></a><span data-ttu-id="ddca7-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="ddca7-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="ddca7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddca7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddca7-105">Indica a dónde pertenece un mensaje en un subproceso de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddca7-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddca7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ddca7-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddca7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ddca7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ddca7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ddca7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddca7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ddca7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ddca7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ddca7-110">Called by:</span></span>  <br/> |<span data-ttu-id="ddca7-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ddca7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="ddca7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddca7-112">Parameters</span></span>

 <span data-ttu-id="ddca7-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="ddca7-113">_cbParent_</span></span>
  
> <span data-ttu-id="ddca7-114">[entrada] Número de bytes en el índice de conversación principal.</span><span class="sxs-lookup"><span data-stu-id="ddca7-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="ddca7-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="ddca7-115">_lpbParent_</span></span>
  
> <span data-ttu-id="ddca7-116">[entrada] Puntero a bytes en el índice de conversación principal.</span><span class="sxs-lookup"><span data-stu-id="ddca7-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="ddca7-117">Puede ser NULL si  _cbParent_ es cero.</span><span class="sxs-lookup"><span data-stu-id="ddca7-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="ddca7-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="ddca7-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="ddca7-119">[salida] Puntero al recuento de bytes en el nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="ddca7-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="ddca7-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="ddca7-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="ddca7-121">[salida] Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.</span><span class="sxs-lookup"><span data-stu-id="ddca7-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ddca7-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddca7-122">Return value</span></span>

<span data-ttu-id="ddca7-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddca7-123">S_OK</span></span> 
  
> <span data-ttu-id="ddca7-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ddca7-124">The call succeeded and has returned the expected value or values.</span></span>
    

