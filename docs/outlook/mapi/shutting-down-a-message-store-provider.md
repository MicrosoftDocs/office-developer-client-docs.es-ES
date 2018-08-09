---
title: Apagar un proveedor de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b5c9874ca465bb0ebed62f218d1512feb1a2f9ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820671"
---
# <a name="shutting-down-a-message-store-provider"></a>Apagar un proveedor de almacén de mensajes

  
  
**Hace referencia a**: Outlook 
  
Si su proveedor es un proveedor de almacén de mensajes, puede apagar en una de las siguientes maneras:
  
- Cuando un cliente o la cola MAPI llama a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Cerrando un proveedor de almacén de mensajes con **StoreLogoff** hace que el apagado se produzca de manera ordenada y controlada. 
    
- Cuando un cliente llama a [IMAPISession::Logoff](imapisession-logoff.md). 
    
La implementación de **IMsgStore::StoreLogoff** debe comenzar mediante una llamada a [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar a MAPI que se está cerrando, que indica que se van a registrar los proveedores de transporte relacionados. Cuando se devuelve **IMsgStore::StoreLogoff** , su autor de la llamada invoca (método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) ) de su almacén de mensajes. Implementar este método **versión** por llamar al método **IUnknown:: Release** del objeto de soporte técnico. 
  
MAPI realiza las siguientes tareas en su implementación de **IUnknown:: Release** para los almacenes de mensajes: 
  
1. Todos los de las estructuras [MAPIUID](mapiuid.md) registradas por el proveedor de almacén de mensajes quita. 
    
2. Quita la fila del proveedor de almacén de mensajes de la tabla de estado.
    
3. Llama a [IMSLogon::Logoff](imslogon-logoff.md) para liberar todos los objetos abiertos, los subobjetos y los objetos de estado. 
    
4. Llama a [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto de inicio de sesión del proveedor de almacén de mensajes. 
    
Algunos clientes podrían omitir la llamada a **IMsgStore::StoreLogoff**, iniciar el apagado de su proveedor de almacén de mensajes con la llamada al método de **IUnknown:: Release** del almacén de mensajes. Un cierre en estas circunstancias sin la llamada a **StoreLogoff** es menos ordenado y controlado. Método de **versión** de su almacén de mensajes para esta posibilidad de controlar y realizar un seguimiento de si se ha producido una llamada a **IMAPISupport::StoreLogoffTransports** de escritura. **StoreLogoffTransports** se debe llamar una vez durante el proceso de cierre. Si detecta en el método de la **versión** que **StoreLogoffTransports** todavía no se ha llamado, invocar con la marca LOGOFF_ABORT. 
  
## <a name="see-also"></a>Vea también



[Apagar un proveedor de servicios](shutting-down-a-service-provider.md)

