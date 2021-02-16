---
title: Enviar o recibir un mensaje a petición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436373"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="82d50-103">Enviar o recibir un mensaje a petición</span><span class="sxs-lookup"><span data-stu-id="82d50-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="82d50-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82d50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82d50-105">Normalmente, los clientes dependen del subsistema MAPI (la cola MAPI y los proveedores de servicios) para controlar el tiempo de transmisión y recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="82d50-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="82d50-106">Sin embargo, puede modificar este intervalo mediante el objeto de estado de la cola MAPI o un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="82d50-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="82d50-107">El [método IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) quita todos los mensajes de una o más colas entrantes o salientes del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="82d50-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="82d50-108">Los siguientes procedimientos describen dos técnicas para enviar o recibir mensajes a petición.</span><span class="sxs-lookup"><span data-stu-id="82d50-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="82d50-109">El primer procedimiento usa el objeto de estado de la cola MAPI para vaciar las colas de todos los proveedores de transporte del perfil; El segundo procedimiento vacía la cola de un único proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="82d50-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="82d50-110">Para vaciar todas las colas entrantes o salientes en una sola operación</span><span class="sxs-lookup"><span data-stu-id="82d50-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="82d50-111">Llame [a IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="82d50-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="82d50-112">Llame al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar el conjunto de columnas **a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="82d50-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="82d50-113">Crear una restricción de propiedad mediante una [estructura SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_RESOURCE_TYPE** con MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="82d50-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="82d50-114">Llame [a HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction,** para recuperar la fila que representa el estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="82d50-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="82d50-115">Pase la **PR_ENTRYID** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="82d50-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="82d50-116">Llame al método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) de la cola MAPI, pasando la marca FLUSH_NO_UI para suprimir la interfaz de usuario y la marca FLUSH_DOWNLOAD o FLUSH_UPLOAD para vaciar las colas entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="82d50-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="82d50-117">Libere el objeto de estado y la tabla de estado, así como la estructura [SRowSet](srowset.md) asignada a la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d50-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="82d50-118">Para vaciar las colas entrantes o salientes individualmente por el proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="82d50-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="82d50-119">Llame [a IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="82d50-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="82d50-120">Llame al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar el conjunto de columnas **PR_ENTRYID** y **PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="82d50-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="82d50-121">Crear una restricción de propiedad mediante una [estructura SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_RESOURCE_TYPE** con MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="82d50-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="82d50-122">Llame [a HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction,** para recuperar las filas proporcionadas por los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="82d50-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="82d50-123">Para cada fila devuelta desde **HrQueryAllRows**:</span><span class="sxs-lookup"><span data-stu-id="82d50-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="82d50-124">Pase la **PR_ENTRYID** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="82d50-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="82d50-125">Compruebe que el objeto de estado de transporte admite el método **FlushQueues** comprobando que su propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tiene la marca STATUS_FLUSH_QUEUES establecida.</span><span class="sxs-lookup"><span data-stu-id="82d50-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="82d50-126">Si se admite, llame [a IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="82d50-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="82d50-127">Si no se admite, llame al método **IMAPIStatus::FlushQueues** de la cola MAPI y pase el identificador de entrada del transporte en el _parámetro lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="82d50-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="82d50-128">Vea el procedimiento anterior para obtener instrucciones sobre cómo obtener acceso al objeto de estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="82d50-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="82d50-129">Establezca la FLUSH_DOWNLOAD para vaciar las colas salientes o la marca FLUSH_UPLOAD para vaciar las colas entrantes.</span><span class="sxs-lookup"><span data-stu-id="82d50-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="82d50-130">Libere el objeto de estado y la tabla de estado, así como la estructura [SRowSet](srowset.md) asignada a la tabla.</span><span class="sxs-lookup"><span data-stu-id="82d50-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="82d50-131">La cola MAPI respeta la marca FLUSH_NO_UI la mayoría de los proveedores de transporte LAN.</span><span class="sxs-lookup"><span data-stu-id="82d50-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="82d50-132">Sin embargo, no todos los proveedores de transporte respetan esta marca, especialmente aquellos que usan un módem explícitamente y el Servicio de acceso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="82d50-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="82d50-133">RAS no se diseñó para permitir a los clientes suprimir la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="82d50-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="82d50-134">Es posible configurar un cliente para que pueda conectarse sin necesidad de la interacción de un usuario, pero es difícil y requiere conocimientos amplios de los servicios de mensajes del cliente.</span><span class="sxs-lookup"><span data-stu-id="82d50-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

