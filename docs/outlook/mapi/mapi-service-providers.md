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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346679"
---
# <a name="mapi-service-providers"></a>Proveedores de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay tres tipos comunes de proveedores de servicios:
  
- Proveedores de libretas de direcciones.
    
- Proveedores de almacenamiento de mensajes.
    
- Proveedores de transporte.
    
La libreta de direcciones y los proveedores de almacenamiento de mensajes tienen muchas similitudes. Registran un identificador único con MAPI que usan para crear identificadores de entrada para sus objetos. Proporcionan una jerarquía de objetos y propiedades a las que los clientes pueden tener acceso y manipular. Para sus objetos container, admiten una tabla de jerarquía y una tabla de contenido. Admiten la notificación de eventos en estas tablas y, opcionalmente, en objetos individuales para que se pueda informar a los clientes de los cambios que se producen durante la sesión. Cuando las operaciones se convierten en largas, pueden mostrar un indicador de progreso para informar al usuario del estado de la operación. Los clientes pueden comunicarse con los proveedores de almacenamiento de mensajes y la libreta de direcciones indirectamente a través de MAPI mediante el uso de las interfaces [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) y [IMAPISession: IUnknown](imapisessioniunknown.md) o directamente mediante una de las interfaces del proveedor de servicios en el siguiente tabla. 
  
|**Interfaces del proveedor de libreta de direcciones**|**Interfaces de proveedor de almacén de mensajes**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Los proveedores de transporte difieren de la libreta de direcciones y los proveedores de almacenamiento de mensajes en la forma en que se comunican con MAPI y con los clientes. Los proveedores de transporte suelen esperar a que MAPI les pida información en lugar de iniciar la comunicación. A diferencia de los demás proveedores, los proveedores de transporte no admiten una variedad de objetos y tablas a los que los clientes acceden con frecuencia. Sin embargo, admiten un objeto de estado, al igual que todos los proveedores de servicios, y publican sus propiedades en la tabla de estado. Mientras que la libreta de direcciones y los proveedores de almacenamiento de mensajes llaman al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores únicos para construir sus identificadores de entrada, los proveedores de transporte llaman al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para Registre identificadores únicos, así como tipos de direcciones para asumir la responsabilidad de la entrega de mensajes concretos. 
  
El proveedor de servicios debe tener tres archivos de encabezado: un archivo de encabezado público y dos archivos internos. Use el archivo de encabezado público para la configuración y documentar las propiedades y sus valores. Incluya en uno de los archivos de encabezado internos todos los encabezados MAPI públicos necesarios; este archivo de encabezado debe incluirse en todos los archivos de origen del proveedor de servicios. Use el otro archivo interno para definir los identificadores de recursos.
  
La libreta de direcciones, el almacén de mensajes y los proveedores de transporte realizan las siguientes tareas:
  
- Proporcione una función de punto de entrada. 
    
- Proporcione un proveedor y un objeto de inicio de sesión para controlar el inicio de sesión y la inicialización. 
    
- Si el proveedor pertenece a un servicio de mensajes, suministre una función de punto de entrada del servicio de mensajes. 
    
- Admite la configuración mediante la implementación de una hoja de propiedades.
    
- Implemente un objeto de estado y admita la tabla de estado. 
    
- Controlar el cierre.
    
## <a name="see-also"></a>Vea también



[Conceptos de MAPI](mapi-concepts.md)

