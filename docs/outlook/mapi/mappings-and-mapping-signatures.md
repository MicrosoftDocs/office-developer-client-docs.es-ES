---
title: Asignaciones y firmas de asignación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410017"
---
# <a name="mappings-and-mapping-signatures"></a>Asignaciones y firmas de asignación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un proveedor de servicios admite propiedades con nombre, cada conjunto de pares de identificadores y nombres se denomina asignación. Los proveedores de servicios pueden admitir una asignación o varias. Es decir, un proveedor de almacén de mensajes, por ejemplo, puede implementar los **métodos GetIDsFromNames** y **GetNamesFromIDs** para que todos sus objetos de almacén de mensajes, carpetas y mensajes funcionen con una única lista de nombres y sus identificadores correspondientes. Otro proveedor de almacén de mensajes puede tener una lista para cada carpeta y los mensajes contenidos en ella, o bien implementar una lista única para cada mensaje y cada carpeta. Los proveedores de almacén de mensajes que usan una asignación única para cada mensaje no deben permitir que las propiedades con nombre aparezcan en las tablas de contenido de la carpeta porque para un nombre de propiedad determinado, el identificador de la propiedad variará de un mensaje a otro. MAPI recomienda que los proveedores lo mantengan sencillo y funcionen con una lista única para todos sus objetos, incluidas las tablas. 
  
Para cada asignación, los proveedores de servicios deben proporcionar una firma de asignación. Una firma de asignación es un valor binario, normalmente un GUID, que identifica de forma única un conjunto de identificadores de propiedad y sus nombres correspondientes. Las firmas de asignación se almacenan en la propiedad **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de un objeto. Los proveedores de servicios deben cambiar el valor de **su propiedad PR_MAPPING_SIGNATURE** cada vez que se realiza un cambio en la asignación que representa. Por ejemplo, **PR_MAPPING_SIGNATURE** debe actualizarse si se asigna un nuevo identificador a un nombre o se agrega un nuevo par de nombre e identificador. 
  
Los clientes que trabajan con las propiedades con nombre de los objetos usan las propiedades **PR_MAPPING_SIGNATURE** de los objetos en comparación y operaciones de copia. Para comparar los identificadores de propiedad con nombre que pertenecen a dos objetos, los clientes que no usan firmas de asignación deben llamar a [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) en ambos objetos para recuperar los nombres de cada uno de los identificadores. El uso de las firmas de asignación de objetos puede hacer innecesaria esta llamada. Cuando dos objetos tienen el mismo valor para **sus PR_MAPPING_SIGNATURE,** usan la misma asignación. Los identificadores que usan la misma asignación se pueden comparar directamente. Los proveedores de servicios que implementan [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md) también pueden aprovechar la firma de asignación de un objeto. Al copiar propiedades con nombre entre objetos, los proveedores de servicios pueden evitar el paso de conversión cuando los objetos de origen y de destino tienen la misma firma de asignación. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)


[Propiedades con nombre MAPI](mapi-named-properties.md)

