---
title: Implementación de la tabla de visualización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339952"
---
# <a name="display-table-implementation"></a>Implementación de la tabla de visualización

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de presentación se usa para mostrar una hoja de propiedades, un cuadro de diálogo especial compuesto por una o más páginas de propiedades con fichas dedicadas a mostrar y posiblemente editar una o más propiedades. Una tabla de visualización asociada a cada tabla de presentación es una implementación de [IAttach: IMAPIProp](iattachimapiprop.md) . La implementación de [IMAPIProp](imapipropiunknown.md) mantiene los datos de propiedad que se presentan en la hoja de propiedades. 
  
Las filas de una tabla de presentación representan los controles en la hoja de propiedades. La mayoría de los controles se pueden asociar con propiedades mantenidas con la implementación de **IMAPIProp** . Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Las columnas de una tabla de presentación representan propiedades del control, como su posición en la hoja de propiedades, su tipo, estructura asociada e identificador. Para obtener una lista completa de las columnas de la tabla de visualización necesarias, consulte [Display tables](display-tables.md).
  
MAPI muestra una hoja de propiedades al usuario de una aplicación cliente mediante la lectura de valores de propiedad de la implementación de **IMAPIProp** asociada con la tabla de presentación o de la tabla de presentación directamente. A medida que el usuario trabaja con la hoja de propiedades, cambiando valores en los controles, las llamadas MAPI [IMAPIProp:: SetProps](imapiprop-setprops.md) para guardar un control modificado si está establecida la marca DT_SET_IMMEDIATE del control. Para los controles sin la marca DT_SET_IMMEDIATE establecida, los cambios en las propiedades se guardan cuando el usuario cierra el cuadro de diálogo haciendo clic en el botón **Aceptar** o **aplicar ahora** . Cuando se hace clic en uno de estos botones o en el botón **Cancelar** , MAPI quita la hoja de propiedades de la vista. 
  
MAPI obtiene acceso a la tabla de visualización mediante una llamada al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) en la implementación de **IMAPIProp** y solicitando la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) o la hereda en un llamada que ha realizado a MAPI, como [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).
  
La primera técnica de acceso se usa cuando se solicita a los proveedores de la libreta de direcciones que muestren detalles sobre los usuarios de mensajería o las listas de distribución. Se produce el siguiente procesamiento:
  
1. Un cliente llama al método [IAddrBook::D etails](iaddrbook-details.md) . 
    
2. MAPI llama al método [IABLogon:: OpenEntry](iablogon-openentry.md) del proveedor de la libreta de direcciones para obtener acceso al usuario de mensajería que representa la entrada seleccionada. 
    
3. MAPI llama al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del usuario de mensajería para recuperar la propiedad **PR_DETAILS_TABLE** , la tabla de presentación del cuadro de diálogo Detalles. 
    
4. MAPI muestra el cuadro de diálogo, controla la interacción del usuario con la información y lo quita cuando el usuario ha finalizado. 
    
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

