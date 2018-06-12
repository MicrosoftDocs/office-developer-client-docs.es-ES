---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtiene una cadena que representa un identificador único de redes sociales para una conexión de red social determinado.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821240"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="c5cd0-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="c5cd0-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="c5cd0-104">Obtiene una cadena que representa un identificador único de redes sociales para una conexión de red social determinado.</span><span class="sxs-lookup"><span data-stu-id="c5cd0-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="c5cd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5cd0-105">Parameters</span></span>

<span data-ttu-id="c5cd0-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="c5cd0-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="c5cd0-107">[out] Una cadena que contiene un identificador único de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="c5cd0-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5cd0-108">Notas</span><span class="sxs-lookup"><span data-stu-id="c5cd0-108">Remarks</span></span>

<span data-ttu-id="c5cd0-109">Un identificador único de red es una cadena que identifica la red social del proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c5cd0-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="c5cd0-110">Este método también puede devolver E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c5cd0-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5cd0-111">Ver también</span><span class="sxs-lookup"><span data-stu-id="c5cd0-111">See also</span></span>

- [<span data-ttu-id="c5cd0-112">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5cd0-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

