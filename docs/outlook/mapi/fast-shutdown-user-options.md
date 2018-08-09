---
title: Opciones de usuario de apagado rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Última modificación: 26 de junio de 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816785"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="ce563-103">Opciones de usuario de apagado rápido</span><span class="sxs-lookup"><span data-stu-id="ce563-103">Fast shutdown user options</span></span>

<span data-ttu-id="ce563-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce563-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce563-105">Este tema describen las tres del registro opciones de Windows que están disponibles, a partir de Microsoft Outlook 2010 y ahora incluyen Microsoft Outlook 2013, de apagado rápido de los clientes MAPI de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ce563-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="ce563-106">Los administradores pueden usar esta configuración del registro para especificar el comportamiento de apagado de cliente preferido según la compatibilidad con los proveedores MAPI de apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce563-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="ce563-107">El Administrador de la configuración, a su vez, determina cómo responde el subsistema MAPI a la llamada del cliente MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en términos de soporte de apagado rápido disponibles.</span><span class="sxs-lookup"><span data-stu-id="ce563-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="ce563-108">Aunque una configuración del registro refleja las preferencias del administrador en el nivel de usuario de apagado rápido para todos los clientes MAPI, un desarrollador de cliente MAPI puede decidir si el cliente admite apagado rápido independientemente de otros clientes MAPI y el configuración de registro del administrador.</span><span class="sxs-lookup"><span data-stu-id="ce563-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="ce563-109">No obstante, para apagado rápido para efectuarse correctamente, el usuario debe tener la configuración del registro necesaria, un cliente MAPI debe iniciar el apagado rápido mediante el uso de la [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interfaz y proveedores MAPI que funcionan con la cliente debe implementar la [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interfaz para admitir apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce563-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="ce563-110">La lista siguiente describen las tres opciones de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce563-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="ce563-111">Opción 1: El subsistema MAPI permite apagado rápido, a menos que excluir explícitamente los proveedores MAPI</span><span class="sxs-lookup"><span data-stu-id="ce563-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="ce563-112">A partir de Outlook 2010, este es el comportamiento predeterminado cuando Outlook es el cliente MAPI; no es necesariamente el comportamiento predeterminado para otros clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce563-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="ce563-113">Para especificar explícitamente esta opción para Outlook, los administradores pueden elegir establecer la siguiente clave del registro y el valor.</span><span class="sxs-lookup"><span data-stu-id="ce563-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="ce563-114">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ce563-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="ce563-115">Valor:</span><span class="sxs-lookup"><span data-stu-id="ce563-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="ce563-116">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de S\_Aceptar el mismo tiempo que ningún proveedor MAPI que tiene un activo MAPI sesión con el cliente de MAPI explícitamente ha optado por fuera de la compatibilidad de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="ce563-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="ce563-117">Un proveedor de MAPI opte fuera de apagado rápido implementando el método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para devolver un error (MAPI\_E\_NO\_soporte técnico).</span><span class="sxs-lookup"><span data-stu-id="ce563-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="ce563-118">Si uno o más proveedores MAPI devuelven un error en **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve MAPI_\E_\NO\_soporte a **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="ce563-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="ce563-119">A menos que un proveedor MAPI opte out, la devuelve del subsistema MAPI S\_Aceptar, incluso si uno o más proveedores no han implementado el **IMAPIProviderShutdown: IUnknown** interfaz.</span><span class="sxs-lookup"><span data-stu-id="ce563-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="ce563-120">Opción 2: El subsistema MAPI permite apagado rápido sólo si todos los proveedores MAPI explícitamente opte por</span><span class="sxs-lookup"><span data-stu-id="ce563-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="ce563-121">Los administradores deben establecer explícitamente la siguiente clave del registro y el valor para especificar esta preferencia de apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce563-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="ce563-122">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ce563-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="ce563-123">Valor:</span><span class="sxs-lookup"><span data-stu-id="ce563-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="ce563-124">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de S\_Aceptar si todos los proveedores MAPI que tengan sesiones activas con el apagado rápido de la compatibilidad de cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce563-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="ce563-125">Un proveedor de MAPI, muestra su soporte mediante la implementación de **IMAPIProviderShutdown::QueryFastShutdown** para devolver un código de error que no sean (S\_Aceptar).</span><span class="sxs-lookup"><span data-stu-id="ce563-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="ce563-126">Si uno o más proveedores MAPI devuelven MAPI\_E\_NO\_de soporte técnico, o no implementar **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve un código de error a **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="ce563-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="ce563-127">Opción 3: Un administrador deshabilita la compatibilidad con cierre rápido de cliente</span><span class="sxs-lookup"><span data-stu-id="ce563-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="ce563-128">Los administradores deben establecer explícitamente la siguiente clave del registro y valor para deshabilitar la compatibilidad de apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce563-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="ce563-129">Clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ce563-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="ce563-130">Valor:</span><span class="sxs-lookup"><span data-stu-id="ce563-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="ce563-131">Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de MAPI_E_NO_SUPPORT, independientemente de si cualquier proveedor MAPI compatible con rapidez en el cierre.</span><span class="sxs-lookup"><span data-stu-id="ce563-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="ce563-132">En esta configuración del registro, el subsistema MAPI nunca llama al método **IMAPIProviderShutdown::QueryFastShutdown** o [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de cualquiera de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="ce563-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ce563-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce563-133">See also</span></span>

- [<span data-ttu-id="ce563-134">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="ce563-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="ce563-135">Información general sobre el apagado rápido</span><span class="sxs-lookup"><span data-stu-id="ce563-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="ce563-136">Procedimientos recomendados para el apagado rápido</span><span class="sxs-lookup"><span data-stu-id="ce563-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

