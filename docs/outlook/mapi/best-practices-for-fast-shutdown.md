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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318147"
---
# <a name="best-practices-for-fast-shutdown"></a>Procedimientos recomendados para el apagado rápido

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se recomiendan los procedimientos recomendados para administradores, clientes MAPI y proveedores MAPI para usar la configuración del registro de Windows y las interfaces de apagado rápido para minimizar la pérdida de datos durante el cierre del cliente.
  
- Para que un cliente MAPI realice un apagado rápido correctamente para que los procesos del proveedor no tengan la pérdida de datos, el cliente MAPI debe llamar primero al método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . A continuación, el cliente debe continuar con los métodos [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) y [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) según la compatibilidad del subsistema MAPI para el apagado rápido, como se indica en el valor devuelto de ** IMAPIClientShutdown:: QueryFastShutdown**. Como cliente MAPI, Microsoft Outlook no llama a **IMAPIClientShutdown:: NotifyProcessShutdown** o **IMAPIClientShutdown::D ofastshutdown** si **IMAPIClientShutdown:: QueryFastShutdown** devuelve un error. Si el administrador ha deshabilitado el apagado rápido en el registro de Windows, el subsistema MAPI devolverá MAPI_E_NO_SUPPORT a **IMAPIClientShutdown:: QueryFastShutdown**. En este caso, el subsistema MAPI no informará a los proveedores MAPI de una salida de proceso de cliente inmediato. Por lo tanto, si un cliente MAPI no tiene en cuenta este código de retorno de error, continúa con el apagado rápido y desconecta todas las referencias externas, todos los proveedores MAPI cargados tendrán pérdida de datos. 
    
- Los proveedores MAPI deben implementar la interfaz [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para llevar a cabo los pasos oportunos y necesarios para evitar la pérdida de datos debido a que el cliente desconecta las referencias externas antes de que el cliente salga. Un proveedor debe posponer todo lo que no sea esencial para guardar datos en su almacén de datos principal. Por ejemplo, un proveedor de transporte debe posponer las operaciones en segundo plano innecesarias que comprueban si hay correo nuevo, un proveedor de la libreta de direcciones debe posponer la descarga de los cambios recientes de su servidor, y un proveedor de almacén debe posponer las tareas de mantenimiento como compactación o indización. 
    
- Los usuarios que quieren que los clientes de MAPI salgan en cuanto los cierren deben usar la configuración predeterminada del registro que permite el apagado rápido a menos que un proveedor decida.
    
- Una vez que un cliente MAPI llama a **IMAPIClientShutdown::D ofastshutdown**, no debe realizar ninguna llamada adicional a MAPI, incluida la función [MAPIUninitialize](mapiuninitialize.md) . El cliente no debe usar MAPI para el resto de la duración del proceso del cliente. 
    
- Un cliente MAPI nunca debe llamar directamente a la interfaz **IMAPIProviderShutdown** de un proveedor. Los clientes MAPI siempre deben usar la interfaz [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) . 
    
- Si un proveedor MAPI tiene que asegurarse de que no se usa el apagado rápido mientras se carga, debe implementar la interfaz **IMAPIProviderShutdown** y devolver MAPI_E_NO_SUPPORT para el método **IMAPIProviderShutdown:: QueryFastShutdown** . Sin embargo, para los clientes MAPI como Outlook, esto hará que el cliente abandone el apagado rápido y tarde más tiempo en cerrarse. 
    
## <a name="see-also"></a>Vea también



[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)
  
[Información general sobre el apagado rápido](fast-shutdown-overview.md)
  
[Opciones de usuario de apagado rápido](fast-shutdown-user-options.md)

