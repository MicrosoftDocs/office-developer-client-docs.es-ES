---
title: Introducción al apagado rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Última modificación: 26 de junio de 2012'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427209"
---
# <a name="fast-shutdown-overview"></a>Introducción al apagado rápido

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El apagado rápido es un mecanismo para que un cliente MAPI inicie un apagado rápido del proceso de cliente, notificando a todos los proveedores con los que el cliente tiene una sesión MAPI activa para guardar los datos y la configuración antes de que salga el proceso de cliente. En este tema se describe el mecanismo básico del apagado rápido. 

A partir Microsoft Outlook 2010 y ahora incluyendo Microsoft Outlook 2013, el subsistema MAPI proporciona la [interfaz IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) Outlook y otros clientes MAPI pueden adoptar el apagado rápido como mecanismo predeterminado para salir del proceso de cliente. Una configuración de nivel de usuario en el registro Windows del equipo cliente controla la adopción del apagado rápido para todos los clientes MAPI para ese usuario en ese equipo. Para obtener más información sobre la configuración del Registro, [vea Fast Shutdown User Options](fast-shutdown-user-options.md).
  
Si un cliente MAPI necesita adoptar el apagado rápido, debe usar la interfaz **IMAPIClientShutdown : IUnknown.** A continuación se muestra el curso típico de los eventos cuando el cliente intenta apagar: 
  
1. El cliente MAPI inicia el cierre llamando al método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) para determinar si el subsistema MAPI admite el apagado rápido. 
    
2. El subsistema MAPI responde con la compatibilidad de apagado rápido disponible a la llamada **IMAPIClientShutdown::QueryFastShutdown** del cliente mediante el procedimiento siguiente: 
    
    1. El subsistema MAPI llama al método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para cada proveedor MAPI con el que el proceso de cliente MAPI tenga una sesión MAPI activa, si el proveedor ha implementado la [interfaz IMAPIProviderShutdown : IUnknown.](imapiprovidershutdowniunknown.md) 
        
       > [!NOTE]
       >  El subsistema MAPI siempre consulta y notifica a los proveedores MAPI a través de la interfaz **IMAPIProviderShutdown : IUnknown** dentro de cada sesión MAPI en el siguiente orden:
       > 1. Proveedores de transporte
       > 2. Proveedores de libreta de direcciones
       > 3. Proveedores de la tienda 
    
    2. Según la configuración del Registro de cierre rápido para ese usuario en el equipo cliente, el subsistema MAPI especifica el código de devolución adecuado a **IMAPIClientShutdown::QueryFastShutdown**. El código devuelto es S_OK o MAPI_E_NO_SUPPORT.
        
    3. El cliente MAPI llama al método [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) para indicar al subsistema MAPI la intención de cerrar. 
        
    4. El subsistema MAPI indica a cada proveedor MAPI cargado que el cliente MAPI se apagará. Para los proveedores que han implementado la interfaz **IMAPIProviderShutdown : IUnknown,** el subsistema MAPI llama al método [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondiente. 
        
    5. El cliente MAPI llama al método [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) para indicar al subsistema MAPI que el proceso de cliente está saliendo inmediatamente. 
        
    6. El subsistema MAPI indica a cada proveedor MAPI cargado que el proceso de cliente MAPI está saliendo. Para los proveedores que han implementado la interfaz **IMAPIProviderShutdown : IUnknown,** el subsistema MAPI llama al método [IMAPIProviderShutdown::D oFastShutdown](imapiprovidershutdown-dofastshutdown.md) correspondiente. En este punto, estos proveedores MAPI deben comprobar que todas las acciones necesarias, como guardar datos y opciones de configuración, se completen para que el cliente MAPI desconecte inmediatamente todas las referencias y salga. 
    
## <a name="see-also"></a>Vea también

- [Cierre del cliente en MAPI](client-shutdown-in-mapi.md)
- [Opciones de usuario de apagado rápido](fast-shutdown-user-options.md)
- [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md)

