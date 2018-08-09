---
title: Objetos de estado MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818225"
---
# <a name="mapi-status-objects"></a>Objetos de estado MAPI

  
  
**Hace referencia a**: Outlook 
  
Objetos de estado notificar información acerca de los recursos MAPI. Por ejemplo, un proveedor de servicios, el proceso de envío o recepción de MAPI o la libreta de direcciones.
  
Hay un objeto de estado proporcionar información acerca de cada proveedor de servicios individuales en el perfil actual. Es responsable de la implementación de objetos de estado de la libreta de direcciones, el proceso de envío o recepción de MAPI y el subsistema MAPI. El objeto de estado de subsistema proporciona información global. El objeto de estado de la libreta de direcciones integrada proporciona el estado de todos los proveedores de libreta de direcciones operativo actualmente.
  
Cada objeto de estado se incluye en la tabla de estado, una tabla que mantienen MAPI que proporciona a los clientes con toda la información de estado de la sesión. Para obtener más información, vea [Las tablas de estado](status-tables.md). Los clientes pueden tener acceso a un objeto de estado concreto a través de la tabla o, para un proveedor de servicios, a través de su objeto de inicio de sesión. Por ejemplo, para obtener acceso a objetos de estado de un proveedor libreta de direcciones, un cliente puede llamar a **IABLogon::OpenStatusEntry**. Para obtener más información, vea [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Los clientes pueden usar objetos de estado para:
  
- Obtenga información sobre el estado de una sesión.
    
- Supervisar un proveedor de servicios.
    
- Transmisión de mensajes de control.
    
- Ver o cambiar la configuración y el estado de un recurso.
    
Cada objeto de estado implementa la interfaz **IMAPIStatus** . Para obtener más información, vea [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). Sin embargo, no todos los objetos estado es totalmente compatible con cada método **IMAPIStatus** . Debido a que no hay variación en los métodos que son compatibles con un objeto de estado, los clientes necesitan obtener más información acerca de un objeto determinado estado antes de que puedan utilizarla. Objetos de estado necesarios para publicar información acerca de sus características en las tres propiedades siguientes: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obtener más información acerca de cómo implementar un objeto de estado, vea [Implementación de objeto de estado](status-object-implementation.md). Para obtener más información acerca del uso de un objeto de estado, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).
  

