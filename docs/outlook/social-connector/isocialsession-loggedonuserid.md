---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: Devuelve un valor de tipo string que representa el identificador de usuario de red social del usuario que ha iniciado sesión actualmente.
ms.openlocfilehash: dcc81d7acf8a839e7fe3249cc0eb06f96c113b56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821119"
---
# <a name="isocialsessionloggedonuserid"></a><span data-ttu-id="60763-103">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="60763-103">ISocialSession::LoggedOnUserID</span></span>

<span data-ttu-id="60763-104">Devuelve un valor de tipo string que representa el identificador de usuario de red social del usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="60763-104">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span> 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="60763-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="60763-105">Property value</span></span>

<span data-ttu-id="60763-106">Una cadena que contiene el identificador de usuario de red social del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="60763-106">A string that contains the social network user ID of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60763-107">Ver también</span><span class="sxs-lookup"><span data-stu-id="60763-107">See also</span></span>

- [<span data-ttu-id="60763-108">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="60763-108">ISocialSession::LoggedOnUserName</span></span>](isocialsession-loggedonusername.md)  
- [<span data-ttu-id="60763-109">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="60763-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

