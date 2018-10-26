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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579525"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="5ae1e-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5ae1e-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="5ae1e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ae1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ae1e-105">Cancela devoluciones de llamada para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="5ae1e-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5ae1e-106">Parameters</span></span>

 <span data-ttu-id="5ae1e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ae1e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5ae1e-108">[entrada] Marcas para cancelar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="5ae1e-109">Se admite el valor MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="5ae1e-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="5ae1e-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="5ae1e-111">[entrada] Símbolo (token) advise que identifica el registro de devolución de llamada que debe cancelarse.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ae1e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ae1e-112">Return value</span></span>

<span data-ttu-id="5ae1e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ae1e-113">S_OK</span></span>
  
> <span data-ttu-id="5ae1e-114">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-114">The call was successful.</span></span> <span data-ttu-id="5ae1e-115">Esta llamada debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ae1e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ae1e-116">Remarks</span></span>

<span data-ttu-id="5ae1e-117">Quita el registro de la devolución de llamada que se ha asociado con *ulAdviseToken* devuelto desde una llamada anterior a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="5ae1e-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="5ae1e-118">Hace que el objeto **IMAPIOfflineMgr** liberar su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado con *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="5ae1e-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ae1e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae1e-119">See also</span></span>



[<span data-ttu-id="5ae1e-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="5ae1e-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="5ae1e-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5ae1e-121">MAPI Constants</span></span>](mapi-constants.md)

