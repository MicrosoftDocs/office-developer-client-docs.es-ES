---
title: Acerca de las restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433111"
---
# <a name="about-restrictions"></a>Acerca de las restricciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una restricción es una forma de limitar el número de filas de una vista a solo aquellas filas con valores para las columnas que coinciden con criterios específicos. Hay muchas oportunidades distintas para usar restricciones con tablas. Las aplicaciones cliente pueden usar restricciones, por ejemplo, para filtrar una tabla de contenido para los mensajes enviados por una persona determinada, para buscar filas que no admiten una propiedad o que han establecido una propiedad en un valor específico, o para buscar destinatarios duplicados en un mensaje. 
  
Los métodos [IMAPITable:: Restrict](imapitable-restrict.md) and [IMAPITable:: FindRow](imapitable-findrow.md) se usan para establecer restricciones en una tabla. **Restrict** aplica la restricción a la tabla sin recuperar ninguna fila. Para recuperar sólo las filas que cumplan la restricción, es necesario realizar una llamada posterior a [IMAPITable:: QueryRows](imapitable-queryrows.md) o a un método similar. **FindRow** aplica la restricción y recupera la primera fila del table que coincide con los criterios. **FindRow** aplica una restricción temporal, que solo existe durante la duración de la llamada, mientras que **Restrict** aplica una restricción más permanente. 
  
Algunos clientes pueden crear una restricción mediante el uso de columnas que no están en el conjunto de columnas actual. Admitir una restricción de este tipo es opcional y los implementadores de tablas que lo admiten agregan valor, especialmente para las tablas de contenido. Los implementadores de la tabla que no lo admiten pueden devolver el valor MAPI_E_TOO_COMPLEX de una llamada a **Restrict** o el valor MAPI_E_NOT_FOUND de una llamada **FindRow** . 
  
Los clientes deben tener en cuenta que, aunque el proveedor no admita restricciones en las columnas que no están en el conjunto de columnas actual, obtendrá un mejor rendimiento general al especificar las columnas que pretenden usar en sus restricciones con el [IMAPITable:: SetColumns](imapitable-setcolumns.md) .
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

