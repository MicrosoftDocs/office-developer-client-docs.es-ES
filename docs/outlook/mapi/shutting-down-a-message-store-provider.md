---
title: Apagar un proveedor de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339203"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="7c97b-103">Apagar un proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="7c97b-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="7c97b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c97b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c97b-105">Si su proveedor es un proveedor de almacenamiento de mensajes, puede apagarse de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="7c97b-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="7c97b-106">Cuando un cliente o la cola MAPI llama a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="7c97b-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="7c97b-107">El cierre de un proveedor de almacén de mensajes **con StoreLogoff** hace que el apagado se produzca de forma ordenada y controlada.</span><span class="sxs-lookup"><span data-stu-id="7c97b-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="7c97b-108">Cuando un cliente llama [a IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="7c97b-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="7c97b-109">La implementación de **IMsgStore::StoreLogoff** debe comenzar llamando a [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar a MAPI de que se está apagando, lo que indica que se debe cerrar la sesión de los proveedores de transporte relacionados.</span><span class="sxs-lookup"><span data-stu-id="7c97b-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="7c97b-110">Cuando **se devuelve IMsgStore::StoreLogoff,** el autor de la llamada invoca el método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c97b-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="7c97b-111">Implemente **este método Release** llamando al método **IUnknown::Release del** objeto de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="7c97b-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="7c97b-112">MAPI realiza las siguientes tareas en su implementación de **IUnknown::Release para** almacenes de mensajes:</span><span class="sxs-lookup"><span data-stu-id="7c97b-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="7c97b-113">Quita todas las estructuras [MAPIUID](mapiuid.md) registradas por el proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c97b-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="7c97b-114">Quita la fila del proveedor del almacén de mensajes de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="7c97b-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="7c97b-115">Llama [a IMSLogon::Logoff](imslogon-logoff.md) para liberar todos los objetos abiertos, subobjetos y objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="7c97b-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="7c97b-116">Llama [a IUnknown::Release para](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) liberar el objeto de inicio de sesión del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c97b-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="7c97b-117">Algunos clientes pueden omitir la llamada a **IMsgStore::StoreLogoff,** iniciando el apagado del proveedor del almacén de mensajes con la llamada al método **IUnknown::Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c97b-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="7c97b-118">Un apagado en estas circunstancias sin la llamada a **StoreLogoff** es menos ordenado y controlado.</span><span class="sxs-lookup"><span data-stu-id="7c97b-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="7c97b-119">Escriba el método **Release** del almacén de mensajes para controlar esta posibilidad y realizar un seguimiento de si se ha producido o no una llamada a **IMAPISupport::StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="7c97b-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="7c97b-120">**Se debe llamar a StoreLogoffTransports** una vez durante el proceso de apagado.</span><span class="sxs-lookup"><span data-stu-id="7c97b-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="7c97b-121">Si detectas en el **método Release** que aún no se ha llamado a **StoreLogoffTransports,** invoquelo con la LOGOFF_ABORT local.</span><span class="sxs-lookup"><span data-stu-id="7c97b-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c97b-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c97b-122">See also</span></span>



[<span data-ttu-id="7c97b-123">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="7c97b-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

