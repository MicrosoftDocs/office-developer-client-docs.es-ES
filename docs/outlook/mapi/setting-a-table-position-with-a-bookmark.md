---
title: Establecer una posición de tabla con un marcador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422463"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Establecer una posición de tabla con un marcador

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un marcador es un recurso que indica una ubicación determinada en una tabla. Establecer un marcador permite volver a una posición más adelante, una característica que puede mejorar significativamente el rendimiento de las operaciones de tabla. MAPI define tres marcadores estándar: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Apunta a la fila actual de una tabla.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Apunta a la primera fila de una tabla.  <br/> |
|BOOKMARK_END  <br/> |Apunta a la última fila de una tabla.  <br/> |
   
Los implementadores de tablas son necesarios para admitir estos marcadores estándar y también pueden admitir otros. Sin embargo, como los marcadores son recursos y los recursos son limitados, los usuarios de marcadores deben liberarlos tan pronto como sea posible. 
  
 **Para establecer un marcador en la posición actual de la tabla**
  
- Llame [a IMAPITable::CreateBookmark](imapitable-createbookmark.md). En ocasiones, no habrá suficiente memoria disponible para asignar el nuevo marcador, lo que hace que **CreateBookmark** devuelva el MAPI_E_UNABLE_TO_COMPLETE error. 
    
 **Para liberar un marcador**
  
- Llame [a IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover el cursor a una posición marcada**
  
- Llame [a IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** establece un nuevo valor para la BOOKMARK_CURRENT posición. **SeekRow** se puede usar, por ejemplo, para colocar una tabla de diez filas desde la posición actual o para empezar de nuevo al principio. Los clientes o proveedores de servicios pueden buscar el marcador actual, inicial o final de una tabla, o cualquier otra posición asociada a un marcador predefinido. Pueden moverse en una dirección hacia delante o hacia atrás y limitar la operación a un número especificado de filas. Como regla general, los autores de llamadas deben buscar a través de no más de 50 filas con **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) debe usarse con un número mayor de filas. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

