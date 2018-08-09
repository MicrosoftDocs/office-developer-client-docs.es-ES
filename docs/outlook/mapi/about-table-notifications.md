---
title: Información sobre las notificaciones de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816360"
---
# <a name="about-table-notifications"></a>Información sobre las notificaciones de tabla

  
  
**Hace referencia a**: Outlook 
  
Los clientes a menudo se basan en las notificaciones de tabla para obtener más información de los cambios a objetos en lugar de registrar para recibir notificaciones directamente desde los objetos. Los cambios más frecuentes que impedir que se envíen notificaciones incluyen la adición, eliminación o modificación de una fila y cualquier error crítico. Cuando se reciben las notificaciones, los clientes pueden determinar si debe realizar otra llamada a volver a cargar en la tabla. 
  
Debido a que las notificaciones de tabla son asincrónicas, hay algunos problemas que pueden hacer que las notificaciones de tratamiento de menos de un proceso sencillo:
  
- Los datos que se pasan en la estructura [TABLE_NOTIFICATION](table_notification.md) no es posible que representan el estado más reciente de la tabla. Por ejemplo, un cliente podría realizar un cambio en un mensaje y, a continuación, decida eliminarla. El proveedor de almacenamiento de mensaje implementación de la tabla de contenido que incluye el mensaje envía dos notificaciones: un evento TABLE_ROW_MODIFIED seguido de un evento TABLE_ROW_DELETED. Dependiendo de cómo el proveedor de almacenamiento de mensaje veces las notificaciones, el cliente podría recibir la notificación TABLE_ROW_MODIFIED después de la eliminación de la fila. 
    
- El conjunto incluye con una notificación de columnas pueden ser diferente del conjunto actual de columna de la tabla. MAPI requiere que el conjunto de columnas de notificación coinciden con el conjunto de columnas que estaba en efecto en el momento en que se generó la notificación. Debido a que es posible que un cliente pueda llamar a [IMAPITable::SetColumns](imapitable-setcolumns.md) para modificar la columna establecer en cualquier momento, incluso después de una notificación: no se pueden sincronizar los conjuntos de dos columnas. 
    
- Tabla solo se envían para las filas que forman parte de la vista. Es decir, si una fila se excluye de la vista debido a una restricción o porque la tabla está en un estado contraído, no se enviarán ninguna notificación si cambia de esa fila. Además, no se envían a informar a un cliente sobre un cambio en el estado de la categoría.
    
Los clientes deben tener en cuenta que no todas las tablas admiten la notificación TABLE_SORT_DONE y deben estar preparadas para controlar esta condición por:
  
1. Forzar la ordenación ser sincrónico.
    
2. Volver a cargar las filas de la tabla cuando [SortTable](imapitable-sorttable.md) devuelve. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

