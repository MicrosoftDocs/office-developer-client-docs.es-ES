---
title: IUnknown IMAPIProviderShutdown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409660"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite al subsistema MAPI informar a un proveedor MAPI del apagado rápido de un cliente MAPI, de modo que el proveedor MAPI pueda responder al cierre.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objetos de proveedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)o [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementado por:  <br/> |Proveedor MAPI  <br/> |
|Llamado por:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Consulta al proveedor MAPI para obtener compatibilidad con el apagado rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido para que el proveedor pueda emprender acciones para evitar la pérdida de datos.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica al proveedor MAPI que el cliente MAPI está saliendo inmediatamente, de modo que el proveedor MAPI mantendrá los cambios para evitar la pérdida de datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El apagado rápido permite que un cliente MAPI salga de su proceso en un breve período de tiempo, afortunadamente después de que el cliente y los proveedores MAPI cargados hayan guardado la configuración y los datos de MAPI. El cliente MAPI siempre inicia un apagado rápido y debe consultar el subsistema MAPI para obtener compatibilidad con el apagado rápido de los proveedores MAPI cargados. Un administrador puede establecer el registro de Windows en el nivel de usuario para especificar el nivel de compatibilidad con proveedores que es necesario para permitir el apagado rápido de todos los clientes MAPI. Para obtener más información acerca de la configuración del registro, consulte [Opciones de usuario de apagado rápido](fast-shutdown-user-options.md). Sin embargo, para que el apagado rápido se produzca correctamente sin pérdida de datos, los proveedores MAPI deben implementar la interfaz **IMAPIProviderShutdown** . 
  
Un proveedor MAPI que deba admitir el apagado rápido del cliente debe devolver S_OK al subsistema MAPI en el método **IMAPIProviderShutdown:: QueryFastShutdown** . Cuando el subsistema MAPI llama a continuación a los métodos **IMAPIProviderShutdown:: NotifyProcessShutdown** y **IMAPIProviderShutdown::D ofastshutdown** , el proveedor MAPI debe realizar las acciones necesarias para guardar la configuración y los datos de MAPI y Prepárese para la salida del cliente. 
  
Los proveedores MAPI que no necesitan admitir el apagado rápido de cliente deben seguir implementando la interfaz **IMAPIProviderShutdown** y tienen el método **IMAPIProviderShutdown:: QueryFastShutdown** devuelve MAPI_E_NO_SUPPORT. Para Outlook como cliente MAPI, esto hace que Outlook espere a que se liberen todas las referencias externas antes de su salida. 
  
En función de la configuración del registro de Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido del cliente. 
  
Para obtener más información acerca del proceso de apagado rápido, consulte [información general sobre el apagado rápido](fast-shutdown-overview.md). Para obtener información acerca de cómo llevar a cabo el apagado rápido correctamente, consulte [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

