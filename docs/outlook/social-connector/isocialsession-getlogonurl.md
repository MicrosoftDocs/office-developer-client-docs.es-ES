---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en el explorador al usuario durante la autenticación Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427916"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="63242-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="63242-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="63242-104">Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en el explorador al usuario durante la autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="63242-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="63242-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="63242-105">Parameters</span></span>

<span data-ttu-id="63242-106">_url_</span><span class="sxs-lookup"><span data-stu-id="63242-106">_url_</span></span>
  
> <span data-ttu-id="63242-107">contempla Una cadena que contiene una dirección URL para el formulario usado en la autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="63242-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63242-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63242-108">Remarks</span></span>

<span data-ttu-id="63242-109">Una vez que el formulario se presenta al usuario, se llama al método [ISocialSession:: LogonWeb](isocialsession-logonweb.md) con una cadena vacía para __ el parámetro connecten.</span><span class="sxs-lookup"><span data-stu-id="63242-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63242-110">Ver también</span><span class="sxs-lookup"><span data-stu-id="63242-110">See also</span></span>

- [<span data-ttu-id="63242-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63242-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

