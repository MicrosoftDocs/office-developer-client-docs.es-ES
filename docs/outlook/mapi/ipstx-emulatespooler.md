---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a8e353bbb4f276169ae26ba9d05821158bf55f00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817948"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="797dc-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="797dc-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="797dc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="797dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="797dc-105">Establece un almacén local para emular al administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.</span><span class="sxs-lookup"><span data-stu-id="797dc-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="797dc-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="797dc-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="797dc-107">[entrada] Establezca este parámetro en True si el almacén local debe emular la cola de impresión; establézcalo en False si no.</span><span class="sxs-lookup"><span data-stu-id="797dc-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="797dc-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="797dc-108">Remarks</span></span>

<span data-ttu-id="797dc-109">Un almacén local llama a **IPSTX::EmulateSpooler** para que actúe como un Outlook protocolo administrador, los mensajes de la cola de impresión en la cola de salida para el servidor back-end (por ejemplo, el servidor MSN o AOL) para el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="797dc-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="797dc-110">El almacén de emula un administrador de cola durante la sincronización, a continuación, llama a estos dos métodos:</span><span class="sxs-lookup"><span data-stu-id="797dc-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="797dc-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obtener la cola de mensajes saliente en el almacén.</span><span class="sxs-lookup"><span data-stu-id="797dc-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="797dc-112">Este método se ejecuta correctamente sólo si el almacén de emula al administrador de protocolos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="797dc-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="797dc-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger el acceso exclusivo a un mensaje en la cola de salida justo antes de enviar al servidor.</span><span class="sxs-lookup"><span data-stu-id="797dc-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="797dc-114">Este método se ejecuta correctamente sólo si el almacén de emula al administrador de protocolos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="797dc-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="797dc-115">Después de enviar el mensaje, el almacén de llama a este método nuevo para liberar el único acceso a ella.</span><span class="sxs-lookup"><span data-stu-id="797dc-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="797dc-116">Con respecto a Outlook 2002, el Administrador de protocolos de Outlook reemplaza a la cola MAPI y se convirtió en responsable para los mensajes salientes de puesta en cola de los servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="797dc-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="797dc-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="797dc-117">See also</span></span>



[<span data-ttu-id="797dc-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="797dc-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="797dc-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="797dc-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

