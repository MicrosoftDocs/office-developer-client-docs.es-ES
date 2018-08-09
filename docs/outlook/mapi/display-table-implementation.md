---
title: Implementación de la tabla para mostrar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816675"
---
# <a name="display-table-implementation"></a>Implementación de la tabla para mostrar

  
  
**Hace referencia a**: Outlook 
  
Una tabla para mostrar se usa para mostrar una hoja de propiedades, un cuadro de diálogo especial que se compone de una o más páginas con fichas (propiedad) dedicado a mostrar y, posiblemente, editar una o más propiedades. Asociada con cada para mostrar tabla es un [IAttach: IMAPIProp](iattachimapiprop.md) implementación de la interfaz. La implementación de [IMAPIProp](imapipropiunknown.md) mantiene los datos de propiedad que se presentan en la hoja de propiedades. 
  
Las filas de una tabla para mostrar representan los controles en la hoja de propiedades. La mayoría de los controles se pueden asociados con las propiedades que se mantiene con la implementación de **IMAPIProp** . Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Las columnas de una tabla para mostrar representan las propiedades del control, como su posición en la hoja de propiedades, su tipo, estructura asociada e identificador. Para obtener una lista completa de las columnas de tabla para mostrar necesarios, vea [Mostrar tablas](display-tables.md).
  
MAPI muestra una hoja de propiedades para el usuario de una aplicación cliente mediante la lectura de los valores de propiedad desde la implementación de **IMAPIProp** asociado a la tabla para mostrar o desde la tabla para mostrar directamente. Mientras el usuario trabaja con la hoja de propiedades, cambiar los valores de los controles MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para guardar un control modificado si se establece la marca DT_SET_IMMEDIATE del control. Para los controles sin establecer el indicador DT_SET_IMMEDIATE, se guardan los cambios realizados en las propiedades cuando el usuario cierra el cuadro de diálogo haciendo clic en el botón **Aceptar** o **Aplicar ahora** . Cuando se hace clic en cualquiera de estos botones o el botón **Cancelar** , MAPI quita la hoja de propiedades de la vista. 
  
MAPI obtiene acceso a la tabla para mostrar por llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en la implementación de **IMAPIProp** y solicitar la propiedad de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) o mediante la herencia de un llamada realizados en MAPI, como [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
La primera técnica de acceso se usa cuando los proveedores de la libreta de direcciones se le pida que mostrar detalles acerca de la mensajería a los usuarios o las listas de distribución. Se produce el procesamiento siguiente:
  
1. Un cliente llama al método de [IAddrBook::Details](iaddrbook-details.md) . 
    
2. MAPI llama al método [IABLogon::OpenEntry](iablogon-openentry.md) del proveedor de libreta de direcciones para tener acceso el usuario de mensajería que representa la entrada seleccionada. 
    
3. MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del usuario de mensajería para recuperar la propiedad **PR_DETAILS_TABLE** , en la tabla para mostrar para el cuadro de diálogo detalles. 
    
4. Muestra el cuadro de diálogo, controlar la interacción del usuario con la información MAPI y lo quita cuando el usuario ha terminado. 
    
## <a name="see-also"></a>Vea también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

