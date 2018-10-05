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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386057"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="25312-103">Apagar un proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="25312-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="25312-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25312-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25312-105">Si su proveedor es un proveedor de almacén de mensajes, puede apagar en una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="25312-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="25312-106">Cuando un cliente o la cola MAPI llama a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="25312-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="25312-107">Cerrando un proveedor de almacén de mensajes con **StoreLogoff** hace que el apagado se produzca de manera ordenada y controlada.</span><span class="sxs-lookup"><span data-stu-id="25312-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="25312-108">Cuando un cliente llama a [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="25312-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="25312-109">La implementación de **IMsgStore::StoreLogoff** debe comenzar mediante una llamada a [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar a MAPI que se está cerrando, que indica que se van a registrar los proveedores de transporte relacionados.</span><span class="sxs-lookup"><span data-stu-id="25312-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="25312-110">Cuando se devuelve **IMsgStore::StoreLogoff** , su autor de la llamada invoca (método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) ) de su almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="25312-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="25312-111">Implementar este método **versión** por llamar al método **IUnknown:: Release** del objeto de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="25312-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="25312-112">MAPI realiza las siguientes tareas en su implementación de **IUnknown:: Release** para los almacenes de mensajes:</span><span class="sxs-lookup"><span data-stu-id="25312-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="25312-113">Todos los de las estructuras [MAPIUID](mapiuid.md) registradas por el proveedor de almacén de mensajes quita.</span><span class="sxs-lookup"><span data-stu-id="25312-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="25312-114">Quita la fila del proveedor de almacén de mensajes de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="25312-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="25312-115">Llama a [IMSLogon::Logoff](imslogon-logoff.md) para liberar todos los objetos abiertos, los subobjetos y los objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="25312-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="25312-116">Llama a [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto de inicio de sesión del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="25312-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="25312-117">Algunos clientes podrían omitir la llamada a **IMsgStore::StoreLogoff**, iniciar el apagado de su proveedor de almacén de mensajes con la llamada al método de **IUnknown:: Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="25312-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="25312-118">Un cierre en estas circunstancias sin la llamada a **StoreLogoff** es menos ordenado y controlado.</span><span class="sxs-lookup"><span data-stu-id="25312-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="25312-119">Método de **versión** de su almacén de mensajes para esta posibilidad de controlar y realizar un seguimiento de si se ha producido una llamada a **IMAPISupport::StoreLogoffTransports** de escritura.</span><span class="sxs-lookup"><span data-stu-id="25312-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="25312-120">**StoreLogoffTransports** se debe llamar una vez durante el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="25312-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="25312-121">Si detecta en el método de la **versión** que **StoreLogoffTransports** todavía no se ha llamado, invocar con la marca LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="25312-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25312-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="25312-122">See also</span></span>



[<span data-ttu-id="25312-123">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="25312-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

