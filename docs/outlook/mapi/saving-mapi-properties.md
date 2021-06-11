---
title: Guardar propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425893"
---
# <a name="saving-mapi-properties"></a>Guardar propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchos objetos admiten un modelo de procesamiento de transacciones por el que los cambios en las propiedades no se realizan de forma permanente hasta que se confirman más adelante. Mientras que los cambios en las propiedades los controlan los [métodos IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) [IMAPIProp::SaveChanges](imapiprop-savechanges.md)controla el paso de confirmación. No es hasta después de una llamada correcta a **SaveChanges** a la que se puede tener acceso a la versión más reciente de las propiedades de un objeto. 
  
Cuando **SaveChanges** devuelve el valor de error MAPI_E_OBJECT_CHANGED, se trata de una advertencia de que otro cliente está confirmando simultáneamente cambios en el objeto. Es posible, según el proveedor que implemente el objeto, que varios clientes abran correctamente un objeto llamando a su método **OpenEntry** con el conjunto de marcas MAPI_MODIFY, lo que les proporciona acceso de lectura y escritura. El objeto que se devuelve de una llamada **OpenEntry** de este tipo es una instantánea de los datos de almacenamiento. Cada intento posterior de cambiar estos datos puede sobrescribir el intento anterior. 
  
Al recibir MAPI_E_OBJECT_CHANGED **de SaveChanges,** un cliente tiene la opción de: 
  
- Realice una copia del objeto para contener los cambios.
    
- Realice otra llamada a **SaveChanges,** especificando FORCE_SAVE. 
    
Al llamar a **SaveChanges** con FORCE_SAVE marca sobrescribe el guardado anterior y hace que los cambios de un cliente se realicen de forma permanente. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

