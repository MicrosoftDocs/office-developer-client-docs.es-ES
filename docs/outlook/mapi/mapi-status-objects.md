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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309537"
---
# <a name="mapi-status-objects"></a>Objetos de estado MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de estado notifican información sobre los recursos MAPI. Por ejemplo, un proveedor de servicios, el proceso de envío y recepción de MAPI o la libreta de direcciones.
  
Hay un objeto status que proporciona información acerca de cada proveedor de servicios individual en el perfil actual. MAPI es responsable de implementar objetos de estado para el subsistema, el proceso de envío y recepción de MAPI y la libreta de direcciones. El objeto de estado de subsistema proporciona información global. El objeto de estado de la libreta de direcciones integrada proporciona el estado de todos los proveedores de la libreta de direcciones actualmente en funcionamiento.
  
Cada objeto status se incluye en la tabla de estado, una tabla que mantiene MAPI y que proporciona a los clientes toda la información de estado de la sesión. Para obtener más información, vea [tablas de estado](status-tables.md). Los clientes pueden tener acceso a un objeto de estado concreto a través de la tabla o, en el caso de un proveedor de servicios, a través de su objeto de inicio de sesión. Por ejemplo, para tener acceso a un objeto de estado de un proveedor de libreta de direcciones, un cliente puede llamar a **IABLogon:: OpenStatusEntry**. Para obtener más información, vea [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).
  
Los clientes pueden usar objetos de estado para:
  
- Obtenga información sobre el estado de una sesión.
    
- Supervisar a un proveedor de servicios.
    
- Controlar la transmisión de mensajes.
    
- Ver o cambiar la configuración y el estado de un recurso.
    
Cada objeto status implementa la interfaz **IMAPIStatus** . Para obtener más información, vea [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). Sin embargo, no todos los objetos status admiten completamente todos los métodos **IMAPIStatus** . Dado que hay variación en los métodos admitidos por un objeto status, los clientes necesitan obtener información sobre un objeto status determinado para poder usarlo. Los objetos de estado son necesarios para publicar información sobre sus características en las siguientes tres propiedades: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obtener más información sobre la implementación de un objeto status, vea status ( [implementación de objetos](status-object-implementation.md)). Para obtener más información acerca del uso de un objeto status, vea [tabla de estado y objetos de estado](status-table-and-status-objects.md).
  

