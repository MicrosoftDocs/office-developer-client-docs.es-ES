---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 81b7b0c235f610e7aaa0c17ecd1760df5d382552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587974"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="0b862-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b862-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="0b862-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b862-105">Permite que el subsistema MAPI informar a un proveedor de MAPI del cierre rápido de un cliente MAPI, por lo que el proveedor MAPI puede responder a la que se cerró.</span><span class="sxs-lookup"><span data-stu-id="0b862-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b862-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0b862-106">Header file:</span></span>  <br/> |<span data-ttu-id="0b862-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b862-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0b862-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="0b862-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0b862-109">Objetos de proveedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)o [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0b862-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="0b862-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0b862-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0b862-111">Proveedor MAPI</span><span class="sxs-lookup"><span data-stu-id="0b862-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="0b862-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0b862-112">Called by:</span></span>  <br/> |<span data-ttu-id="0b862-113">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="0b862-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="0b862-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="0b862-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0b862-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="0b862-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="0b862-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="0b862-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0b862-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="0b862-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0b862-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="0b862-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0b862-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="0b862-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="0b862-120">Las consultas que admite el proveedor MAPI de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="0b862-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="0b862-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="0b862-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="0b862-122">Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="0b862-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="0b862-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="0b862-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="0b862-124">Indica que el proveedor MAPI que el cliente MAPI está saliendo inmediatamente, para que el proveedor MAPI guardará los cambios para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="0b862-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b862-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b862-125">Remarks</span></span>

<span data-ttu-id="0b862-126">Cierre rápido permite que un cliente MAPI salir de su proceso dentro de una hora corta, es de esperar que después de que el cliente y se carga proveedores MAPI han guardado de datos y la configuración de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0b862-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="0b862-127">El cliente MAPI siempre inicia un apagado rápido y debe consultar el subsistema MAPI para soporte técnico de apagado rápido de los proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="0b862-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="0b862-128">Un administrador puede establecer el registro de Windows en el nivel de usuario para especificar el nivel de compatibilidad de proveedor que es necesario para permitir que cierre rápido de todos los clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="0b862-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="0b862-129">Para obtener más información acerca de la configuración del registro, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="0b862-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="0b862-130">Sin embargo, para que apagado rápido correctamente se produzca sin pérdida de datos, proveedores MAPI deben implementar la interfaz de **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="0b862-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="0b862-131">Un proveedor de MAPI que necesita para admitir apagado rápido de cliente debe devolver S_OK para el subsistema MAPI en el método **IMAPIProviderShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="0b862-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="0b862-132">Cuando el subsistema MAPI posteriormente llama a los métodos **IMAPIProviderShutdown::NotifyProcessShutdown** y **IMAPIProviderShutdown::DoFastShutdown** , el proveedor MAPI debe realizar las acciones necesarias para guardar los datos y la configuración de MAPI y Preparar para salir del cliente.</span><span class="sxs-lookup"><span data-stu-id="0b862-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="0b862-133">Proveedores MAPI que no es necesario para admitir el apagado rápido cliente aún deben implementar la interfaz **IMAPIProviderShutdown** y tener el método **IMAPIProviderShutdown::QueryFastShutdown** devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0b862-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="0b862-134">Para Outlook como un cliente MAPI, esto hace que Outlook que se debe esperar para que todas las referencias externas a liberarse antes de que exista.</span><span class="sxs-lookup"><span data-stu-id="0b862-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="0b862-135">Dependiendo del registro de Windows del usuario configuración de apagado rápido, no se implementa la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="0b862-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="0b862-136">Para obtener más información acerca del proceso de apagado rápido, consulte [Información general de cierre rápido](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b862-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="0b862-137">Para obtener información acerca de cómo llevar a cabo apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="0b862-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b862-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0b862-138">See also</span></span>



[<span data-ttu-id="0b862-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0b862-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="0b862-140">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="0b862-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

