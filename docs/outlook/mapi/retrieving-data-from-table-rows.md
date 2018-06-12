---
title: Recuperación de datos de las filas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820525"
---
# <a name="retrieving-data-from-table-rows"></a>Recuperación de datos de las filas de tabla

  
  
**Se aplica a**: Outlook 
  
Recuperación de filas de una tabla implica:
  
- Obtención de los valores de propiedad para todas las columnas.
    
- Modificación de la posición actual.
    
Una de las columnas necesarias en la mayoría de las tablas es un identificador de entrada: la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), que se pueden utilizar para abrir el objeto que representa la fila. Normalmente, este identificador de entrada es un identificador de entrada a corto plazo, uno que no se conserva más allá de la duración de la tabla. Sin embargo, puede ser un identificador a largo plazo si el proveedor de implementación de la tabla sólo admite un tipo de identificador de entrada.
  
Los clientes y proveedores de servicios pueden realizar una de las llamadas para recuperar las filas siguientes:
  
|||
|:-----|:-----|
|[IMAPITable:: QueryRows](imapitable-queryrows.md) <br/> |Recupera un número especificado de filas a partir de la fila actual en una dirección hacia delante o hacia atrás.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Recupera todas las filas de una tabla.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera una fila en una tabla de acuerdo con el valor de su columna de índice. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) generalmente es la columna de índice para una tabla.  <br/> |
   
Cuando una propiedad opcional se incluye como una de las columnas de una tabla, mientras que otros usuarios podrían no algunas de las filas deberían los valores válidos para la columna. Si existe un valor válido para una columna depende de si la propiedad establece el objeto que proporciona la información de la fila. Dependiendo de la implementación del objeto, se puede representar una propiedad que no existe en la tabla como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) o un valor arbitrario. Los usuarios de las tablas deben tener cuidados diferenciar entre las propiedades que existen y tienen valores sin sentido y las propiedades que existen y tienen valores válidos. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

