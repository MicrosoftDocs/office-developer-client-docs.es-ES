---
title: Comprobar la configuración del proveedor de servicios
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418851"
---
# <a name="verifying-service-provider-configuration"></a>Comprobar la configuración del proveedor de servicios
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El método de inicio de sesión ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) debe comprobar la configuración del proveedor. Esto implica comprobar que todas las propiedades necesarias para el funcionamiento completo se establecen correctamente. Cada proveedor requiere un número diferente de propiedades; la configuración depende del proveedor y del grado de interacción del usuario que permita. Algunos proveedores de servicios mantienen todas las propiedades necesarias en el perfil. 

Otros proveedores de servicios mantienen un conjunto parcial de propiedades en el perfil y solicitan al usuario valores que faltan. Sin embargo, otros proveedores no almacenan propiedades en el perfil en absoluto, ya que dependen del usuario para proporcionar toda la información necesaria para la configuración.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Para recuperar las propiedades almacenadas en el perfil
  
1. Llama [a IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)y pasa [el MAPIUID](mapiuid.md) del proveedor como parámetro de entrada. 
    
2. Llame a los [métodos IMAPIProp::GetProps](imapiprop-getprops.md) o [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la sección de perfil para recuperar propiedades individuales o una lista de propiedades. 
    
### <a name="to-set-properties-from-user-information"></a>Para establecer propiedades a partir de la información del usuario
  
Mostrar una hoja de propiedades, si MAPI no ha establecido una marca que prohíba la presentación. Las siguientes marcas indican que no se puede presentar una interfaz de usuario.
  
|**Flag**|**Proveedor de servicios**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Proveedor de libreta de direcciones  <br/> |
|LOGON_NO_DIALOG  <br/> |Proveedor de transporte  <br/> |
|MDB_NO_DIALOG  <br/> |Proveedor de almacén de mensajes  <br/> |
   
Si el proveedor no almacena todas sus propiedades de configuración en el perfil, lo que requiere la interacción del usuario, y MAPI pasa una de las marcas de supresión del cuadro de diálogo al método de inicio de sesión, MAPI_E_UNCONFIGURED. También devuelve este error cuando no se establece la marca de supresión de cuadros de diálogo, pero el usuario no proporciona toda la información necesaria.
  
Cuando el proveedor de servicios produce un error en su método de inicio de sesión MAPI_E_UNCONFIGURED, MAPI llama de nuevo a la función de punto de entrada. Si la información no se puede encontrar con la segunda llamada, la sesión podría finalizar, en función de la importancia que tenga el proveedor de servicios. 
  
En la siguiente ilustración se muestra la lógica necesaria para la configuración en el método de inicio de sesión del proveedor de servicios. 
  
**Diagrama de flujo de comprobación de configuración**
  
![Diagrama de flujo de verificación de configuración]Diagrama de flujo de verificación de(media/amapi_62.gif "configuración")
  
## <a name="see-also"></a>Vea también

- [Implementación del inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

