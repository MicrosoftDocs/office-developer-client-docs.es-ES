---
title: Apagar un proveedor de servicios
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
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="d2ca9-103">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="d2ca9-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="d2ca9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ca9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ca9-105">Cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar la sesión y apagar todos los proveedores de servicios activos, MAPI a su vez llama a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="d2ca9-106">[IABLogon::Logoff para](iablogon-logoff.md) proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="d2ca9-107">[IMSLogon::Logoff para](imslogon-logoff.md) proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="d2ca9-108">[IXPLogon::TransportLogoff para](ixplogon-transportlogoff.md) proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="d2ca9-109">Estos métodos tienen implementaciones similares.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-109">These methods have similar implementations.</span></span> <span data-ttu-id="d2ca9-110">Las tareas principales que realiza un método de cierre de sesión son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="d2ca9-111">Liberar todos los objetos abiertos, incluidos los subobjetos y los objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="d2ca9-112">Llamar al método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para disminuir su recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="d2ca9-113">Quitar todas las estructuras [MAPIUID](mapiuid.md) registradas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="d2ca9-114">Quitar la fila del proveedor en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="d2ca9-115">Realizar cualquier tarea relacionada con la limpieza de recursos, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="d2ca9-116">Terminación de una conexión con un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="d2ca9-117">Disminuir el número de referencias en el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="d2ca9-118">Quitar el objeto de inicio de sesión de la lista de objetos de inicio de sesión que almacena el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="d2ca9-119">En modo de depuración, emitiendo seguimientos para localizar objetos que tienen pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="d2ca9-120">Cuando el método de cierre de sesión devuelve, MAPI llama a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="d2ca9-121">El método **IUnknown::Release** del objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="d2ca9-122">Método Shutdown del objeto **de** proveedor para realizar las tareas de limpieza finales.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="d2ca9-123">Según el tipo de proveedor, se llama a uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="d2ca9-124">[IABProvider::Shutdown](iabprovider-shutdown.md) para proveedores de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d2ca9-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="d2ca9-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) para proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="d2ca9-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="d2ca9-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="d2ca9-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="d2ca9-127">Método **IUnknown::Release** del objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="d2ca9-128">Si el proveedor es un almacén de mensajes, una llamada de cliente a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) también iniciará el proceso de apagado.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="d2ca9-129">**StoreLogoff** cierra un proveedor de almacén de mensajes en particular y no tiene ningún efecto en la sesión.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="d2ca9-130">Solo se puede cerrar un proveedor de almacén de mensajes con este método; no hay ninguna forma explícita de cerrar una libreta de direcciones o un proveedor de transporte en particular.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="d2ca9-131">Para obtener información sobre cómo responder a una llamada **a StoreLogoff,** vea [Apagar un proveedor de almacén de mensajes](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d2ca9-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="d2ca9-132">La DLL del proveedor se descargará cuando MAPI llame a la función de API de Win32 **FreeLibrary**, una llamada que se realiza después de que el último cliente activo haya llamado [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="d2ca9-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="d2ca9-133">Para este momento, el proveedor de servicios habrá terminado de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2ca9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2ca9-134">See also</span></span>



[<span data-ttu-id="d2ca9-135">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ca9-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

