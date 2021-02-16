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
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339203"
---
# <a name="shutting-down-a-message-store-provider"></a>Apagar un proveedor de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si su proveedor es un proveedor de almacenamiento de mensajes, puede apagarse de una de las siguientes maneras:
  
- Cuando un cliente o la cola MAPI llama a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). El cierre de un proveedor de almacén de mensajes **con StoreLogoff** hace que el apagado se produzca de forma ordenada y controlada. 
    
- Cuando un cliente llama [a IMAPISession::Logoff](imapisession-logoff.md). 
    
La implementación de **IMsgStore::StoreLogoff** debe comenzar llamando a [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar a MAPI de que se está apagando, lo que indica que se debe cerrar la sesión de los proveedores de transporte relacionados. Cuando **se devuelve IMsgStore::StoreLogoff,** el autor de la llamada invoca el método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del almacén de mensajes. Implemente **este método Release** llamando al método **IUnknown::Release del** objeto de soporte técnico. 
  
MAPI realiza las siguientes tareas en su implementación de **IUnknown::Release para** almacenes de mensajes: 
  
1. Quita todas las estructuras [MAPIUID](mapiuid.md) registradas por el proveedor de almacenamiento de mensajes. 
    
2. Quita la fila del proveedor del almacén de mensajes de la tabla de estado.
    
3. Llama [a IMSLogon::Logoff](imslogon-logoff.md) para liberar todos los objetos abiertos, subobjetos y objetos de estado. 
    
4. Llama [a IUnknown::Release para](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) liberar el objeto de inicio de sesión del proveedor del almacén de mensajes. 
    
Algunos clientes pueden omitir la llamada a **IMsgStore::StoreLogoff,** iniciando el apagado del proveedor del almacén de mensajes con la llamada al método **IUnknown::Release** del almacén de mensajes. Un apagado en estas circunstancias sin la llamada a **StoreLogoff** es menos ordenado y controlado. Escriba el método **Release** del almacén de mensajes para controlar esta posibilidad y realizar un seguimiento de si se ha producido o no una llamada a **IMAPISupport::StoreLogoffTransports.** **Se debe llamar a StoreLogoffTransports** una vez durante el proceso de apagado. Si detectas en el **método Release** que aún no se ha llamado a **StoreLogoffTransports,** invoquelo con la LOGOFF_ABORT local. 
  
## <a name="see-also"></a>Consulte también



[Apagar un proveedor de servicios](shutting-down-a-service-provider.md)

