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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339731"
---
# <a name="selecting-a-receive-folder"></a>Selección de una carpeta de recepción

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una carpeta de recepción es donde se colocan los mensajes entrantes de una clase determinada. Para IPM y los mensajes de informe relacionados, MAPI asigna la bandeja de entrada como carpeta de recepción predeterminada. Para los mensajes de IPC y los informes relacionados, MAPI asigna la carpeta raíz del almacén de mensajes como la carpeta de recepción predeterminada. Puede cambiar estas asignaciones o realizar asignaciones adicionales para otras clases de mensajes. Es opcional realizar asignaciones de carpetas de recepción explícitas para las clases de mensaje compatibles con el cliente.
  
Cuando una clase de mensaje entrante no tiene una carpeta de recepción asignada, el proveedor de almacenamiento de mensajes utiliza automáticamente la carpeta de recepción para la clase que coincide con el prefijo más largo posible de la clase entrante. Por ejemplo, si el cliente recibe un mensaje de la clase IPM. Nota. MyDocument y la única carpeta de recepción que se ha establecido es la bandeja de entrada de los mensajes IPM, este mensaje se colocará en la bandeja de entrada porque IPM. Note. MyDocument deriva de la clase base IPM.
  
Cuando se asigna una carpeta de recepción para los mensajes IPC, no use nunca una carpeta del subárbol IPM. Estas carpetas deben reservarse solo para mensajes IPM. Use en su lugar una carpeta contenida en la carpeta raíz del almacén de mensajes. 
  
 **Para crear una carpeta de recepción para una clase de mensaje IPM**
  
1. Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) con **PR_IPM_SUBTREE_ENTRYID** como el identificador de entrada para abrir la carpeta raíz del subárbol IPM en el almacén de mensajes. 
    
3. Llame a [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
4. Llame a [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a la clase de mensaje IPM. 
    
 **Para crear una carpeta de recepción para una clase de mensaje IPC**
  
1. Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) con un identificador de entrada null para abrir la carpeta raíz del almacén de mensajes. 
    
2. Llame a [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción. 
    
3. Llame a [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a la clase de mensaje IPC. 
    
Asigne la carpeta de recepción que usa para los mensajes para los mensajes de informe relacionados. Por ejemplo, si el cliente recibe IPM. Mensajes de notas, configure una carpeta de recepción para el futuro de IPM. Mensajes de nota y la misma carpeta de recepción para futuros mensajes de informe. IPM. Note.
  

