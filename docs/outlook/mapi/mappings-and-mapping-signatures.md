---
title: Asignaciones y asignación de firmas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 16f192ae816aba2dd0e34a42fba211c3ef70ba47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818296"
---
# <a name="mappings-and-mapping-signatures"></a>Asignaciones y asignación de firmas

  
  
**Se aplica a**: Outlook 
  
Cuando un proveedor de servicios es compatible con las propiedades con nombre, cada conjunto de pares de identificador y el nombre se conoce como una asignación. Proveedores de servicios pueden admitir una asignación o en varios. Que es, un proveedor de almacén de mensajes, por ejemplo, puede implementar los métodos **a GetIDsFromNames** y **GetNamesFromIDs** para todas las de su mensaje, carpeta y objetos de almacén de mensajes para trabajar con una sola lista de nombres y sus correspondientes identificadores. Otro proveedor de almacenamiento de mensaje podría tener una lista de todas las carpetas y los mensajes contenidos dentro de él, o implementar una lista única para cada mensaje y todas las carpetas. Los proveedores de almacén de mensajes que usan una asignación única para todos los mensajes no deben permitir propiedades con nombre que aparezca en sus tablas de contenido de carpeta porque para un nombre de propiedad determinada, el identificador de la propiedad será diferentes de un mensaje a. MAPI se recomienda que los proveedores de mantener simple y operan con una sola lista de todos sus objetos incluidas las tablas. 
  
Para cada asignación, proveedores de servicios deben proporcionar una firma de asignación. Una firma de asignación es un valor binario, suele ser un GUID que identifica de forma exclusiva un conjunto de identificadores de las propiedades y sus nombres correspondientes. Asignación de firmas se almacenan en una propiedad del objeto **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). Proveedores de servicios deben cambiar el valor de su propiedad **PR_MAPPING_SIGNATURE** cada vez que se realiza un cambio en la asignación que representa. Por ejemplo, **PR_MAPPING_SIGNATURE** debe actualizarse si se asigna un nuevo identificador a un nombre o un nombre nuevo y se agrega el par de identificador. 
  
Los clientes de trabajar con las propiedades de objetos con nombre utilice las propiedades de los objetos **PR_MAPPING_SIGNATURE** en las operaciones de comparación y copia. Para comparar los identificadores que pertenecen a dos objetos, los clientes que no utilizan firmas de asignación deben llamar a [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) en ambos objetos para recuperar los nombres de cada uno de los identificadores de propiedad con nombre. Uso de las firmas de asignación de objetos, esta llamada puede representar innecesarios. Cuando dos objetos tienen el mismo valor para sus propiedades **PR_MAPPING_SIGNATURE** , usan la misma asignación. Se pueden comparar directamente identificadores que usan la misma asignación. Proveedores de servicios que implementan [IMAPIProp::CopyTo](imapiprop-copyto.md) y [IMAPIProp::CopyProps](imapiprop-copyprops.md) también pueden aprovechar las ventajas de firma de asignación de un objeto. Al copiar las propiedades entre objetos con nombre, los proveedores de servicios pueden evitar el paso de conversión cuando los objetos de origen y de destino tienen la misma firma de asignación. 
  
## <a name="see-also"></a>Ver también



[IMAPIProp: IUnknown](imapipropiunknown.md)


[Con el nombre de las propiedades de MAPI](mapi-named-properties.md)

