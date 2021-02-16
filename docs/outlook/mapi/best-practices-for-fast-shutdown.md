---
title: Procedimientos recomendados para el apagado rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426971"
---
# <a name="best-practices-for-fast-shutdown"></a>Procedimientos recomendados para el apagado rápido

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se recomiendan los procedimientos recomendados para que los administradores, clientes MAPI y proveedores MAPI usen la configuración del Registro de Windows y las interfaces de apagado rápido para minimizar la pérdida de datos durante el cierre del cliente.
  
- Para que un cliente MAPI realice el apagado rápido correctamente para que los procesos del proveedor no generen pérdida de datos, el cliente MAPI debe llamar primero al método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) A continuación, el cliente debe continuar con los métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) en función de la compatibilidad del subsistema MAPI para el apagado rápido, como se indica en el valor devuelto de **IMAPIClientShutdown::QueryFastShutdown**. Como cliente MAPI, Microsoft Outlook no llama a **IMAPIClientShutdown::NotifyProcessShutdown** ni **IMAPIClientShutdown::D oFastShutdown** si **IMAPIClientShutdown::QueryFastShutdown** devuelve un error. Si el administrador ha deshabilitado el apagado rápido en el Registro de Windows, el subsistema MAPI devolverá MAPI_E_NO_SUPPORT a **IMAPIClientShutdown::QueryFastShutdown**. En este caso, el subsistema MAPI no informaría a los proveedores MAPI de una salida inmediata del proceso de cliente. Por lo tanto, si un cliente MAPI hace caso omiso de este código de devolución de error, continúa con el apagado rápido y desconecta todas las referencias externas, todos los proveedores MAPI cargados tendrán pérdida de datos. 
    
- Los proveedores MAPI deben implementar la interfaz [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) para llevar a cabo los pasos necesarios y a tiempo para evitar la pérdida de datos debido a que el cliente desconecta las referencias externas antes de que el cliente salga. Un proveedor debe posponer todo lo demás que no sea esencial para guardar datos en su almacén de datos principal. Por ejemplo, un proveedor de transporte debe posponer operaciones en segundo plano innecesarias que comprueben si hay correo nuevo, un proveedor de libreta de direcciones debe posponer la descarga de los cambios recientes de su servidor y un proveedor de almacenamiento debe posponer tareas de mantenimiento como compactar o indizar. 
    
- Los usuarios que deban salir de los clientes MAPI tan pronto como los cierren deben usar la configuración predeterminada del Registro que permite el apagado rápido a menos que un proveedor no lo haga.
    
- Una vez que un cliente MAPI llama a **IMAPIClientShutdown::D oFastShutdown**, no debe realizar llamadas adicionales a MAPI, incluida la función [MAPIUninitialize.](mapiuninitialize.md) El cliente no debe usar MAPI para el resto de la duración del proceso de cliente. 
    
- Un cliente MAPI nunca debe llamar directamente a la interfaz **IMAPIProviderShutdown de un** proveedor. Los clientes MAPI siempre deben usar [la interfaz IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) 
    
- Si un proveedor MAPI necesita asegurarse de que no se usa el apagado rápido mientras se carga, debe implementar la interfaz **IMAPIProviderShutdown** y devolver MAPI_E_NO_SUPPORT para el método **IMAPIProviderShutdown::QueryFastShutdown.** Sin embargo, en el caso de clientes MAPI como Outlook, esto hará que el cliente abandone el apagado rápido y que se deba tardar más tiempo en apagarse. 
    
## <a name="see-also"></a>Vea también



[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)
  
[Información general sobre el apagado rápido](fast-shutdown-overview.md)
  
[Opciones de usuario de apagado rápido](fast-shutdown-user-options.md)

