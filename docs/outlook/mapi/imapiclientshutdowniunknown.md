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
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435337"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que un cliente MAPI lleve a cabo el apagado rápido del proceso de cliente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |[IMAPISession (objeto)](imapisessioniunknown.md)  <br/> |
|Implementado por:  <br/> |Subsistema MAPI  <br/> |
|Llamado por:  <br/> |Cliente MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Consulta el subsistema MAPI para obtener compatibilidad con el apagado rápido que proporcionan los proveedores MAPI cargados.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indica la intención del cliente MAPI de continuar con el apagado.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indica la intención del cliente MAPI de salir del proceso de cliente inmediatamente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El propósito del apagado rápido es permitir que un cliente MAPI y cualquier proveedor MAPI cargado con el que el cliente MAPI tenga una sesión MAPI activa guarden la configuración y los datos mapi. Esto permite al cliente MAPI desconectar todas las referencias externas y salir sin causar ninguna pérdida de datos. Un cliente MAPI que necesita realizar un apagado rápido debe usar la **interfaz IMAPIClientShutdown.** El cliente MAPI puede obtener un puntero a esta interfaz llamando al método IUnknown::QueryInterface en cualquier [objeto IMAPISession.](imapisessioniunknown.md) 
  
Un cliente MAPI siempre inicia un apagado rápido llamando al método **IMAPIClientShutdown::QueryFastShutdown.** El subsistema MAPI responde a la consulta del cliente MAPI comprobando si los proveedores MAPI cargados admiten el apagado rápido del cliente. El administrador puede usar la Windows del Registro para ayudar a determinar el nivel de compatibilidad del proveedor que es necesario para que los clientes MAPI continúen con el apagado rápido. Para obtener más información, vea [Fast Shutdown User Options](fast-shutdown-user-options.md).
  
Para continuar con el apagado rápido, el cliente llama al método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar al subsistema MAPI la intención de cerrar. A continuación, el cliente llama al método **IMAPIClientShutdown::D oFastShutdown** para indicar que el proceso de cliente se está saliendo inmediatamente. 
  
Para obtener más información sobre el apagado rápido, vea [Fast Shutdown Overview](fast-shutdown-overview.md). Para obtener información sobre cómo realizar el apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

