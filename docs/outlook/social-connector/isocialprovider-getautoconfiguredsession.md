---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Obtiene una interfaz ISocialSession configurada automáticamente.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417444"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="892b6-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="892b6-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="892b6-104">Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="892b6-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="892b6-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="892b6-105">Parameters</span></span>

<span data-ttu-id="892b6-106">_session_</span><span class="sxs-lookup"><span data-stu-id="892b6-106">_session_</span></span>
  
> <span data-ttu-id="892b6-107">[salida] Una interfaz **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="892b6-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="892b6-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="892b6-108">Remarks</span></span>

<span data-ttu-id="892b6-109">La interfaz **ISocialSession** devuelta se registra automáticamente en la red, basándose en un método específico para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="892b6-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="892b6-110">El proveedor debe devolver el error OSC_E_NOT_IMPLEMENTED si la red social no admite la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="892b6-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="892b6-111">Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="892b6-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="892b6-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="892b6-112">See also</span></span>

- [<span data-ttu-id="892b6-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="892b6-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

