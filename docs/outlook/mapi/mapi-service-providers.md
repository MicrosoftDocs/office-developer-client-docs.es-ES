---
title: Proveedores de servicios de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571909"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="ebb24-103">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb24-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="ebb24-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebb24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebb24-105">Hay tres tipos comunes de proveedores de servicios:</span><span class="sxs-lookup"><span data-stu-id="ebb24-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="ebb24-106">Los proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ebb24-106">Address book providers.</span></span>
    
- <span data-ttu-id="ebb24-107">Proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ebb24-107">Message store providers.</span></span>
    
- <span data-ttu-id="ebb24-108">Los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="ebb24-108">Transport providers.</span></span>
    
<span data-ttu-id="ebb24-109">Proveedores de almacén de libreta de direcciones y el mensaje de dirección tienen muchas similitudes.</span><span class="sxs-lookup"><span data-stu-id="ebb24-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="ebb24-110">Registrar a un identificador único MAPI que usa para construir los identificadores de entrada para sus objetos.</span><span class="sxs-lookup"><span data-stu-id="ebb24-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="ebb24-111">Proporcionan una jerarquía de objetos y propiedades que los clientes pueden obtener acceso y manipular.</span><span class="sxs-lookup"><span data-stu-id="ebb24-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="ebb24-112">Para sus objetos del contenedor, que admiten una tabla de jerarquías y una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ebb24-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="ebb24-113">Admite la notificación de eventos en estas tablas y, opcionalmente, en los objetos individuales para que los clientes pueden estar informados de los cambios que se producen durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="ebb24-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="ebb24-114">Cuando se convierten en operaciones prolongadas, puede mostrar un indicador de progreso para informar al usuario del estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ebb24-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="ebb24-115">Los clientes pueden comunicarse con los proveedores de almacén de libreta de direcciones y el mensaje de dirección puede ser MAPI indirectamente a través mediante el uso de la [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) y [IMAPISession: IUnknown](imapisessioniunknown.md) interfaces o directamente mediante una de las interfaces de proveedor de servicio en el tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ebb24-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="ebb24-116">**Interfaces del proveedor de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="ebb24-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="ebb24-117">**Interfaces del proveedor de almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="ebb24-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebb24-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ebb24-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="ebb24-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebb24-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="ebb24-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ebb24-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="ebb24-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ebb24-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="ebb24-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebb24-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="ebb24-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebb24-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="ebb24-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebb24-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="ebb24-125">Los proveedores de transporte difieren de dirección libreta de direcciones y el mensaje de los proveedores de almacén de la manera en que se comunican con MAPI y con los clientes.</span><span class="sxs-lookup"><span data-stu-id="ebb24-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="ebb24-126">Los proveedores de transporte normalmente espere de MAPI pedir información en lugar de iniciar la comunicación.</span><span class="sxs-lookup"><span data-stu-id="ebb24-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="ebb24-127">A diferencia de los otros proveedores, los proveedores de transporte no admite una gran variedad de objetos y las tablas que se tiene acceso con frecuencia por los clientes.</span><span class="sxs-lookup"><span data-stu-id="ebb24-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="ebb24-128">Sin embargo, son compatibles con un objeto de estado, tal y como no todos los proveedores de servicios y publicar sus propiedades en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="ebb24-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="ebb24-129">Mientras que los proveedores de almacén de libreta de direcciones y el mensaje de dirección llamar al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar los identificadores únicos para construir sus identificadores de entrada, los proveedores de transporte llame al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para Registrar identificadores únicos, así como los tipos de direcciones para que asume la responsabilidad de la entrega de mensajes determinados.</span><span class="sxs-lookup"><span data-stu-id="ebb24-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="ebb24-130">Su proveedor de servicios debe tener tres archivos de encabezado: un archivo de encabezado público y dos archivos internos.</span><span class="sxs-lookup"><span data-stu-id="ebb24-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="ebb24-131">Usar el archivo de encabezado pública para la configuración y para documentar las propiedades y sus valores.</span><span class="sxs-lookup"><span data-stu-id="ebb24-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="ebb24-132">Incluir en uno de los archivos de encabezado interno todos los los necesarios pública MAPI encabezados; Este archivo de encabezado debe incluirse en todos los archivos de origen del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="ebb24-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="ebb24-133">Utilice el otro archivo interno para definir los identificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebb24-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="ebb24-134">Libreta de direcciones, almacén de mensajes y los proveedores de transporte realizan las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="ebb24-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="ebb24-135">Proporcionar una función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ebb24-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="ebb24-136">Proporcionar un proveedor y el objeto de inicio de sesión para controlar el inicio de sesión y la inicialización.</span><span class="sxs-lookup"><span data-stu-id="ebb24-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="ebb24-137">Si el proveedor pertenece a un servicio de mensajes, proporcionar una función de punto de entrada de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ebb24-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="ebb24-138">Admite la configuración mediante la implementación de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ebb24-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="ebb24-139">Implementar un objeto de estado y admitir la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="ebb24-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="ebb24-140">Controlador de apagado.</span><span class="sxs-lookup"><span data-stu-id="ebb24-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebb24-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ebb24-141">See also</span></span>



[<span data-ttu-id="ebb24-142">Conceptos MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb24-142">MAPI Concepts</span></span>](mapi-concepts.md)

