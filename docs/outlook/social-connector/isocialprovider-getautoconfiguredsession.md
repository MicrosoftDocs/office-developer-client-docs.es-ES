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
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821128"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="fa6d5-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="fa6d5-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="fa6d5-104">Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d5-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="fa6d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa6d5-105">Parameters</span></span>

<span data-ttu-id="fa6d5-106">_sesión_</span><span class="sxs-lookup"><span data-stu-id="fa6d5-106">_session_</span></span>
  
> <span data-ttu-id="fa6d5-107">[out] Una interfaz **ISocialSession** .</span><span class="sxs-lookup"><span data-stu-id="fa6d5-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa6d5-108">Notas</span><span class="sxs-lookup"><span data-stu-id="fa6d5-108">Remarks</span></span>

<span data-ttu-id="fa6d5-109">La interfaz devuelta de **ISocialSession** se registra automáticamente a la red, en función de un método que es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fa6d5-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="fa6d5-110">El proveedor debe devolver el error OSC_E_NOT_IMPLEMENTED si la red social no admite la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="fa6d5-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="fa6d5-111">Para obtener información acerca de los códigos de error, vea [Códigos de Error de Outlook Social Connector proveedor](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d5-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa6d5-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa6d5-112">See also</span></span>

- [<span data-ttu-id="fa6d5-113">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa6d5-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

