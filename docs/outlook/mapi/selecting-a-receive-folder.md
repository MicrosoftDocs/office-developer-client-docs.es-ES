---
title: Seleccionar una carpeta de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820599"
---
# <a name="selecting-a-receive-folder"></a>Seleccionar una carpeta de recepción

  
  
**Hace referencia a**: Outlook 
  
Una carpeta de recepción es donde se colocan los mensajes entrantes de una clase determinada. Para IPM y los mensajes de informe relacionados, MAPI asigna la Bandeja de entrada, como el valor predeterminado de recepción carpeta. Para IPC y los mensajes de informe relacionados, MAPI asigna la carpeta raíz del almacén de mensajes, como el valor predeterminado de recepción carpeta. Puede cambiar estas asignaciones o realizar asignaciones adicionales para otras clases de mensaje. Realizar explícita de recepción las asignaciones de carpeta de su cliente compatibles mensaje clases es opcional.
  
Cuando una clase de mensaje entrante no tiene una carpeta de recepción asignado, el proveedor de almacén de mensajes utiliza automáticamente la carpeta de recepción para la clase que coincide con el prefijo más largo posible de la clase entrante. Por ejemplo, si el cliente recibe un mensaje de clase IPM. Recibe Note.MyDocument y la única carpeta que se ha establecido es la Bandeja de entrada para los mensajes IPM, este mensaje se colocará en la Bandeja de entrada porque IPM. Note.MyDocument se deriva de la clase base IPM.
  
Cuando se asigna una carpeta de recepción de mensajes IPC, nunca use una carpeta desde el subárbol IPM. Estas carpetas se deben reservarse IPM sólo para mensajes. Use en su lugar una carpeta que se encuentra dentro de la carpeta raíz del almacén de mensajes. 
  
 **Para crear una carpeta de recepción para una clase de mensaje IPM**
  
1. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Llamar a [IMsgStore::OpenEntry](imsgstore-openentry.md) con **PR_IPM_SUBTREE_ENTRYID** como el identificador de entrada para abrir la carpeta raíz del subárbol IPM en el almacén de mensajes. 
    
3. Llame a [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
4. Llame a [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a su clase de mensaje IPM. 
    
 **Para crear una carpeta de recepción para una clase de mensaje IPC**
  
1. Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con un identificador de entrada null para abrir la carpeta raíz del almacén de mensajes. 
    
2. Llame a [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
3. Llame a [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a su clase de mensaje IPC. 
    
Asignar la carpeta de recepción que usa para los mensajes para los mensajes de informe relacionados. Por ejemplo, si el cliente recibe IPM. Los mensajes de nota, configurar una carpeta de recepción para futura IPM. Los mensajes de nota y el mismo reciben carpeta para los mensajes futuros de Report.IPM.Note.
  

