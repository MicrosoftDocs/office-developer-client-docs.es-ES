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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285381"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="c931d-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="c931d-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="c931d-104">Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en el explorador al usuario durante la autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="c931d-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="c931d-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="c931d-105">Parameters</span></span>

<span data-ttu-id="c931d-106">_url_</span><span class="sxs-lookup"><span data-stu-id="c931d-106">_url_</span></span>
  
> <span data-ttu-id="c931d-107">contempla Una cadena que contiene una dirección URL para el formulario usado en la autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="c931d-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c931d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c931d-108">Remarks</span></span>

<span data-ttu-id="c931d-109">Una vez que el formulario se presenta al usuario, se llama al método [ISocialSession:: LogonWeb](isocialsession-logonweb.md) con una cadena vacía para __ el parámetro connecten.</span><span class="sxs-lookup"><span data-stu-id="c931d-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c931d-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="c931d-110">See also</span></span>

- [<span data-ttu-id="c931d-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c931d-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

