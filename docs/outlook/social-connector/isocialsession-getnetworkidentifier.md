---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtiene una cadena que representa un identificador de red social único para una conexión de red social específica.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285340"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="4fa93-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="4fa93-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="4fa93-104">Obtiene una cadena que representa un identificador de red social único para una conexión de red social específica.</span><span class="sxs-lookup"><span data-stu-id="4fa93-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="4fa93-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="4fa93-105">Parameters</span></span>

<span data-ttu-id="4fa93-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="4fa93-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="4fa93-107">contempla Una cadena que contiene un identificador de red social único.</span><span class="sxs-lookup"><span data-stu-id="4fa93-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fa93-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fa93-108">Remarks</span></span>

<span data-ttu-id="4fa93-109">Un identificador de red único es una cadena que identifica la red social del proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="4fa93-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="4fa93-110">Este método también puede devolver E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="4fa93-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fa93-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fa93-111">See also</span></span>

- [<span data-ttu-id="4fa93-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fa93-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

