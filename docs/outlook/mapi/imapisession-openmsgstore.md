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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325770"
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

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo de direcciones comunes y otras pantallas relacionadas.
    
_cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
_lpEntryID_
  
> a Un puntero al identificador de entrada del almacén de mensajes que se va a abrir. El parámetro _lpEntryID_ no debe ser nulo. 
    
_lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al almacén de mensajes. Pasar NULL hace que el parámetro _lppMDB_ devuelva un puntero a la interfaz estándar para un almacén de mensajes (**IMsgStore**).
    
_ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
  - MAPI_BEST_ACCESS: solicita que se abra el almacén de mensajes con el máximo de permisos de red permitidos para el usuario y los permisos de aplicación de cliente máximos. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el almacén de mensajes debe abrirse con permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el almacén de mensajes debe abrirse con permiso de solo lectura. 
      
  - MAPI_DEFERRED_ERRORS: permite que **OpenMsgStore** se devuelva correctamente, posiblemente antes de que el almacén de mensajes esté completamente disponible para el cliente que realiza la llamada. Si el almacén de mensajes no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error. 
      
  - MDB\_NO_DIALOG: evita que se muestren los cuadros de diálogo de inicio de sesión. Si se establece esta marca y **OpenMsgStore** tiene información de configuración insuficiente para abrir el almacén de mensajes sin la ayuda del usuario, devuelve MAPI_E_LOGON_FAILED. Si no se establece esta marca, el proveedor de almacenamiento de mensajes puede solicitar al usuario que corrija un nombre o una contraseña o que realice otras acciones necesarias para establecer una conexión con el almacén de mensajes. 
      
  - MDB\_NO_MAIL: no se debe usar el almacén de mensajes para enviar o recibir correo. Cuando se establece esta marca, MAPI no notifica a la cola MAPI que se está abriendo este almacén de mensajes.
      
  - MDB\_online: en el modo de intercambio en caché, un cliente o proveedor de servicios puede llamar a este método con MDB_ONLINE para invalidar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto. No puede abrir un almacén de Exchange en modo en caché y en modo no en caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.
      
  - MDB_TEMPORARY: indica a MAPI que el almacén de mensajes no es permanente y no debe agregarse a la tabla de almacén de mensajes. Esta marca se usa para iniciar sesión en el almacén de mensajes, de modo que la información se pueda recuperar mediante programación desde la sección de perfil. 
      
  - MDB_WRITE: solicita permiso de lectura/escritura al almacén de mensajes.
    
_lppMDB_
  
> contempla Puntero a un puntero del almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El almacén de mensajes se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un almacén de mensajes para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> El almacén de mensajes indicado por _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de la configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó correctamente, pero el proveedor de almacenamiento de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para obtener la información de error del proveedor, llame al método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: OpenMsgStore** abre un almacén de mensajes en particular. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El nivel de permisos predeterminado para los almacenes de mensajes es de solo lectura. Si establece la marca MDB_WRITE, es posible que no se le conceda permiso de lectura y escritura. El nivel final de acceso que MAPI asigna al almacén de mensajes depende de su nivel de permisos, el propio almacén de mensajes y el proveedor de almacenamiento de mensajes. 
  
Si llama a **OpenMsgStore** para abrir un almacén de mensajes con permiso de solo lectura, ocurrirá lo siguiente: 
  
- La propiedad **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la tienda no tendrá su almacén\_MODIFY_OK ni los\_bits de CREATE_OK de almacén establecidos. 
    
- Las llamadas para abrir uno de los mensajes o carpetas del almacén de mensajes mediante el uso de [IMAPISession:: OpenEntry](imapisession-openentry.md) con el indicador MAPI_MODIFY establecido producirán un error. 
    
- Se producirá un error en las llamadas para abrir una de las propiedades de los mensajes o carpetas del almacén de mensajes mediante el uso de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con la marca MAPI_MODIFY. 
    
- Se producirá un error en las llamadas a cualquiera de los siguientes métodos: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Se producirá un error en las llamadas a los siguientes métodos si el destino del mensaje copiado es de sólo lectura, si el destino es el mismo que el almacén de mensajes de origen o si es otro almacén de solo lectura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI usa el método **IMAPISession:: OpenMsgStore** para abrir un almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
- [Uso de macros para el control de errores](using-macros-for-error-handling.md)

