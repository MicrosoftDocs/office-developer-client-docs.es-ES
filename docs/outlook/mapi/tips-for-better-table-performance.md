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
ms.openlocfilehash: da49b4d8251f6b0b69d2ffbf80194943215675e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564167"
---
# <a name="tips-for-better-table-performance"></a>Sugerencias para mejorar el rendimiento de tabla
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Debido a que muchas de las operaciones de tabla pueden llevar mucho tiempo y no hay ninguna manera de indicar el progreso, es útil usar las siguientes técnicas para mejorar el rendimiento:
  
- **Realizar [IMAPITable: IUnknown](imapitableiunknown.md) llama en el orden correcto**
    
   Los clientes y proveedores de servicios pueden trabajar con tablas en una variedad de formas. Puede abrir la tabla y recuperar los datos para todas las filas con el conjunto de columnas predeterminado y criterio de ordenación. Como alternativa, se puede modificar esta vista predeterminada de la tabla para cambiar el conjunto de columnas, cambiar el criterio de ordenación o establecer una restricción para limitar el ámbito de la tabla. Los usuarios de la tabla que se van a realizar una o varias de estas operaciones antes de recuperar los datos deben realizarlas en el orden siguiente:
    
    1. Definir una columna establecida con [IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Establecer una restricción con [IMAPITable:: Restrict](imapitable-restrict.md).
        
    3. Definir un criterio de ordenación con [SortTable](imapitable-sorttable.md).
    
    Llevar a cabo estas tareas en este orden, limita el número de filas y columnas que se va a ordenar, lo que mejora el rendimiento.
    
- **Retraso de una operación utilizando la marca TBL_BATCH si es posible**
    
    Establecer el TBL\_indicador de lote en un método permite al implementador tabla recopilar varias llamadas antes de actuar en uno de ellos. En lugar de realizar potencialmente muchas llamadas a un servidor remoto; un implementador de la tabla uno, puede hacer que realizan todas las operaciones a la vez. Los resultados de las operaciones no se evalúan hasta que sean necesarios. 
    
    Por ejemplo, cuando un cliente llama a [IMAPITable:: Restrict](imapitable-restrict.md) para especificar una restricción con el TBL\_por lotes indicador establecido, la restricción no es necesario que entran en efecto hasta que el cliente llama [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos. Esto permite que el implementador de tabla combinar el trabajo de dos llamadas en uno. La tabla de usuarios que permite aprovechar el TBL\_marca por lotes debe tener en cuenta que los errores en las siguientes condiciones pueden ser más complejo. 
    
    Debido a que controla los errores de una operación retrasada es similar a la gestión de los errores cuando el MAPI\_se establece la marca DEFERRED_ERRORS, consulte [Aplazamiento de errores de MAPI](deferring-mapi-errors.md) para obtener más información. 
    
- **Mantener una memoria caché de propiedades usadas con más frecuencia**
    
    Proveedores de servicios de implementación de las tablas pueden reducir el tiempo necesario para crear una vista mediante el almacenamiento en memoria caché copias de las propiedades del objeto usados con más frecuencia. Es necesario recompilar conservar una copia de estas propiedades en ahorra memoria tener que recuperar desde el objeto cada vez que la vista.
    
## <a name="see-also"></a>Recursos adicionales

- [Tablas MAPI](mapi-tables.md)

