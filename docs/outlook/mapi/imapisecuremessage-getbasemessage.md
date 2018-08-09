---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817420"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="391da-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="391da-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="391da-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="391da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="391da-105">Recupera el subyacentes [IMessage: IMAPIProp](imessageimapiprop.md) esta [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) se encapsula.</span><span class="sxs-lookup"><span data-stu-id="391da-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="391da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="391da-106">Parameters</span></span>

 <span data-ttu-id="391da-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="391da-107">_ppmsg_</span></span>
  
> <span data-ttu-id="391da-108">[out] Un objeto de mensaje seguro.</span><span class="sxs-lookup"><span data-stu-id="391da-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="391da-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="391da-109">Return value</span></span>

<span data-ttu-id="391da-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="391da-110">S_OK</span></span>
  
> <span data-ttu-id="391da-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="391da-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="391da-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="391da-112">See also</span></span>



[<span data-ttu-id="391da-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="391da-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="391da-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="391da-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

