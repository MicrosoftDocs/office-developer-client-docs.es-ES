---
title: Estado de implementación de objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336340"
---
# <a name="status-object-implementation"></a>Estado de implementación de objeto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de servicios deben implementar un objeto de estado y proporcionar propiedades desde él a la tabla de estado de la sesión. Puede incluir una o más filas en la tabla de estado, según el número de recursos que controle. Un proveedor de transporte, por ejemplo, debe crear una fila en la tabla de estado para cada cola de mensajes que administra. Cuando se producen cambios, se debe actualizar la fila de tabla de estado adecuada. Los objetos status se implementan para proporcionar acceso tanto a la información incluida en la tabla de estado como a información adicional no incluida en la tabla.
  
### <a name="to-implement-a-status-object"></a>Para implementar un objeto status

1. Implemente **el método OpenStatusEntry** del objeto de inicio de sesión. Cuando los clientes desean abrir el objeto de estado, llaman a [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI cumple la solicitud abierta llamando al método **OpenStatusEntry** del proveedor, lo que hace que el proveedor abra su objeto de estado y devuelva al cliente un puntero a su **implementación IMAPIStatus.** En la **implementación de OpenStatusEntry,** siga estos pasos: 
    
   1. Realice las siguientes tareas si el objeto de inicio de sesión aún no ha creado un objeto de estado:
    
      1. Llame al método [IMAPISupport::OpenProfileSection del](imapisupport-openprofilesection.md) objeto de soporte técnico para obtener acceso a la sección de perfil del proveedor. 
          
      2. Cree un nuevo objeto de estado.
          
      3. Almacene una referencia a la sección de perfil en el objeto de estado del proveedor y llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de la sección de perfil para incrementar su recuento de referencias. 
          
      4. Almacene una referencia al objeto de inicio de sesión en el objeto de estado del proveedor y llame al método **IUnknown::AddRef** del objeto de inicio de sesión para incrementar su recuento de referencias. 
          
      5. Almacene una referencia al objeto de estado en el objeto de inicio de sesión del proveedor.
    
   2. Llame al método **IUnknown::AddRef** del objeto de estado para incrementar su recuento de referencias en el objeto de inicio de sesión. 
    
   3. Establezca la propiedad del objeto de **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) en MAPI_STATUS.
    
   4. Establezca el  _parámetro de salida lppMAPIStatus_ para que apunte al objeto status y devuelva. 
    
   5. Compruebe el _parámetro de entrada ulFlags._ Si se establece en MAPI_MODIFY y el proveedor admite acceso de lectura y escritura a su objeto de estado, devuelva un objeto que se puede escribir. Sin embargo, si el proveedor no admite el acceso de lectura y escritura a su objeto de estado, no se producirá un error. Devuelve un objeto de estado de solo lectura. Los clientes que esperan recibir objetos de estado de lectura y escritura deben comprobar que se ha concedido permiso de lectura y escritura antes de intentar realizar cambios. 
    
2. Establezca todas las propiedades de objeto de estado y tabla de estado necesarias. Las propiedades que incluya en la fila de la tabla de estado deben estar disponibles a través del objeto de estado, excepto las propiedades calculadas por MAPI. Las propiedades necesarias son las siguientes:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implemente [los métodos IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) adecuados para su proveedor. Según el proveedor, no es necesario implementar los cuatro métodos de **IMAPIStatus**. Cada proveedor debe implementar una versión de solo lectura de los métodos de la interfaz [IMAPIProp : IUnknown](imapipropiunknown.md) y el [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 

   Los proveedores de transporte también deben implementar [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)y todos los proveedores deben admitir [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). Sin embargo, la compatibilidad [con IMAPIStatus::ChangePassword](imapistatus-changepassword.md) es opcional. Solo los proveedores de servicios que requieren contraseñas y desean permitir que los usuarios las cambien mediante programación necesitan implementar este método. Para cada método que admita, establezca el bit correspondiente en la **PR_RESOURCE_METHODS** propiedad. Por ejemplo, si solo admite **ValidateState** y **SettingsDialog,** **establezca PR_RESOURCE_METHODS** en lo siguiente: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Los clientes deben comprobar el valor **de PR_RESOURCE_METHODS** antes de intentar llamar al objeto de estado. Controla las llamadas a cualquiera de los métodos no compatibles devolviendo MAPI_E_NO_SUPPORT. 
    
4. Llama [a IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) durante el inicio de sesión para agregar la fila o filas a la tabla de estado. Pase una matriz de valores de propiedad que contenga la información de columna de la fila y 0 para el _parámetro ulFlags._ Si en algún momento más adelante en la sesión cambia el estado del proveedor y es necesario actualizar la información de columna, vuelva a llamar a **ModifyStatusRow** con el STATUSROW_UPDATE marca establecida. 
    
Para obtener más información acerca de los objetos de estado, vea [Objetos de estado MAPI](mapi-status-objects.md).
  
## <a name="see-also"></a>Vea también

- [Proveedores de servicios MAPI](mapi-service-providers.md)

