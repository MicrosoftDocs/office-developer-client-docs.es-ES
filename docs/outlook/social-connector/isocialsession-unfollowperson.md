---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Quita la persona identificada por el parámetro userID como un amigo en la red social.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418438"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="c2ac1-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="c2ac1-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="c2ac1-104">Quita la persona identificada por el parámetro  _userID_ como un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="c2ac1-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="c2ac1-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2ac1-105">Parameters</span></span>

<span data-ttu-id="c2ac1-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="c2ac1-106">_userID_</span></span>
  
> <span data-ttu-id="c2ac1-107">[entrada] Cadena que contiene un identificador de usuario de red social para una persona.</span><span class="sxs-lookup"><span data-stu-id="c2ac1-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2ac1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2ac1-108">Remarks</span></span>

<span data-ttu-id="c2ac1-109">El  _parámetro userID_ debe ser un identificador de usuario válido para la persona de la red social.</span><span class="sxs-lookup"><span data-stu-id="c2ac1-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="c2ac1-110">Si el proveedor de Outlook Social Connector (OSC) ha establecido **doNotFollowPerson** como **true** en el XML para las funcionalidades, el proveedor debe devolver el error OSC_E_NOT_FOUND en caso de que el identificador de usuario pasado no coincida con un usuario de la red.</span><span class="sxs-lookup"><span data-stu-id="c2ac1-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="c2ac1-111">Si el proveedor ha establecido **doNotFollowPerson** como **false** en las capacidades, el proveedor debe devolver el OSC_E_FAIL error.</span><span class="sxs-lookup"><span data-stu-id="c2ac1-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="c2ac1-112">Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c2ac1-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2ac1-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ac1-113">See also</span></span>

- [<span data-ttu-id="c2ac1-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2ac1-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

