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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817218"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="29354-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29354-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="29354-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29354-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29354-105">Permite a un cliente MAPI para llevar a cabo el apagado rápido del proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="29354-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29354-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="29354-106">Header file:</span></span>  <br/> |<span data-ttu-id="29354-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29354-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="29354-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="29354-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="29354-109">Objeto [IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="29354-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="29354-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="29354-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="29354-111">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="29354-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="29354-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="29354-112">Called by:</span></span>  <br/> |<span data-ttu-id="29354-113">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="29354-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="29354-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="29354-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="29354-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="29354-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="29354-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="29354-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="29354-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="29354-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="29354-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="29354-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="29354-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="29354-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="29354-120">Las consultas admiten el subsistema MAPI para apagado rápido proporcionado por proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="29354-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="29354-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="29354-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="29354-122">Indica la intención de continuar con la del cliente MAPI cerrado.</span><span class="sxs-lookup"><span data-stu-id="29354-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="29354-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="29354-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="29354-124">Indica la intención del cliente MAPI para salir inmediatamente el proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="29354-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29354-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29354-125">Remarks</span></span>

<span data-ttu-id="29354-126">El propósito de apagado rápido es permitir que un cliente MAPI y cualquier proveedor MAPI cargado con la que el cliente MAPI tiene una sesión activa de MAPI para guardar los datos y la configuración de MAPI.</span><span class="sxs-lookup"><span data-stu-id="29354-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="29354-127">Esto permite que el cliente MAPI desconectar todas las referencias externas y salir sin que se produzca ninguna pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="29354-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="29354-128">Un cliente MAPI que necesita para llevar a cabo el apagado rápido debe usar la interfaz **IMAPIClientShutdown** .</span><span class="sxs-lookup"><span data-stu-id="29354-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="29354-129">El cliente MAPI puede obtener un puntero a esta interfaz llamando al método IUnknown:: QueryInterface en cualquier objeto [IMAPISession](imapisessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="29354-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="29354-130">Un cliente MAPI siempre inicia un apagado rápido llamando al método **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="29354-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="29354-131">El subsistema MAPI se responde a la consulta del cliente MAPI comprobando si proveedores MAPI cargados admiten apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="29354-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="29354-132">El administrador puede usar la configuración del registro de Windows para ayudar a determinar el nivel de compatibilidad de proveedor que es necesario para los clientes MAPI continuar con el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="29354-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="29354-133">Para obtener más información, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="29354-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="29354-134">Para continuar con el apagado rápido, el cliente llama al método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar al subsistema MAPI la intención de apagado.</span><span class="sxs-lookup"><span data-stu-id="29354-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="29354-135">El cliente, a continuación, llama al método de **IMAPIClientShutdown::DoFastShutdown** para indicar que el proceso de cliente está saliendo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="29354-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="29354-136">Para obtener más información acerca de apagado rápido, consulte [Información general de cierre rápido](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29354-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="29354-137">Para obtener información sobre cómo se realiza correctamente apagado rápido, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="29354-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29354-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="29354-138">See also</span></span>



[<span data-ttu-id="29354-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="29354-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="29354-140">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="29354-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
