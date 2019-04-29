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
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438956"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="1d041-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="1d041-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="1d041-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d041-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d041-105">Establece un almacén local para emular el administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.</span><span class="sxs-lookup"><span data-stu-id="1d041-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="1d041-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="1d041-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="1d041-107">a Establezca este parámetro en true si el almacén local debe emular la cola de impresión; de lo contrario, establézcalo en false.</span><span class="sxs-lookup"><span data-stu-id="1d041-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1d041-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d041-108">Remarks</span></span>

<span data-ttu-id="1d041-109">Un almacén local llama a **IPSTX:: EmulateSpooler** para actuar como administrador de protocolos de Outlook, poniendo en cola los mensajes de la cola de salida en el servidor back-end (por ejemplo, MSN Server o AOL Server) para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="1d041-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="1d041-110">Emular una cola de impresión durante la sincronización, el almacén llama a estos dos métodos:</span><span class="sxs-lookup"><span data-stu-id="1d041-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="1d041-111">**[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obtener la cola de salida de mensajes en el almacén.</span><span class="sxs-lookup"><span data-stu-id="1d041-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="1d041-112">Este método se ejecuta correctamente sólo si el almacén está emulando el administrador de protocolos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1d041-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="1d041-113">**[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** para proteger el acceso único a un mensaje en la cola de salida justo antes de enviarlo al servidor.</span><span class="sxs-lookup"><span data-stu-id="1d041-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="1d041-114">Este método se ejecuta correctamente sólo si el almacén está emulando el administrador de protocolos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1d041-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="1d041-115">Después de enviar el mensaje, el almacén llama de nuevo a este método para liberar el acceso único al mismo.</span><span class="sxs-lookup"><span data-stu-id="1d041-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1d041-116">Desde Outlook 2002, el administrador de protocolos de Outlook reemplazó la cola de espera de MAPI y se convirtió en poner en cola los mensajes salientes a los servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="1d041-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d041-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="1d041-117">See also</span></span>



[<span data-ttu-id="1d041-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1d041-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="1d041-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="1d041-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

