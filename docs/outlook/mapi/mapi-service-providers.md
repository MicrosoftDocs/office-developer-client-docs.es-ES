---
title: Proveedores de servicios MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346679"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="d25a1-103">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="d25a1-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="d25a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d25a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d25a1-105">Hay tres tipos comunes de proveedores de servicios:</span><span class="sxs-lookup"><span data-stu-id="d25a1-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="d25a1-106">Proveedores de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d25a1-106">Address book providers.</span></span>
    
- <span data-ttu-id="d25a1-107">Proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d25a1-107">Message store providers.</span></span>
    
- <span data-ttu-id="d25a1-108">Proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="d25a1-108">Transport providers.</span></span>
    
<span data-ttu-id="d25a1-109">La libreta de direcciones y los proveedores de almacenamiento de mensajes tienen muchas similitudes.</span><span class="sxs-lookup"><span data-stu-id="d25a1-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="d25a1-110">Registran un identificador único con MAPI que usan para crear identificadores de entrada para sus objetos.</span><span class="sxs-lookup"><span data-stu-id="d25a1-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="d25a1-111">Proporcionan una jerarquía de objetos y propiedades a las que los clientes pueden tener acceso y manipular.</span><span class="sxs-lookup"><span data-stu-id="d25a1-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="d25a1-112">Para sus objetos container, admiten una tabla de jerarquía y una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="d25a1-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="d25a1-113">Admiten la notificación de eventos en estas tablas y, opcionalmente, en objetos individuales para que se pueda informar a los clientes de los cambios que se producen durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="d25a1-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="d25a1-114">Cuando las operaciones se convierten en largas, pueden mostrar un indicador de progreso para informar al usuario del estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d25a1-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="d25a1-115">Los clientes pueden comunicarse con los proveedores de almacenamiento de mensajes y la libreta de direcciones indirectamente a través de MAPI mediante el uso de las interfaces [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) y [IMAPISession: IUnknown](imapisessioniunknown.md) o directamente mediante una de las interfaces del proveedor de servicios en el siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d25a1-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="d25a1-116">**Interfaces del proveedor de libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="d25a1-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="d25a1-117">**Interfaces de proveedor de almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="d25a1-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d25a1-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d25a1-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="d25a1-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d25a1-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="d25a1-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d25a1-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="d25a1-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d25a1-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="d25a1-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d25a1-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="d25a1-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d25a1-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="d25a1-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d25a1-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="d25a1-125">Los proveedores de transporte difieren de la libreta de direcciones y los proveedores de almacenamiento de mensajes en la forma en que se comunican con MAPI y con los clientes.</span><span class="sxs-lookup"><span data-stu-id="d25a1-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="d25a1-126">Los proveedores de transporte suelen esperar a que MAPI les pida información en lugar de iniciar la comunicación.</span><span class="sxs-lookup"><span data-stu-id="d25a1-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="d25a1-127">A diferencia de los demás proveedores, los proveedores de transporte no admiten una variedad de objetos y tablas a los que los clientes acceden con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="d25a1-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="d25a1-128">Sin embargo, admiten un objeto de estado, al igual que todos los proveedores de servicios, y publican sus propiedades en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="d25a1-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="d25a1-129">Mientras que la libreta de direcciones y los proveedores de almacenamiento de mensajes llaman al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores únicos para construir sus identificadores de entrada, los proveedores de transporte llaman al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para Registre identificadores únicos, así como tipos de direcciones para asumir la responsabilidad de la entrega de mensajes concretos.</span><span class="sxs-lookup"><span data-stu-id="d25a1-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="d25a1-130">El proveedor de servicios debe tener tres archivos de encabezado: un archivo de encabezado público y dos archivos internos.</span><span class="sxs-lookup"><span data-stu-id="d25a1-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="d25a1-131">Use el archivo de encabezado público para la configuración y documentar las propiedades y sus valores.</span><span class="sxs-lookup"><span data-stu-id="d25a1-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="d25a1-132">Incluya en uno de los archivos de encabezado internos todos los encabezados MAPI públicos necesarios; este archivo de encabezado debe incluirse en todos los archivos de origen del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d25a1-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="d25a1-133">Use el otro archivo interno para definir los identificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="d25a1-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="d25a1-134">La libreta de direcciones, el almacén de mensajes y los proveedores de transporte realizan las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d25a1-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="d25a1-135">Proporcione una función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d25a1-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="d25a1-136">Proporcione un proveedor y un objeto de inicio de sesión para controlar el inicio de sesión y la inicialización.</span><span class="sxs-lookup"><span data-stu-id="d25a1-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="d25a1-137">Si el proveedor pertenece a un servicio de mensajes, suministre una función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d25a1-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="d25a1-138">Admite la configuración mediante la implementación de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d25a1-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="d25a1-139">Implemente un objeto de estado y admita la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="d25a1-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="d25a1-140">Controlar el cierre.</span><span class="sxs-lookup"><span data-stu-id="d25a1-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d25a1-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d25a1-141">See also</span></span>



[<span data-ttu-id="d25a1-142">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="d25a1-142">MAPI Concepts</span></span>](mapi-concepts.md)

