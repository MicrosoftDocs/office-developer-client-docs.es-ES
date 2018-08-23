---
title: Administrar perfiles y servicios de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 124f4875834e035e29d4c63e52789bf07f18258d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587547"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="bd990-103">Administrar perfiles y servicios de mensaje</span><span class="sxs-lookup"><span data-stu-id="bd990-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="bd990-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd990-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd990-105">Perfiles y mensaje puede implicar la administración del servicio de creación de nuevos perfiles, eliminar perfiles anteriores y modificar el contenido de los perfiles existentes mediante la modificación de los servicios de mensaje y los proveedores de servicios de contenidos en ellos.</span><span class="sxs-lookup"><span data-stu-id="bd990-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="bd990-106">No todos los clientes admiten la administración de servicio de perfil y mensaje como características estándar.</span><span class="sxs-lookup"><span data-stu-id="bd990-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="bd990-107">Algunos clientes no tienen nada más que hacer con los perfiles de permitir que sus usuarios seleccionar una en tiempo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="bd990-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="bd990-108">Si se admite la administración del servicio de perfil o mensaje, lo más probable es que va a usar las siguientes interfaces que se implementan mediante MAPI:</span><span class="sxs-lookup"><span data-stu-id="bd990-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="bd990-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar un servicio de mensajes en un perfil, accesible a través de [IMAPISession::AdminServices](imapisession-adminservices.md) o [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="bd990-110">Clientes de mensajería, normalmente llaman **IMAPISession** mientras los clientes de configuración o los clientes que no enviar o recibir mensajes, llamar **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="bd990-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="bd990-111">Siempre que sea posible, llame al método de **IProfAdmin** , porque no provoca que se inicie el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd990-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="bd990-112">Para obtener más información acerca del uso de la interfaz de **IMsgServiceAdmin** , consulte los temas siguientes: [configuración de un servicio de mensajes](configuring-a-message-service.md), [Copiar un servicio de mensajes](copying-a-message-service.md)y [eliminación de un servicio de mensajes](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="bd990-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar un perfil, accesible a través de la función [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="bd990-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="bd990-114">Para obtener más información acerca del uso de la interfaz **IProfAdmin** , vea los siguientes temas: [creación de un perfil de uso de código personalizado](creating-a-profile-by-using-custom-code.md), [Copiar un perfil](copying-a-profile.md), [eliminación de un perfil](deleting-a-profile.md), [Buscar un nombre de perfil](finding-a-profile-name.md)y [configuración un Perfil predeterminado](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="bd990-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) para mantener las propiedades de una sección de perfil, puede tener acceso a través del método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) o [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="bd990-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="bd990-116">Para obtener más información acerca de las secciones de perfiles, consulte [Perfiles de MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="bd990-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar los proveedores de servicios en un servicio de mensajes, accesible a través de [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="bd990-118">Para obtener más información acerca del uso de la interfaz de **IProviderAdmin** , consulte [Adición o eliminación de proveedores en un servicio de mensajes](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd990-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="bd990-119">Tenga cuidado en el soporte técnico de administración del servicio de perfil y el mensaje.</span><span class="sxs-lookup"><span data-stu-id="bd990-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="bd990-120">No hay ningún medidas de seguridad para proteger el negativamente modificar un perfil que está en uso.</span><span class="sxs-lookup"><span data-stu-id="bd990-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="bd990-121">MAPI puede impedir la eliminación de un perfil de uso, pero no puede impedir la eliminación de cada servicio de mensajes en ella.</span><span class="sxs-lookup"><span data-stu-id="bd990-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="bd990-122">Si se elimina cada servicio de mensajes en un perfil, todos los proveedores de servicios en estos servicios detendrán lo que provoca resultados impredecibles que se produzca.</span><span class="sxs-lookup"><span data-stu-id="bd990-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bd990-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd990-123">In this section</span></span>

[<span data-ttu-id="bd990-124">Crear un perfil</span><span class="sxs-lookup"><span data-stu-id="bd990-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="bd990-125">Describe cómo crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="bd990-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="bd990-126">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="bd990-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="bd990-127">Describe cómo copiar un perfil.</span><span class="sxs-lookup"><span data-stu-id="bd990-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="bd990-128">Eliminar un perfil</span><span class="sxs-lookup"><span data-stu-id="bd990-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="bd990-129">Describe cómo eliminar un perfil.</span><span class="sxs-lookup"><span data-stu-id="bd990-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="bd990-130">Establecer un perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="bd990-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="bd990-131">Describe cómo establecer un perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd990-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="bd990-132">Buscar un nombre de perfil</span><span class="sxs-lookup"><span data-stu-id="bd990-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="bd990-133">Se describe cómo encontrar un nombre de un perfil.</span><span class="sxs-lookup"><span data-stu-id="bd990-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="bd990-134">Agregar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd990-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="bd990-135">Describe cómo agregar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd990-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="bd990-136">Configurar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd990-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="bd990-137">Se describe cómo configurar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd990-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="bd990-138">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd990-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="bd990-139">Describe cómo copiar un servicio de mensajes a un perfil.</span><span class="sxs-lookup"><span data-stu-id="bd990-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="bd990-140">Eliminar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd990-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="bd990-141">Describe cómo eliminar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd990-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="bd990-142">Agregar o eliminar los proveedores de servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd990-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="bd990-143">Describe cómo agregar o eliminar proveedores en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd990-143">Describes how to add or delete providers in a message service.</span></span>
    

