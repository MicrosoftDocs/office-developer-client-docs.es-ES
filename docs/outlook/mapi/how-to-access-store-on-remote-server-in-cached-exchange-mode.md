---
title: Tener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816987"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="84af6-103">Tener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="84af6-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="84af6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84af6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84af6-105">Este tema contiene un ejemplo de código en C++ que se muestra cómo usar el indicador **MAPI_NO_CACHE** para abrir una carpeta o un mensaje en un almacén de mensajes en el servidor remoto cuando Microsoft Office Outlook está en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="84af6-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="84af6-106">El modo de intercambio en caché permite que Outlook para utilizar una copia local del buzón de un usuario mientras Outlook mantiene una conexión en línea a una copia remota de buzón de correo del usuario en el servidor de Exchange remoto.</span><span class="sxs-lookup"><span data-stu-id="84af6-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="84af6-107">Cuando Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, las soluciones MAPI que inicie sesión en la misma sesión también están conectadas en el almacén de mensajes almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="84af6-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="84af6-108">Los datos que se tiene acceso y los cambios que se realizan se realizan con la copia local del buzón.</span><span class="sxs-lookup"><span data-stu-id="84af6-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="84af6-109">Un proveedor de servicio o cliente puede invalidar la conexión con el almacén de mensajes local y abrir un mensaje o una carpeta en el almacén remoto estableciendo el bit de **MAPI_NO_CACHE** en el parámetro *ulFlags* al llamar a **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="84af6-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="84af6-110">El ejemplo de código siguiente muestra cómo llamar a **IMsgStore::OpenEntry** con el indicador **MAPI_NO_CACHE** establecido en el parámetro *ulFlags* para abrir la carpeta raíz en el almacén de mensajes remoto.</span><span class="sxs-lookup"><span data-stu-id="84af6-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
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

<span data-ttu-id="84af6-111">Si se abre el almacén de mensajes con el indicador **MDB_ONLINE** en el servidor remoto, no es necesario usar el indicador **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="84af6-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84af6-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="84af6-112">See also</span></span>

- [<span data-ttu-id="84af6-113">Información sobre las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="84af6-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="84af6-114">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="84af6-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="84af6-115">Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché</span><span class="sxs-lookup"><span data-stu-id="84af6-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

