---
title: Recorrer la carpeta Bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594491"
---
# <a name="traversing-the-inbox-folder"></a>Recorrer la carpeta Bandeja de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para desplazarse por todos los mensajes en la Bandeja de entrada**
  
1. Llame a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar el identificador de entrada de la Bandeja de entrada. 
    
2. Llame a **IMAPIFolder::OpenEntry** para abrir la Bandeja de entrada. 
    
3. Llamar al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la Bandeja de entrada para recuperar la tabla de contenido. 
    
4. Llamar el contenido [IMAPITable::SetColumns](imapitable-setcolumns.md) al método de la tabla para limitar la columna establecida en la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y todas las columnas que necesite. 
    
5. Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar un grupo de filas. 
    
6. Hasta que ya no hay ninguna fila en la tabla de contenido:
    
1. Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir el mensaje representado por el identificador de entrada de cada fila. 
    
2. Asigne el parámetro _lppUnk_ a un puntero de interfaz **IMessage** local. 
    
3. Trabajar con las propiedades del mensaje.
    
4. Liberar el puntero que señala el parámetro _lppUnk_ . 
    
5. Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar el siguiente grupo de filas. 
    
7. Versión en la tabla de contenido.
    

