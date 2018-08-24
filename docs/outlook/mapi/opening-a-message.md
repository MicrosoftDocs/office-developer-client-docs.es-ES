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
ms.openlocfilehash: e0701e64469576a8241002a6ff11299d1c343556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582983"
---
# <a name="opening-a-message"></a><span data-ttu-id="3020e-103">Abrir un mensaje</span><span class="sxs-lookup"><span data-stu-id="3020e-103">Opening a message</span></span>
 
<span data-ttu-id="3020e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3020e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="3020e-105">Para abrir un mensaje</span><span class="sxs-lookup"><span data-stu-id="3020e-105">To open a message</span></span>
  
1. <span data-ttu-id="3020e-106">Recuperar el identificador del mensaje entrada de uno de los siguientes orígenes:</span><span class="sxs-lookup"><span data-stu-id="3020e-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="3020e-107">La fila que representa el mensaje en la tabla de contenido de su carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="3020e-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="3020e-108">Para obtener más información sobre cómo trabajar con una tabla de contenido de carpeta, vea [Las tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3020e-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="3020e-109">El miembro **lpEntryID** de la estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que se envía con una notificación de correo nuevo.</span><span class="sxs-lookup"><span data-stu-id="3020e-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="3020e-110">Para obtener más información acerca de la recepción y control de notificaciones, vea [Controlar notificaciones](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3020e-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="3020e-111">Una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) del mensaje que solicita la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3020e-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="3020e-112">Llame a uno de los siguientes métodos de **OpenEntry** para abrir el mensaje, la opción de configuración _lpEntryID_ para el identificador de entrada del mensaje:</span><span class="sxs-lookup"><span data-stu-id="3020e-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="3020e-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3020e-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="3020e-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3020e-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="3020e-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3020e-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="3020e-116">El método más rápido puede usarse solo para los mensajes entrantes e implica llamar al método **IMAPIFolder::OpenEntry** de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="3020e-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="3020e-117">El siguiente método más rápido, llamar al método de **IMsgStore::OpenEntry** del almacén de mensajes, es fácil de usar para todos los mensajes como es el método más lento, al llamar a **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="3020e-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3020e-118">Las carpetas y sus tablas de contenido se pueden cerrar en cualquier momento sin afectar negativamente a cualquiera de los mensajes que se abrieron desde dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="3020e-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="3020e-119">Para abrir un mensaje que se ha guardado en el disco</span><span class="sxs-lookup"><span data-stu-id="3020e-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="3020e-120">Llamar a **StgOpenStorage** para recuperar un puntero de interfaz **IStorage** , pasando el nombre del archivo de mensaje para el parámetro _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="3020e-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="3020e-121">Llame a **OpenIMsgOnIStg** para recuperar un puntero de interfaz **IMessage** para tener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="3020e-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


