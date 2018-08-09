---
title: Abrir un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4ea75f723a2fcb242d8b9a516498855aa20cfdd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818434"
---
# <a name="opening-a-message"></a>Abrir un mensaje
 
**Hace referencia a**: Outlook 
  
### <a name="to-open-a-message"></a>Para abrir un mensaje
  
1. Recuperar el identificador del mensaje entrada de uno de los siguientes orígenes:
    
   - La fila que representa el mensaje en la tabla de contenido de su carpeta principal. Para obtener más información sobre cómo trabajar con una tabla de contenido de carpeta, vea [Las tablas de contenido](contents-tables.md).
    
   - El miembro **lpEntryID** de la estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que se envía con una notificación de correo nuevo. Para obtener más información acerca de la recepción y control de notificaciones, vea [Controlar notificaciones](handling-notifications.md).
    
   - Una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) del mensaje que solicita la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Llame a uno de los siguientes métodos de **OpenEntry** para abrir el mensaje, la opción de configuración _lpEntryID_ para el identificador de entrada del mensaje: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  El método más rápido puede usarse solo para los mensajes entrantes e implica llamar al método **IMAPIFolder::OpenEntry** de la carpeta de recepción. El siguiente método más rápido, llamar al método de **IMsgStore::OpenEntry** del almacén de mensajes, es fácil de usar para todos los mensajes como es el método más lento, al llamar a **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Las carpetas y sus tablas de contenido se pueden cerrar en cualquier momento sin afectar negativamente a cualquiera de los mensajes que se abrieron desde dentro de ellos. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Para abrir un mensaje que se ha guardado en el disco
  
1. Llamar a **StgOpenStorage** para recuperar un puntero de interfaz **IStorage** , pasando el nombre del archivo de mensaje para el parámetro _pwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Llame a **OpenIMsgOnIStg** para recuperar un puntero de interfaz **IMessage** para tener acceso al mensaje. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


