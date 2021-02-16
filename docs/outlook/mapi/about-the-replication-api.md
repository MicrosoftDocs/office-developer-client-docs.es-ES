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
# <a name="about-the-replication-api"></a><span data-ttu-id="1d7cf-103">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1d7cf-103">About the Replication API</span></span>

  
  
<span data-ttu-id="1d7cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d7cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d7cf-105">La API de replicación proporciona la funcionalidad de un proveedor de almacén de mensajes MAPI para sincronizar elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local privado basado en .pst que se crea para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1d7cf-106">Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación de acuerdo con las instrucciones de [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="1d7cf-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="1d7cf-107">El proveedor debe usar la API solo en un almacén personal creado para sí mismo y no en almacenes personales creados para otros proveedores, porque es posible que los almacenes personales creados para otros proveedores ya tengan configurados sus propios mecanismos de replicación con el servidor respectivo.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="1d7cf-108">Por ejemplo, un archivo de carpetas sin conexión (.ost) mantiene su propia relación de replicación con un servidor de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="1d7cf-109">Para usar la API de replicación, un proveedor de almacén de mensajes MAPI primero debe abrir y encapsular un almacén local basado en .pst llamando a **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="1d7cf-110">A continuación, el proveedor puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** e **[IPSTX,](ipstxiunknown.md)** para llevar a cabo la replicación.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="1d7cf-111">**IPSTX** se proporciona consultando en [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)y **IOSTX** lo proporciona **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="1d7cf-112">Interfaz IOSTX</span><span class="sxs-lookup"><span data-stu-id="1d7cf-112">The IOSTX Interface</span></span>

<span data-ttu-id="1d7cf-113">La **interfaz IOSTX** es la interfaz principal que realiza la sincronización en la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="1d7cf-114">**IOSTX** mueve el almacén local a través de una serie de estados, recuperando información en cada estado sobre los cambios en el almacén local, así como informando al almacén local de los cambios en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="1d7cf-115">La API de replicación también especifica muchas estructuras de datos que admiten la sincronización.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="1d7cf-116">Un proveedor de almacén, como cliente de esta API, usa la API de replicación para encapsular el almacén local y desplazarse por estos estados, insertar los cambios en el almacén local (como los cambios en la jerarquía de carpetas o la adición de nuevos elementos) en el servidor, y también recuperar información sobre los cambios en el servidor y proporcionar esa información a la interfaz **IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="1d7cf-117">La **interfaz IOSTX** adopta la sincronización de cambios incremental (ICS) proporcionada por Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="1d7cf-118">Para obtener más información acerca de ICS, vea [Criterios de evaluación de ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d7cf-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="1d7cf-119">Mediante **IOSTX,** el cliente usa ICS para supervisar y sincronizar los cambios incrementales en la jerarquía o el contenido de un almacén local.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="1d7cf-120">Interfaz IPSTX</span><span class="sxs-lookup"><span data-stu-id="1d7cf-120">The IPSTX Interface</span></span>

 <span data-ttu-id="1d7cf-121">**IPSTX** y otras cinco interfaces \*\*IPSTX *n* \*\* que heredan de **IPSTX** proporcionan funcionalidad auxiliar que se puede usar al realizar la replicación a través de la interfaz **IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="1d7cf-122">Por ejemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** le permite hacer que el almacén local emule el Administrador de protocolo de Outlook para colar mensajes salientes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="1d7cf-123">Para obtener más información acerca de las transiciones de estado durante la replicación, vea [Acerca de la máquina de estado de replicación.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="1d7cf-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="1d7cf-124">API de replicación</span><span class="sxs-lookup"><span data-stu-id="1d7cf-124">The Replication API</span></span>

<span data-ttu-id="1d7cf-125">La API de replicación proporciona las siguientes definciones, tipos de datos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1d7cf-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="1d7cf-126">Para obtener una implementación de ejemplo de un proveedor de almacenamiento para archivos de carpetas personales ajustados (PST), consulte Acerca del [proveedor de almacén de ARCHIVOS PST ajustados de ejemplo.](about-the-sample-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="1d7cf-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="1d7cf-127">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="1d7cf-127">Definitions:</span></span>
  
- [<span data-ttu-id="1d7cf-128">Constantes para la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1d7cf-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="1d7cf-129">Funciones:</span><span class="sxs-lookup"><span data-stu-id="1d7cf-129">Functions:</span></span>
  
- <span data-ttu-id="1d7cf-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="1d7cf-131">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="1d7cf-131">Data types:</span></span>
  
- <span data-ttu-id="1d7cf-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="1d7cf-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="1d7cf-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="1d7cf-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="1d7cf-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="1d7cf-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="1d7cf-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="1d7cf-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="1d7cf-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="1d7cf-141">**[Sincronizar](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="1d7cf-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="1d7cf-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="1d7cf-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="1d7cf-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="1d7cf-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="1d7cf-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="1d7cf-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="1d7cf-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="1d7cf-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="1d7cf-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="1d7cf-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="1d7cf-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="1d7cf-154">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="1d7cf-154">Interfaces:</span></span>
  
- <span data-ttu-id="1d7cf-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="1d7cf-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="1d7cf-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="1d7cf-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="1d7cf-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="1d7cf-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="1d7cf-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7cf-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

