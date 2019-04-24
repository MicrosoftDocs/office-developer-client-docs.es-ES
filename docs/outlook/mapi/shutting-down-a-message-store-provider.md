---
title: Apagar un proveedor de almacenamiento de mensajes
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
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="f6a18-103">Apagar un proveedor de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="f6a18-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="f6a18-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6a18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6a18-105">Si su proveedor es un proveedor de almacenamiento de mensajes, se puede cerrar de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="f6a18-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="f6a18-106">Cuando un cliente o la cola MAPI llama a [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="f6a18-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="f6a18-107">Al apagar un proveedor de almacenamiento de mensajes con **StoreLogoff** , el apagado se produce de forma ordenada y controlada.</span><span class="sxs-lookup"><span data-stu-id="f6a18-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="f6a18-108">Cuando un cliente llama a [IMAPISession:: Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="f6a18-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="f6a18-109">La implementación de **IMsgStore:: StoreLogoff** debe empezar por llamar a [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar a MAPI de que se está cerrando, lo que indica que se debe cerrar la sesión de todos los proveedores de transporte relacionados.</span><span class="sxs-lookup"><span data-stu-id="f6a18-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="f6a18-110">Cuando **IMsgStore:: StoreLogoff** devuelve, su autor de la llamada invoca el método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6a18-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="f6a18-111">Implemente este método de **lanzamiento** llamando al método **IUnknown:: Release** del objeto support.</span><span class="sxs-lookup"><span data-stu-id="f6a18-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="f6a18-112">MAPI realiza las siguientes tareas en su implementación de **IUnknown:: Release** para los almacenes de mensajes:</span><span class="sxs-lookup"><span data-stu-id="f6a18-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="f6a18-113">Quita todas las estructuras [MAPIUID](mapiuid.md) registradas por el proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6a18-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="f6a18-114">Quita la fila del proveedor de almacenamiento de mensajes de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="f6a18-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="f6a18-115">Llama a [IMSLogon:: Logoff](imslogon-logoff.md) para liberar todos los objetos, los subobjetos y los objetos de estado abiertos.</span><span class="sxs-lookup"><span data-stu-id="f6a18-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="f6a18-116">Llama a [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto de inicio de sesión del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6a18-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="f6a18-117">Algunos clientes pueden omitir la llamada a **IMsgStore:: StoreLogoff**, lo que inicia el cierre del proveedor de almacenamiento de mensajes con la llamada al método **IUnknown:: Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6a18-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="f6a18-118">Un cierre en estas circunstancias sin la llamada a **StoreLogoff** es menos ordenado y controlado.</span><span class="sxs-lookup"><span data-stu-id="f6a18-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="f6a18-119">Escriba el método de **liberación** del almacén de mensajes para controlar esta posibilidad y realizar un seguimiento de si se ha producido o no una llamada a **IMAPISupport:: StoreLogoffTransports** .</span><span class="sxs-lookup"><span data-stu-id="f6a18-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="f6a18-120">**StoreLogoffTransports** debe llamarse una vez durante el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="f6a18-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="f6a18-121">Si detecta en su método de **liberación** que todavía no se ha llamado a **StoreLogoffTransports** , lo invoca con la marca LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="f6a18-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6a18-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6a18-122">See also</span></span>



[<span data-ttu-id="f6a18-123">Cerrar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="f6a18-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

