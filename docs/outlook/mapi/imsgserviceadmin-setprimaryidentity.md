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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817746"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="b08f6-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="b08f6-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="b08f6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b08f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b08f6-105">Designa un servicio de mensajes para ser el proveedor de la identidad principal para el perfil.</span><span class="sxs-lookup"><span data-stu-id="b08f6-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="b08f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b08f6-106">Parameters</span></span>

 <span data-ttu-id="b08f6-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="b08f6-107">_lpUID_</span></span>
  
> <span data-ttu-id="b08f6-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes proporcionar la identidad principal, o NULL, que indica que **SetPrimaryIdentity** debe borrar la identidad actual.</span><span class="sxs-lookup"><span data-stu-id="b08f6-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="b08f6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b08f6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b08f6-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b08f6-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b08f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b08f6-111">Return value</span></span>

<span data-ttu-id="b08f6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b08f6-112">S_OK</span></span> 
  
> <span data-ttu-id="b08f6-113">El servicio de mensajes se ha asignado correctamente el proveedor de la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="b08f6-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="b08f6-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b08f6-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b08f6-115">**SetPrimaryIdentity** intentó designar un servicio de mensajes que tiene la marca SERVICE_NO_PRIMARY_IDENTITY establecer en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b08f6-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b08f6-116">Notas</span><span class="sxs-lookup"><span data-stu-id="b08f6-116">Remarks</span></span>

<span data-ttu-id="b08f6-117">El método **IMsgServiceAdmin::SetPrimaryIdentity** establece un servicio de mensajes como el proveedor de la identidad principal para el perfil.</span><span class="sxs-lookup"><span data-stu-id="b08f6-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="b08f6-118">La identidad principal normalmente es el usuario que ha iniciado sesión en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b08f6-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="b08f6-119">Se representan mediante tres propiedades:</span><span class="sxs-lookup"><span data-stu-id="b08f6-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="b08f6-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b08f6-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="b08f6-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b08f6-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="b08f6-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b08f6-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="b08f6-123">Cada proveedor de servicios en el servicio de mensajes designados establece estas tres propiedades en el nombre para mostrar, el identificador de entrada y la clave de búsqueda del usuario de mensajería que proporciona la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="b08f6-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="b08f6-124">Los clientes pueden recuperar el identificador de entrada de la identidad principal al llamar al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="b08f6-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="b08f6-125">La propiedad **PR_RESOURCE_FLAGS** se establece a STATUS_PRIMARY_IDENTITY para cada proveedor que es un miembro del servicio de mensajes que proporciona la identidad principal y a SERVICE_PRIMARY_IDENTITY para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b08f6-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="b08f6-126">Cuando un proveedor de servicios no puede facilitar la identidad principal para su servicio de mensajes, establece **PR_RESOURCE_FLAGS** a STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b08f6-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b08f6-127">**SetPrimaryIdentity** establece la propiedad **PR_RESOURCE_FLAGS** de cada servicio de mensajes que no proporciona la identidad principal a SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b08f6-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="b08f6-128">Cada proveedor de servicios de mensaje MAPI tiene información sobre puede establecer una identidad para cada uno de sus usuarios cuando un cliente inicia sesión en el servicio.</span><span class="sxs-lookup"><span data-stu-id="b08f6-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="b08f6-129">Sin embargo, debido a que MAPI admite conexiones a varios proveedores de servicio para cada sesión MAPI, no hay ninguna definición firme de identidad de un usuario determinado para la sesión MAPI como un todo; depende de la identidad del usuario en el servicio que está implicado.</span><span class="sxs-lookup"><span data-stu-id="b08f6-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="b08f6-130">Los clientes pueden llamar a **SetPrimaryIdentity** para designar una de las muchas identidades establecidas para un usuario por servicios de mensajes como la identidad principal para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="b08f6-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b08f6-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="b08f6-131">See also</span></span>



[<span data-ttu-id="b08f6-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b08f6-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="b08f6-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b08f6-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b08f6-134">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b08f6-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

