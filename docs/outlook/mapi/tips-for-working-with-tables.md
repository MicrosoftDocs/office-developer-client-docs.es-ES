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
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439740"
---
# <a name="tips-for-working-with-tables"></a>Sugerencias para trabajar con tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trabajar con una tabla MAPI es algo parecido a trabajar con una tabla de base de datos relacional. Un usuario puede limitar el número de filas y columnas en la vista y especificar su orden. Las filas se pueden recuperar de una en una o en grupos. Un cursor que realiza un seguimiento de la posición actual se puede mover a un lugar específico de la tabla. 
  
Para trabajar con tablas, los clientes usan la interfaz de solo lectura, [IMAPITable : IUnknown](imapitableiunknown.md), mientras que los proveedores de servicios, en función de si son propietarios de los datos en los que se basa la tabla, pueden usar **IMAPITable** o [ITableData : IUnknown](itabledataiunknown.md). Las operaciones definidas en estas interfaces se pueden clasificar como operaciones que todos los usuarios de tablas pueden invocar o que no se usan tanto porque son más avanzadas. Algunas de las operaciones avanzadas son más complejas de implementar; otros ya no son más complejos, pero son de interés para una pequeña mayoría de componentes MAPI. 
  
Las operaciones más comunes son:
  
- Operaciones de columna, que afectan a una sola columna. Entre ellas se incluyen la especificación de las propiedades que se incluirán en el conjunto de columnas y el orden en que deben incluirse.
    
- Operaciones de fila, que afectan a una sola fila. Entre ellas se incluyen la recuperación de datos y las operaciones de mantenimiento: agregar, eliminar y modificar una sola fila o filas.
    
- Operaciones globales, que afectan a toda la tabla. Entre ellas se incluyen la notificación de eventos, la búsqueda y la ordenación.
    
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

