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
# <a name="opening-a-message"></a><span data-ttu-id="fddb6-103">Abrir un mensaje</span><span class="sxs-lookup"><span data-stu-id="fddb6-103">Opening a message</span></span>
 
<span data-ttu-id="fddb6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fddb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="fddb6-105">Para abrir un mensaje</span><span class="sxs-lookup"><span data-stu-id="fddb6-105">To open a message</span></span>
  
1. <span data-ttu-id="fddb6-106">Recupere el identificador de entrada del mensaje desde uno de los siguientes orígenes:</span><span class="sxs-lookup"><span data-stu-id="fddb6-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="fddb6-107">La fila que representa el mensaje en la tabla de contenido de su carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="fddb6-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="fddb6-108">Para obtener más información sobre cómo trabajar con una tabla contenido de la carpeta, vea [tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fddb6-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="fddb6-109">El miembro **lpEntryID** de la estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que se envía con una nueva notificación de correo.</span><span class="sxs-lookup"><span data-stu-id="fddb6-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="fddb6-110">Para obtener más información acerca de la recepción y el control de notificaciones, consulte [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fddb6-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="fddb6-111">Una llamada al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del mensaje solicitando la propiedad \*\*\*\* de ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fddb6-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="fddb6-112">Llame a uno de los siguientes métodos de **OpenEntry** para abrir el mensaje, estableciendo _lpEntryID_ en el identificador de entrada del mensaje:</span><span class="sxs-lookup"><span data-stu-id="fddb6-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="fddb6-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fddb6-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="fddb6-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fddb6-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="fddb6-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fddb6-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="fddb6-116">El método más rápido solo puede usarse para los mensajes entrantes e implica llamar al método **IMAPIFolder:: OpenEntry** de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="fddb6-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="fddb6-117">El siguiente método más rápido, que llama al método **IMsgStore:: OpenEntry** del almacén de mensajes, se puede usar para todos los mensajes, al igual que el método más lento, que llama a **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="fddb6-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fddb6-118">Las carpetas y sus tablas de contenido pueden cerrarse en cualquier momento sin afectar negativamente a ninguno de los mensajes que se abrieron desde dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="fddb6-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="fddb6-119">Para abrir un mensaje que se ha guardado en el disco</span><span class="sxs-lookup"><span data-stu-id="fddb6-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="fddb6-120">Llamar a **StgOpenStorage** para recuperar un puntero de interfaz **IStorage** , pasando el nombre del archivo de mensaje para el parámetro _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="fddb6-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="fddb6-121">Llame a **OpenIMsgOnIStg** para recuperar un puntero de interfaz **IMessage** para tener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="fddb6-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


