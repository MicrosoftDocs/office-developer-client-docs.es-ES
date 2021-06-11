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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409618"
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
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del objeto que se debe abrir.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al objeto. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándar para objetos de libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución e [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulOpenFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos máximos de red permitidos para el autor de la llamada. Por ejemplo, si el autor de la llamada tiene permiso de lectura y escritura, el objeto debe abrirse como lectura y escritura; si el autor de la llamada tiene permiso de solo lectura, el objeto debe abrirse como de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto sea totalmente accesible para el autor de la llamada. Si el objeto no es accesible, realizar una llamada de objeto posterior puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
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
  
> El identificador de entrada pasado en el  _parámetro lpEntryID_ tiene un formato irreconocible. Este valor normalmente se devuelve si el proveedor de libreta de direcciones que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::OpenEntry** se implementa para todos los objetos de soporte del proveedor de servicios. Los proveedores de servicios llaman a **IMAPISupport::OpenEntry** para recuperar un puntero a una interfaz que se puede usar para obtener acceso a un objeto determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llama **a IMAPISupport::OpenEntry** solo cuando no sepas qué tipo de objeto estás abriendo. Si sabe que está abriendo una carpeta o un mensaje, llame a [IMsgStore::OpenEntry en su](imsgstore-openentry.md) lugar. Si sabe que está abriendo un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más rápidos **que IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** abre todos los objetos como de solo lectura, a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro  _ulFlags_ y los permisos sean suficientes. Establecer una de estas marcas no garantiza un tipo determinado de acceso; los permisos que se le concedan dependen del nivel de acceso, el objeto y el proveedor de servicios propietario del objeto. Para determinar el nivel de acceso del objeto abierto, recupere su **propiedad PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Compruebe el valor devuelto en el  _parámetro lpulObjType para_ determinar que el tipo de objeto devuelto es lo que esperaba. Si el tipo de objeto es el esperado, convierte el puntero del parámetro  _lppUnk_ en un puntero del tipo adecuado. Por ejemplo, si va a abrir una carpeta, convierte  _lppUnk_ en un puntero de tipo LPMAPIFOLDER. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

