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
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426390"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto y devuelve un puntero de interfaz para obtener acceso adicional.
  
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
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del objeto que se debe abrir.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándar para objetos de libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución e [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden usar las siguientes marcas:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura. 
    
MAPI_CACHE_OK
  
> Use todos los medios, incluidas las libretas de direcciones sin conexión, para realizar la resolución de nombres.
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo caché de Exchange y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto esté totalmente disponible para el cliente que realiza la llamada. Si el objeto no está disponible, realizar una llamada de objeto posterior puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicita permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se concede permiso de lectura y escritura. 
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para realizar la resolución de nombres. Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.
    
SHOW_SOFT_DELETES
  
> Mostrar los elementos que están marcados actualmente como eliminados temporalmente (es decir, están en la fase de tiempo de retención de elementos eliminados).
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [salida] Puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó modificar un objeto de solo lectura o se intentó obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay ningún objeto asociado con el identificador de entrada pasado en el _parámetro lpEntryID._ 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada pasado en  _el parámetro lpEntryID_ está en un formato irreconocible. Normalmente, este valor se devuelve si el proveedor de servicios que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::OpenEntry** abre un almacén de mensajes o un objeto de libreta de direcciones, devolviendo un puntero a una interfaz que se puede usar para tener acceso al objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

> [!IMPORTANT]
> Al abrir entradas de carpeta en un almacén público, como carpetas y mensajes, use [IMsgStore::OpenEntry](imsgstore-openentry.md) en lugar de **IMAPISession::OpenEntry**. Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil. 
  
Llame **a IMAPISession::OpenEntry** solo cuando no sepa qué tipo de objeto está abriendo. Si sabe que está abriendo una carpeta o un mensaje, llame a [IMsgStore::OpenEntry](imsgstore-openentry.md). Si sabe que está abriendo un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más **rápidos que IMAPISession::OpenEntry**. 
  
MAPI abre todos los objetos con permiso de solo lectura, a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el _parámetro ulFlags._ Establecer una de estas marcas no garantiza un tipo concreto de acceso; los permisos concedidos dependen del proveedor de servicios, el nivel de acceso y el objeto. Para determinar el nivel de acceso del objeto abierto, recupere **su** PR_ACCESS_LEVEL ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Llamar a **IMAPISession::OpenEntry** y establecer  _lpEntryID_ para que apunte al identificador de entrada de un almacén de mensajes es lo mismo que llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) con la marca MDB_NO_DIALOG establecida. La configuración de la marca también es equivalente, excepto que para solicitar permiso de lectura y escritura con **OpenMsgStore,** debe establecer la marca MDB_WRITE en lugar de MAPI_MODIFY. 
  
Compruebe el valor devuelto en el  _parámetro lpulObjType para_ determinar si el tipo de objeto devuelto es el esperado. Si el tipo de objeto no es el tipo esperado, convierte el puntero del parámetro  _lppUnk_ en un puntero del tipo adecuado. Por ejemplo, si abre una carpeta, convierte  _lppUnk_ en un puntero de tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa el **método IMAPISession::OpenEntry** para abrir un objeto.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

