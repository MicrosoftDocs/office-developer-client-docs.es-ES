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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395178"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="c85e0-103">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="c85e0-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="c85e0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c85e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c85e0-105">Cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar la sesión y apagar todos los proveedores de servicio de active, MAPI a su vez llama a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c85e0-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="c85e0-106">[IABLogon::Logoff](iablogon-logoff.md) para los proveedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c85e0-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="c85e0-107">[IMSLogon::Logoff](imslogon-logoff.md) para los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c85e0-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="c85e0-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="c85e0-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="c85e0-109">Estos métodos tienen implementaciones similar.</span><span class="sxs-lookup"><span data-stu-id="c85e0-109">These methods have similar implementations.</span></span> <span data-ttu-id="c85e0-110">Las principales tareas que realiza un método de cierre de sesión son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c85e0-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="c85e0-111">Liberación de todos los objetos abiertos, incluidos los subobjetos y objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="c85e0-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="c85e0-112">Llamar al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para reducir su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="c85e0-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="c85e0-113">Eliminación de todas las estructuras [MAPIUID](mapiuid.md) registradas de su proveedor de.</span><span class="sxs-lookup"><span data-stu-id="c85e0-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="c85e0-114">Eliminación de fila de su proveedor en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="c85e0-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="c85e0-115">Llevar a cabo las tareas relacionadas con la limpieza de recursos, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c85e0-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="c85e0-116">Finalización de una conexión con un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="c85e0-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="c85e0-117">Disminuir la referencia de recuento en el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c85e0-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="c85e0-118">Quitar el objeto de inicio de sesión de la lista de objetos de inicio de sesión que almacena su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c85e0-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="c85e0-119">En el modo de depuración, emitir seguimientos para localizar los objetos que se han perdido la memoria.</span><span class="sxs-lookup"><span data-stu-id="c85e0-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="c85e0-120">Cuando se devuelve el método de cierre de sesión, MAPI llama a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c85e0-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="c85e0-121">Método de **IUnknown:: Release** del objeto su inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c85e0-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="c85e0-122">Método de **cierre** del objeto de su proveedor para llevar a cabo las tareas de limpieza final.</span><span class="sxs-lookup"><span data-stu-id="c85e0-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="c85e0-123">Según el tipo de su proveedor, se llama uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c85e0-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="c85e0-124">[IABProvider::Shutdown](iabprovider-shutdown.md) para los proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="c85e0-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="c85e0-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) para los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c85e0-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="c85e0-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) para los proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="c85e0-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="c85e0-127">Método de **IUnknown:: Release** del objeto de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c85e0-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="c85e0-128">Si su proveedor es un almacén de mensajes, una llamada de cliente a [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) también iniciará el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="c85e0-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="c85e0-129">**StoreLogoff** cierra un proveedor de almacén de mensaje concreto y no tiene ningún efecto en la sesión.</span><span class="sxs-lookup"><span data-stu-id="c85e0-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="c85e0-130">Solo un proveedor de almacén de mensajes se puede cerrar con este método; No hay ninguna forma explícita para cerrar un proveedor de transporte o de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="c85e0-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="c85e0-131">Para obtener información acerca de cómo responder a una **StoreLogoff** de llamadas, vea [Cerrando hacia abajo un mensaje de proveedor de almacenamiento](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c85e0-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="c85e0-132">Archivo DLL de su proveedor se descargará cuando llama a la función API de Win32 **FreeLibrary**, una llamada que se realiza después de que el último cliente activo ha llamado [MAPIUninitialize](mapiuninitialize.md)MAPI.</span><span class="sxs-lookup"><span data-stu-id="c85e0-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="c85e0-133">En este momento, su proveedor de servicios habrá terminado de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="c85e0-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c85e0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c85e0-134">See also</span></span>



[<span data-ttu-id="c85e0-135">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="c85e0-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

