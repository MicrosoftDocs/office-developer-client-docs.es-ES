---
title: Información sobre las restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816361"
---
# <a name="about-restrictions"></a>Información sobre las restricciones

  
  
**Hace referencia a**: Outlook 
  
Una restricción es una forma de limitar el número de filas en una vista para sólo las filas con los valores de las columnas que coincidan con criterios específicos. Hay muchas oportunidades diferentes para el uso de restricciones con tablas. Las aplicaciones de cliente pueden usar restricciones, por ejemplo, para filtrar una tabla de contenido para los mensajes enviados por una persona específica, para buscar las filas que no son compatibles con una propiedad o han establecido una propiedad en un valor específico o para buscar los destinatarios duplicados dentro de un Mensaje. 
  
Se usan los métodos [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md) para establecer restricciones en una tabla. **Restringir** la restricción se aplica a la tabla sin tener que recuperar todas las filas. Para recuperar sólo las filas que cumplen la restricción, se requiere una llamada posterior al [IMAPITable:: QueryRows](imapitable-queryrows.md) o un método similar. **FindRow** se aplica la restricción y recupera la primera fila en la tabla que coincida con los criterios. **FindRow** se aplica una restricción temporal, que es en existencia sólo para la duración de la llamada, mientras que **Restrict** se aplica una restricción más permanente. 
  
Algunos clientes pueden generar una restricción de uso de columnas que no están en la columna actual conjunto. Compatibilidad con esta restricción es opcional y los implementadores de la tabla que lo admitan agregar valor, especialmente para las tablas de contenido. Los implementadores de tabla que no admiten pueden devolver el valor MAPI_E_TOO_COMPLEX de una llamada **Restrict** o el valor MAPI_E_NOT_FOUND desde una llamada de **FindRow** . 
  
Los clientes deben tener en cuenta que, incluso si el proveedor admite restricciones en columnas no está en el conjunto actual de columna, va a obtener un mejor rendimiento general mediante la especificación de las columnas que se va a utilizar en sus restricciones con [IMAPITable::SetColumns](imapitable-setcolumns.md) .
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

