---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Agrega la persona identificada por los parámetros emailAddresses y displayName como un amigo del usuario que ha iniciado sesión en la red social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429834"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="b272a-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="b272a-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="b272a-104">Agrega la persona identificada por los parámetros  _emailAddresses_ y  _displayName_ como un amigo del usuario que ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="b272a-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="b272a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b272a-105">Parameters</span></span>

<span data-ttu-id="b272a-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="b272a-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="b272a-107">[entrada] Matriz que contiene una o varias direcciones SMTP válidas para una persona en la red social.</span><span class="sxs-lookup"><span data-stu-id="b272a-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="b272a-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="b272a-108">_displayName_</span></span>
  
> <span data-ttu-id="b272a-109">[entrada] Cadena que contiene el nombre para mostrar de la persona que se agregará como amigo.</span><span class="sxs-lookup"><span data-stu-id="b272a-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b272a-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b272a-110">Remarks</span></span>

<span data-ttu-id="b272a-111">Si outlook Social Connector (OSC) proporciona más que la dirección SMTP en la matriz en el parámetro **emailAddresses,** el proveedor de OSC puede suponer que el primer elemento es la dirección SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="b272a-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="b272a-112">Si el proveedor ha establecido el elemento **followPerson** como **true** en el **XML** de capacidades y ninguno de los elementos de  _emailAddresses_ coincide con un usuario de la red, el proveedor debe devolver el error OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="b272a-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="b272a-113">Si el proveedor ha establecido **followPerson** como **false** en las capacidades, el proveedor debe devolver el OSC_E_FAIL error.</span><span class="sxs-lookup"><span data-stu-id="b272a-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="b272a-114">Si el método **FollowPersonEx** se realiza correctamente, el proveedor puede usar la cadena del parámetro  _displayName_ para dirigirse a la persona en cualquier correo electrónico de confirmación de amigos posterior, en lugar de dirigirse a la persona por la dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="b272a-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="b272a-115">Por otro lado, el proveedor debe ser capaz de controlar el OSC pasando una cadena vacía para el _parámetro displayName._</span><span class="sxs-lookup"><span data-stu-id="b272a-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="b272a-116">Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en el XML de capacidades, el OSC llama **a FollowPersonEx** en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="b272a-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="b272a-117">Si el proveedor ha establecido **followPerson** como **true** pero no implementa la interfaz **ISocialSession2,** o **FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llama a **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="b272a-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b272a-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b272a-118">See also</span></span>

- [<span data-ttu-id="b272a-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b272a-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

