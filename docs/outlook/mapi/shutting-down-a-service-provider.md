---
title: Apagar un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395178"
---
# <a name="shutting-down-a-service-provider"></a>Apagar un proveedor de servicios

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar la sesión y apagar todos los proveedores de servicio de active, MAPI a su vez llama a los métodos siguientes: 
  
- [IABLogon::Logoff](iablogon-logoff.md) para los proveedores de la libreta de direcciones. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) para los proveedores de almacén de mensajes. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para los proveedores de transporte. 
    
Estos métodos tienen implementaciones similar. Las principales tareas que realiza un método de cierre de sesión son los siguientes:
  
- Liberación de todos los objetos abiertos, incluidos los subobjetos y objetos de estado.
    
- Llamar al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para reducir su recuento de referencia. 
    
- Eliminación de todas las estructuras [MAPIUID](mapiuid.md) registradas de su proveedor de. 
    
- Eliminación de fila de su proveedor en la tabla de estado.
    
- Llevar a cabo las tareas relacionadas con la limpieza de recursos, como las siguientes:
    
  - Finalización de una conexión con un servidor remoto.
    
  - Disminuir la referencia de recuento en el objeto de inicio de sesión.
    
  - Quitar el objeto de inicio de sesión de la lista de objetos de inicio de sesión que almacena su proveedor.
    
  - En el modo de depuración, emitir seguimientos para localizar los objetos que se han perdido la memoria.
    
Cuando se devuelve el método de cierre de sesión, MAPI llama a lo siguiente:
  
- Método de **IUnknown:: Release** del objeto su inicio de sesión. 
    
- Método de **cierre** del objeto de su proveedor para llevar a cabo las tareas de limpieza final. Según el tipo de su proveedor, se llama uno de los métodos siguientes: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) para los proveedores de la libreta de direcciones 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) para los proveedores de almacén de mensajes 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) para los proveedores de transporte 
    
- Método de **IUnknown:: Release** del objeto de su proveedor. 
    
Si su proveedor es un almacén de mensajes, una llamada de cliente a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) también iniciará el proceso de cierre. **StoreLogoff** cierra un proveedor de almacén de mensaje concreto y no tiene ningún efecto en la sesión. Solo un proveedor de almacén de mensajes se puede cerrar con este método; No hay ninguna forma explícita para cerrar un proveedor de transporte o de la libreta de direcciones determinada. Para obtener información acerca de cómo responder a una **StoreLogoff** de llamadas, vea [Cerrando hacia abajo un mensaje de proveedor de almacenamiento](shutting-down-a-message-store-provider.md).
  
Archivo DLL de su proveedor se descargará cuando llama a la función API de Win32 **FreeLibrary**, una llamada que se realiza después de que el último cliente activo ha llamado [MAPIUninitialize](mapiuninitialize.md)MAPI. En este momento, su proveedor de servicios habrá terminado de cerrarse. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

