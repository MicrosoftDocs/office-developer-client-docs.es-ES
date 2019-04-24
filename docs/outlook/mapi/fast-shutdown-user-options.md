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
# <a name="fast-shutdown-user-options"></a>Opciones de usuario de apagado rápido

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Este artículo describe las tres configuraciones del registro de Windows que están disponibles desde Microsoft Outlook 2010 y ahora incluyen Microsoft Outlook 2013 para el cierre rápido de clientes MAPI de un usuario. Los administradores pueden usar estas configuraciones del registro para especificar el comportamiento de cierre preferido del cliente según la compatibilidad con los proveedores MAPI para el apagado rápido del cliente. A su vez, la configuración del administrador determina cómo responde el subsistema MAPI a las llamadas del cliente MAPI a [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en relación con el soporte disponible de apagado rápido. 
  
Aunque una configuración de registro refleja las preferencias del administrador a nivel de usuario para el apagado rápido para todos los clientes MAPI, un desarrollador de cliente MAPI puede decidir si el cliente admite el apagado rápido independientemente de lo que ocurra con otros clientes MAPI y de la configuración de registro del administrador. No obstante, para que el apagado rápido se produzca correctamente, el usuario debe tener la configuración de registro necesaria, un cliente MAPI debe iniciar el apagado rápido mediante la interfaz [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) y los proveedores MAPI que colaboran con el cliente deben implementar la interfaz [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para permitir el apagado rápido del cliente. 
  
En la lista siguiente se describen las tres opciones a nivel de usuario.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Opción 1: el subsistema MAPI permite el apagado rápido, a menos que los proveedores MAPI decidan explícitamente no hacerlo 
    
Desde Outlook 2010, este es el comportamiento predeterminado cuando Outlook es el cliente MAPI; no es necesariamente el comportamiento predeterminado para otros clientes de MAPI. Para especificar explícitamente esta opción para Outlook, los administradores puede establecer la clave del registro y el valor siguientes.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo S\_Aceptar, siempre y cuando no haya ningún proveedor MAPI con una sesión MAPI activa con el cliente MAPI que haya rechazado explícitamente el soporte de apagado rápido. 

Un proveedor MAPI anula el apagado rápido al implementar el método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para devolver un error (MAPI\_E\_NO\_SUPPORT). Si uno o varios proveedores MAPI devuelven un error en **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**. 

A menos que un proveedor MAPI decida anularlo, el subsistema MAPI devuelve S\_Aceptar, incluso si uno o varios proveedores no han implementado la interfaz **IMAPIProviderShutdown: IUnknown**. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Opción 2: el subsistema MAPI permite el apagado rápido, solo si todos los proveedores MAPI muestran su acuerdo explícitamente 
    
Los administradores deben establecer explícitamente la clave del registro y el valor siguientes para especificar esta preferencia para el apagado rápido del cliente.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo S\_Aceptar, siempre que todos los proveedores MAPI con una sesión activa con el cliente MAPI hayan aceptado el soporte de apagado rápido. Un proveedor MAPI muestra su acuerdo al implementar **IMAPIProviderShutdown::QueryFastShutdown** para devolver un código de no error (S\_Aceptar). 

Si uno o varios proveedores MAPI devuelven un error MAPI\_E\_NO\_SUPPORT o no implementan **IMAPIProviderShutdown::QueryFastShutdown**, el subsistema MAPI devuelve un código de error a **IMAPIClientShutdown::QueryFastShutdown**.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Opción 3: un administrador deshabilita la compatibilidad con el cierre rápido del cliente
    
Los administradores deben establecer explícitamente la clave del registro y el valor siguientes para anular su aceptación del apagado rápido del cliente.
    
Clave del registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Cuando un cliente MAPI inicia un apagado rápido y llama a **IMAPIClientShutdown::QueryFastShutdown** para hacer una consulta sobre el soporte de apagado rápido, el subsistema MAPI responde a la consulta devolviendo MAPI_E_NO_SUPPORT, independientemente de si alguno de los proveedores MAPI acepta el cierre rápido. En esta configuración del registro, el subsistema MAPI no llama nunca a los métodos **IMAPIProviderShutdown::QueryFastShutdown** o [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de cualquiera de los proveedores. 
    
## <a name="see-also"></a>Vea también

- [Cierre del cliente en MAPI](client-shutdown-in-mapi.md)
- [Información general sobre el apagado rápido](fast-shutdown-overview.md)
- [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md)

