---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817777"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Hace referencia a**: Outlook 
  
Se abre una carpeta o un mensaje y devuelve un puntero de interfaz para aún más el acceso. 
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ _._
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto para abrir o NULL. Si _lpEntryID_ se establece en NULL, **OpenEntry** abre la carpeta raíz para el almacén de mensajes. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto. Si se pasa NULL da como resultado el objeto de la interfaz estándar ([IMAPIFolder](imapifolderimapicontainer.md) para las carpetas) y [IMessage](imessageimapiprop.md) para los mensajes que se devuelven. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que se abre el objeto mediante el uso de los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto mediante el uso de permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto mediante el uso de permisos de sólo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada. Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de sólo lectura y los clientes no deben trabajar en la suposición de que se concede el permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado para modificar un objeto de sólo lectura o para obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_NO_CACHE
  
> Cuando un almacén se abre en modo en caché, puede llamar a un proveedor de servicio o cliente **IMsgStore::OpenEntry**, establecer el indicador MAPI_NO_CACHE para abrir un elemento o una carpeta en el almacén remoto. Si se abre el almacén de mensajes con el indicador MDB_ONLINE en el servidor remoto, no es necesario usar el indicador MAPI_NO_CACHE.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::OpenEntry** abre una carpeta o un mensaje y devuelve un puntero a una interfaz que se puede usar para aún más el acceso. 
  
> [!IMPORTANT]
> Al abrir entradas de la carpeta en un almacén público, como las carpetas y mensajes, use **IMsgStore::OpenEntry** en lugar de [IMAPISession::OpenEntry](imapisession-openentry.md). Esto garantiza que funcionan las carpetas públicas correctamente cuando se definen varias cuentas de Exchange en un perfil. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las carpetas y los mensajes se abren automáticamente con permisos de sólo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ . Establecer uno de estos marcadores no garantiza un tipo concreto de permiso; dependen de los permisos que se conceden en el proveedor de almacenamiento de mensajes, su nivel de acceso y el objeto. Para determinar el nivel de acceso del objeto abierto, recuperar su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Aunque **IMsgStore::OpenEntry** puede utilizarse para abrir cualquier carpeta o mensaje, suele ser más rápido utilizar el método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si dispone de acceso a la carpeta principal de la carpeta o el mensaje que se va a abrir. 
  
Comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es lo que esperaba. Si el tipo de objeto no es del tipo esperado, convertir el puntero desde el parámetro _lppUnk_ a un puntero del tipo apropiado. Por ejemplo, si va a abrir una carpeta, convierta _lppUnk_ a un puntero de tipo **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utiliza el método **IMsgStore::OpenEntry** para abrir el objeto asociado con un identificador de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

