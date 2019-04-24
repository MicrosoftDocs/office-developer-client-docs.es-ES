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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283089"
---
# <a name="saving-mapi-properties"></a>Guardar propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchos objetos admiten un modelo de procesamiento de transacciones en el que los cambios en las propiedades no se hacen permanentes hasta que se confirmen en un momento posterior. Mientras que los cambios en las propiedades se controlan mediante los métodos [IMAPIProp:: SetProps](imapiprop-setprops.md) y [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) , el paso de confirmación se controla mediante [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). No es posible que, después de una llamada correcta a **SaveChanges** , se pueda obtener acceso a la versión más reciente de las propiedades de un objeto. 
  
Cuando **SaveChanges** devuelve el valor de error MAPI_E_OBJECT_CHANGED, se trata de una advertencia de que otro cliente está confirmando simultáneamente los cambios realizados en el objeto. Según el proveedor que implemente el objeto, es posible que varios clientes puedan abrir correctamente un objeto llamando a su método **OpenEntry** con el indicador MAPI_MODIFY, dándole acceso de lectura y escritura. El objeto que se devuelve desde una llamada de **OpenEntry** es una instantánea de los datos de almacenamiento. Cada intento posterior de cambiar estos datos puede sobrescribir el intento anterior. 
  
Al recibir MAPI_E_OBJECT_CHANGED de **SaveChanges**, un cliente tiene la opción de: 
  
- Realice una copia del objeto para que contenga los cambios.
    
- Realice otra llamada a **SaveChanges**, especificando FORCE_SAVE. 
    
La llamada a **SaveChanges** con la marca FORCE_SAVE sobrescribe el guardado anterior y hace permanentes los cambios de un cliente. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

