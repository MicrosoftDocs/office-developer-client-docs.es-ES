---
title: Selección de una carpeta de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428420"
---
# <a name="selecting-a-receive-folder"></a>Selección de una carpeta de recepción

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una carpeta de recepción es donde se colocan los mensajes entrantes de una clase determinada. Para ipm y mensajes de informe relacionados, MAPI asigna la Bandeja de entrada como carpeta de recepción predeterminada. Para IPC y mensajes de informe relacionados, MAPI asigna la carpeta raíz del almacén de mensajes como la carpeta de recepción predeterminada. Puede cambiar estas asignaciones o realizar asignaciones adicionales para otras clases de mensaje. Realizar asignaciones explícitas de carpetas de recepción para las clases de mensaje admitidas del cliente es opcional.
  
Cuando una clase de mensaje entrante no tiene asignada una carpeta de recepción, el proveedor del almacén de mensajes usa automáticamente la carpeta de recepción para la clase que coincide con el prefijo más largo posible de la clase entrante. Por ejemplo, si el cliente recibe un mensaje de clase IPM. Note.MyDocument y la única carpeta de recepción que se ha establecido es la Bandeja de entrada para mensajes IPM, este mensaje se colocará en la Bandeja de entrada porque IPM. Note.MyDocument deriva de la clase base IPM.
  
Al asignar una carpeta de recepción para mensajes IPC, nunca use una carpeta del subárbol IPM. Estas carpetas deben reservarse solo para mensajes IPM. Use en su lugar una carpeta que esté incluida en la carpeta raíz del almacén de mensajes. 
  
 **Para crear una carpeta de recepción para una clase de mensaje IPM**
  
1. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Llama [a IMsgStore::OpenEntry](imsgstore-openentry.md) con **PR_IPM_SUBTREE_ENTRYID** como identificador de entrada para abrir la carpeta raíz del subárbol IPM en el almacén de mensajes. 
    
3. Llama [a IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
4. Llama [a IMsgStore::SetReceiveFolder para](imsgstore-setreceivefolder.md) asignar la nueva carpeta a la clase de mensaje IPM. 
    
 **Para crear una carpeta de recepción para una clase de mensaje IPC**
  
1. Llama [a IMsgStore::OpenEntry con](imsgstore-openentry.md) un identificador de entrada nulo para abrir la carpeta raíz del almacén de mensajes. 
    
2. Llama [a IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
3. Llama [a IMsgStore::SetReceiveFolder para](imsgstore-setreceivefolder.md) asignar la nueva carpeta a la clase de mensaje IPC. 
    
Asigna la carpeta de recepción que usas para los mensajes de los mensajes de informe relacionados. Por ejemplo, si el cliente recibe IPM. Tenga en cuenta los mensajes, configure una carpeta de recepción para el IPM futuro. Tenga en cuenta los mensajes y la misma carpeta de recepción para futuros mensajes Report.IPM.Note.
  

