---
title: Administrar un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416541"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="6314b-103">Administrar un proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="6314b-103">Handling a transport provider</span></span>
  
<span data-ttu-id="6314b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6314b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6314b-105">Los clientes se comunican con proveedores de transporte a través de objetos de estado proporcionados por proveedores de transporte y la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="6314b-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="6314b-106">Los clientes obtienen acceso a objetos de estado [llamando a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) recuperar la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="6314b-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="6314b-107">Los objetos status implementan la interfaz [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) que tiene métodos para configurar proveedores, vaciar colas de mensajes entrantes y salientes, establecer contraseñas y validación de estado.</span><span class="sxs-lookup"><span data-stu-id="6314b-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="6314b-108">Para obtener más información acerca de los objetos de estado, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6314b-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="6314b-109">[Enviar o recibir un mensaje a petición:](sending-or-receiving-a-message-on-demand.md)describe cómo enviar o recibir un mensaje a petición.</span><span class="sxs-lookup"><span data-stu-id="6314b-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="6314b-110">[Configuración del orden de](setting-transport-order.md)transporte: describe cómo establecer el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="6314b-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="6314b-111">[Reconfigurar un proveedor de transporte:](reconfiguring-a-transport-provider.md)describe cómo reconfigurar un proveedor de transporte y qué propiedades están disponibles para establecer.</span><span class="sxs-lookup"><span data-stu-id="6314b-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

