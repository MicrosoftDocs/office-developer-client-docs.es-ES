---
title: Eliminar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582948"
---
# <a name="deleting-a-recipient"></a>Eliminar un destinatario

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
 **Para quitar entradas de la libreta de direcciones de uno o más de un contenedor modificable**
  
- Llame al método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , pasando una matriz de identificadores de entrada que representan las entradas de la libreta de direcciones que se va a eliminar. **DeleteEntries** puede devolver una advertencia, MAPI_W_PARTIAL_COMPLETION, para indicar que no se pudo eliminar una o varias de las entradas. Pruebe para este valor devuelto a la macro **HR_FAILED** y llamar al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) del contenedor si se necesita más información acerca del problema. 
    
Cuando se mantiene un puntero a la estructura [ADRENTRY](adrentry.md) de una entrada eliminada en la memoria caché, podrá recuperar propiedades mediante su identificador de entrada. Esto es debido a que la entrada sólo se marca para su eliminación. MAPI mantiene un nivel de acceso a estas entradas marcadas por diseño. 
  

