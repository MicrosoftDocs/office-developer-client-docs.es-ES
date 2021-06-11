---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426922"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="e960a-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="e960a-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="e960a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e960a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e960a-105">Registra un cliente para recibir devoluciones de llamada en un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e960a-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="e960a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e960a-106">Parameters</span></span>

 <span data-ttu-id="e960a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e960a-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="e960a-108">[in] Marcas que modifican el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="e960a-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="e960a-109">Solo se admite MAPIOFFLINE_ADVISE_DEFAULT valor.</span><span class="sxs-lookup"><span data-stu-id="e960a-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="e960a-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="e960a-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="e960a-111">[in] Información sobre el tipo de devolución de llamada, cuándo recibir una devolución de llamada, una interfaz de devolución de llamada para el autor de la llamada y otros detalles.</span><span class="sxs-lookup"><span data-stu-id="e960a-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="e960a-112">También contiene un token de cliente que Outlook para enviar devoluciones de llamada de notificación posteriores al autor de la llamada del cliente.</span><span class="sxs-lookup"><span data-stu-id="e960a-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="e960a-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="e960a-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="e960a-114">[salida] Un token de aviso devuelto al autor de la llamada del cliente para cancelar posteriormente la devolución de llamada del objeto.</span><span class="sxs-lookup"><span data-stu-id="e960a-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e960a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e960a-115">Return value</span></span>

<span data-ttu-id="e960a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e960a-116">S_OK</span></span>
  
> <span data-ttu-id="e960a-117">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e960a-117">The call was successful.</span></span>
    
<span data-ttu-id="e960a-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e960a-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="e960a-119">Se ha especificado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e960a-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="e960a-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="e960a-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="e960a-121">La interfaz de devolución de llamada especificada en  *pAdviseInfo*  no es válida.</span><span class="sxs-lookup"><span data-stu-id="e960a-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e960a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e960a-122">Remarks</span></span>

<span data-ttu-id="e960a-123">Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="e960a-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="e960a-124">El cliente puede comprobar los tipos de devoluciones de llamada compatibles con el objeto mediante **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="e960a-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="e960a-125">El cliente puede determinar el tipo y otros detalles sobre la devolución de llamada que desea y, a continuación, llamar a **IMAPIOfflineMgr::Advise** para registrarse para recibir dichas devoluciones de llamada sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="e960a-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e960a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e960a-126">See also</span></span>



[<span data-ttu-id="e960a-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="e960a-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="e960a-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e960a-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="e960a-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e960a-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e960a-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="e960a-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

