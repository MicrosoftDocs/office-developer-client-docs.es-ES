---
title: Sugerencias para mejorar el rendimiento de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412516"
---
# <a name="tips-for-better-table-performance"></a>Sugerencias para mejorar el rendimiento de tabla
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Dado que muchas de las operaciones de tabla pueden llevar mucho tiempo y no hay forma de indicar el progreso, resulta útil usar las siguientes técnicas para mejorar el rendimiento:
  
- **Realizar [IMAPITable: llamadas IUnknown](imapitableiunknown.md) en el orden correcto**
    
   Los clientes y los proveedores de servicios pueden trabajar con tablas de varias maneras. Pueden abrir la tabla y recuperar los datos de todas las filas mediante el conjunto de columnas predeterminado y el criterio de ordenación. Como alternativa, pueden modificar esta vista predeterminada de la tabla cambiando el conjunto de columnas, cambiando el criterio de ordenación o estableciendo una restricción para restringir el ámbito de la tabla. Los usuarios de tabla que tienen la intención de realizar una o varias de estas operaciones antes de recuperar los datos deben realizarlos en el siguiente orden:
    
    1. Definir un conjunto de columnas [con IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Establecer una restricción con [IMAPITable::Restrict](imapitable-restrict.md).
        
    3. Defina un criterio de ordenación [con IMAPITable::SortTable](imapitable-sorttable.md).
    
    Realizar estas tareas en este orden limita el número de filas y columnas que se ordenarán, lo que mejora el rendimiento.
    
- **Retrasar una operación mediante la marca TBL_BATCH si es posible**
    
    Al establecer la marca TBL BATCH en un método, el implementador de tabla puede recopilar varias llamadas antes de \_ actuar en cualquiera de ellas. En lugar de realizar potencialmente muchas llamadas a un servidor remoto; un implementador de tabla puede realizar una, realizando todas las operaciones a la vez. Los resultados de las operaciones no se evalúan hasta que son necesarias. 
    
    Por ejemplo, cuando un cliente llama a [IMAPITable::Restrict](imapitable-restrict.md) para especificar una restricción con la marca TBL BATCH establecida, la restricción no tiene que entrar en vigor hasta que el cliente llama a \_ [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar los datos. Esto permite al implementador de tabla combinar el trabajo de dos llamadas en una. Los usuarios de tablas que aprovechan la marca TBL BATCH deben ser conscientes de que el control de errores en estas \_ condiciones puede ser más complejo. 
    
    Dado que controlar los errores de una operación retrasada es similar al control de los errores cuando se establece la marca DEFERRED_ERRORS MAPI, vea \_ [Aplazar](deferring-mapi-errors.md) errores MAPI para obtener más información. 
    
- **Conservar una memoria caché de propiedades usadas habitualmente**
    
    Los proveedores de servicios que implementan tablas pueden reducir el tiempo que se tarda en crear una vista almacenando en caché copias de propiedades de objeto de uso común. Mantener una copia de estas propiedades en la memoria ahorra tener que recuperarlas del objeto cada vez que se debe volver a crear la vista.
    
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

