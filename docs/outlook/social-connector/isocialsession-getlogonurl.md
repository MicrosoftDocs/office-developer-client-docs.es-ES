---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtiene un valor de tipo string que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821113"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="54171-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="54171-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="54171-104">Obtiene un valor de tipo string que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.</span><span class="sxs-lookup"><span data-stu-id="54171-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="54171-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54171-105">Parameters</span></span>

<span data-ttu-id="54171-106">_url_</span><span class="sxs-lookup"><span data-stu-id="54171-106">_url_</span></span>
  
> <span data-ttu-id="54171-107">[out] Una cadena que contiene una dirección URL para el formulario usado en la autenticación web.</span><span class="sxs-lookup"><span data-stu-id="54171-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54171-108">Notas</span><span class="sxs-lookup"><span data-stu-id="54171-108">Remarks</span></span>

<span data-ttu-id="54171-109">Después de que el formulario se presenta al usuario, se llama al método de [ISocialSession::LogonWeb](isocialsession-logonweb.md) con una cadena vacía para el parámetro de _configuración_ .</span><span class="sxs-lookup"><span data-stu-id="54171-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54171-110">Ver también</span><span class="sxs-lookup"><span data-stu-id="54171-110">See also</span></span>

- [<span data-ttu-id="54171-111">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="54171-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

