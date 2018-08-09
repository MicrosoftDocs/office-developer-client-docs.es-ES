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
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817458"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite que el subsistema MAPI informar a un proveedor de MAPI del cierre rápido de un cliente MAPI, por lo que el proveedor MAPI puede responder a la que se cerró.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de proveedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)o [IMSProvider](imsprovideriunknown.md) <br/> |
|Se implementa mediante:  <br/> |Proveedor MAPI  <br/> |
|Llamado por:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Las consultas que admite el proveedor MAPI de apagado rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica que el proveedor MAPI que el cliente MAPI está saliendo inmediatamente, para que el proveedor MAPI guardará los cambios para evitar la pérdida de datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cierre rápido permite que un cliente MAPI salir de su proceso dentro de una hora corta, es de esperar que después de que el cliente y se carga proveedores MAPI han guardado de datos y la configuración de MAPI. El cliente MAPI siempre inicia un apagado rápido y debe consultar el subsistema MAPI para soporte técnico de apagado rápido de los proveedores MAPI cargados. Un administrador puede establecer el registro de Windows en el nivel de usuario para especificar el nivel de compatibilidad de proveedor que es necesario para permitir que cierre rápido de todos los clientes MAPI. Para obtener más información acerca de la configuración del registro, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md). Sin embargo, para que apagado rápido correctamente se produzca sin pérdida de datos, proveedores MAPI deben implementar la interfaz de **IMAPIProviderShutdown** . 
  
Un proveedor de MAPI que necesita para admitir apagado rápido de cliente debe devolver S_OK para el subsistema MAPI en el método **IMAPIProviderShutdown::QueryFastShutdown** . Cuando el subsistema MAPI posteriormente llama a los métodos **IMAPIProviderShutdown::NotifyProcessShutdown** y **IMAPIProviderShutdown::DoFastShutdown** , el proveedor MAPI debe realizar las acciones necesarias para guardar los datos y la configuración de MAPI y Preparar para salir del cliente. 
  
Proveedores MAPI que no es necesario para admitir el apagado rápido cliente aún deben implementar la interfaz **IMAPIProviderShutdown** y tener el método **IMAPIProviderShutdown::QueryFastShutdown** devolver MAPI_E_NO_SUPPORT. Para Outlook como un cliente MAPI, esto hace que Outlook que se debe esperar para que todas las referencias externas a liberarse antes de que exista. 
  
Dependiendo del registro de Windows del usuario configuración de apagado rápido, no se implementa la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido de cliente. 
  
Para obtener más información acerca del proceso de apagado rápido, consulte [Información general de cierre rápido](fast-shutdown-overview.md). Para obtener información acerca de cómo llevar a cabo apagado rápido correctamente, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)
  
[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

