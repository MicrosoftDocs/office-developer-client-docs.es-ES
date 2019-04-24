---
title: IUnknown IMAPIClientShutdown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350879"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite a un cliente MAPI realizar un apagado rápido del proceso de cliente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objeto [IMAPISession](imapisessioniunknown.md)  <br/> |
|Implementado por:  <br/> |Subsistema MAPI  <br/> |
|Llamado por:  <br/> |Cliente MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Consulta el subsistema MAPI para obtener compatibilidad con el apagado rápido que proporcionan los proveedores MAPI cargados.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indica la intención del cliente MAPI de continuar con el cierre.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indica la intención del cliente MAPI de salir inmediatamente del proceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El propósito del apagado rápido es permitir a un cliente MAPI y a cualquier proveedor MAPI cargado con el que el cliente MAPI haya una sesión de MAPI activa para guardar la configuración y los datos de MAPI. Esto permite al cliente MAPI desconectar todas las referencias externas y salir sin provocar pérdida de datos. Un cliente MAPI que necesite realizar un apagado rápido debe usar la interfaz **IMAPIClientShutdown** . El cliente MAPI puede obtener un puntero a esta interfaz llamando al método IUnknown:: QueryInterface en cualquier objeto [IMAPISession](imapisessioniunknown.md) . 
  
Un cliente MAPI siempre inicia un apagado rápido mediante una llamada al método **IMAPIClientShutdown:: QueryFastShutdown** . El subsistema MAPI responde a la consulta del cliente MAPI comprobando si los proveedores MAPI cargados admiten el apagado rápido del cliente. El administrador puede usar la configuración del registro de Windows para ayudar a determinar el nivel de compatibilidad del proveedor que es necesario para que los clientes MAPI continúen con el apagado rápido. Para obtener más información, consulte [Opciones de usuario de apagado rápido](fast-shutdown-user-options.md).
  
Para continuar con el apagado rápido, el cliente llama al método **IMAPIClientShutdown:: NotifyProcessShutdown** para indicar al subsistema MAPI la intención de cerrarse. A continuación, el cliente llama al método **IMAPIClientShutdown::D ofastshutdown** para indicar que el proceso de cliente está saliendo inmediatamente. 
  
Para obtener más información acerca del apagado rápido, consulte [información general sobre el apagado rápido](fast-shutdown-overview.md). Para obtener información acerca de cómo realizar el apagado rápido correctamente, consulte [procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

