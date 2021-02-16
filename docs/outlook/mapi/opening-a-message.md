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
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411095"
---
# <a name="opening-a-message"></a>Abrir un mensaje
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Para abrir un mensaje
  
1. Recupere el identificador de entrada del mensaje de uno de los siguientes orígenes:
    
   - Fila que representa el mensaje en la tabla de contenido de su carpeta principal. Para obtener más información acerca de cómo trabajar con una tabla de contenido de carpeta, vea [Tablas de contenido.](contents-tables.md)
    
   - El **miembro lpEntryID** de [la NEWMAIL_NOTIFICATION](newmail_notification.md) que se envía con una nueva notificación de correo. Para obtener más información acerca de la recepción y el tratamiento de notificaciones, vea [Control de notificaciones.](handling-notifications.md)
    
   - Una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) del mensaje que solicita la **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Llame a uno de los siguientes **métodos OpenEntry** para abrir el mensaje, estableciendo  _lpEntryID_ en el identificador de entrada del mensaje: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  El método más rápido solo se puede usar para los mensajes entrantes e implica llamar al método **IMAPIFolder::OpenEntry** de la carpeta de recepción. El siguiente método más rápido, que llama al método **IMsgStore::OpenEntry** del almacén de mensajes, se puede usar para todos los mensajes como el método más lento, llamando a **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Las carpetas y sus tablas de contenido se pueden cerrar en cualquier momento sin afectar negativamente a ninguno de los mensajes que se abrieron desde dentro de ellas. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Para abrir un mensaje que se ha guardado en el disco
  
1. Llama **a StgOpenStorage para** recuperar un puntero de interfaz **IStorage** y pasa el nombre del archivo de mensaje para el _parámetro pwcsName._ 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Llama **a OpenIMsgOnIStg para** recuperar un puntero de interfaz **IMessage** para obtener acceso al mensaje. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


