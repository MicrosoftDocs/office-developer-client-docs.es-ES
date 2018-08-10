---
title: Implementación de objeto de estado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 379378f2092f7b119a40ac44cbdcfa03f254b448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820773"
---
# <a name="status-object-implementation"></a>Implementación de objeto de estado

**Hace referencia a**: Outlook 
  
Todos los proveedores de servicio deben implementar un objeto de estado y proporcione las propiedades de él en la tabla de estado de sesión. Puede incluir una o varias filas en la tabla de estado, según el número de recursos que controlan. Por ejemplo, un proveedor de transporte, debe crear una fila en la tabla de estado para cada cola de mensajes que administra. Cuando se producen cambios, se debe actualizar la fila de la tabla de estado apropiado. Para proporcionar acceso a la información incluida en la tabla de estado y a información adicional que no se incluyen en la tabla que se implementan los objetos de estado.
  
### <a name="to-implement-a-status-object"></a>Para implementar un objeto de estado

1. Implemente el método **OpenStatusEntry** de su objeto de inicio de sesión. Cuando los clientes desean abrir el objeto de estado, que llamen [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI cumple la solicitud abierta mediante una llamada al método **OpenStatusEntry** de su proveedor, lo que provoca que el proveedor abrir su objeto de estado y devolver al cliente un puntero a su implementación **IMAPIStatus** . En la implementación de **OpenStatusEntry** , complete los siguientes pasos: 
    
   1. Si el objeto de inicio de sesión todavía no ha creado un objeto de estado, realice las siguientes tareas:
    
      1. Llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte para obtener acceso a la sección de perfil de su proveedor. 
          
      2. Crear un nuevo objeto de estado.
          
      3. Almacenar una referencia a la sección de perfil en el objeto de estado de su proveedor y llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de la sección de perfil para incrementar su recuento de referencia. 
          
      4. Almacenar una referencia al objeto de inicio de sesión en el objeto de estado de su proveedor y llamar al método **IUnknown:: AddRef** del objeto de inicio de sesión para incrementar su recuento de referencia. 
          
      5. Almacenar una referencia al objeto de estado en el objeto de inicio de sesión de su proveedor.
    
   2. Llamar al método **IUnknown:: AddRef** del objeto de estado para incrementar su recuento de referencia en el objeto de inicio de sesión. 
    
   3. Establecer propiedad de **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) del objeto de estado a MAPI_STATUS.
    
   4. Establezca el parámetro de salida _lppMAPIStatus_ para apuntar al objeto de estado y devolver. 
    
   5. Compruebe el parámetro de entrada _ulFlags_ . Si se establece en MAPI_MODIFY y su proveedor admite el acceso de lectura y escritura a su objeto de estado, devolver un objeto grabable. Sin embargo, si su proveedor no admite el acceso de lectura y escritura a su objeto de estado, no producirá un error. Devolver un objeto de estado que es de sólo lectura. Los clientes que se esperan recibir objetos de estado de lectura y escritura deben comprobar que se ha concedido permiso de lectura y escritura antes de intentar realizar cambios. 
    
2. Establecer todas el estado requerido objeto y estado de las propiedades de tabla. Las propiedades que incluyen en la fila de la tabla de estado deben estar disponibles a través de su objeto de estado, excepto para las propiedades calculadas por MAPI. Las propiedades necesarias son los siguientes:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implementar la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) métodos que son adecuados para su proveedor. Dependiendo del proveedor, no es necesario implementar todos de los cuatro métodos de **IMAPIStatus**. Todos los proveedores deben implementar una versión de solo lectura de los métodos de la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz y el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 

   Los proveedores de transporte también deben implementar [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md), y todos los proveedores deben admitir [SettingsDialog](imapistatus-settingsdialog.md). Sin embargo, la compatibilidad con [IMAPIStatus](imapistatus-changepassword.md) es opcional. Proveedores de servicios que requieren que las contraseñas y desean permitir a los usuarios cambiar ellos mediante programación necesitan implementar este método. Para cada método que admita, establezca el bit correspondiente en la propiedad **PR_RESOURCE_METHODS** . Por ejemplo, si admite sólo **ValidateState** y **diálogo Configuración** , establezca **PR_RESOURCE_METHODS** en lo siguiente: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Los clientes deben comprobar el valor de **PR_RESOURCE_METHODS** antes de intentar llamar a su objeto de estado. Controlar las llamadas a cualquiera de los métodos no admitidos mediante la devolución de MAPI_E_NO_SUPPORT. 
    
4. Llamar a [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) durante el inicio de sesión para agregar la fila o las filas a la tabla de estado. Pase una matriz de valores de propiedad que contiene la información de columna de la fila y 0 para el parámetro _ulFlags indicado_ . Si en algún momento más adelante en la sesión de los cambios del estado de su proveedor y lo pasa a ser necesarios para actualizar la información de columna, vuelva a llamar **ModifyStatusRow** con el conjunto de marca STATUSROW_UPDATE. 
    
Para obtener más información acerca de los objetos de estado, vea [Objetos de estado de MAPI](mapi-status-objects.md).
  
## <a name="see-also"></a>Vea también

- [Proveedores de servicios de MAPI](mapi-service-providers.md)

