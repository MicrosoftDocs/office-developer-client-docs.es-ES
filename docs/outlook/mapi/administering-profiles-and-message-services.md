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
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816401"
---
# <a name="administering-profiles-and-message-services"></a>Administrar perfiles y servicios de mensaje

  
  
**Hace referencia a**: Outlook 
  
Perfiles y mensaje puede implicar la administración del servicio de creación de nuevos perfiles, eliminar perfiles anteriores y modificar el contenido de los perfiles existentes mediante la modificación de los servicios de mensaje y los proveedores de servicios de contenidos en ellos. No todos los clientes admiten la administración de servicio de perfil y mensaje como características estándar. Algunos clientes no tienen nada más que hacer con los perfiles de permitir que sus usuarios seleccionar una en tiempo de inicio de sesión.
  
Si se admite la administración del servicio de perfil o mensaje, lo más probable es que va a usar las siguientes interfaces que se implementan mediante MAPI:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar un servicio de mensajes en un perfil, accesible a través de [IMAPISession::AdminServices](imapisession-adminservices.md) o [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Clientes de mensajería, normalmente llaman **IMAPISession** mientras los clientes de configuración o los clientes que no enviar o recibir mensajes, llamar **IProfAdmin**. Siempre que sea posible, llame al método de **IProfAdmin** , porque no provoca que se inicie el servicio de mensajes. Para obtener más información acerca del uso de la interfaz de **IMsgServiceAdmin** , consulte los temas siguientes: [configuración de un servicio de mensajes](configuring-a-message-service.md), [Copiar un servicio de mensajes](copying-a-message-service.md)y [eliminación de un servicio de mensajes](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar un perfil, accesible a través de la función [MAPIAdminProfiles](mapiadminprofiles.md) . Para obtener más información acerca del uso de la interfaz **IProfAdmin** , vea los siguientes temas: [creación de un perfil de uso de código personalizado](creating-a-profile-by-using-custom-code.md), [Copiar un perfil](copying-a-profile.md), [eliminación de un perfil](deleting-a-profile.md), [Buscar un nombre de perfil](finding-a-profile-name.md)y [configuración un Perfil predeterminado](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) para mantener las propiedades de una sección de perfil, puede tener acceso a través del método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) o [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . Para obtener más información acerca de las secciones de perfiles, consulte [Perfiles de MAPI](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar los proveedores de servicios en un servicio de mensajes, accesible a través de [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Para obtener más información acerca del uso de la interfaz de **IProviderAdmin** , consulte [Adición o eliminación de proveedores en un servicio de mensajes](adding-or-deleting-providers-in-a-message-service.md).
    
Tenga cuidado en el soporte técnico de administración del servicio de perfil y el mensaje. No hay ningún medidas de seguridad para proteger el negativamente modificar un perfil que está en uso. MAPI puede impedir la eliminación de un perfil de uso, pero no puede impedir la eliminación de cada servicio de mensajes en ella. Si se elimina cada servicio de mensajes en un perfil, todos los proveedores de servicios en estos servicios detendrán lo que provoca resultados impredecibles que se produzca.
  
## <a name="in-this-section"></a>En esta sección

[Crear un perfil](creating-a-profile.md)
  
> Describe cómo crear un perfil.
    
[Copiar un perfil](copying-a-profile.md)
  
> Describe cómo copiar un perfil.
    
[Eliminar un perfil](deleting-a-profile.md)
  
> Describe cómo eliminar un perfil.
    
[Establecer un perfil predeterminado](setting-a-default-profile.md)
  
> Describe cómo establecer un perfil predeterminado.
    
[Buscar un nombre de perfil](finding-a-profile-name.md)
  
> Se describe cómo encontrar un nombre de un perfil.
    
[Agregar un servicio de mensajes](adding-a-message-service.md)
  
> Describe cómo agregar un servicio de mensajes.
    
[Configurar un servicio de mensajes](configuring-a-message-service.md)
  
> Se describe cómo configurar un servicio de mensajes.
    
[Copiar un servicio de mensajes](copying-a-message-service.md)
  
> Describe cómo copiar un servicio de mensajes a un perfil.
    
[Eliminar un servicio de mensajes](deleting-a-message-service.md)
  
> Describe cómo eliminar un servicio de mensajes.
    
[Agregar o eliminar los proveedores de servicio de mensajes](adding-or-deleting-providers-in-a-message-service.md)
  
> Describe cómo agregar o eliminar proveedores en un servicio de mensajes.
    

