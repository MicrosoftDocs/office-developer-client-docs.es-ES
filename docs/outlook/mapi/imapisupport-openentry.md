---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326351"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto y devuelve un puntero de interfaz para obtener más acceso. 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
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
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto. Al pasar NULL se obtiene la interfaz estándar del objeto que se devuelve. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulOpenFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos de red máximos permitidos para el autor de la llamada. Por ejemplo, si el autor de la llamada tiene permiso de lectura y escritura, el objeto debe abrirse como de lectura y escritura; Si el autor de la llamada tiene permiso de solo lectura, el objeto debe abrirse como de sólo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenEntry** vuelva correctamente, posiblemente antes de que el objeto sea totalmente accesible para el autor de la llamada. Si el objeto no es accesible, realizar una llamada subsiguiente a un objeto puede dar como resultado un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de solo lectura y los llamadores no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> contempla Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de solo lectura o se ha intentado obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay un objeto asociado con el identificador de entrada pasado en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada pasado en el parámetro _lpEntryID_ tiene un formato irreconocible. Normalmente, este valor se devuelve si el proveedor de la libreta de direcciones que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: OpenEntry** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios llaman a **IMAPISupport:: OpenEntry** para recuperar un puntero a una interfaz que se puede usar para obtener acceso a un objeto en particular. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **IMAPISupport:: OpenEntry** solo cuando no sepa qué tipo de objeto está abriendo. Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) en su lugar. Si sabe que va a abrir un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más rápidos que **IMAPISupport:: OpenEntry**. 
  
 **IMAPISupport:: OpenEntry** abre todos los objetos como de solo lectura, a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ y los permisos sean suficientes. La configuración de uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se conceden dependen del nivel de acceso, el objeto y el proveedor de servicios que posee el objeto. Para determinar el nivel de acceso del objeto abierto, recupere su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Compruebe el valor devuelto en el parámetro _lpulObjType_ para determinar que el tipo de objeto devuelto es lo que esperaba. Si el tipo de objeto es el esperado, convierta el puntero del parámetro _lppUnk_ en un puntero del tipo apropiado. Por ejemplo, si abre una carpeta, convierta _lppUnk_ en un puntero de tipo LPMAPIFOLDER. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

