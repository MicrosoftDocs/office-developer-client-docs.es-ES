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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321843"
---
# <a name="about-table-notifications"></a>Acerca de las notificaciones de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes suelen basarse en las notificaciones de tabla para obtener información sobre los cambios en los objetos en lugar de registrarse para recibir notificaciones directamente de los objetos. Los cambios típicos que provocan que se envíen las notificaciones son la adición, la eliminación o la modificación de una fila y cualquier error crítico. Cuando llegan las notificaciones, los clientes pueden determinar si hacen otra llamada para volver a cargar la tabla. 
  
Como las notificaciones de tabla son asincrónicas, hay algunos problemas que pueden hacer que las notificaciones de control sean menos que sencillas:
  
- Es posible que los datos pasados en la estructura [TABLE_NOTIFICATION](table_notification.md) no representen el estado más actual de la tabla. Por ejemplo, es posible que un cliente realice un cambio en un mensaje y, a continuación, decida eliminarlo. El proveedor de almacenamiento de mensajes que implementa la tabla de contenido que incluye el mensaje envía dos notificaciones: un evento TABLE_ROW_MODIFIED seguido de un evento TABLE_ROW_DELETED. Según el modo en que el proveedor de almacenamiento de mensajes multiplica las notificaciones, es posible que el cliente reciba la notificación TABLE_ROW_MODIFIED después de eliminar la fila. 
    
- El conjunto de columnas incluido en una notificación podría ser diferente al conjunto de columnas actual de la tabla. MAPI requiere que el conjunto de columnas de notificación se ajuste a la columna que estaba en vigor en el momento en que se generó la notificación. Debido a que es posible que un cliente llame a [IMAPITable:: SetColumns](imapitable-setcolumns.md) para alterar el conjunto de columnas en cualquier momento, incluso después de una notificación, es posible que los dos conjuntos de columnas no se sincronicen. 
    
- Las notificaciones de tabla solo se envían para las filas que forman parte de la vista. Es decir, si una fila se excluye de la vista debido a una restricción o porque la tabla está en estado contraído, no se enviará ninguna notificación si la fila cambia. Además, no se envía ninguna notificación para informar a un cliente sobre un cambio en el estado de la categoría.
    
Los clientes deben tener en cuenta que no todas las tablas admiten la notificación TABLE_SORT_DONE y deben estar preparadas para controlar esta condición:
  
1. Obligar a la ordenación a ser sincrónica.
    
2. Volver a cargar las filas de la tabla cuando se devuelve [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

