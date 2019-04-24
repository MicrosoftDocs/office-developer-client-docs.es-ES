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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329417"
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del objeto que se va a abrir.
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto abierto. Al pasar NULL, se devuelve la interfaz estándar del objeto. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra mediante el número máximo de permisos de red permitidos para el usuario y el máximo acceso a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura. 
    
MAPI_CACHE_OK
  
> Use todos los medios, incluidas las libretas de direcciones sin conexión, para realizar la resolución de nombres.
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenEntry** se devuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el cliente que realiza la llamada. Si el objeto no está disponible, realizar una llamada subsiguiente a un objeto puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se conceda permiso de lectura y escritura. 
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para realizar la resolución de nombres. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que están marcados actualmente como eliminados temporalmente (es decir, se encuentran en la fase de tiempo de retención de elementos eliminados).
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> contempla Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se ha abierto correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de solo lectura o se ha intentado obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay un objeto asociado con el identificador de entrada pasado en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada pasado en el parámetro _lpEntryID_ tiene un formato irreconocible. Normalmente, este valor se devuelve si el proveedor de servicios que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: OpenEntry** abre un objeto de la libreta de direcciones o un almacén de mensajes, que devuelve un puntero a una interfaz que se puede usar para tener acceso al objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

> [!IMPORTANT]
> Al abrir las entradas de carpeta en un almacén público, como carpetas y mensajes, use [IMsgStore:: OpenEntry](imsgstore-openentry.md) en lugar de **IMAPISession:: OpenEntry**. Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil. 
  
Llame a **IMAPISession:: OpenEntry** solo cuando no sepa qué tipo de objeto está abriendo. Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md). Si sabe que va a abrir un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más rápidos que **IMAPISession:: OpenEntry**. 
  
MAPI abre todos los objetos con permiso de solo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ . La configuración de uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se conceden dependen del proveedor de servicios, el nivel de acceso y el objeto. Para determinar el nivel de acceso del objeto abierto, recupere su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Llamar a **IMAPISession:: OpenEntry** y establecer _lpEntryID_ para que apunten al identificador de entrada de un almacén de mensajes es el mismo que llamar al método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) con la marca MDB_NO_DIALOG establecida. La configuración de la marca también es equivalente, excepto en que para solicitar el permiso de lectura/escritura con **OpenMsgStore**, debe establecer la marca MDB_WRITE en lugar de MAPI_MODIFY. 
  
Compruebe el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es el esperado. Si el tipo de objeto no es el tipo que esperaba, convierta el puntero del parámetro _lppUnk_ en un puntero del tipo apropiado. Por ejemplo, si abre una carpeta, convierta _lppUnk_ en un puntero de tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa el método **IMAPISession:: OpenEntry** para abrir un objeto.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

