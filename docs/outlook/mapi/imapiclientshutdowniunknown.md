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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817218"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite a un cliente MAPI para llevar a cabo el apagado rápido del proceso de cliente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objeto [IMAPISession](imapisessioniunknown.md)  <br/> |
|Se implementa mediante:  <br/> |Subsistema MAPI  <br/> |
|Llamado por:  <br/> |Cliente MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Las consultas admiten el subsistema MAPI para apagado rápido proporcionado por proveedores MAPI cargados.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indica la intención de continuar con la del cliente MAPI cerrado.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indica la intención del cliente MAPI para salir inmediatamente el proceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El propósito de apagado rápido es permitir que un cliente MAPI y cualquier proveedor MAPI cargado con la que el cliente MAPI tiene una sesión activa de MAPI para guardar los datos y la configuración de MAPI. Esto permite que el cliente MAPI desconectar todas las referencias externas y salir sin que se produzca ninguna pérdida de datos. Un cliente MAPI que necesita para llevar a cabo el apagado rápido debe usar la interfaz **IMAPIClientShutdown** . El cliente MAPI puede obtener un puntero a esta interfaz llamando al método IUnknown:: QueryInterface en cualquier objeto [IMAPISession](imapisessioniunknown.md) . 
  
Un cliente MAPI siempre inicia un apagado rápido llamando al método **IMAPIClientShutdown::QueryFastShutdown** . El subsistema MAPI se responde a la consulta del cliente MAPI comprobando si proveedores MAPI cargados admiten apagado rápido del cliente. El administrador puede usar la configuración del registro de Windows para ayudar a determinar el nivel de compatibilidad de proveedor que es necesario para los clientes MAPI continuar con el apagado rápido. Para obtener más información, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).
  
Para continuar con el apagado rápido, el cliente llama al método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar al subsistema MAPI la intención de apagado. El cliente, a continuación, llama al método de **IMAPIClientShutdown::DoFastShutdown** para indicar que el proceso de cliente está saliendo inmediatamente. 
  
Para obtener más información acerca de apagado rápido, consulte [Información general de cierre rápido](fast-shutdown-overview.md). Para obtener información sobre cómo se realiza correctamente apagado rápido, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

