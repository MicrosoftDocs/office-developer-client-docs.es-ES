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
# <a name="fast-shutdown-user-options"></a>Opciones de usuario de apagado rápido

**Se aplica a**: Outlook 
  
Este tema describen las tres del registro opciones de Windows que están disponibles, a partir de Microsoft Outlook 2010 y ahora incluyen Microsoft Outlook 2013, de apagado rápido de los clientes MAPI de un usuario. Los administradores pueden usar esta configuración del registro para especificar el comportamiento de apagado de cliente preferido según la compatibilidad con los proveedores MAPI de apagado rápido de cliente. El Administrador de la configuración, a su vez, determina cómo responde el subsistema MAPI a la llamada del cliente MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en términos de soporte de apagado rápido disponibles. 
  
Aunque una configuración del registro refleja las preferencias del administrador en el nivel de usuario de apagado rápido para todos los clientes MAPI, un desarrollador de cliente MAPI puede decidir si el cliente admite apagado rápido independientemente de otros clientes MAPI y el configuración de registro del administrador. No obstante, para apagado rápido para efectuarse correctamente, el usuario debe tener la configuración del registro necesaria, un cliente MAPI debe iniciar el apagado rápido mediante el uso de la [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interfaz y proveedores MAPI que funcionan con la cliente debe implementar la [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interfaz para admitir apagado rápido de cliente. 
  
La lista siguiente describen las tres opciones de nivel de usuario.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Opción 1: El subsistema MAPI permite apagado rápido, a menos que excluir explícitamente los proveedores MAPI 
    
A partir de Outlook 2010, este es el comportamiento predeterminado cuando Outlook es el cliente MAPI; no es necesariamente el comportamiento predeterminado para otros clientes MAPI. Para especificar explícitamente esta opción para Outlook, los administradores pueden elegir establecer la siguiente clave del registro y el valor.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de S\_Aceptar el mismo tiempo que ningún proveedor MAPI que tiene un activo MAPI sesión con el cliente de MAPI explícitamente ha optado por fuera de la compatibilidad de apagado rápido. 

Un proveedor de MAPI opte fuera de apagado rápido implementando el método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para devolver un error (MAPI\_E\_NO\_soporte técnico). Si uno o más proveedores MAPI devuelven un error en **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve MAPI_\E_\NO\_soporte a **IMAPIClientShutdown::QueryFastShutdown**. 

A menos que un proveedor MAPI opte out, la devuelve del subsistema MAPI S\_Aceptar, incluso si uno o más proveedores no han implementado el **IMAPIProviderShutdown: IUnknown** interfaz. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Opción 2: El subsistema MAPI permite apagado rápido sólo si todos los proveedores MAPI explícitamente opte por 
    
Los administradores deben establecer explícitamente la siguiente clave del registro y el valor para especificar esta preferencia de apagado rápido de cliente.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de S\_Aceptar si todos los proveedores MAPI que tengan sesiones activas con el apagado rápido de la compatibilidad de cliente MAPI. Un proveedor de MAPI, muestra su soporte mediante la implementación de **IMAPIProviderShutdown::QueryFastShutdown** para devolver un código de error que no sean (S\_Aceptar). 

Si uno o más proveedores MAPI devuelven MAPI\_E\_NO\_de soporte técnico, o no implementar **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve un código de error a **IMAPIClientShutdown::QueryFastShutdown** .
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Opción 3: Un administrador deshabilita la compatibilidad con cierre rápido de cliente
    
Los administradores deben establecer explícitamente la siguiente clave del registro y valor para deshabilitar la compatibilidad de apagado rápido de cliente.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para consultar para soporte técnico de apagado rápido, el subsistema MAPI se responde a la consulta mediante la devolución de MAPI_E_NO_SUPPORT, independientemente de si cualquier proveedor MAPI compatible con rapidez en el cierre. En esta configuración del registro, el subsistema MAPI nunca llama al método **IMAPIProviderShutdown::QueryFastShutdown** o [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de cualquiera de los proveedores. 
    
## <a name="see-also"></a>Ver también

- [Cierre del cliente de MAPI](client-shutdown-in-mapi.md)
- [Información general de apagado rápido](fast-shutdown-overview.md)
- [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md)

