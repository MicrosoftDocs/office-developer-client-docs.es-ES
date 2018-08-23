---
title: Tratamiento de un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567954"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="f8b09-103">Tratamiento de un proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="f8b09-103">Handling a transport provider</span></span>
  
<span data-ttu-id="f8b09-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8b09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8b09-105">Los clientes se comuniquen con los proveedores de transporte a través de objetos de estado proporcionados por los proveedores de transporte y la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f8b09-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="f8b09-106">Los clientes de acceso a objetos de estado mediante una llamada a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="f8b09-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="f8b09-107">Objetos de estado implementan el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) de la interfaz, que tiene métodos para configurar proveedores, vaciado entrante y saliente colas de mensajes, las contraseñas de configuración y validación de estado.</span><span class="sxs-lookup"><span data-stu-id="f8b09-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="f8b09-108">Para obtener más información acerca de los objetos de estado, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f8b09-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="f8b09-109">[Enviar o recibir un mensaje de petición](sending-or-receiving-a-message-on-demand.md): se describe cómo enviar o recibir un mensaje de petición.</span><span class="sxs-lookup"><span data-stu-id="f8b09-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="f8b09-110">[El orden de configuración de transporte](setting-transport-order.md): describe cómo establecer el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="f8b09-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="f8b09-111">[Volver a configurar un proveedor de transporte](reconfiguring-a-transport-provider.md): se describe cómo volver a configurar un proveedor de transporte y qué propiedades están disponibles para establecer.</span><span class="sxs-lookup"><span data-stu-id="f8b09-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

