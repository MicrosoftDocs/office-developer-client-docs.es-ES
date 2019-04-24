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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330236"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="d7e79-103">Administración de perfiles y servicios de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="d7e79-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7e79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7e79-105">La administración de perfiles y del servicio de mensajes puede implicar la creación de nuevos perfiles, la eliminación de perfiles antiguos y la modificación del contenido de los perfiles existentes mediante el cambio de los servicios de mensajes y los proveedores de servicios que contienen.</span><span class="sxs-lookup"><span data-stu-id="d7e79-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="d7e79-106">No todos los clientes admiten el perfil y la administración del servicio de mensajes como características estándar.</span><span class="sxs-lookup"><span data-stu-id="d7e79-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="d7e79-107">Algunos clientes no tienen nada más que hacer con los perfiles que permitir que los usuarios seleccionen uno durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d7e79-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="d7e79-108">Si admite la administración de perfiles o del servicio de mensajes, lo más probable es que use las siguientes interfaces que se implementan mediante MAPI:</span><span class="sxs-lookup"><span data-stu-id="d7e79-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="d7e79-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar un servicio de mensajes en un perfil, accesible a través de [IMAPISession:: AdminServices](imapisession-adminservices.md) o [IProfAdmin:: AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="d7e79-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="d7e79-110">Los clientes de mensajería suelen llamar a **IMAPISession** mientras los clientes de configuración o los clientes que no envían o reciben mensajes, llaman a **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="d7e79-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="d7e79-111">Siempre que sea posible, llame al método **IProfAdmin** porque no hace que se inicie el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="d7e79-112">Para obtener más información acerca del uso de la interfaz **IMsgServiceAdmin** , consulte los siguientes temas: [configurar un servicio de mensajes](configuring-a-message-service.md), [copiar un servicio](copying-a-message-service.md)de mensajes y [eliminar un servicio de mensajes](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="d7e79-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="d7e79-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar un perfil, accesible a través de la función [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="d7e79-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="d7e79-114">Para obtener más información acerca del uso de la interfaz **IProfAdmin** , vea los temas siguientes: [creación de un perfil mediante código personalizado](creating-a-profile-by-using-custom-code.md), [copia de un perfil](copying-a-profile.md), [eliminación de un perfil](deleting-a-profile.md), [búsqueda de un nombre de perfil](finding-a-profile-name.md)y [configuración de un Perfil predeterminado](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="d7e79-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="d7e79-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) para mantener las propiedades de una sección de perfil, a las que se puede tener acceso a través del método [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) o [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="d7e79-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="d7e79-116">Para obtener más información acerca de las secciones de perfil, consulte [MAPI](mapi-profiles.md)profiles.</span><span class="sxs-lookup"><span data-stu-id="d7e79-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="d7e79-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar los proveedores de servicios en un servicio de mensajes, a los que se puede tener acceso a través de [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="d7e79-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="d7e79-118">Para obtener más información acerca del uso de la interfaz **IProviderAdmin** , vea [Agregar o eliminar proveedores en un servicio de mensajes](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="d7e79-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="d7e79-119">Tenga cuidado con la compatibilidad de la administración de perfiles y del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="d7e79-120">No hay ninguna protección que proteger contra la modificación adversa de un perfil que está en uso.</span><span class="sxs-lookup"><span data-stu-id="d7e79-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="d7e79-121">MAPI puede impedir que se elimine un perfil en uso, pero no puede impedir que se eliminen todos los servicios de mensajes que contenga.</span><span class="sxs-lookup"><span data-stu-id="d7e79-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="d7e79-122">Si elimina todos los servicios de mensajes de un perfil, todos los proveedores de servicios de estos servicios se detendrán, con lo que se producirán resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="d7e79-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d7e79-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d7e79-123">In this section</span></span>

[<span data-ttu-id="d7e79-124">Creación de un perfil</span><span class="sxs-lookup"><span data-stu-id="d7e79-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="d7e79-125">Describe cómo crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e79-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="d7e79-126">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="d7e79-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="d7e79-127">Describe cómo copiar un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e79-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="d7e79-128">Eliminación de un perfil</span><span class="sxs-lookup"><span data-stu-id="d7e79-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="d7e79-129">Describe cómo eliminar un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e79-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="d7e79-130">Establecer un perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="d7e79-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="d7e79-131">Describe cómo establecer un perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d7e79-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="d7e79-132">Buscar un nombre de perfil</span><span class="sxs-lookup"><span data-stu-id="d7e79-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="d7e79-133">Describe cómo encontrar un nombre de un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e79-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="d7e79-134">Adición de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="d7e79-135">Describe cómo agregar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="d7e79-136">Configuración de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="d7e79-137">Describe cómo configurar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="d7e79-138">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="d7e79-139">Describe cómo copiar un servicio de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e79-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="d7e79-140">Eliminación de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="d7e79-141">Describe cómo eliminar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="d7e79-142">Adición o eliminación de proveedores en un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7e79-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="d7e79-143">Describe cómo agregar o eliminar proveedores en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7e79-143">Describes how to add or delete providers in a message service.</span></span>
    

