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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327800"
---
# <a name="tips-for-better-table-performance"></a>Sugerencias para mejorar el rendimiento de tabla
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Debido a que muchas de las operaciones de tabla pueden llevar mucho tiempo y no hay forma de indicar el progreso, es útil usar las siguientes técnicas para mejorar el rendimiento:
  
- **Realizar el método [IMAPITable:](imapitableiunknown.md) las llamadas a IUnknown en el orden correcto**
    
   Los clientes y los proveedores de servicios pueden trabajar con tablas de varias formas. Pueden abrir la tabla y recuperar los datos de todas las filas con el conjunto de columnas y el criterio de ordenación predeterminados. Como alternativa, pueden modificar esta vista predeterminada de la tabla cambiando el conjunto de columnas, cambiando el criterio de ordenación o estableciendo una restricción para restringir el ámbito de la tabla. Las tablas que los usuarios intentan realizar una o varias de estas operaciones antes de recuperar los datos deben realizarse en el orden siguiente:
    
    1. Defina un conjunto de columnas con [IMAPITable:: SetColumns](imapitable-setcolumns.md).
        
    2. Establezca una restricción con el [IMAPITable:: Restrict](imapitable-restrict.md).
        
    3. Definir un criterio de ordenación con [IMAPITable:: SortTable](imapitable-sorttable.md).
    
    La realización de estas tareas en este orden limita el número de filas y columnas que se van a ordenar, lo que mejora el rendimiento.
    
- **ReTrasar una operación mediante la marca TBL_BATCH, si es posible**
    
    Si se establece\_la marca de lote de tbl en un método, el implementador de tablas puede recopilar varias llamadas antes de actuar en una de ellas. En lugar de realizar potencialmente muchas llamadas a un servidor remoto; un implementador de tablas puede realizar uno, realizando todas las operaciones al mismo tiempo. Los resultados de las operaciones no se evalúan hasta que se necesitan. 
    
    Por ejemplo, cuando un cliente llama a [IMAPITable:: Restrict](imapitable-restrict.md) para especificar una restricción con el\_indicador de lote de tbl, la restricción no tiene que entrar en vigor hasta que el cliente llame a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos. Esto permite que el implementador de tablas Combine el trabajo de dos llamadas en una. Los usuarios de la tabla que se beneficien de la marca de lote de TBL\_deben tener en cuenta que el control de errores en estas condiciones puede ser más complejo. 
    
    Como controlar los errores de una operación retrasada es similar a controlar los errores cuando se\_establece la marca MAPI DEFERRED_ERRORS, vea difiriendo [MAPI Errors](deferring-mapi-errors.md) para obtener más información. 
    
- **Mantener una caché de las propiedades más usadas**
    
    Los proveedores de servicios que implementan tablas pueden reducir el tiempo que se tarda en crear una vista mediante el almacenamiento en caché de las propiedades de objeto usadas con más frecuencia. Al mantener una copia de estas propiedades en la memoria, se evita tener que recuperarlas del objeto cada vez que se debe volver a crear la vista.
    
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

