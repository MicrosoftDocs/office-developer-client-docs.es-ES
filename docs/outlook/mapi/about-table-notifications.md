---
title: Acerca de las notificaciones de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417955"
---
# <a name="about-table-notifications"></a>Acerca de las notificaciones de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes a menudo dependen de las notificaciones de tabla para obtener información sobre los cambios en los objetos en lugar de registrarse para recibir notificaciones directamente de los objetos. Los cambios típicos que hacen que se envíen notificaciones incluyen la adición, eliminación o modificación de una fila y cualquier error crítico. Cuando llegan las notificaciones, los clientes pueden determinar si se realiza otra llamada para volver a cargar la tabla. 
  
Dado que las notificaciones de tabla son asincrónicas, hay algunos problemas que pueden hacer que el control de notificaciones sea menos sencillo:
  
- Es posible que los datos [pasados TABLE_NOTIFICATION](table_notification.md) estructura no representen el estado más actual de la tabla. Por ejemplo, un cliente puede realizar un cambio en un mensaje y, a continuación, decidir eliminarlo. El proveedor del almacén de mensajes que implementa la tabla de contenido que incluye el mensaje envía dos notificaciones: un evento TABLE_ROW_MODIFIED seguido de un evento TABLE_ROW_DELETED mensaje. Según el modo en que el proveedor del almacén de mensajes recibe notificaciones, es posible que el cliente reciba la notificación TABLE_ROW_MODIFIED después de eliminar la fila. 
    
- El conjunto de columnas incluido con una notificación puede ser diferente del conjunto de columnas actual de la tabla. MAPI requiere que el conjunto de columnas de notificación coincida con el conjunto de columnas que estaba en vigor en el momento en que se generó la notificación. Dado que es posible que un cliente llame a [IMAPITable::SetColumns](imapitable-setcolumns.md) para modificar el conjunto de columnas en cualquier momento (incluso después de una notificación), es posible que los dos conjuntos de columnas no se sincronicen. 
    
- Las notificaciones de tabla solo se envían para las filas que forman parte de la vista. Es decir, si una fila se excluye de la vista debido a una restricción o porque la tabla está en estado contraído, no se enviará ninguna notificación si cambia esa fila. Además, no se envían notificaciones para informar a un cliente sobre un cambio en el estado de categoría.
    
Los clientes deben tener en cuenta que no todas las tablas admiten la notificación TABLE_SORT_DONE y deben estar preparados para controlar esta condición mediante:
  
1. Forzar que la ordenación sea sincrónica.
    
2. Volver a cargar las filas de la tabla [cuando IMAPITable::SortTable](imapitable-sorttable.md) devuelve. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

