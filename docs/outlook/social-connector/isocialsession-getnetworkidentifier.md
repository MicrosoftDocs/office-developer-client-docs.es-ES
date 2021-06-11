---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtiene una cadena que representa un identificador de red social único para una conexión de red social determinada.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433279"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="5a176-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="5a176-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="5a176-104">Obtiene una cadena que representa un identificador de red social único para una conexión de red social determinada.</span><span class="sxs-lookup"><span data-stu-id="5a176-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="5a176-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a176-105">Parameters</span></span>

<span data-ttu-id="5a176-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="5a176-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="5a176-107">[salida] Cadena que contiene un identificador de red social único.</span><span class="sxs-lookup"><span data-stu-id="5a176-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a176-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a176-108">Remarks</span></span>

<span data-ttu-id="5a176-109">Un identificador de red único es una cadena que identifica la red social del Outlook social connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="5a176-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="5a176-110">Este método también puede devolver E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5a176-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a176-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a176-111">See also</span></span>

- [<span data-ttu-id="5a176-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a176-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

