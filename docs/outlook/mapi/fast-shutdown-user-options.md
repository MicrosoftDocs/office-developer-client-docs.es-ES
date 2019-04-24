---
title: Opciones de usuario de apagado rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Última modificación: 26 de junio de 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341079"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="85b57-103">Opciones de usuario de apagado rápido</span><span class="sxs-lookup"><span data-stu-id="85b57-103">Fast shutdown user options</span></span>

<span data-ttu-id="85b57-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85b57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85b57-105">Este artículo describe las tres configuraciones del registro de Windows que están disponibles desde Microsoft Outlook 2010 y ahora incluyen Microsoft Outlook 2013 para el cierre rápido de clientes MAPI de un usuario.</span><span class="sxs-lookup"><span data-stu-id="85b57-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="85b57-106">Los administradores pueden usar estas configuraciones del registro para especificar el comportamiento de cierre preferido del cliente según la compatibilidad con los proveedores MAPI para el apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="85b57-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="85b57-107">A su vez, la configuración del administrador determina cómo responde el subsistema MAPI a las llamadas del cliente MAPI a [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en relación con el soporte disponible de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="85b57-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="85b57-108">Aunque una configuración de registro refleja las preferencias del administrador a nivel de usuario para el apagado rápido para todos los clientes MAPI, un desarrollador de cliente MAPI puede decidir si el cliente admite el apagado rápido independientemente de lo que ocurra con otros clientes MAPI y de la configuración de registro del administrador.</span><span class="sxs-lookup"><span data-stu-id="85b57-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="85b57-109">No obstante, para que el apagado rápido se produzca correctamente, el usuario debe tener la configuración de registro necesaria, un cliente MAPI debe iniciar el apagado rápido mediante la interfaz [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) y los proveedores MAPI que colaboran con el cliente deben implementar la interfaz [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para permitir el apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="85b57-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="85b57-110">En la lista siguiente se describen las tres opciones a nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="85b57-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="85b57-111">Opción 1: el subsistema MAPI permite el apagado rápido, a menos que los proveedores MAPI decidan explícitamente no hacerlo</span><span class="sxs-lookup"><span data-stu-id="85b57-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="85b57-112">Desde Outlook 2010, este es el comportamiento predeterminado cuando Outlook es el cliente MAPI; no es necesariamente el comportamiento predeterminado para otros clientes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85b57-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="85b57-113">Para especificar explícitamente esta opción para Outlook, los administradores puede establecer la clave del registro y el valor siguientes.</span><span class="sxs-lookup"><span data-stu-id="85b57-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="85b57-114">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="85b57-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="85b57-115">Valor:</span><span class="sxs-lookup"><span data-stu-id="85b57-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="85b57-116">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo S\_Aceptar, siempre y cuando no haya ningún proveedor MAPI con una sesión MAPI activa con el cliente MAPI que haya rechazado explícitamente el soporte de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="85b57-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="85b57-117">Un proveedor MAPI anula el apagado rápido al implementar el método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para devolver un error (MAPI\_E\_NO\_SUPPORT).</span><span class="sxs-lookup"><span data-stu-id="85b57-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="85b57-118">Si uno o varios proveedores MAPI devuelven un error en **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="85b57-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="85b57-119">A menos que un proveedor MAPI decida anularlo, el subsistema MAPI devuelve S\_Aceptar, incluso si uno o varios proveedores no han implementado la interfaz **IMAPIProviderShutdown: IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="85b57-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="85b57-120">Opción 2: el subsistema MAPI permite el apagado rápido, solo si todos los proveedores MAPI muestran su acuerdo explícitamente</span><span class="sxs-lookup"><span data-stu-id="85b57-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="85b57-121">Los administradores deben establecer explícitamente la clave del registro y el valor siguientes para especificar esta preferencia para el apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="85b57-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="85b57-122">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="85b57-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="85b57-123">Valor:</span><span class="sxs-lookup"><span data-stu-id="85b57-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="85b57-124">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo S\_Aceptar, siempre que todos los proveedores MAPI con una sesión activa con el cliente MAPI hayan aceptado el soporte de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="85b57-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="85b57-125">Un proveedor MAPI muestra su acuerdo al implementar **IMAPIProviderShutdown::QueryFastShutdown** para devolver un código de no error (S\_Aceptar).</span><span class="sxs-lookup"><span data-stu-id="85b57-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="85b57-126">Si uno o varios proveedores MAPI devuelven un error MAPI\_E\_NO\_SUPPORT o no implementan **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve un código de error a **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="85b57-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="85b57-127">Opción 3: un administrador deshabilita la compatibilidad con el cierre rápido del cliente</span><span class="sxs-lookup"><span data-stu-id="85b57-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="85b57-128">Los administradores deben establecer explícitamente la clave del registro y el valor siguientes para anular su aceptación del apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="85b57-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="85b57-129">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="85b57-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="85b57-130">Valor:</span><span class="sxs-lookup"><span data-stu-id="85b57-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="85b57-131">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo MAPI_E_NO_SUPPORT, independientemente de si alguno de los proveedores MAPI acepta el cierre rápido.</span><span class="sxs-lookup"><span data-stu-id="85b57-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="85b57-132">En esta configuración del registro, el subsistema MAPI no llama nunca a los métodos **IMAPIProviderShutdown::QueryFastShutdown** o [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de cualquiera de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="85b57-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="85b57-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="85b57-133">See also</span></span>

- [<span data-ttu-id="85b57-134">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="85b57-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="85b57-135">Información general sobre el apagado rápido</span><span class="sxs-lookup"><span data-stu-id="85b57-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="85b57-136">Procedimientos recomendados para el apagado rápido</span><span class="sxs-lookup"><span data-stu-id="85b57-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

