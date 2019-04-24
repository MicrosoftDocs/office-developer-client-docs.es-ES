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
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322396"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="ac7fc-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="ac7fc-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="ac7fc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac7fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac7fc-105">Recupera el [IMessage: IMAPIProp](imessageimapiprop.md) subyacente que este [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) está encapsulando.</span><span class="sxs-lookup"><span data-stu-id="ac7fc-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="ac7fc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac7fc-106">Parameters</span></span>

 <span data-ttu-id="ac7fc-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="ac7fc-107">_ppmsg_</span></span>
  
> <span data-ttu-id="ac7fc-108">contempla Un objeto de mensaje seguro.</span><span class="sxs-lookup"><span data-stu-id="ac7fc-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac7fc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac7fc-109">Return value</span></span>

<span data-ttu-id="ac7fc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac7fc-110">S_OK</span></span>
  
> <span data-ttu-id="ac7fc-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ac7fc-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac7fc-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac7fc-112">See also</span></span>



[<span data-ttu-id="ac7fc-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac7fc-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="ac7fc-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac7fc-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

