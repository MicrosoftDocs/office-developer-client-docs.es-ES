---
title: Información sobre la API de replicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816351"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="264d6-103">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="264d6-103">About the Replication API</span></span>

  
  
<span data-ttu-id="264d6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="264d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="264d6-105">La API de replicación proporciona la funcionalidad para un proveedor de almacén de mensajes MAPI sincronizar los elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local privado basada en .pst que se crea para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="264d6-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="264d6-106">Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación según las instrucciones en [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="264d6-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="264d6-107">El proveedor debe usar la API sólo en un almacén personal creado para sí mismo y no en almacenes personales creados para otros proveedores, debido a que los almacenes de personal crean para otros proveedores es posible que ya ha configurado sus propios mecanismos de replicación con el servidor respectivo.</span><span class="sxs-lookup"><span data-stu-id="264d6-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="264d6-108">Por ejemplo, un archivo de carpetas sin conexión (.ost) mantiene su propia relación de replicación con un servidor de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="264d6-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="264d6-109">Para usar la API de replicación, un proveedor de almacén de mensajes MAPI en primer lugar debe abrir y se ajusta a un almacén local basada en .pst mediante una llamada a **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="264d6-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="264d6-110">El proveedor, a continuación, puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación.</span><span class="sxs-lookup"><span data-stu-id="264d6-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="264d6-111">**IPSTX** se proporciona mediante la consulta en [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), y **IOSTX** es proporcionado por **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="264d6-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="264d6-112">La interfaz de IOSTX</span><span class="sxs-lookup"><span data-stu-id="264d6-112">The IOSTX Interface</span></span>

<span data-ttu-id="264d6-113">La interfaz **IOSTX** es la interfaz principal que realiza la sincronización de la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="264d6-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="264d6-114">**IOSTX** mueve el almacén local a través de una serie de Estados, recuperación de información de cada estado acerca de los cambios en el almacén local, así como para informar el almacén local de los cambios realizados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="264d6-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="264d6-115">La API de replicación especifica también muchas de las estructuras de datos que admiten la sincronización.</span><span class="sxs-lookup"><span data-stu-id="264d6-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="264d6-116">Un proveedor de almacenamiento, como un cliente a esta API, usa la API de replicación para ajustar el almacén local y mover a través de estos Estados, e inserta los cambios en el almacén local (por ejemplo, los cambios en la jerarquía de carpetas o la adición de nuevos elementos) para el servidor y también recuperar información acerca de los cambios en el servidor y proporcionar esa información a la interfaz **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="264d6-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="264d6-117">La interfaz de **IOSTX** adopta la sincronización de cambio Incremental (ICS) proporcionado por Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="264d6-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="264d6-118">Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="264d6-118">For more information about ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="264d6-119">A través de **IOSTX**, el cliente utiliza ICS para supervisar y sincronizar los cambios incrementales en la jerarquía o el contenido en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="264d6-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="264d6-120">La interfaz de IPSTX</span><span class="sxs-lookup"><span data-stu-id="264d6-120">The IPSTX Interface</span></span>

 <span data-ttu-id="264d6-121">**IPSTX** y cinco otro ** IPSTX *n* ** las interfaces que heredan de **IPSTX** proporcionan funciones auxiliares que se pueden usar al realizar la replicación a través de la interfaz **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="264d6-121">**IPSTX** and five other **IPSTX *n* ** interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="264d6-122">Por ejemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permite que el almacén local emular al administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.</span><span class="sxs-lookup"><span data-stu-id="264d6-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="264d6-123">Para obtener más información acerca de las transiciones de estado durante la replicación, vea [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="264d6-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="264d6-124">La API de replicación</span><span class="sxs-lookup"><span data-stu-id="264d6-124">The Replication API</span></span>

<span data-ttu-id="264d6-125">La API de replicación proporciona las definiciones, tipos de datos e interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="264d6-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="264d6-126">Para una implementación de ejemplo de un proveedor de almacén de archivos de carpetas personales (PST) ajustados, vea [Acerca de ejemplo ajustado PST almacenar proveedor](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="264d6-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="264d6-127">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="264d6-127">Definitions:</span></span>
  
- [<span data-ttu-id="264d6-128">Constantes de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="264d6-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="264d6-129">Funciones:</span><span class="sxs-lookup"><span data-stu-id="264d6-129">Functions:</span></span>
  
- <span data-ttu-id="264d6-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="264d6-131">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="264d6-131">Data types:</span></span>
  
- <span data-ttu-id="264d6-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="264d6-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="264d6-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="264d6-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="264d6-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="264d6-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="264d6-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="264d6-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="264d6-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="264d6-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="264d6-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="264d6-143">**[ESTADO DE SINCRONIZACIÓN](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="264d6-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="264d6-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="264d6-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="264d6-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="264d6-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="264d6-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="264d6-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="264d6-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="264d6-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="264d6-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="264d6-154">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="264d6-154">Interfaces:</span></span>
  
- <span data-ttu-id="264d6-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="264d6-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="264d6-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="264d6-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="264d6-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="264d6-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="264d6-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="264d6-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

