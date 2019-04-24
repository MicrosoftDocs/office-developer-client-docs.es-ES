---
title: Cerrar un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339210"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="8f703-103">Cerrar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="8f703-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="8f703-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f703-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f703-105">Cuando un cliente llama al método [IMAPISession:: Logoff](imapisession-logoff.md) para finalizar la sesión y cerrar todos los proveedores de servicios activos, MAPI a su vez llama a los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="8f703-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="8f703-106">[IABLogon:: Logoff](iablogon-logoff.md) para los proveedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8f703-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="8f703-107">[IMSLogon:: Logoff](imslogon-logoff.md) para proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8f703-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="8f703-108">[IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) para proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="8f703-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="8f703-109">Estos métodos tienen implementaciones similares.</span><span class="sxs-lookup"><span data-stu-id="8f703-109">These methods have similar implementations.</span></span> <span data-ttu-id="8f703-110">Las tareas principales que realiza un método Logoff son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f703-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="8f703-111">Liberar todos los objetos abiertos, incluidos los objetos subobjetos y de estado.</span><span class="sxs-lookup"><span data-stu-id="8f703-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="8f703-112">Llamar al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto support para disminuir su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="8f703-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="8f703-113">Quitar todas las estructuras [MAPIUID](mapiuid.md) registradas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f703-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="8f703-114">Quitar la fila del proveedor en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="8f703-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="8f703-115">Realizar las tareas relacionadas con la limpieza de recursos, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f703-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="8f703-116">Terminar una conexión con un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="8f703-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="8f703-117">Disminuye el recuento de referencia en el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8f703-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="8f703-118">Quitar el objeto de inicio de sesión de la lista de objetos de inicio de sesión que su proveedor almacena.</span><span class="sxs-lookup"><span data-stu-id="8f703-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="8f703-119">En modo de depuración, emitir seguimientos para localizar objetos que han perdido memoria.</span><span class="sxs-lookup"><span data-stu-id="8f703-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="8f703-120">Cuando vuelve el método logoff, MAPI llama a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8f703-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="8f703-121">El método **IUnknown:: Release** del objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8f703-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="8f703-122">El método **Shutdown** del objeto de proveedor para realizar cualquier tarea final de limpieza.</span><span class="sxs-lookup"><span data-stu-id="8f703-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="8f703-123">Según el tipo de proveedor, se llama a uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="8f703-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="8f703-124">[IABProvider:: Shutdown](iabprovider-shutdown.md) para proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="8f703-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="8f703-125">[IMSProvider:: Shutdown](imsprovider-shutdown.md) para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="8f703-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="8f703-126">[IXPProvider:: Shutdown](ixpprovider-shutdown.md) para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="8f703-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="8f703-127">El método **IUnknown:: Release** del objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f703-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="8f703-128">Si su proveedor es un almacén de mensajes, una llamada de cliente a [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) también iniciará el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="8f703-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="8f703-129">**StoreLogoff** cierra un proveedor de almacenamiento de mensajes determinado y no tiene ningún efecto en la sesión.</span><span class="sxs-lookup"><span data-stu-id="8f703-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="8f703-130">Solo se puede apagar un proveedor de almacenamiento de mensajes con este método; no hay una forma explícita de cerrar una libreta de direcciones o un proveedor de transporte en particular.</span><span class="sxs-lookup"><span data-stu-id="8f703-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="8f703-131">Para obtener información sobre cómo responder a una llamada de **StoreLogoff** , vea el apartado sobre cómo [apagar un proveedor de almacén de mensajes](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f703-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="8f703-132">La DLL del proveedor se descargará cuando MAPI llame a la función **FreeLibrary**de la API de Win32, una llamada que se realiza después de que el último cliente activo haya llamado a [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="8f703-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="8f703-133">En este momento, el proveedor de servicios habrá terminado de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="8f703-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f703-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f703-134">See also</span></span>



[<span data-ttu-id="8f703-135">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="8f703-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

