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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339210"
---
# <a name="shutting-down-a-service-provider"></a>Apagar un proveedor de servicios

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar la sesión y apagar todos los proveedores de servicios activos, MAPI a su vez llama a los métodos siguientes: 
  
- [IABLogon::Logoff para](iablogon-logoff.md) proveedores de libreta de direcciones. 
    
- [IMSLogon::Logoff para](imslogon-logoff.md) proveedores de almacén de mensajes. 
    
- [IXPLogon::TransportLogoff para](ixplogon-transportlogoff.md) proveedores de transporte. 
    
Estos métodos tienen implementaciones similares. Las tareas principales que realiza un método de cierre de sesión son las siguientes:
  
- Liberar todos los objetos abiertos, incluidos los subobjetos y los objetos de estado.
    
- Llamar al método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para disminuir su recuento de referencias. 
    
- Quitar todas las estructuras [MAPIUID](mapiuid.md) registradas del proveedor. 
    
- Quitar la fila del proveedor en la tabla de estado.
    
- Realizar cualquier tarea relacionada con la limpieza de recursos, como las siguientes:
    
  - Terminación de una conexión con un servidor remoto.
    
  - Disminuir el número de referencias en el objeto de inicio de sesión.
    
  - Quitar el objeto de inicio de sesión de la lista de objetos de inicio de sesión que almacena el proveedor.
    
  - En modo de depuración, emitiendo seguimientos para localizar objetos que tienen pérdida de memoria.
    
Cuando el método de cierre de sesión devuelve, MAPI llama a lo siguiente:
  
- El método **IUnknown::Release** del objeto de inicio de sesión. 
    
- Método Shutdown del objeto **de** proveedor para realizar las tareas de limpieza finales. Según el tipo de proveedor, se llama a uno de los siguientes métodos: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) para proveedores de libreta de direcciones 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) para proveedores de almacén de mensajes 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) para proveedores de transporte 
    
- Método **IUnknown::Release** del objeto de proveedor. 
    
Si el proveedor es un almacén de mensajes, una llamada de cliente a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) también iniciará el proceso de apagado. **StoreLogoff** cierra un proveedor de almacén de mensajes en particular y no tiene ningún efecto en la sesión. Solo se puede cerrar un proveedor de almacén de mensajes con este método; no hay ninguna forma explícita de cerrar una libreta de direcciones o un proveedor de transporte en particular. Para obtener información sobre cómo responder a una llamada **a StoreLogoff,** vea [Apagar un proveedor de almacén de mensajes](shutting-down-a-message-store-provider.md).
  
La DLL del proveedor se descargará cuando MAPI llame a la función de API de Win32 **FreeLibrary**, una llamada que se realiza después de que el último cliente activo haya llamado [MAPIUninitialize](mapiuninitialize.md). Para este momento, el proveedor de servicios habrá terminado de cerrarse. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

