---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591019"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre un objeto y devuelve un puntero de interfaz de acceso adicional.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto que se va a abrir.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto. Pasando NULL, devuelve la interfaz del objeto estándar. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándares para objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que se abre el objeto mediante el uso de los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto con permiso de sólo lectura. 
    
MAPI_CACHE_OK
  
> Usar todos los medios, incluidos libretas de direcciones sin conexión, para llevar a cabo la resolución de nombres.
    
MAPI_CACHE_ONLY
  
> Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada. Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de sólo lectura y los clientes no deben trabajar en la suposición de que se concede el permiso de lectura y escritura. 
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
SHOW_SOFT_DELETES
  
> Mostrar los elementos que actualmente están marcados como suaves eliminan (es decir, se encuentran en la retención de elementos eliminados fase de tiempo).
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se ha abierto correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de sólo lectura o se ha intentado tener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No es un objeto asociado con el identificador de entrada que se pasa en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada que se pasa en el parámetro _lpEntryID_ está en un formato no reconoce. Normalmente, este valor se devuelve si el proveedor de servicio que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

Abre el método de **IMAPISession::OpenEntry** un mensaje almacenar o direcciones de objeto de libro, devuelve un puntero a una interfaz que puede utilizarse para tener acceso al objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

> [!IMPORTANT]
> Al abrir entradas de la carpeta en un almacén público, como las carpetas y mensajes, use [IMsgStore::OpenEntry](imsgstore-openentry.md) en lugar de **IMAPISession::OpenEntry**. Esto garantiza que funcionan las carpetas públicas correctamente cuando se definen varias cuentas de Exchange en un perfil. 
  
Llame a **IMAPISession::OpenEntry** sólo cuando no sabe qué tipo de objeto que va a abrir. Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore::OpenEntry](imsgstore-openentry.md). Si sabe que va a abrir un contenedor de la libreta de direcciones, un usuario de mensajería, o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más rápidos que **IMAPISession::OpenEntry**. 
  
MAPI abre todos los objetos con permisos de sólo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ . Establecer uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se conceden dependen del proveedor de servicios, el nivel de acceso y el objeto. Para determinar el nivel de acceso del objeto abierto, recuperar su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Al llamar a **IMAPISession::OpenEntry** y configuración _lpEntryID_ para que apunte al identificador de entrada de un almacén de mensajes es el mismo que llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) con la marca MDB_NO_DIALOG establecer. La configuración del indicador también es equivalente, excepto en que se va a solicitar el permiso de lectura y escritura con **OpenMsgStore**, debe establecer la marca MDB_WRITE en lugar de MAPI_MODIFY. 
  
Comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es lo que esperaba. Si el tipo de objeto no es del tipo que esperaba, convertir el puntero desde el parámetro _lppUnk_ a un puntero del tipo apropiado. Por ejemplo, si va a abrir una carpeta, convierta _lppUnk_ a un puntero de tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utiliza el método **IMAPISession::OpenEntry** para abrir un objeto.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

