---
title: Subprocesos en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820859"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="d02c0-103">Subprocesos en MAPI</span><span class="sxs-lookup"><span data-stu-id="d02c0-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="d02c0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d02c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d02c0-105">Un subproceso es la entidad básica a la que el sistema operativo asigna tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="d02c0-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="d02c0-106">Un subproceso tiene su propio registros, la pila, la prioridad y el almacenamiento, pero comparte una dirección espacio y el proceso de los recursos, como los tokens de acceso.</span><span class="sxs-lookup"><span data-stu-id="d02c0-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="d02c0-107">Los subprocesos comparten también memoria, con lo que haya escrito otro subproceso de lectura de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="d02c0-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="d02c0-108">Los clientes MAPI usan los siguientes modelos de subprocesamiento genéricos.</span><span class="sxs-lookup"><span data-stu-id="d02c0-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="d02c0-109">**Modelo de subprocesos**</span><span class="sxs-lookup"><span data-stu-id="d02c0-109">**Threading model**</span></span>|<span data-ttu-id="d02c0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d02c0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d02c0-111">Modelo de subprocesamiento único</span><span class="sxs-lookup"><span data-stu-id="d02c0-111">Single threading model</span></span>  <br/> |<span data-ttu-id="d02c0-112">Todos los objetos se usan en el único subproceso.</span><span class="sxs-lookup"><span data-stu-id="d02c0-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="d02c0-113">Modelo de subprocesamiento controlado</span><span class="sxs-lookup"><span data-stu-id="d02c0-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="d02c0-114">Un objeto puede usarse solo en el subproceso que lo creó.</span><span class="sxs-lookup"><span data-stu-id="d02c0-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="d02c0-115">Modelo de subprocesamiento libre o subproceso de terceros</span><span class="sxs-lookup"><span data-stu-id="d02c0-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="d02c0-116">Un objeto puede usarse en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="d02c0-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="d02c0-117">MAPI utiliza el modelo de subprocesamiento libre, compatibilidad con objetos de subprocesos que se pueden usar en cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="d02c0-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="d02c0-118">OLE utiliza el modelo de subprocesamiento controlado.</span><span class="sxs-lookup"><span data-stu-id="d02c0-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="d02c0-119">El modelo de subprocesos de apartamento es compatible con los objetos que se deben transferir explícitamente cuando un subproceso distinto del que creó el objeto necesita utilizar ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d02c0-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="d02c0-120">El mecanismo que utiliza OLE para transferir los objetos de un subproceso a otro se conoce como cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="d02c0-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="d02c0-121">El cálculo de referencias implica un objeto de código auxiliar y un objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="d02c0-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="d02c0-122">Estos objetos especiales empaquetar los parámetros de la interfaz en el objeto se puede ordenar, transferir estos parámetros para el otro subproceso y desempaquetar ellos a su llegada.</span><span class="sxs-lookup"><span data-stu-id="d02c0-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="d02c0-123">Conflicto entre los dos modelos de multiproceso se produce cuando se envía un objeto MAPI subprocesamiento libre a otro proceso con OLE "ligero" llamada a procedimiento remoto o LRPC.</span><span class="sxs-lookup"><span data-stu-id="d02c0-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="d02c0-124">LRPC cambia semántica del objeto de subprocesamiento libre para subprocesamiento controlado por interpone interfaces de proxy y código auxiliar con comportamiento entre el objeto y su autor de la llamada de subprocesamiento controlado.</span><span class="sxs-lookup"><span data-stu-id="d02c0-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="d02c0-125">Conocimiento de las situaciones en MAPI que conducen a este conflicto puede ayudar a los clientes y proveedores de servicios de impedir que se produzca problemas.</span><span class="sxs-lookup"><span data-stu-id="d02c0-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="d02c0-126">Puede tener acceso a un objeto MAPI:</span><span class="sxs-lookup"><span data-stu-id="d02c0-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="d02c0-127">A través de llamadas directas a sus métodos mediante una interfaz de puntero devuelto por un proveedor de servicios o MAPI vinculadas al proceso del cliente, como el objeto de sesión devuelto desde [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="d02c0-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="d02c0-128">A través de llamadas indirectas a sus métodos con un puntero de interfaz devuelto por cualquier proveedor de servicios, como el objeto de carpeta copió desde otra carpeta en [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="d02c0-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="d02c0-129">A través de una función de devolución de llamada, como el método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pasada a un proveedor de servicios o a MAPI en una llamada **Advise** o los métodos que pueden mostrar el progreso de una operación prolongada.</span><span class="sxs-lookup"><span data-stu-id="d02c0-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

