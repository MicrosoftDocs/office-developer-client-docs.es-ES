---
title: Implementación de tabla para mostrar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435267"
---
# <a name="display-table-implementation"></a>Implementación de tabla para mostrar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla para mostrar se usa para mostrar una hoja de propiedades, un cuadro de diálogo especial compuesto por una o más páginas de propiedades con pestañas dedicadas a mostrar y, posiblemente, editar una o más propiedades. Asociado a cada tabla para mostrar se encuentra una [implementación de interfaz IAttach : IMAPIProp.](iattachimapiprop.md) La [implementación de IMAPIProp](imapipropiunknown.md) mantiene los datos de propiedad que se presentan en la hoja de propiedades. 
  
Las filas de una tabla para mostrar representan los controles de la hoja de propiedades. La mayoría de los controles se pueden asociar con propiedades mantenidas con la **implementación de IMAPIProp.** Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Las columnas de una tabla para mostrar representan propiedades del control, como su posición en la hoja de propiedades, su tipo, estructura asociada e identificador. Para obtener una lista completa de las columnas de tabla para mostrar necesarias, vea [Mostrar tablas](display-tables.md).
  
MAPI muestra una hoja de propiedades al usuario de una aplicación cliente al leer los valores de propiedad de la **implementación IMAPIProp** asociada a la tabla para mostrar o directamente desde la tabla para mostrar. A medida que el usuario trabaja con la hoja de propiedades, cambiando los valores de los controles, MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para guardar un control modificado si se establece la marca de DT_SET_IMMEDIATE del control. Para los controles sin el conjunto DT_SET_IMMEDIATE marca, los cambios en las propiedades se guardan cuando el usuario descarta el cuadro de diálogo haciendo clic en **el botón Aceptar** o **Aplicar** ahora. Cuando se hace clic  en cualquiera de estos botones o en el botón Cancelar, MAPI quita la hoja de propiedades de la vista. 
  
MAPI obtiene acceso a la tabla para mostrar llamando al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en la implementación **imapiprop** y solicitando la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) o heredando en una llamada realizada a MAPI, como [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
La primera técnica de acceso se usa cuando se pide a los proveedores de libretas de direcciones que muestren detalles sobre los usuarios de mensajería o las listas de distribución. Se produce el siguiente procesamiento:
  
1. Un cliente llama al [método IAddrBook::D etails.](iaddrbook-details.md) 
    
2. MAPI llama al método [IABLogon::OpenEntry](iablogon-openentry.md) del proveedor de libreta de direcciones para obtener acceso al usuario de mensajería que representa la entrada seleccionada. 
    
3. MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del usuario de mensajería para recuperar la propiedad **PR_DETAILS_TABLE,** la tabla para mostrar del cuadro de diálogo detalles. 
    
4. MAPI muestra el cuadro de diálogo, controlando la interacción del usuario con la información y la quita cuando el usuario ha terminado. 
    
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

