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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339651"
---
# <a name="tips-for-working-with-tables"></a>Sugerencias para trabajar con tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trabajar con una tabla MAPI es un poco como trabajar con una tabla de base de datos relacional. Un usuario puede limitar el número de filas y columnas de la vista y especificar su orden. Las filas se pueden recuperar de una en una o en grupos. Un cursor que realiza un seguimiento de la posición actual puede moverse a un lugar específico de la tabla. 
  
Para trabajar con tablas, los clientes usan la interfaz de solo lectura, [IMAPITable: IUnknown](imapitableiunknown.md), mientras que los proveedores de servicios, dependiendo de si son propietarios de los datos en los que se basa la tabla, pueden usar el **IMAPITable** o [ITableData: IUnknown](itabledataiunknown.md). Las operaciones definidas en estas interfaces se pueden clasificar como operaciones que todos los usuarios de tablas realizan o pueden invocar y operaciones que no se usan tan generalizadas porque son más avanzadas. Algunas de las operaciones avanzadas son más complejas de implementar; otras no son más complejas, pero son de interés para una pequeña minoría de componentes MAPI. 
  
Las operaciones más comunes son las siguientes:
  
- Operaciones de columna, que afectan a columnas únicas. Incluyen la especificación de las propiedades que se van a incluir en el conjunto de columnas y el orden en que deben incluirse.
    
- Operaciones de fila que afectan a filas individuales. Entre ellas se incluyen la recuperación de datos y las operaciones de mantenimiento: agregar, eliminar y modificar una fila o filas individuales.
    
- Operaciones globales, que afectan a toda la tabla. Entre estos se incluyen la notificación de eventos, la búsqueda y la ordenación.
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

