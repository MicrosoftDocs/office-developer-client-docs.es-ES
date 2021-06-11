---
title: Administración de perfiles y servicios de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410563"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="785c1-103">Administración de perfiles y servicios de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="785c1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="785c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="785c1-105">La administración de perfiles y servicios de mensajes puede implicar la creación de nuevos perfiles, la eliminación de perfiles antiguos y la modificación del contenido de los perfiles existentes cambiando los servicios de mensajes y los proveedores de servicios contenidos en ellos.</span><span class="sxs-lookup"><span data-stu-id="785c1-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="785c1-106">No todos los clientes admiten la administración de perfiles y servicios de mensajes como características estándar.</span><span class="sxs-lookup"><span data-stu-id="785c1-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="785c1-107">Algunos clientes no tienen nada más que ver con los perfiles que permitir que sus usuarios seleccionen uno al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="785c1-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="785c1-108">Si admite la administración del servicio de mensajes o perfiles, lo más probable es que use las siguientes interfaces implementadas por MAPI:</span><span class="sxs-lookup"><span data-stu-id="785c1-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="785c1-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar un servicio de mensajes en un perfil, accesible a través de [IMAPISession::AdminServices](imapisession-adminservices.md) o [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="785c1-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="785c1-110">Los clientes de mensajería suelen llamar **a IMAPISession** mientras los clientes de configuración, o los clientes que no envían ni reciben mensajes, llaman **a IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="785c1-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="785c1-111">Siempre que sea posible, llame al **método IProfAdmin** porque no hace que se pueda iniciar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="785c1-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="785c1-112">Para obtener más información acerca del uso de la interfaz **IMsgServiceAdmin,** vea los temas siguientes: [Configuración](configuring-a-message-service.md)de un servicio de [mensajes,](copying-a-message-service.md)Copia de un servicio de mensajes y Eliminación de un servicio [de mensajes](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="785c1-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="785c1-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar un perfil, accesible a través de la [función MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="785c1-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="785c1-114">Para obtener más información acerca del uso de la interfaz **IProfAdmin,** vea los temas [siguientes:](creating-a-profile-by-using-custom-code.md)Creación de un perfil mediante código [personalizado,](copying-a-profile.md)Copia de un [perfil,](deleting-a-profile.md)Eliminación de un perfil [,](finding-a-profile-name.md)Búsqueda de un nombre de perfil y Configuración de un perfil [predeterminado.](setting-a-default-profile.md)</span><span class="sxs-lookup"><span data-stu-id="785c1-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="785c1-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) para mantener las propiedades de una sección de perfil, accesible a través del método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) o [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="785c1-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="785c1-116">Para obtener más información acerca de las secciones de perfil, vea [Perfiles MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="785c1-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="785c1-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar los proveedores de servicios en un servicio de mensajes, accesible a través [de IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="785c1-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="785c1-118">Para obtener más información acerca del uso de **la interfaz IProviderAdmin,** vea [Agregar o eliminar proveedores en un servicio de mensajes.](adding-or-deleting-providers-in-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="785c1-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="785c1-119">Tenga cuidado en la compatibilidad con la administración del servicio de mensajes y perfiles.</span><span class="sxs-lookup"><span data-stu-id="785c1-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="785c1-120">No hay medidas de seguridad para proteger contra la modificación negativa de un perfil que está en uso.</span><span class="sxs-lookup"><span data-stu-id="785c1-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="785c1-121">MAPI puede impedir que elimine un perfil en uso, pero no puede impedir que elimine todos los servicios de mensajes en él.</span><span class="sxs-lookup"><span data-stu-id="785c1-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="785c1-122">Si elimina todos los servicios de mensajes de un perfil, todos los proveedores de servicios de estos servicios dejarán de provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="785c1-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="785c1-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="785c1-123">In this section</span></span>

[<span data-ttu-id="785c1-124">Creación de un perfil</span><span class="sxs-lookup"><span data-stu-id="785c1-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="785c1-125">Describe cómo crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="785c1-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="785c1-126">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="785c1-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="785c1-127">Describe cómo copiar un perfil.</span><span class="sxs-lookup"><span data-stu-id="785c1-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="785c1-128">Eliminar un perfil</span><span class="sxs-lookup"><span data-stu-id="785c1-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="785c1-129">Describe cómo eliminar un perfil.</span><span class="sxs-lookup"><span data-stu-id="785c1-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="785c1-130">Establecer un perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="785c1-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="785c1-131">Describe cómo establecer un perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="785c1-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="785c1-132">Buscar un nombre de perfil</span><span class="sxs-lookup"><span data-stu-id="785c1-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="785c1-133">Describe cómo buscar un nombre de un perfil.</span><span class="sxs-lookup"><span data-stu-id="785c1-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="785c1-134">Agregar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="785c1-135">Describe cómo agregar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="785c1-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="785c1-136">Configuración de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="785c1-137">Describe cómo configurar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="785c1-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="785c1-138">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="785c1-139">Describe cómo copiar un servicio de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="785c1-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="785c1-140">Eliminación de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="785c1-141">Describe cómo eliminar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="785c1-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="785c1-142">Agregar o eliminar proveedores en un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="785c1-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="785c1-143">Describe cómo agregar o eliminar proveedores en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="785c1-143">Describes how to add or delete providers in a message service.</span></span>
    

