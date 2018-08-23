---
title: Guardar las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5125fc8f3e36087a05802c38127a8402ae67d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576305"
---
# <a name="saving-mapi-properties"></a>Guardar las propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchos objetos admiten un modelo de transacción de procesamiento según el cual los cambios realizados en las propiedades no se realizan permanentes hasta que se confirman en un momento posterior. Mientras que los cambios realizados en las propiedades se controlan mediante los métodos [IMAPIProp::SetProps](imapiprop-setprops.md) y [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , el paso de confirmación se controla mediante [IMAPIProp::SaveChanges](imapiprop-savechanges.md). No es hasta después de una llamada satisfactoria a **SaveChanges** que se puede tener acceso a la versión más reciente de propiedades de un objeto. 
  
Cuando **SaveChanges** devuelve el valor de error MAPI_E_OBJECT_CHANGED, esto es una advertencia de que otro cliente simultáneamente es confirmar los cambios en el objeto. Es posible, según el proveedor que se implementa correctamente el objeto, para que varios clientes para abrir un objeto llamando a su método **OpenEntry** con el conjunto de marca MAPI_MODIFY, para concederles acceso de lectura y escritura. El objeto que se devuelve desde como una llamada **OpenEntry** es una instantánea de los datos de almacenamiento. Cada intento posterior de cambiar estos datos puede sobrescribir el intento anterior. 
  
Tras recibir MAPI_E_OBJECT_CHANGED de **SaveChanges**, un cliente tiene la opción de: 
  
- Realizar una copia del objeto para contener los cambios.
    
- Realizar otra llamada a **SaveChanges**, especificación FORCE_SAVE. 
    
Llamada a **SaveChanges** con la marca FORCE_SAVE sobrescribe la anterior guardar y hace que los cambios de un cliente permanente. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

