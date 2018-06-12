---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Quita a la persona identificada por el parámetro userID como amigo en la red social.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821127"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="94948-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="94948-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="94948-104">Quita a la persona identificada por el parámetro _userID_ como amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="94948-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="94948-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94948-105">Parameters</span></span>

<span data-ttu-id="94948-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="94948-106">_userID_</span></span>
  
> <span data-ttu-id="94948-107">[entrada] Una cadena que contiene un identificador de usuario de redes sociales de una persona.</span><span class="sxs-lookup"><span data-stu-id="94948-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94948-108">Notas</span><span class="sxs-lookup"><span data-stu-id="94948-108">Remarks</span></span>

<span data-ttu-id="94948-109">El parámetro _userID_ debe ser un identificador de usuario válido para la persona en la red social.</span><span class="sxs-lookup"><span data-stu-id="94948-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="94948-110">Si el proveedor de Outlook Social Connector (OSC) ha establecido **doNotFollowPerson** como **true** en el XML de **las capacidades**, el proveedor debe devolver el error OSC_E_NOT_FOUND en el caso de que el usuario identificador que se pasó no coincide con un usuario en la red.</span><span class="sxs-lookup"><span data-stu-id="94948-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="94948-111">Si el proveedor ha establecido **doNotFollowPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="94948-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="94948-112">Para obtener información acerca de los códigos de error, vea [Códigos de Error de Outlook Social Connector proveedor](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="94948-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94948-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="94948-113">See also</span></span>

- [<span data-ttu-id="94948-114">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94948-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

