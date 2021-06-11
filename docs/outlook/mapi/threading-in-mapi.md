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
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405544"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="522bd-103">Subprocesos en MAPI</span><span class="sxs-lookup"><span data-stu-id="522bd-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="522bd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="522bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="522bd-105">Un subproceso es la entidad básica a la que un sistema operativo asigna tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="522bd-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="522bd-106">Un subproceso tiene sus propios registros, pila, prioridad y almacenamiento, pero comparte un espacio de direcciones y recursos de proceso como tokens de acceso.</span><span class="sxs-lookup"><span data-stu-id="522bd-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="522bd-107">Los subprocesos también comparten memoria, con un subproceso que lee lo que otro subproceso ha escrito.</span><span class="sxs-lookup"><span data-stu-id="522bd-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="522bd-108">Los clientes MAPI usan los siguientes modelos de subprocesos genéricos.</span><span class="sxs-lookup"><span data-stu-id="522bd-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="522bd-109">**Modelo de subprocesos**</span><span class="sxs-lookup"><span data-stu-id="522bd-109">**Threading model**</span></span>|<span data-ttu-id="522bd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="522bd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="522bd-111">Modelo de subproceso único</span><span class="sxs-lookup"><span data-stu-id="522bd-111">Single threading model</span></span>  <br/> |<span data-ttu-id="522bd-112">Todos los objetos se usan en el único subproceso.</span><span class="sxs-lookup"><span data-stu-id="522bd-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="522bd-113">Modelo de subprocesos de departamentos</span><span class="sxs-lookup"><span data-stu-id="522bd-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="522bd-114">Un objeto solo se puede usar en el subproceso que lo creó.</span><span class="sxs-lookup"><span data-stu-id="522bd-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="522bd-115">Modelo de subprocesos gratuitos o de grupo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="522bd-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="522bd-116">Se puede usar un objeto en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="522bd-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="522bd-117">MAPI usa el modelo de subprocesos gratuitos, que admite objetos seguros para subprocesos que se pueden usar en cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="522bd-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="522bd-118">OLE usa el modelo de subprocesos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="522bd-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="522bd-119">El modelo de subprocesos de departamentos admite objetos que deben transferirse explícitamente cuando un subproceso distinto del que creó el objeto necesita usar ese objeto.</span><span class="sxs-lookup"><span data-stu-id="522bd-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="522bd-120">El mecanismo que OLE usa para transferir objetos de un subproceso a otro se conoce como cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="522bd-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="522bd-121">El cálculo de referencias implica un objeto stub y un objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="522bd-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="522bd-122">Estos objetos especiales empaquetan los parámetros de la interfaz del objeto que se va a calcular, transfieren estos parámetros al otro subproceso y los desenvasan al llegar.</span><span class="sxs-lookup"><span data-stu-id="522bd-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="522bd-123">El conflicto entre los dos modelos multiproceso se produce cuando se envía un objeto MAPI de subproceso libre a otro proceso mediante llamada a procedimiento remoto "ligera" OLE o LRPC.</span><span class="sxs-lookup"><span data-stu-id="522bd-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="522bd-124">LRPC cambia la semántica del objeto de subprocesos libres a subprocesos de departamentos mediante la interposición de interfaces de código auxiliar y proxy con el comportamiento de subproceso de apartamento entre el objeto y su autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="522bd-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="522bd-125">El conocimiento de las situaciones en MAPI que llevan a este conflicto puede ayudar a los clientes y proveedores de servicios a evitar que se produzcan problemas.</span><span class="sxs-lookup"><span data-stu-id="522bd-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="522bd-126">Se puede obtener acceso a un objeto MAPI:</span><span class="sxs-lookup"><span data-stu-id="522bd-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="522bd-127">A través de llamadas directas a sus métodos mediante un puntero de interfaz devuelto por un proveedor de servicios o MAPI vinculado al proceso del cliente, como el objeto de sesión devuelto de [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="522bd-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="522bd-128">A través de llamadas indirectas a sus métodos mediante un puntero de interfaz devuelto por cualquier proveedor de servicios, como el objeto folder copiado de otra carpeta en [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="522bd-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="522bd-129">A través de una función de devolución de llamada, como el método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pasado a un proveedor de servicios o a MAPI en una llamada **Advise** o los métodos que pueden mostrar el progreso de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="522bd-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

