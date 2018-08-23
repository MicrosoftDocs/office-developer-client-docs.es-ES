---
title: Sugerencias para trabajar con tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d9b4d6a469904058b0484428dbf20a90119e96bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586140"
---
# <a name="tips-for-working-with-tables"></a>Sugerencias para trabajar con tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trabajar con una MAPI tabla es un poco like trabajar con una tabla de base de datos relacional. Un usuario puede limitar el número de filas y columnas en la vista y especificar su orden. Filas pueden ser recuperado uno a la vez o en grupos. Un cursor que realiza un seguimiento de la posición actual se puede mover a una ubicación específica en la tabla. 
  
Para trabajar con tablas, los clientes usan la interfaz de sólo lectura, [IMAPITable: IUnknown](imapitableiunknown.md), mientras que los proveedores de servicios, dependiendo de si son propietarios de los datos que se basa en la tabla, pueden usar cualquier **IMAPITable** o [ITableData: IUnknown](itabledataiunknown.md). Las operaciones definidas en estas interfaces se pueden clasificar como operaciones que o pueden invocar todos los usuarios de las tablas y las operaciones que no se utilizan como ampliamente porque más avanzadas. Algunas de las operaciones avanzadas son más complejas de implementar; otros usuarios no más complejas, pero son de interés para una minoría de componentes MAPI. 
  
Las operaciones más comunes son:
  
- Operaciones de columna, que afectan a columnas individuales. Éstas incluyen la especificación de las propiedades que se deben incluir en el conjunto de columnas y el orden en el que se deben incluir.
    
- Operaciones de fila, que afectan a filas individuales. Entre estas incluyen la recuperación de datos y las operaciones de mantenimiento: adición, eliminación y modificación de una sola fila o las filas.
    
- Operaciones globales que afectan a toda la tabla. Éstas incluyen la notificación de eventos, búsqueda y la ordenación.
    
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

