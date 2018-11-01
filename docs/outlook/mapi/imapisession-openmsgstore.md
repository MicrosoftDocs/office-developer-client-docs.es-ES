---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fdf75787153f9a85e6a7bcddff44cf2c468a7975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595037"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Se abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para aún más el acceso. 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parámetros

_ulUIParam_
  
> [entrada] Un identificador de la ventana primaria del cuadro de diálogo dirección común y otros relacionados con la muestra.
    
_cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
_lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del almacén de mensajes que se va a abrir. El parámetro _lpEntryID_ no debe ser NULL. 
    
_lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al almacén de mensajes. Pasando NULL hace que el parámetro _lppMDB_ devolver un puntero a la interfaz estándar para un almacén de mensajes (**IMsgStore**).
    
_ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
  - MAPI_BEST_ACCESS: Las solicitudes que se abre el almacén de mensajes con los permisos de red máximo permiten para el usuario y el número máximo de clientes permisos de la aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el almacén de mensajes con permiso de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el almacén de mensajes con permiso de sólo lectura. 
      
  - MAPI_DEFERRED_ERRORS: Permite **OpenMsgStore** devolver correctamente, posiblemente antes de que el mensaje almacén es completamente disponible para el cliente de la llamada. Si el almacén de mensajes no está disponible, realizar una llamada de objeto posteriores puede provocar un error. 
      
  - MDB\_NO_DIALOG: impide que la presentación de cuadros de diálogo de inicio de sesión. Si se establece este indicador y **OpenMsgStore** dispone de información de configuración incompleta para abrir el almacén de mensajes sin ayuda del usuario, devuelve MAPI_E_LOGON_FAILED. Si no se establece este indicador, el proveedor de almacenamiento de mensajes puede preguntar al usuario para corregir un nombre o una contraseña o para llevar a cabo otras acciones que son necesarios para establecer una conexión con el almacén de mensajes. 
      
  - MDB\_NO_MAIL: el almacén de mensajes no se debe usar para enviar o recibir correo. Cuando se establece este marcador, MAPI no notifica a la cola MAPI que se va a abrir este almacén de mensajes.
      
  - MDB\_ONLINE: en modo caché de Exchange, un proveedor de servicio o cliente puede llamar a este método con MDB_ONLINE para reemplazar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto. No se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.
      
  - MDB_TEMPORARY: Indica a MAPI que el almacén de mensajes no es permanente y no se debe agregar a la tabla de almacenamiento de mensajes. Este indicador se utiliza para iniciar sesión en el almacén de mensajes, por lo que la información se puede recuperar mediante programación desde la sección de perfil. 
      
  - MDB_WRITE: Las solicitudes de lectura y escritura permiso para el almacén de mensajes.
    
_lppMDB_
  
> [out] Puntero a un puntero del almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El almacén de mensajes se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a un almacén de mensajes para los que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> El almacén de mensajes indicado por _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha realizado correctamente, pero el proveedor de almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para obtener la información de error desde el proveedor, llame al método [IMAPISession::GetLastError](imapisession-getlasterror.md) . Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::OpenMsgStore** abre un almacén de mensajes determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El nivel de permisos predeterminado para los almacenes de mensajes es de sólo lectura. Si se establece la marca MDB_WRITE, que aún es posible que no se concedido permiso de lectura y escritura. El nivel final de acceso que se asigna MAPI para el almacén de mensajes depende de su nivel de permiso, el mensaje almacén propio y el proveedor de almacén de mensajes. 
  
Si se llama **OpenMsgStore** para abrir un almacén de mensajes con permiso de sólo lectura, ocurrirá lo siguiente: 
  
- El almacén **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) (propiedad) no tendrá su almacén de\_MODIFY_OK y almacén de\_CREATE_OK bits conjunto. 
    
- Se producirá un error en las llamadas para abrir uno de los mensajes o las carpetas del almacén de mensajes mediante el uso de [IMAPISession::OpenEntry](imapisession-openentry.md) con el conjunto de marca MAPI_MODIFY. 
    
- Se producirá un error en las llamadas para abrir una de las propiedades de los mensajes o las carpetas del almacén de mensajes mediante el uso de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con la marca MAPI_MODIFY. 
    
- Se producirá un error en las llamadas a cualquiera de los métodos siguientes: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Las llamadas a los métodos siguientes se producirá un error si el destino del mensaje copiado de es de sólo lectura, si el destino es el mismo que el almacén de mensajes de origen o es otro almacén de sólo lectura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI utiliza el método **IMAPISession::OpenMsgStore** para abrir un almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
- [Usar Macros para el tratamiento de errores](using-macros-for-error-handling.md)

