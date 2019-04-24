---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317335"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="395fe-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="395fe-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="395fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="395fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="395fe-105">Proporciona acceso a la tabla cola de salida, una tabla que contiene información sobre todos los mensajes de la cola de salida del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="395fe-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="395fe-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="395fe-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="395fe-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="395fe-107">Parameters</span></span>

 <span data-ttu-id="395fe-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="395fe-108">_ulFlags_</span></span>
  
> <span data-ttu-id="395fe-109">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="395fe-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="395fe-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="395fe-110">_lppTable_</span></span>
  
> <span data-ttu-id="395fe-111">contempla Un puntero a un puntero a la tabla de colas de salida.</span><span class="sxs-lookup"><span data-stu-id="395fe-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="395fe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="395fe-112">Return value</span></span>

<span data-ttu-id="395fe-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="395fe-113">S_OK</span></span> 
  
> <span data-ttu-id="395fe-114">La tabla de cola de salida se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="395fe-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="395fe-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="395fe-115">Remarks</span></span>

<span data-ttu-id="395fe-116">El método **IMsgStore:: GetOutgoingQueue** proporciona al administrador de trabajos en cola MAPI acceso a la tabla que muestra la cola de mensajes salientes del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="395fe-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="395fe-117">Normalmente, los mensajes se colocan en la tabla de colas de salida después de llamar al método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="395fe-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="395fe-118">Sin embargo, como el orden de envío afecta al orden de preprocesamiento y envío al proveedor de transporte, algunos mensajes que se marcaron para enviar podrían no aparecer inmediatamente en la tabla de colas de salida.</span><span class="sxs-lookup"><span data-stu-id="395fe-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="395fe-119">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="395fe-119">Notes to implementers</span></span>

<span data-ttu-id="395fe-120">Para obtener una lista de las propiedades que deben incluirse como columnas en la tabla cola de salida, consulte [tablas de colas de salida](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="395fe-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="395fe-121">Debido a que la cola MAPI está diseñada para aceptar mensajes de un almacén de mensajes en orden ascendente de tiempo de envío, permita que la cola MAPI ordene la tabla cola de salida para que se ajuste a este orden o que se establezca como criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="395fe-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="395fe-122">Debe admitir notificaciones para la tabla de colas de mensajes salientes, lo que garantiza que la cola MAPI recibirá una notificación cuando cambie el contenido de la cola.</span><span class="sxs-lookup"><span data-stu-id="395fe-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="395fe-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="395fe-123">See also</span></span>



[<span data-ttu-id="395fe-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="395fe-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="395fe-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="395fe-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

