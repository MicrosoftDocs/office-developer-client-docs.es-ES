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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351236"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Establecer una posición de tabla con un marcador

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un marcador es un recurso que indica una ubicación determinada de una tabla. Establecer un marcador permite volver a una posición posterior, una característica que puede mejorar significativamente el rendimiento de las operaciones de tabla. MAPI define tres marcadores estándar: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Apunta a la fila actual de una tabla.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Apunta a la primera fila de una tabla.  <br/> |
|BOOKMARK_END  <br/> |Apunta a la última fila de una tabla.  <br/> |
   
Los implementadores de tablas son necesarios para admitir estos marcadores estándar y también pueden admitir otros. Sin embargo, dado que los marcadores son recursos y los recursos son limitados, los usuarios de marcadores deben liberarlos tan pronto como sea posible. 
  
 **Para establecer un marcador en la posición de la tabla actual**
  
- Llame al [IMAPITable:: CreateBookmark](imapitable-createbookmark.md). De vez en cuando no habrá suficiente memoria disponible para asignar el nuevo marcador, lo que hará que **CreateBookmark** devuelva el valor de error MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Para liberar un marcador**
  
- Llame al [IMAPITable:: FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover el cursor a una posición con marcador**
  
- Llame al [IMAPITable:: SeekRow](imapitable-seekrow.md). **SeekRow** establece un nuevo valor para la posición BOOKMARK_CURRENT. **SeekRow** puede usarse, por ejemplo, para colocar una tabla diez filas a partir de la posición actual o para volver a empezar desde el principio. Los clientes o proveedores de servicios pueden buscar el actual, el principio o el final de una tabla, o cualquier otra posición asociada con un marcador predefinido. Se pueden mover en una dirección hacia delante o hacia atrás, y limitar la operación a un número especificado de filas. Como regla, los autores de la llamada deben buscar en más de 50 filas con **SeekRow**; El [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) debe usarse con un número mayor de filas. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

