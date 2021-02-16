---
title: Registro de identificadores únicos del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410178"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="9b4da-103">Registro de identificadores únicos del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="9b4da-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="9b4da-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b4da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b4da-105">La libreta de direcciones, el almacén de mensajes y los proveedores de transporte usan un identificador único conocido como [MAPIUID](mapiuid.md) para registrarse en objetos de servicio de varios tipos.</span><span class="sxs-lookup"><span data-stu-id="9b4da-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="9b4da-106">Un **MAPIUID** es un identificador de 16 bytes que contiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="9b4da-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="9b4da-107">Puede crear un **MAPIUID** mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="9b4da-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="9b4da-108">Definir una constante.</span><span class="sxs-lookup"><span data-stu-id="9b4da-108">Define a constant.</span></span>
    
2. <span data-ttu-id="9b4da-109">Invoque la Visual Studio *Crear GUID*\* .</span><span class="sxs-lookup"><span data-stu-id="9b4da-109">Invoke the Visual Studio *Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="9b4da-110">Por ejemplo, un proveedor de libreta de direcciones puede incluir la siguiente constante en un archivo de encabezado para definir **un MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="9b4da-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="9b4da-111">**Para registrar un MAPIUID si su proveedor es un proveedor de libreta de direcciones o almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="9b4da-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="9b4da-112">Llame [a IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="9b4da-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="9b4da-113">Registre un **MAPIUID** para cada objeto de inicio de sesión del que cree una instancia e incluya **este MAPIUID** en los primeros 16 bytes del miembro **ab** de cada identificador de entrada que cree.</span><span class="sxs-lookup"><span data-stu-id="9b4da-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="9b4da-114">MAPI usa **estructuras MAPIUID** para asociar objetos con proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9b4da-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="9b4da-115">Cuando un cliente llama al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un objeto, MAPI examina la parte **MAPIUID** del identificador de entrada, que coincide con el **MAPIUID** registrado, para determinar qué objeto de inicio de sesión debe recibir la solicitud abierta.</span><span class="sxs-lookup"><span data-stu-id="9b4da-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="9b4da-116">Si el proveedor es un transporte, registre una o más estructuras **MAPIUID** cuando MAPI llame al método **IXPLogon::AddressTypes.**</span><span class="sxs-lookup"><span data-stu-id="9b4da-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="9b4da-117">MAPI usa las **estructuras MAPIUID registradas** por los proveedores de transporte para asignar la responsabilidad de la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9b4da-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="9b4da-118">Aunque los proveedores de servicios suelen registrar un **único MAPIUID,** puede registrar varias **estructuras MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="9b4da-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="9b4da-119">Si su proveedor de libreta de direcciones o almacén de mensajes admite varios objetos de inicio de sesión, quizás al permitir que un usuario agregue más de una instancia del proveedor a su perfil, es posible que desee implementar un **MAPIUID** diferente para cada objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="9b4da-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="9b4da-120">Existen otras razones para admitir más de un **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="9b4da-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="9b4da-121">Debe admitir más de una versión del proveedor y los identificadores de entrada deben representar la versión adecuada.</span><span class="sxs-lookup"><span data-stu-id="9b4da-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="9b4da-122">Asignar un **MAPIUID diferente** para cada versión.</span><span class="sxs-lookup"><span data-stu-id="9b4da-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="9b4da-123">Desea distinguir entre los tipos de objetos que admite.</span><span class="sxs-lookup"><span data-stu-id="9b4da-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="9b4da-124">Por ejemplo, es posible que un proveedor de libreta de direcciones desee registrar un **MAPIUID** para usarlo en los identificadores de entrada de sus objetos de usuario de mensajería y un **MAPIUID** diferente para usar para listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="9b4da-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="9b4da-125">Cuando hay varios objetos de inicio de sesión que están activos simultáneamente, tiene sentido tener estructuras **MAPIUID** únicas para cada uno.</span><span class="sxs-lookup"><span data-stu-id="9b4da-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="9b4da-126">Esto aumenta la precisión con la que MAPI coincide con los identificadores de entrada de los proveedores de servicios y ahorra trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b4da-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="9b4da-127">Cuando cada objeto de inicio de sesión tiene su propio identificador único, MAPI puede garantizar que cualquier solicitud que enruta a un objeto de inicio de sesión puede ser manejada por ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9b4da-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="9b4da-128">Cuando los objetos de inicio de sesión comparten estructuras **MAPIUID,** MAPI enruta la solicitud al primer objeto de inicio de sesión identificado por **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="9b4da-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="9b4da-129">Si uno de los objetos de inicio de sesión recibe una solicitud que no puede procesar porque no controla el identificador de entrada, pase la solicitud al siguiente objeto de inicio de sesión antes de devolver un error.</span><span class="sxs-lookup"><span data-stu-id="9b4da-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b4da-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b4da-130">See also</span></span>



[<span data-ttu-id="9b4da-131">Implementación del inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="9b4da-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

