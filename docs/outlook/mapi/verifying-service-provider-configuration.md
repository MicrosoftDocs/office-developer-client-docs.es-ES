---
title: Comprobar la configuración del proveedor de servicio
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589640"
---
# <a name="verifying-service-provider-configuration"></a>Comprobar la configuración del proveedor de servicio
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El método de inicio de sesión ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) debe comprobar la configuración de su proveedor. Esto implica comprobar que todas las propiedades necesarias para la operación completa se establecen correctamente. Cada proveedor requiere un número diferente de propiedades; configuración depende de su proveedor y el grado de interacción del usuario que va a permitir. Algunos proveedores de servicios tenga todas las propiedades necesarias en el perfil. 

Otros proveedores de servicios de mantener un conjunto parcial de propiedades en el perfil y pedir al usuario los valores que faltan. Aún otros proveedores no almacene las propiedades en el perfil en absoluto, confiar en el usuario para proporcionar toda la información necesaria para la configuración de.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Para recuperar las propiedades almacenadas en el perfil
  
1. Llame a [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), pasando el [MAPIUID](mapiuid.md) de su proveedor como un parámetro de entrada. 
    
2. Llame a métodos [IMAPIProp::GetProps](imapiprop-getprops.md) o [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la sección de perfil para recuperar las propiedades individuales o una lista de propiedades. 
    
### <a name="to-set-properties-from-user-information"></a>Para establecer las propiedades de información del usuario
  
Mostrar una hoja de propiedades, si MAPI no ha establecido una marca de prohibición de la presentación. Los siguientes marcadores de indican que no se puede presentar una interfaz de usuario.
  
|**Flag**|**Proveedor de servicios**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Proveedor de la libreta de direcciones  <br/> |
|LOGON_NO_DIALOG  <br/> |Proveedor de transporte  <br/> |
|MDB_NO_DIALOG  <br/> |Proveedor de almacén de mensajes  <br/> |
   
Si su proveedor no almacenar todas sus propiedades de configuración en el perfil, requerir la interacción del usuario, y MAPI uno de los indicadores de supresión del cuadro de diálogo pasa al método de inicio de sesión, devolver MAPI_E_UNCONFIGURED. También puede devolver este error cuando no está establecido el indicador de supresión del cuadro de diálogo, pero el usuario no proporciona toda la información necesaria.
  
Cuando su proveedor de servicios se produce un error de su método de inicio de sesión con MAPI_E_UNCONFIGURED, MAPI llama la función de punto de entrada de nuevo. Si la información no se puede encontrar con la segunda llamada, es posible que terminar la sesión, dependiendo de cómo importante es de su proveedor de servicios. 
  
En la siguiente ilustración se muestra la lógica de requerido para la configuración en el método de inicio de sesión del proveedor de servicio. 
  
**Diagrama de flujo de comprobación de configuración**
  
![Diagrama de flujo de comprobación de configuración] (media/amapi_62.gif "Diagrama de flujo de comprobación de configuración")
  
## <a name="see-also"></a>Recursos adicionales

- [Implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

