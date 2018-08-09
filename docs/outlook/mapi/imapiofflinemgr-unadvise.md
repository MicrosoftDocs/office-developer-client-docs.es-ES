---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817385"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="f381b-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f381b-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="f381b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f381b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f381b-105">Cancela devoluciones de llamada para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f381b-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="f381b-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f381b-106">Parameters</span></span>

 <span data-ttu-id="f381b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f381b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f381b-108">[entrada] Marcas para cancelar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f381b-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="f381b-109">Se admite el valor MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="f381b-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="f381b-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="f381b-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="f381b-111">[entrada] Símbolo (token) advise que identifica el registro de devolución de llamada que debe cancelarse.</span><span class="sxs-lookup"><span data-stu-id="f381b-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f381b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f381b-112">Return value</span></span>

<span data-ttu-id="f381b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f381b-113">S_OK</span></span>
  
> <span data-ttu-id="f381b-114">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="f381b-114">The call was successful.</span></span> <span data-ttu-id="f381b-115">Esta llamada debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="f381b-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f381b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f381b-116">Remarks</span></span>

<span data-ttu-id="f381b-117">Quita el registro de la devolución de llamada que se ha asociado con *ulAdviseToken* devuelto desde una llamada anterior a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="f381b-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="f381b-118">Hace que el objeto **IMAPIOfflineMgr** liberar su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado con *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="f381b-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f381b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f381b-119">See also</span></span>



[<span data-ttu-id="f381b-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="f381b-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="f381b-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f381b-121">MAPI Constants</span></span>](mapi-constants.md)

