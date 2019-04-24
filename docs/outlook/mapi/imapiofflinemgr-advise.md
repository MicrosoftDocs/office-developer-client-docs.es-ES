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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321430"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="a9fe2-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="a9fe2-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="a9fe2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9fe2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9fe2-105">Registra un cliente para recibir las devoluciones de llamada en un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="a9fe2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a9fe2-106">Parameters</span></span>

 <span data-ttu-id="a9fe2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9fe2-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="a9fe2-108">a Marcas que modifican el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="a9fe2-109">Solo se admite el valor MAPIOFFLINE_ADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="a9fe2-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="a9fe2-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="a9fe2-111">a Información sobre el tipo de devolución de llamada, Cuándo recibir una devolución de llamada, una interfaz de devolución de llamada para la persona que llama y otros detalles.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="a9fe2-112">También contiene un token de cliente que Outlook usa para enviar devoluciones de llamada de notificación posteriores al llamador del cliente.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="a9fe2-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="a9fe2-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="a9fe2-114">contempla Un token de aviso devuelto al llamador del cliente para cancelar posteriormente la devolución de llamada para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9fe2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9fe2-115">Return value</span></span>

<span data-ttu-id="a9fe2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9fe2-116">S_OK</span></span>
  
> <span data-ttu-id="a9fe2-117">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-117">The call was successful.</span></span>
    
<span data-ttu-id="a9fe2-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a9fe2-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="a9fe2-119">Se ha especificado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="a9fe2-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="a9fe2-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="a9fe2-121">La interfaz de devolución de llamada especificada en *pAdviseInfo* no es válida.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a9fe2-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9fe2-122">Remarks</span></span>

<span data-ttu-id="a9fe2-123">Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="a9fe2-124">El cliente puede comprobar los tipos de devoluciones de llamada admitidas por el objeto mediante **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="a9fe2-125">El cliente puede determinar el tipo y otros detalles sobre la devolución de llamada que desea y, a continuación, llamar a **IMAPIOfflineMgr:: Advise** para registrarse para recibir las devoluciones de llamada sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9fe2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9fe2-126">See also</span></span>



[<span data-ttu-id="a9fe2-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="a9fe2-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="a9fe2-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a9fe2-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="a9fe2-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a9fe2-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a9fe2-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="a9fe2-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

