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
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409660"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="4ebe1-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ebe1-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="4ebe1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ebe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ebe1-105">Permite que el subsistema MAPI informe a un proveedor MAPI del apagado rápido de un cliente MAPI, de modo que el proveedor MAPI pueda responder al apagado.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ebe1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ebe1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ebe1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4ebe1-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4ebe1-109">Objetos provider: [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)o [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4ebe1-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="4ebe1-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ebe1-111">Proveedor MAPI</span><span class="sxs-lookup"><span data-stu-id="4ebe1-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="4ebe1-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-112">Called by:</span></span>  <br/> |<span data-ttu-id="4ebe1-113">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="4ebe1-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="4ebe1-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4ebe1-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="4ebe1-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="4ebe1-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="4ebe1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4ebe1-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="4ebe1-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4ebe1-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="4ebe1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4ebe1-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4ebe1-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="4ebe1-120">Consulta al proveedor MAPI la compatibilidad con el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="4ebe1-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="4ebe1-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="4ebe1-122">Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido, de modo que el proveedor puede realizar acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="4ebe1-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4ebe1-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="4ebe1-124">Indica al proveedor MAPI que el cliente MAPI sale inmediatamente, de modo que el proveedor MAPI persistirá en los cambios para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ebe1-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ebe1-125">Remarks</span></span>

<span data-ttu-id="4ebe1-126">El apagado rápido permite que un cliente MAPI salga de su proceso en poco tiempo, con suerte después de que el cliente y los proveedores MAPI cargados han guardado la configuración y los datos mapi.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="4ebe1-127">El cliente MAPI siempre inicia un apagado rápido y debe consultar el subsistema MAPI para obtener compatibilidad con el apagado rápido de los proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="4ebe1-128">Un administrador puede establecer el Windows en el nivel de usuario para especificar el nivel de compatibilidad del proveedor que es necesario para permitir el apagado rápido de todos los clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="4ebe1-129">Para obtener más información acerca de la configuración del Registro, vea [Fast Shutdown User Options](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="4ebe1-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="4ebe1-130">Sin embargo, para que el apagado rápido se produzca correctamente sin pérdida de datos, los proveedores MAPI deben implementar la **interfaz IMAPIProviderShutdown.**</span><span class="sxs-lookup"><span data-stu-id="4ebe1-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="4ebe1-131">Un proveedor MAPI que necesita admitir el apagado rápido del cliente debe devolver S_OK al subsistema MAPI en el **método IMAPIProviderShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="4ebe1-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="4ebe1-132">Cuando el subsistema MAPI llama posteriormente a los métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::D oFastShutdown,** el proveedor MAPI debe realizar las acciones necesarias para guardar la configuración y los datos MAPI y prepararse para la salida del cliente.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="4ebe1-133">Los proveedores MAPI que no necesitan admitir el cierre rápido del cliente deben implementar la interfaz **IMAPIProviderShutdown** y hacer que el método **IMAPIProviderShutdown::QueryFastShutdown** devuelva MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="4ebe1-134">Para Outlook como cliente MAPI, esto hace que Outlook esperar a que se liberarán todas las referencias externas antes de salir.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="4ebe1-135">Según la configuración del Registro Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un cierre rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="4ebe1-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="4ebe1-136">Para obtener más información sobre el proceso de apagado rápido, vea [Fast Shutdown Overview](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4ebe1-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="4ebe1-137">Para obtener información sobre cómo realizar el apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="4ebe1-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ebe1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ebe1-138">See also</span></span>



[<span data-ttu-id="4ebe1-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4ebe1-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="4ebe1-140">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="4ebe1-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

