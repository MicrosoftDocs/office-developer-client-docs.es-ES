---
title: Proveedores de servicios de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571909"
---
# <a name="mapi-service-providers"></a>Proveedores de servicios de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay tres tipos comunes de proveedores de servicios:
  
- Los proveedores de libreta de direcciones.
    
- Proveedores de almacén de mensajes.
    
- Los proveedores de transporte.
    
Proveedores de almacén de libreta de direcciones y el mensaje de dirección tienen muchas similitudes. Registrar a un identificador único MAPI que usa para construir los identificadores de entrada para sus objetos. Proporcionan una jerarquía de objetos y propiedades que los clientes pueden obtener acceso y manipular. Para sus objetos del contenedor, que admiten una tabla de jerarquías y una tabla de contenido. Admite la notificación de eventos en estas tablas y, opcionalmente, en los objetos individuales para que los clientes pueden estar informados de los cambios que se producen durante la sesión. Cuando se convierten en operaciones prolongadas, puede mostrar un indicador de progreso para informar al usuario del estado de la operación. Los clientes pueden comunicarse con los proveedores de almacén de libreta de direcciones y el mensaje de dirección puede ser MAPI indirectamente a través mediante el uso de la [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) y [IMAPISession: IUnknown](imapisessioniunknown.md) interfaces o directamente mediante una de las interfaces de proveedor de servicio en el tabla siguiente. 
  
|**Interfaces del proveedor de la libreta de direcciones**|**Interfaces del proveedor de almacén de mensajes**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Los proveedores de transporte difieren de dirección libreta de direcciones y el mensaje de los proveedores de almacén de la manera en que se comunican con MAPI y con los clientes. Los proveedores de transporte normalmente espere de MAPI pedir información en lugar de iniciar la comunicación. A diferencia de los otros proveedores, los proveedores de transporte no admite una gran variedad de objetos y las tablas que se tiene acceso con frecuencia por los clientes. Sin embargo, son compatibles con un objeto de estado, tal y como no todos los proveedores de servicios y publicar sus propiedades en la tabla de estado. Mientras que los proveedores de almacén de libreta de direcciones y el mensaje de dirección llamar al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar los identificadores únicos para construir sus identificadores de entrada, los proveedores de transporte llame al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para Registrar identificadores únicos, así como los tipos de direcciones para que asume la responsabilidad de la entrega de mensajes determinados. 
  
Su proveedor de servicios debe tener tres archivos de encabezado: un archivo de encabezado público y dos archivos internos. Usar el archivo de encabezado pública para la configuración y para documentar las propiedades y sus valores. Incluir en uno de los archivos de encabezado interno todos los los necesarios pública MAPI encabezados; Este archivo de encabezado debe incluirse en todos los archivos de origen del proveedor de servicio. Utilice el otro archivo interno para definir los identificadores de recursos.
  
Libreta de direcciones, almacén de mensajes y los proveedores de transporte realizan las siguientes tareas:
  
- Proporcionar una función de punto de entrada. 
    
- Proporcionar un proveedor y el objeto de inicio de sesión para controlar el inicio de sesión y la inicialización. 
    
- Si el proveedor pertenece a un servicio de mensajes, proporcionar una función de punto de entrada de servicio de mensaje. 
    
- Admite la configuración mediante la implementación de una hoja de propiedades.
    
- Implementar un objeto de estado y admitir la tabla de estado. 
    
- Controlador de apagado.
    
## <a name="see-also"></a>Recursos adicionales



[Conceptos MAPI](mapi-concepts.md)

