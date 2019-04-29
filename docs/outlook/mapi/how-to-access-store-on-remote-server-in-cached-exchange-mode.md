---
title: Obtener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420734"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="da3b1-103">Obtener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="da3b1-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="da3b1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da3b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da3b1-105">Este tema contiene un ejemplo de código en C++ que muestra cómo usar la marca **MAPI_NO_CACHE** para abrir una carpeta o un mensaje en un almacén de mensajes en el servidor remoto cuando Microsoft Office Outlook está en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="da3b1-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="da3b1-106">El modo caché de Exchange permite a Outlook usar una copia local del buzón de un usuario mientras Outlook mantiene una conexión en línea a una copia remota del buzón del usuario en el servidor remoto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="da3b1-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="da3b1-107">Cuando Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, todas las soluciones MAPI que inicien sesión en la misma sesión también se conectan al almacén de mensajes en caché.</span><span class="sxs-lookup"><span data-stu-id="da3b1-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="da3b1-108">Los datos a los que se obtiene acceso y los cambios realizados se realizan en la copia local del buzón.</span><span class="sxs-lookup"><span data-stu-id="da3b1-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="da3b1-109">Un cliente o un proveedor de servicios puede invalidar la conexión al almacén de mensajes local y abrir un mensaje o una carpeta en el almacén remoto estableciendo el bit de **MAPI_NO_CACHE** en el parámetro *ulFlags* al llamar a **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="da3b1-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="da3b1-110">El siguiente ejemplo de código muestra cómo llamar a **IMsgStore:: OpenEntry** con la marca **MAPI_NO_CACHE** establecida en el parámetro *ulFlags* para abrir la carpeta raíz en el almacén de mensajes remotos.</span><span class="sxs-lookup"><span data-stu-id="da3b1-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="da3b1-111">Si ha abierto el almacén de mensajes con la marca **MDB_ONLINE** en el servidor remoto, no es necesario que use la marca **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="da3b1-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da3b1-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="da3b1-112">See also</span></span>

- [<span data-ttu-id="da3b1-113">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="da3b1-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="da3b1-114">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="da3b1-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="da3b1-115">Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché</span><span class="sxs-lookup"><span data-stu-id="da3b1-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

