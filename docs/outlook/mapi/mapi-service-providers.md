---
title: Proveedores de servicios MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409541"
---
# <a name="mapi-service-providers"></a>Proveedores de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay tres tipos comunes de proveedores de servicios:
  
- Proveedores de libretas de direcciones.
    
- Proveedores de al almacenamiento de mensajes.
    
- Proveedores de transporte.
    
Los proveedores de libreta de direcciones y almacén de mensajes tienen muchas similitudes. Registran un identificador único con MAPI que usan para crear identificadores de entrada para sus objetos. Proporcionan una jerarquía de objetos y propiedades a los que los clientes pueden tener acceso y manipular. Para sus objetos contenedor, admiten una tabla de jerarquía y una tabla de contenido. Admiten la notificación de eventos en estas tablas y, opcionalmente, en objetos individuales para que los clientes puedan recibir información sobre los cambios que se producen durante la sesión. Cuando las operaciones se hacen largas, pueden mostrar un indicador de progreso para informar al usuario del estado de la operación. Los clientes pueden comunicarse con proveedores de libretas de direcciones y de almacén de mensajes indirectamente a través de MAPI mediante el uso de las interfaces [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession : IUnknown](imapisessioniunknown.md) o directamente mediante una de las interfaces del proveedor de servicios de la tabla siguiente. 
  
|**Interfaces de proveedor de libreta de direcciones**|**Interfaces de proveedor de almacenamiento de mensajes**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Los proveedores de transporte difieren de los proveedores de libreta de direcciones y almacén de mensajes en la forma en que se comunican con MAPI y con los clientes. Normalmente, los proveedores de transporte esperan a que MAPI les pida información en lugar de iniciar la comunicación. A diferencia de los demás proveedores, los proveedores de transporte no admiten una variedad de objetos y tablas a los que los clientes tienen acceso habitualmente. Sin embargo, admiten un objeto de estado, al igual que todos los proveedores de servicios, y publican sus propiedades en la tabla de estado. Mientras que los proveedores de libreta de direcciones y almacén de mensajes llaman al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores únicos para crear sus identificadores de entrada, los proveedores de transporte llaman al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para registrar identificadores únicos, así como tipos de dirección para asumir la responsabilidad de la entrega de mensajes concretos. 
  
El proveedor de servicios debe tener tres archivos de encabezado: un archivo de encabezado público y dos archivos internos. Use el archivo de encabezado público para la configuración y para documentar las propiedades y sus valores. Incluir en uno de los archivos de encabezado internos todos los encabezados MAPI públicos necesarios; este archivo de encabezado debe incluirse en todos los archivos de origen del proveedor de servicios. Use el otro archivo interno para definir identificadores de recursos.
  
La libreta de direcciones, el almacén de mensajes y los proveedores de transporte realizan las siguientes tareas:
  
- Proporcionar una función de punto de entrada. 
    
- Proporcionar un proveedor y un objeto de inicio de sesión para controlar el inicio de sesión y la inicialización. 
    
- Si el proveedor pertenece a un servicio de mensajes, proporcione una función de punto de entrada del servicio de mensajes. 
    
- Admitir la configuración mediante la implementación de una hoja de propiedades.
    
- Implementar un objeto de estado y admitir la tabla de estado. 
    
- Controla el apagado.
    
## <a name="see-also"></a>Consulte también



[Conceptos de MAPI](mapi-concepts.md)

