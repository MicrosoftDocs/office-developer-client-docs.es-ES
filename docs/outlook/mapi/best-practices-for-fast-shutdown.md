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
ms.openlocfilehash: 0d9e7caf43bcee654aa92652e94bc8c2ebba18e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816506"
---
# <a name="best-practices-for-fast-shutdown"></a>Procedimientos recomendados para el apagado rápido

  
  
**Hace referencia a**: Outlook 
  
En este tema, se recomienda mejores prácticas para los administradores, los clientes MAPI y proveedores de MAPI usar la configuración del registro de Windows y las interfaces de apagado rápido para minimizar la pérdida de datos durante el cierre del cliente.
  
- Para que un cliente MAPI para llevar a cabo apagado rápido correctamente para que los procesos de proveedor no provocar una pérdida de datos, el cliente MAPI debe llamar al método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . A continuación, debe proceder el cliente con los métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) y [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) en función de apagado rápido, la compatibilidad con del subsistema MAPI indicada por el valor devuelto de ** IMAPIClientShutdown::QueryFastShutdown**. Como un cliente MAPI, Microsoft Outlook no llama a **IMAPIClientShutdown::NotifyProcessShutdown** o **IMAPIClientShutdown::DoFastShutdown** si **IMAPIClientShutdown::QueryFastShutdown** devuelve un error. Si el administrador ha deshabilitado el apagado rápido en el registro de Windows, el subsistema MAPI devolvería MAPI_E_NO_SUPPORT a **IMAPIClientShutdown::QueryFastShutdown**. En este caso, el subsistema MAPI podría no informar a salir de los proveedores MAPI de un proceso de cliente inmediato. Por lo tanto, si un cliente MAPI no tiene en cuenta este código de retorno de error, continúa con rapidez en el cierre y desconecta todas las referencias externas, todos los proveedores MAPI cargados tendrán pérdida de datos. 
    
- Proveedores MAPI deben implementar la [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interfaz para llevar a cabo pasos oportunos y es necesarios para evitar la pérdida de datos debido al cliente desconectar las referencias externas antes de que salga el cliente. Un proveedor debe posponer todo lo demás que es que no son esenciales para guardar datos en su almacén de datos principal. Por ejemplo, un proveedor de transporte debe posponer operaciones en segundo plano innecesarios que buscar correo nuevo, que un proveedor de la libreta de direcciones debe posponer la descarga de los cambios recientes de su servidor, y un proveedor de almacenamiento debe posponer tareas de mantenimiento como Compactar o indización. 
    
- Los usuarios que desean que los clientes MAPI para salir tan pronto como se cierran ellos deben usar la configuración del registro de forma predeterminada que permite apagado rápido a menos que aporta a un proveedor de.
    
- Una vez que un cliente MAPI llama **IMAPIClientShutdown::DoFastShutdown**, no debe hacer que las llamadas MAPI, incluidas la función [MAPIUninitialize](mapiuninitialize.md) adicionales. El cliente no debe utilizar MAPI para el resto de la duración del proceso de cliente. 
    
- Un cliente MAPI nunca directamente debe llamar a la interfaz de **IMAPIProviderShutdown** de un proveedor. Los clientes MAPI siempre deben usar el [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interfaz. 
    
- Si necesita un proveedor de MAPI para asegurarse de que el cierre rápido no se usa mientras se carga, debe implementar la interfaz **IMAPIProviderShutdown** y devolver MAPI_E_NO_SUPPORT para el método **IMAPIProviderShutdown::QueryFastShutdown** . Sin embargo, para los clientes MAPI, como Outlook, esto hará que el cliente abandonar apagado rápido y tomar más tiempo en Apagar. 
    
## <a name="see-also"></a>Vea también



[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)
  
[Información general sobre el apagado rápido](fast-shutdown-overview.md)
  
[Opciones de usuario de apagado rápido](fast-shutdown-user-options.md)

