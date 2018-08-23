---
title: Información general sobre el apagado rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Última modificación: 26 de junio de 2012'
ms.openlocfilehash: 8b8335fb2722e193f0eab1288b8ffdb2aa62df8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577789"
---
# <a name="fast-shutdown-overview"></a>Información general sobre el apagado rápido

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierre rápido es un mecanismo para que un cliente MAPI iniciar un apagado rápido del proceso de cliente, se notifica a todos los proveedores con los que el cliente tiene una sesión activa de MAPI para guardar los datos y la configuración antes de salir del proceso de cliente. En este tema se describe el mecanismo básico de apagado rápido. 

A partir de Microsoft Outlook 2010 y ahora incluyen Microsoft Outlook 2013, el subsistema MAPI proporciona el [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interfaz. Outlook y otros clientes MAPI pueden adoptar apagado rápido como el mecanismo predeterminado para salir del proceso de cliente. Una configuración de nivel de usuario en el registro de Windows del equipo cliente controla la adopción de apagado rápido para todos los clientes MAPI para ese usuario en ese equipo. Para obtener información detallada acerca de la configuración del registro, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).
  
Si un cliente MAPI debe adoptar apagado rápido, debe utilizar el **IMAPIClientShutdown: IUnknown** interfaz. El siguiente es el curso típico de eventos cuando el cliente intenta apagar: 
  
1. El cliente MAPI inicia el apagado llamando al método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) para determinar si el subsistema MAPI admite apagado rápido. 
    
2. El subsistema MAPI responde con la compatibilidad de apagado rápido disponibles a la llamada del cliente **IMAPIClientShutdown::QueryFastShutdown** mediante el procedimiento siguiente: 
    
    1. El subsistema MAPI llama al método de [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para cada proveedor MAPI con la que el proceso de cliente MAPI tiene una sesión MAPI activa, si ha implementado el proveedor de la [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interfaz. 
        
       > [!NOTE]
       >  El subsistema MAPI siempre las consultas y se lo comunica proveedores MAPI a través de la **IMAPIProviderShutdown: IUnknown** interfaz dentro de cada sesión MAPI en el orden siguiente:
       > 1. Proveedores de transporte
       > 2. Proveedores de la libreta de direcciones
       > 3. Proveedores de almacén 
    
    2. Dependiendo de la configuración del registro de apagado rápido para ese usuario en el equipo cliente, el subsistema MAPI especifica que el código de retorno apropiado para **IMAPIClientShutdown::QueryFastShutdown**. El código de retorno es S_OK o MAPI_E_NO_SUPPORT.
        
    3. El cliente MAPI llama al método de [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) para indicar al subsistema MAPI la intención de apagado. 
        
    4. Indica el subsistema MAPI para cada proveedor MAPI cargado que se cerrará el cliente MAPI. Para aquellos proveedores que han implementado el **IMAPIProviderShutdown: IUnknown** interfaz, el subsistema MAPI llama al método [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondiente. 
        
    5. El cliente MAPI llama al método de [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) para indicar al subsistema MAPI que el proceso de cliente está saliendo inmediatamente. 
        
    6. El subsistema MAPI indica a cada proveedor MAPI cargado que está saliendo el proceso de cliente MAPI. Para aquellos proveedores que han implementado el **IMAPIProviderShutdown: IUnknown** interfaz, el subsistema MAPI llama al método [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) correspondiente. En este momento, estos proveedores MAPI deben comprobar que todas las acciones necesarias, como el almacenamiento de datos y la configuración, son completadas en la preparación para el cliente de MAPI desconectar todas las referencias y salir inmediatamente. 
    
## <a name="see-also"></a>Recursos adicionales

- [Cierre del cliente de MAPI](client-shutdown-in-mapi.md)
- [Opciones de usuario de apagado rápido](fast-shutdown-user-options.md)
- [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md)

