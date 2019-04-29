---
title: Eliminación de un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421049"
---
# <a name="deleting-a-recipient"></a>Eliminación de un destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para quitar una o varias entradas de la libreta de direcciones de un contenedor modificable**
  
- Llame al método [IABContainer::D eleteentries](iabcontainer-deleteentries.md) , pasando una matriz de identificadores de entrada que representan las entradas de la libreta de direcciones que se van a eliminar. **DeleteEntries** puede devolver una advertencia, MAPI_W_PARTIAL_COMPLETION, para indicar que no pudo eliminar una o varias entradas. Pruebe este valor devuelto con la macro **HR_FAILED** y llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) del contenedor si se necesita más información sobre el problema. 
    
Si mantiene un puntero a la estructura [ADRENTRY](adrentry.md) de una entrada eliminada en la memoria caché, podrá recuperar las propiedades mediante su identificador de entrada. Esto se debe a que la entrada solo se marca para su eliminación. MAPI mantiene un nivel de acceso a estas entradas marcadas por diseño. 
  

