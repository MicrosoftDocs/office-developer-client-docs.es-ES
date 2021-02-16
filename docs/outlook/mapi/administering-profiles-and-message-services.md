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
# <a name="administering-profiles-and-message-services"></a>Administración de perfiles y servicios de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La administración de perfiles y servicios de mensajes puede implicar la creación de nuevos perfiles, la eliminación de perfiles antiguos y la modificación del contenido de los perfiles existentes cambiando los servicios de mensajes y los proveedores de servicios que contienen. No todos los clientes admiten la administración de perfiles y servicios de mensajes como características estándar. Algunos clientes no tienen nada más que ver con los perfiles que permitir que sus usuarios seleccionen uno al iniciar sesión.
  
Si admite la administración del servicio de mensajes o perfiles, lo más probable es que use las siguientes interfaces implementadas por MAPI:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) para administrar un servicio de mensajes en un perfil, accesible a través de [IMAPISession::AdminServices](imapisession-adminservices.md) o [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Los clientes de mensajería suelen llamar **a IMAPISession** mientras los clientes de configuración, o los clientes que no envían ni reciben mensajes, llaman a **IProfAdmin**. Siempre que sea posible, llame **al método IProfAdmin** porque no hace que se pueda iniciar el servicio de mensajes. Para obtener más información acerca del uso de la interfaz **IMsgServiceAdmin,** vea los siguientes [temas:](configuring-a-message-service.md)Configuración de un servicio de [mensajes,](copying-a-message-service.md)copia de un servicio de mensajes y eliminación de un servicio [de mensajes.](deleting-a-message-service.md)
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) para administrar un perfil, accesible a través de la [función MAPIAdminProfiles.](mapiadminprofiles.md) Para obtener más información acerca del uso de la interfaz **IProfAdmin,** vea los siguientes [temas:](creating-a-profile-by-using-custom-code.md)Creación de un perfil mediante código [personalizado,](copying-a-profile.md)copia de un [perfil,](deleting-a-profile.md)eliminación de un [perfil,](finding-a-profile-name.md)búsqueda de un nombre de perfil y configuración de un perfil [predeterminado.](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) para mantener las propiedades en una sección de perfil, accesibles a través del método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) o [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) Para obtener más información acerca de las secciones de perfil, vea [Perfiles MAPI](mapi-profiles.md).
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) para administrar los proveedores de servicios en un servicio de mensajes, accesible a través de [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Para obtener más información acerca del uso de **la interfaz IProviderAdmin,** vea Agregar o [eliminar proveedores en un servicio de mensajes.](adding-or-deleting-providers-in-a-message-service.md)
    
Tenga cuidado en la compatibilidad con la administración de perfiles y servicios de mensajes. No hay medidas de seguridad para protegerse contra la modificación negativa de un perfil que está en uso. MAPI puede impedir que elimine un perfil en uso, pero no puede impedir que elimine todos los servicios de mensajes que tiene. Si elimina todos los servicios de mensajes de un perfil, todos los proveedores de servicios de estos servicios dejarán de provocar resultados impredecibles.
  
## <a name="in-this-section"></a>En esta sección

[Creación de un perfil](creating-a-profile.md)
  
> Describe cómo crear un perfil.
    
[Copiar un perfil](copying-a-profile.md)
  
> Describe cómo copiar un perfil.
    
[Eliminar un perfil](deleting-a-profile.md)
  
> Describe cómo eliminar un perfil.
    
[Establecer un perfil predeterminado](setting-a-default-profile.md)
  
> Describe cómo establecer un perfil predeterminado.
    
[Buscar un nombre de perfil](finding-a-profile-name.md)
  
> Describe cómo encontrar un nombre de perfil.
    
[Adición de un servicio de mensajes](adding-a-message-service.md)
  
> Describe cómo agregar un servicio de mensajes.
    
[Configuración de un servicio de mensajes](configuring-a-message-service.md)
  
> Describe cómo configurar un servicio de mensajes.
    
[Copiar un servicio de mensajes](copying-a-message-service.md)
  
> Describe cómo copiar un servicio de mensajes en un perfil.
    
[Eliminación de un servicio de mensajes](deleting-a-message-service.md)
  
> Describe cómo eliminar un servicio de mensajes.
    
[Agregar o eliminar proveedores en un servicio de mensajes](adding-or-deleting-providers-in-a-message-service.md)
  
> Describe cómo agregar o eliminar proveedores en un servicio de mensajes.
    

