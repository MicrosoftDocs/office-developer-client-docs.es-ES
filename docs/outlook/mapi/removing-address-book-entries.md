---
title: Quitar entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425263"
---
# <a name="removing-address-book-entries"></a>Quitar entradas de la libreta de direcciones
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se llama al [método IABContainer::D eleteEntries del](iabcontainer-deleteentries.md) contenedor para quitar uno o varios destinatarios. **DeleteEntries** tiene dos parámetros: una matriz de identificadores de entrada que representan los destinatarios que se eliminarán y un valor de marcas reservadas. La eliminación de un destinatario afecta a la tabla de contenido del contenedor; además de eliminar el destinatario, el contenedor debe eliminar la fila de la tabla de contenido que representa al destinatario. Cuando la fila se ha quitado de la tabla, el contenedor debe emitir una notificación de tabla a cada cliente registrado. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Para implementar IABContainer::D eleteEntries
  
1. Elimine cada destinatario representado por el identificador de entrada del contenedor.
    
2. Si la tabla de contenido del contenedor está abierta:
    
   - Envíe una  _notificación fnevTableModified_ con el miembro **ulTableEvent** establecido en TABLE_ROW_DELETED a los clientes registrados para cada fila de tabla de contenido eliminado. Si su proveedor usa la utilidad de notificación, llame [a IMAPISupport::Notify](imapisupport-notify.md) para enviar estas notificaciones. 
    
   - Si el proveedor admite notificaciones de objetos, también envíe una _notificación fnevObjectDeleted._ 
    

