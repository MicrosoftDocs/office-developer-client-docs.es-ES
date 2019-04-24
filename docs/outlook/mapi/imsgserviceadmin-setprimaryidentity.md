---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317363"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="2362e-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="2362e-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="2362e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2362e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2362e-105">Designa un servicio de mensajes para que sea el proveedor de la identidad principal del perfil.</span><span class="sxs-lookup"><span data-stu-id="2362e-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="2362e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2362e-106">Parameters</span></span>

 <span data-ttu-id="2362e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="2362e-107">_lpUID_</span></span>
  
> <span data-ttu-id="2362e-108">a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes para proporcionar la identidad principal, o null, que indica que **SetPrimaryIdentity** debe borrar la identidad actual.</span><span class="sxs-lookup"><span data-stu-id="2362e-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="2362e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2362e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2362e-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2362e-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2362e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2362e-111">Return value</span></span>

<span data-ttu-id="2362e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2362e-112">S_OK</span></span> 
  
> <span data-ttu-id="2362e-113">El servicio de mensajes se asignó correctamente al proveedor de la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="2362e-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="2362e-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2362e-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2362e-115">**SetPrimaryIdentity** intentó designar un servicio de mensajes que tiene la marca SERVICE_NO_PRIMARY_IDENTITY establecida en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2362e-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2362e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2362e-116">Remarks</span></span>

<span data-ttu-id="2362e-117">El método **IMsgServiceAdmin:: SetPrimaryIdentity** establece un servicio de mensajes como el proveedor de la identidad principal del perfil.</span><span class="sxs-lookup"><span data-stu-id="2362e-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="2362e-118">La identidad principal suele ser el usuario que ha iniciado sesión en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2362e-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="2362e-119">Se representa mediante tres propiedades:</span><span class="sxs-lookup"><span data-stu-id="2362e-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="2362e-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2362e-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="2362e-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2362e-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="2362e-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2362e-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="2362e-123">Todos los proveedores de servicios del servicio de mensajes designados establecen estas tres propiedades en el nombre para mostrar, el identificador de entrada y la clave de búsqueda del usuario de mensajería que proporciona la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="2362e-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="2362e-124">Los clientes pueden recuperar el identificador de entrada de la identidad principal llamando al método [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="2362e-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="2362e-125">La propiedad **PR_RESOURCE_FLAGS** se establece en STATUS_PRIMARY_IDENTITY para todos los proveedores que son miembros del servicio de mensajes que proporciona la identidad principal y para SERVICE_PRIMARY_IDENTITY para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2362e-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="2362e-126">Cuando un proveedor de servicios no puede proporcionar la identidad principal para su servicio de mensajes, establece **PR_RESOURCE_FLAGS** en STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="2362e-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="2362e-127">**SetPrimaryIdentity** establece la propiedad **PR_RESOURCE_FLAGS** de cada servicio de mensajes que no proporciona la identidad principal a SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="2362e-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="2362e-128">Cada proveedor de servicios de mensajes con el que MAPI tiene información puede establecer una identidad para cada uno de los usuarios cuando un cliente inicia sesión en el servicio.</span><span class="sxs-lookup"><span data-stu-id="2362e-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="2362e-129">Sin embargo, debido a que MAPI admite conexiones a varios proveedores de servicios para cada sesión de MAPI, no hay ninguna definición de la identidad de un usuario en particular para la sesión MAPI en su conjunto; la identidad de un usuario depende del servicio implicado.</span><span class="sxs-lookup"><span data-stu-id="2362e-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="2362e-130">Los clientes pueden llamar a **SetPrimaryIdentity** para designar una de las muchas identidades que los servicios de mensajes establecen para un usuario como identidad principal para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="2362e-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2362e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2362e-131">See also</span></span>



[<span data-ttu-id="2362e-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="2362e-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="2362e-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2362e-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2362e-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2362e-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

