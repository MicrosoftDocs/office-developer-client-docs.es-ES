---
title: Atravesar la carpeta Bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406559"
---
# <a name="traversing-the-inbox-folder"></a>Atravesar la carpeta Bandeja de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para recorrer todos los mensajes de la Bandeja de entrada**
  
1. Llame [a IMsgStore::GetReceiveFolder para](imsgstore-getreceivefolder.md) recuperar el identificador de entrada de la Bandeja de entrada. 
    
2. Llame **a IMAPIFolder::OpenEntry** para abrir la Bandeja de entrada. 
    
3. Llame al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la Bandeja de entrada para recuperar la tabla de contenido. 
    
4. Llame al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de contenido para limitar el conjunto de columnas **a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y a cualquier otra columna que necesite. 
    
5. Llame [a IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar un grupo de filas. 
    
6. Hasta que ya no haya filas en la tabla de contenido:
    
1. Llame [a IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir el mensaje representado por el identificador de entrada de cada fila. 
    
2. Asigne el  _parámetro lppUnk_ a un puntero de **interfaz IMessage** local. 
    
3. Trabajar con las propiedades del mensaje.
    
4. Libere el puntero al que apunta el _parámetro lppUnk._ 
    
5. Llame [a IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar el siguiente grupo de filas. 
    
7. Libere la tabla de contenido.
    

