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
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309698"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una carpeta o un mensaje y devuelve un puntero de interfaz para obtener más acceso. 
  
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
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ _._
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del objeto que se va a abrir o NULL. Si _lpEntryID_ se establece en null, **OpenEntry** abre la carpeta raíz del almacén de mensajes. 
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto abierto. El paso de resultados NULOs en la interfaz estándar del objeto ([IMAPIFolder](imapifolderimapicontainer.md) para las carpetas y [IMessage](imessageimapiprop.md) para los mensajes) se devuelven. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto. Se pueden usar los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra mediante el número máximo de permisos de red permitidos para el usuario y el máximo acceso a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con el permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse utilizando el permiso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenEntry** se devuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el cliente que realiza la llamada. Si el objeto no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se conceda permiso de lectura y escritura. 
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> contempla Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de solo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_NO_CACHE
  
> Cuando un almacén se abre en el modo en caché, un cliente o un proveedor de servicios puede llamar a **IMsgStore:: OpenEntry**, estableciendo la marca MAPI_NO_CACHE para abrir un elemento o una carpeta en el almacén remoto. Si abre el almacén de mensajes con la marca MDB_ONLINE en el servidor remoto, no es necesario que use la marca MAPI_NO_CACHE.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: OpenEntry** abre una carpeta o un mensaje y devuelve un puntero a una interfaz que se puede usar para obtener más acceso. 
  
> [!IMPORTANT]
> Al abrir las entradas de carpeta en un almacén público, como carpetas y mensajes, use **IMsgStore:: OpenEntry** en lugar de [IMAPISession:: OpenEntry](imapisession-openentry.md). Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las carpetas y los mensajes se abren automáticamente con permiso de solo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ . La configuración de uno de estos marcadores no garantiza un tipo concreto de permiso; los permisos que se concedan dependen del proveedor de almacenamiento de mensajes, el nivel de acceso y el objeto. Para determinar el nivel de acceso del objeto abierto, recupere su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Aunque **IMsgStore:: OpenEntry** se puede usar para abrir cualquier carpeta o mensaje, suele ser más rápido usar el método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) si tiene acceso a la carpeta principal de la carpeta o del mensaje que se va a abrir. 
  
Compruebe el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es el que esperaba. Si el tipo de objeto no es el esperado, convierta el puntero del parámetro _lppUnk_ en un puntero del tipo apropiado. Por ejemplo, si abre una carpeta, convierta _lppUnk_ en un puntero de tipo **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa el método **IMsgStore:: OpenEntry** para abrir el objeto asociado con un identificador de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

