---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435337"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="98d7b-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98d7b-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="98d7b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98d7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98d7b-105">Permite que un cliente MAPI lleve a cabo el apagado rápido del proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="98d7b-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98d7b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="98d7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="98d7b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98d7b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="98d7b-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="98d7b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="98d7b-109">[IMAPISession (objeto)](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="98d7b-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="98d7b-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="98d7b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="98d7b-111">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="98d7b-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="98d7b-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="98d7b-112">Called by:</span></span>  <br/> |<span data-ttu-id="98d7b-113">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="98d7b-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="98d7b-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="98d7b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="98d7b-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="98d7b-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="98d7b-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="98d7b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="98d7b-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="98d7b-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="98d7b-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="98d7b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="98d7b-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="98d7b-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="98d7b-120">Consulta el subsistema MAPI para obtener compatibilidad con el apagado rápido que proporcionan los proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="98d7b-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="98d7b-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="98d7b-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="98d7b-122">Indica la intención del cliente MAPI de continuar con el apagado.</span><span class="sxs-lookup"><span data-stu-id="98d7b-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="98d7b-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="98d7b-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="98d7b-124">Indica la intención del cliente MAPI de salir del proceso de cliente inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="98d7b-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98d7b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98d7b-125">Remarks</span></span>

<span data-ttu-id="98d7b-126">El propósito del apagado rápido es permitir que un cliente MAPI y cualquier proveedor MAPI cargado con el que el cliente MAPI tenga una sesión MAPI activa guarden la configuración y los datos mapi.</span><span class="sxs-lookup"><span data-stu-id="98d7b-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="98d7b-127">Esto permite al cliente MAPI desconectar todas las referencias externas y salir sin causar ninguna pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="98d7b-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="98d7b-128">Un cliente MAPI que necesita realizar un apagado rápido debe usar la **interfaz IMAPIClientShutdown.**</span><span class="sxs-lookup"><span data-stu-id="98d7b-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="98d7b-129">El cliente MAPI puede obtener un puntero a esta interfaz llamando al método IUnknown::QueryInterface en cualquier [objeto IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="98d7b-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="98d7b-130">Un cliente MAPI siempre inicia un apagado rápido llamando al método **IMAPIClientShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="98d7b-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="98d7b-131">El subsistema MAPI responde a la consulta del cliente MAPI comprobando si los proveedores MAPI cargados admiten el apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="98d7b-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="98d7b-132">El administrador puede usar la Windows del Registro para ayudar a determinar el nivel de compatibilidad del proveedor que es necesario para que los clientes MAPI continúen con el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="98d7b-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="98d7b-133">Para obtener más información, vea [Fast Shutdown User Options](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="98d7b-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="98d7b-134">Para continuar con el apagado rápido, el cliente llama al método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar al subsistema MAPI la intención de cerrar.</span><span class="sxs-lookup"><span data-stu-id="98d7b-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="98d7b-135">A continuación, el cliente llama al método **IMAPIClientShutdown::D oFastShutdown** para indicar que el proceso de cliente se está saliendo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="98d7b-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="98d7b-136">Para obtener más información sobre el apagado rápido, vea [Fast Shutdown Overview](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98d7b-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="98d7b-137">Para obtener información sobre cómo realizar el apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="98d7b-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98d7b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="98d7b-138">See also</span></span>



[<span data-ttu-id="98d7b-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="98d7b-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="98d7b-140">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="98d7b-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

