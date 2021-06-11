---
title: IMAPIProviderShutdown IUnknown
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
  
Permite que el subsistema MAPI informe a un proveedor MAPI del apagado rápido de un cliente MAPI, de modo que el proveedor MAPI pueda responder al apagado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos provider: [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)o [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementado por:  <br/> |Proveedor MAPI  <br/> |
|Llamado por:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Consulta al proveedor MAPI la compatibilidad con el apagado rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido, de modo que el proveedor puede realizar acciones para evitar la pérdida de datos.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica al proveedor MAPI que el cliente MAPI sale inmediatamente, de modo que el proveedor MAPI persistirá en los cambios para evitar la pérdida de datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El apagado rápido permite que un cliente MAPI salga de su proceso en poco tiempo, con suerte después de que el cliente y los proveedores MAPI cargados han guardado la configuración y los datos mapi. El cliente MAPI siempre inicia un apagado rápido y debe consultar el subsistema MAPI para obtener compatibilidad con el apagado rápido de los proveedores MAPI cargados. Un administrador puede establecer el Windows en el nivel de usuario para especificar el nivel de compatibilidad del proveedor que es necesario para permitir el apagado rápido de todos los clientes MAPI. Para obtener más información acerca de la configuración del Registro, vea [Fast Shutdown User Options](fast-shutdown-user-options.md). Sin embargo, para que el apagado rápido se produzca correctamente sin pérdida de datos, los proveedores MAPI deben implementar la **interfaz IMAPIProviderShutdown.** 
  
Un proveedor MAPI que necesita admitir el apagado rápido del cliente debe devolver S_OK al subsistema MAPI en el **método IMAPIProviderShutdown::QueryFastShutdown.** Cuando el subsistema MAPI llama posteriormente a los métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::D oFastShutdown,** el proveedor MAPI debe realizar las acciones necesarias para guardar la configuración y los datos MAPI y prepararse para la salida del cliente. 
  
Los proveedores MAPI que no necesitan admitir el cierre rápido del cliente deben implementar la interfaz **IMAPIProviderShutdown** y hacer que el método **IMAPIProviderShutdown::QueryFastShutdown** devuelva MAPI_E_NO_SUPPORT. Para Outlook como cliente MAPI, esto hace que Outlook esperar a que se liberarán todas las referencias externas antes de salir. 
  
Según la configuración del Registro Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un cierre rápido del cliente. 
  
Para obtener más información sobre el proceso de apagado rápido, vea [Fast Shutdown Overview](fast-shutdown-overview.md). Para obtener información sobre cómo realizar el apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

