---
title: Información sobre la API de replicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329522"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="30532-103">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="30532-103">About the Replication API</span></span>

  
  
<span data-ttu-id="30532-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30532-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30532-105">La API de replicación proporciona la funcionalidad necesaria para que un proveedor de almacén de mensajes MAPI sincronice los elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local basado en un archivo. pst privado que se crea para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="30532-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30532-106">Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación siguiendo las instrucciones que se indican en [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="30532-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="30532-107">El proveedor solo debe usar la API en un almacén personal creado para sí mismo, y no en almacenes personales creados para otros proveedores, ya que los almacenes personales creados para otros proveedores pueden haber configurado sus propios mecanismos de replicación con el servidor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="30532-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="30532-108">Por ejemplo, un archivo de carpetas sin conexión (. OST) mantiene su propia relación de replicación con un servidor de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="30532-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="30532-109">Para usar la API de replicación, un proveedor de almacén de mensajes MAPI primero debe abrir y ajustar un almacén local basado en. pst llamando a **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="30532-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="30532-110">A continuación, el proveedor puede usar las principales interfaces de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación.</span><span class="sxs-lookup"><span data-stu-id="30532-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="30532-111">**IPSTX** se proporciona mediante consultas en [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)y **IOSTX** se proporciona mediante **[IPSTX:: GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="30532-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="30532-112">La interfaz IOSTX</span><span class="sxs-lookup"><span data-stu-id="30532-112">The IOSTX Interface</span></span>

<span data-ttu-id="30532-113">La interfaz **IOSTX** es la interfaz principal que realiza la sincronización en la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="30532-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="30532-114">**IOSTX** mueve el almacén local a través de una serie de Estados, recuperando información en cada Estado sobre cambios en el almacén local, e informando al almacén local de cambios en el servidor.</span><span class="sxs-lookup"><span data-stu-id="30532-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="30532-115">La API de replicación también especifica muchas estructuras de datos que admiten la sincronización.</span><span class="sxs-lookup"><span data-stu-id="30532-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="30532-116">Un proveedor de almacenamiento, como cliente de esta API, usa la API de replicación para envolver el almacén local y desplazarse a través de estos Estados e insertar los cambios en el almacén local (como los cambios en la jerarquía de carpetas o la adición de nuevos elementos) al servidor y también recuperar información sobre los cambios en el servidor y la forma de proporcionarla a la interfaz **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="30532-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="30532-117">La interfaz **IOSTX** adopta la sincronización de cambio incremental (ICS) que proporciona Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="30532-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="30532-118">Para obtener más información acerca de ICS, consulte [criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="30532-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="30532-119">A través de **IOSTX**, el cliente usa ICS para supervisar y sincronizar los cambios incrementales de la jerarquía o el contenido de un almacén local.</span><span class="sxs-lookup"><span data-stu-id="30532-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="30532-120">La interfaz IPSTX</span><span class="sxs-lookup"><span data-stu-id="30532-120">The IPSTX Interface</span></span>

 <span data-ttu-id="30532-121">**IPSTX** y otras cinco interfaces \* \* IPSTX *n* \* \* que heredan de **IPSTX** proporcionan funcionalidad auxiliar que se puede usar para realizar la replicación a través de la interfaz de **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="30532-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="30532-122">Por ejemplo, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** permite que el almacén local eMule el administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.</span><span class="sxs-lookup"><span data-stu-id="30532-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="30532-123">Para obtener más información acerca de las transiciones de estado durante la replicación, consulte [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="30532-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="30532-124">La API de replicación</span><span class="sxs-lookup"><span data-stu-id="30532-124">The Replication API</span></span>

<span data-ttu-id="30532-125">La API de replicación proporciona las siguientes definiciones, tipos de datos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="30532-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="30532-126">Para obtener una implementación de ejemplo de un proveedor de almacenamiento para archivos de carpetas personales (PST), vea [acerca del proveedor de almacenamiento PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="30532-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="30532-127">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="30532-127">Definitions:</span></span>
  
- [<span data-ttu-id="30532-128">Constantes para la API de replicación</span><span class="sxs-lookup"><span data-stu-id="30532-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="30532-129">Funciones:</span><span class="sxs-lookup"><span data-stu-id="30532-129">Functions:</span></span>
  
- <span data-ttu-id="30532-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="30532-131">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="30532-131">Data types:</span></span>
  
- <span data-ttu-id="30532-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="30532-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="30532-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="30532-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="30532-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="30532-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="30532-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="30532-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="30532-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="30532-141">**[SINCRONIZÁNDOSE](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="30532-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="30532-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="30532-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="30532-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="30532-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="30532-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="30532-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="30532-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="30532-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="30532-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="30532-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="30532-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="30532-154">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="30532-154">Interfaces:</span></span>
  
- <span data-ttu-id="30532-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="30532-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="30532-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="30532-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="30532-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="30532-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="30532-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="30532-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

