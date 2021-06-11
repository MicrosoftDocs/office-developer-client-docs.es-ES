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
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406748"
---
# <a name="mapi-status-objects"></a>Objetos de estado MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de estado informan sobre los recursos MAPI. Por ejemplo, un proveedor de servicios, el proceso de envío y recepción MAPI o la libreta de direcciones.
  
Hay un objeto de estado que proporciona información sobre cada proveedor de servicios individual en el perfil actual. MAPI es responsable de implementar objetos de estado para el subsistema, el proceso de envío y recepción MAPI y la libreta de direcciones. El objeto de estado del subsistema proporciona información global. El objeto status de la libreta de direcciones integrada proporciona el estado de todos los proveedores de libretas de direcciones que están en funcionamiento actualmente.
  
Cada objeto status se incluye en la tabla de estado, una tabla mantenida por MAPI que proporciona a los clientes toda la información de estado de la sesión. Para obtener más información, vea [Tablas de estado](status-tables.md). Los clientes pueden tener acceso a un objeto de estado determinado a través de la tabla o, para un proveedor de servicios, a través de su objeto de inicio de sesión. Por ejemplo, para obtener acceso al objeto de estado de un proveedor de libreta de direcciones, un cliente puede llamar a **IABLogon::OpenStatusEntry**. Para obtener más información, vea [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Los clientes pueden usar objetos de estado para:
  
- Obtenga información sobre el estado de una sesión.
    
- Supervisar un proveedor de servicios.
    
- Controlar la transmisión de mensajes.
    
- Ver o cambiar la configuración y el estado de un recurso.
    
Cada objeto de estado implementa la **interfaz IMAPIStatus.** Para obtener más información, [vea IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). Sin embargo, no todos los objetos de estado admiten completamente **todos los métodos IMAPIStatus.** Dado que hay variaciones en los métodos admitidos por un objeto de estado, los clientes deben obtener información sobre un objeto de estado determinado antes de poder usarlo. Los objetos Status son necesarios para publicar información sobre sus características en las tres propiedades siguientes: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obtener más información acerca de la implementación de un objeto de estado, vea [Status Object Implementation](status-object-implementation.md). Para obtener más información acerca del uso de un objeto de estado, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).
  

