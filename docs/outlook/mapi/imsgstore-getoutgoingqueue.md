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
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817763"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="ebd97-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="ebd97-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="ebd97-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebd97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebd97-105">Proporciona acceso a la tabla de cola saliente, una tabla que contiene información acerca de todos los mensajes en cola de salida del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ebd97-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="ebd97-106">Se llama a este m�todo s�lo por la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebd97-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ebd97-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ebd97-107">Parameters</span></span>

 <span data-ttu-id="ebd97-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebd97-108">_ulFlags_</span></span>
  
> <span data-ttu-id="ebd97-109">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ebd97-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ebd97-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ebd97-110">_lppTable_</span></span>
  
> <span data-ttu-id="ebd97-111">[out] Un puntero a un puntero a la tabla de cola saliente.</span><span class="sxs-lookup"><span data-stu-id="ebd97-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ebd97-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebd97-112">Return value</span></span>

<span data-ttu-id="ebd97-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebd97-113">S_OK</span></span> 
  
> <span data-ttu-id="ebd97-114">En la tabla cola saliente se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="ebd97-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebd97-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebd97-115">Remarks</span></span>

<span data-ttu-id="ebd97-116">El método **IMsgStore::GetOutgoingQueue** proporciona a la cola MAPI con acceso a la tabla que muestra la cola del almacén de mensajes de los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="ebd97-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="ebd97-117">Normalmente, los mensajes se colocan en la tabla cola saliente después de que se llama a su método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd97-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="ebd97-118">Sin embargo, debido a que el orden de envío afecta al orden de preprocesamiento y envío para el proveedor de transporte, algunos mensajes que se han marcado para el envío es posible que no aparezca en la tabla cola saliente inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ebd97-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ebd97-119">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ebd97-119">Notes to implementers</span></span>

<span data-ttu-id="ebd97-120">Para obtener una lista de las propiedades que se debe incluir como columnas en la tabla cola saliente, vea [Las tablas de cola saliente](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ebd97-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="ebd97-121">Debido a que la cola MAPI está diseñada para aceptar los mensajes de un almacén de mensajes en orden ascendente de tiempo de envío, permitir que la cola MAPI ordenar la tabla de cola saliente para que coincida con este orden o establecer como el criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ebd97-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="ebd97-122">Debe admitir las notificaciones para la tabla de cola de mensajes salientes, asegurarse de que la cola MAPI recibe una notificación cuando cambia el contenido de la cola.</span><span class="sxs-lookup"><span data-stu-id="ebd97-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ebd97-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebd97-123">See also</span></span>



[<span data-ttu-id="ebd97-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ebd97-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="ebd97-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebd97-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
