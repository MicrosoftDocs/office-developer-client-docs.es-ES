---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Agrega a la persona identificada por los parámetros emailAddresses y displayName como amigo para el usuario ha iniciado sesión en la red social.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821136"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="42db5-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="42db5-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="42db5-104">Agrega a la persona identificada por los parámetros _emailAddresses_ y _displayName_ como amigo para el usuario ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="42db5-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="42db5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42db5-105">Parameters</span></span>

<span data-ttu-id="42db5-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="42db5-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="42db5-107">[entrada] Una matriz que contiene una o varias direcciones SMTP válidas para una persona en la red social.</span><span class="sxs-lookup"><span data-stu-id="42db5-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="42db5-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="42db5-108">_displayName_</span></span>
  
> <span data-ttu-id="42db5-109">[entrada] Una cadena que contiene el nombre para mostrar de la persona que se agregará como un amigo.</span><span class="sxs-lookup"><span data-stu-id="42db5-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42db5-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42db5-110">Remarks</span></span>

<span data-ttu-id="42db5-111">Si Outlook Social Connector (OSC) proporciona más información que en la dirección SMTP de la matriz en el parámetro **emailAddresses** , el proveedor de OSC puede asumir que el primer elemento es la dirección SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="42db5-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="42db5-112">Si el proveedor ha establecido el elemento **followPerson** como **true** en el XML de las **capacidades** y ninguno de los elementos de _emailAddresses_ coincide con un usuario en la red, el proveedor debe devolver el error OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="42db5-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="42db5-113">Si el proveedor ha establecido **followPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="42db5-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="42db5-114">Si el método **FollowPersonEx** se realiza correctamente, el proveedor puede utilizar la cadena en el parámetro _displayName_ a la persona en cualquier correo electrónico de confirmación de amigo subsiguientes, en lugar de hacer frente a la persona por la dirección SMTP de direcciones.</span><span class="sxs-lookup"><span data-stu-id="42db5-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="42db5-115">Por otro lado, el proveedor debe ser capaz de controlar el OSC pasando una cadena vacía para el parámetro _displayName_ .</span><span class="sxs-lookup"><span data-stu-id="42db5-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="42db5-116">Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en el XML de las capacidades, el OSC llama a **FollowPersonEx** en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="42db5-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="42db5-117">Si el proveedor ha establecido **followPerson** como **true** pero no implementa la interfaz **ISocialSession2** , o **FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llama **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="42db5-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42db5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="42db5-118">See also</span></span>

- [<span data-ttu-id="42db5-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42db5-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

