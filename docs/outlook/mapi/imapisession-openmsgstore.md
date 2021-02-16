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
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418025"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para obtener más acceso. 
  
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
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo de dirección común y otras pantallas relacionadas.
    
_cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
_lpEntryID_
  
> [entrada] Puntero al identificador de entrada del almacén de mensajes que se va a abrir. El  _parámetro lpEntryID_ no debe ser NULL. 
    
_lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al almacén de mensajes. Pasar NULL hace que  _el parámetro lppMDB_ devuelva un puntero a la interfaz estándar de un almacén de mensajes (**IMsgStore**).
    
_ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden usar las siguientes marcas:
    
  - MAPI_BEST_ACCESS: solicita que el almacén de mensajes se abra con los permisos de red máximos permitidos para el usuario y los permisos máximos de la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el almacén de mensajes debe abrirse con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el almacén de mensajes debe abrirse con permiso de solo lectura. 
      
  - MAPI_DEFERRED_ERRORS: permite que **OpenMsgStore** vuelva correctamente, posiblemente antes de que el almacén de mensajes esté totalmente disponible para el cliente que realiza la llamada. Si el almacén de mensajes no está disponible, realizar una llamada a objeto posterior puede generar un error. 
      
  - MDB \_ NO_DIALOG: impide que se muestren cuadros de diálogo de inicio de sesión. Si se establece esta marca y **OpenMsgStore** no tiene suficiente información de configuración para abrir el almacén de mensajes sin la ayuda del usuario, devuelve MAPI_E_LOGON_FAILED. Si no se establece esta marca, el proveedor del almacén de mensajes puede pedir al usuario que corrija un nombre o contraseña o que realice otras acciones necesarias para establecer una conexión con el almacén de mensajes. 
      
  - MDB \_ NO_MAIL: el almacén de mensajes no debe usarse para enviar o recibir correo. Cuando se establece esta marca, MAPI no notifica a la cola MAPI que se está abierto este almacén de mensajes.
      
  - MDB ONLINE: en modo caché de Exchange, un cliente o proveedor de servicios puede llamar a este método con MDB_ONLINE para invalidar la conexión al almacén de mensajes local y abrir el almacén en el \_ servidor remoto. No puede abrir un almacén de Exchange en modo almacenado en caché y en modo no almacenado en caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.
      
  - MDB_TEMPORARY: indica a MAPI que el almacén de mensajes no es permanente y no debe agregarse a la tabla del almacén de mensajes. Esta marca se usa para iniciar sesión en el almacén de mensajes de modo que la información se pueda recuperar mediante programación desde la sección de perfil. 
      
  - MDB_WRITE: solicita permiso de lectura y escritura en el almacén de mensajes.
    
_lppMDB_
  
> [salida] Puntero a un puntero del almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El almacén de mensajes se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un almacén de mensajes para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> El almacén de mensajes indicado por  _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md) Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::OpenMsgStore** abre un almacén de mensajes determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El nivel de permisos predeterminado para los almacenes de mensajes es de solo lectura. Si establece la marca MDB_WRITE, es posible que aún no se le conceda permiso de lectura y escritura. El nivel final de acceso que MAPI asigna al almacén de mensajes depende del nivel de permisos, del propio almacén de mensajes y del proveedor del almacén de mensajes. 
  
Si llama a **OpenMsgStore para** abrir un almacén de mensajes con permiso de solo lectura, se producirá lo siguiente: 
  
- La propiedad **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén no tendrá los bits MODIFY_OK \_ y STORE CREATE_OK \_ bits. 
    
- Las llamadas para abrir uno de los mensajes o carpetas del almacén de mensajes mediante [IMAPISession::OpenEntry](imapisession-openentry.md) con la marca MAPI_MODIFY se producirá un error. 
    
- Las llamadas para abrir una de las propiedades de los mensajes o carpetas del almacén de mensajes mediante [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con la marca MAPI_MODIFY error. 
    
- Se producirá un error en las llamadas a cualquiera de los métodos siguientes: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Las llamadas a los métodos siguientes producirán un error si el destino del mensaje copiado es de solo lectura, si el destino es el mismo que el almacén de mensajes de origen o si es otro almacén de solo lectura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI usa el **método IMAPISession::OpenMsgStore** para abrir un almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
- [Uso de macros para el control de errores](using-macros-for-error-handling.md)

