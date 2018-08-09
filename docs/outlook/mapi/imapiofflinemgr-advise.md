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
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817379"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="4b97d-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="4b97d-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="4b97d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b97d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b97d-105">Registra un cliente para recibir las devoluciones de llamada en un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4b97d-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="4b97d-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4b97d-106">Parameters</span></span>

 <span data-ttu-id="4b97d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b97d-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="4b97d-108">[entrada] Marcas que modifican el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="4b97d-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="4b97d-109">Se admite el valor MAPIOFFLINE_ADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="4b97d-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="4b97d-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="4b97d-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="4b97d-111">[entrada] Información sobre el tipo de devolución de llamada, cuándo se debe recibir una devolución de llamada, una interfaz de devolución de llamada para el autor de la llamada y otros detalles.</span><span class="sxs-lookup"><span data-stu-id="4b97d-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="4b97d-112">También contiene un símbolo (token) de cliente que utiliza Outlook en el envío de las devoluciones de llamada de la notificación posterior al autor de llamada de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b97d-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="4b97d-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="4b97d-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="4b97d-114">[out] Un token de advise devuelve al autor de la llamada de cliente para cancelar la devolución de llamada para el objeto posteriormente.</span><span class="sxs-lookup"><span data-stu-id="4b97d-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b97d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b97d-115">Return value</span></span>

<span data-ttu-id="4b97d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b97d-116">S_OK</span></span>
  
> <span data-ttu-id="4b97d-117">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="4b97d-117">The call was successful.</span></span>
    
<span data-ttu-id="4b97d-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4b97d-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="4b97d-119">Se ha especificado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="4b97d-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="4b97d-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="4b97d-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="4b97d-121">La interfaz de devolución de llamada especificada en *pAdviseInfo* no es válida.</span><span class="sxs-lookup"><span data-stu-id="4b97d-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4b97d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b97d-122">Remarks</span></span>

<span data-ttu-id="4b97d-123">Al abrir un objeto sin conexión con **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="4b97d-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="4b97d-124">El cliente puede comprobar para los tipos de devoluciones de llamada admitidos por el objeto utilizando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b97d-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="4b97d-125">El cliente puede determinar el tipo y otros detalles acerca de la devolución de llamada que desea y, a continuación, llame a **IMAPIOfflineMgr::Advise** para registrarse y para recibir esas devoluciones de llamada sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="4b97d-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b97d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b97d-126">See also</span></span>



[<span data-ttu-id="4b97d-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="4b97d-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="4b97d-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4b97d-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="4b97d-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4b97d-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4b97d-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="4b97d-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

