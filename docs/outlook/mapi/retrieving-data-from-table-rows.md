---
title: Recuperación de datos de filas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405257"
---
# <a name="retrieving-data-from-table-rows"></a>Recuperación de datos de filas de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recuperar filas de una tabla implica:
  
- Obtener los valores de propiedad de todas las columnas.
    
- Modificar la posición actual.
    
Una de las columnas necesarias en la mayoría de las tablas es un identificador de entrada **( la** propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) que se puede usar para abrir el objeto que representa la fila. Este identificador de entrada suele ser un identificador de entrada a corto plazo, que no persiste más allá de la duración de la tabla. Sin embargo, puede ser un identificador a largo plazo si el proveedor de servicios que implementa la tabla solo admite un tipo de identificador de entrada.
  
Los clientes y proveedores de servicios pueden realizar una de las siguientes llamadas para recuperar filas:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Recupera un número especificado de filas a partir de la fila actual en una dirección hacia delante o hacia atrás.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Recupera todas las filas de una tabla.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera una fila de una tabla según el valor de su columna de índice. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) suele ser la columna de índice de una tabla.  <br/> |
   
Cuando se incluye una propiedad opcional como una de las columnas de una tabla, es posible que algunas de las filas tengan valores válidos para la columna, mientras que otras no. Si existe un valor válido para una columna depende de si el objeto que proporciona la información de la fila establece la propiedad. Según la implementación del objeto, una propiedad inexistente se puede representar en la tabla como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) o un valor arbitrario. Los usuarios de tablas deben tener cuidado de diferenciar entre propiedades que no existen y que tienen valores y propiedades sin sentido que existen y tienen valores válidos. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

