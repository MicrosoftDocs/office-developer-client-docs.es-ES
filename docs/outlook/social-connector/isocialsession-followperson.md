---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Agrega a la persona identificada por el parámetro emailAddress como amigo para el usuario ha iniciado sesión en la red social.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821118"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="12576-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="12576-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="12576-104">Agrega a la persona identificada por el parámetro _emailAddress_ como amigo para el usuario ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="12576-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="12576-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12576-105">Parameters</span></span>

<span data-ttu-id="12576-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="12576-106">_emailAddress_</span></span>
  
> <span data-ttu-id="12576-107">[entrada] Una cadena que contiene una dirección de correo electrónico de una persona.</span><span class="sxs-lookup"><span data-stu-id="12576-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12576-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12576-108">Remarks</span></span>

<span data-ttu-id="12576-109">El parámetro _emailAddress_ debe ser una dirección SMTP válida.</span><span class="sxs-lookup"><span data-stu-id="12576-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="12576-110">Si el proveedor de Outlook Social Connector (OSC) ha establecido el método **followPerson** como **true** en **las capacidades**y el argumento para _emailAddress_ no coincide con un usuario en la red, el proveedor debe devolver el OSC_E_NOT_FOUND error.</span><span class="sxs-lookup"><span data-stu-id="12576-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="12576-111">Si el proveedor ha establecido **followPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="12576-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="12576-112">Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en **funciones**, el OSC llamará a [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) en lugar de **ISocialSession::FollowPerson **.</span><span class="sxs-lookup"><span data-stu-id="12576-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="12576-113">Si el proveedor no implementa la interfaz **ISocialSession2** o **ISocialSession2::FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llamará a **ISocialSession::FollowPerson** siempre que el proveedor ha establecido ** followPerson** como **true** en **funciones**.</span><span class="sxs-lookup"><span data-stu-id="12576-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="12576-114">Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="12576-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="12576-115">La hora de decidir si implementar **ISocalSession::FollowPerson** o **ISocialSession2::FollowPersonEx**, se debe tener en cuenta si su proveedor de las necesidades de los otros métodos de **ISocialSession2**y si puede usar el _ djsplayName_ parámetro en **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="12576-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12576-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="12576-116">See also</span></span>

- [<span data-ttu-id="12576-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12576-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

