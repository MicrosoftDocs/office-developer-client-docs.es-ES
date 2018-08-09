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
ms.openlocfilehash: 04bf7f2ddda7377df72417df2472246a2cf329bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817534"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Hace referencia a**: Outlook 
  
Se abre un objeto y devuelve un puntero de interfaz para aún más el acceso. 
  
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

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto que se va a abrir.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto. Si se pasa NULL da como resultado la interfaz del objeto estándar que se devuelven. Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md). Las interfaces estándares para objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulOpenFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abran con los permisos de red máximo permitidos para el autor de la llamada. Por ejemplo, si el autor de la llamada tiene permiso de lectura y escritura, se debe abrir el objeto como de lectura y escritura; Si el autor de la llamada tiene permiso de sólo lectura, se debe abrir el objeto como de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto es totalmente accesible para el autor de la llamada. Si el objeto no es accesible, realizar una llamada de objeto subsiguientes se puede producir un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de sólo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de sólo lectura, o se ha intentado tener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No es un objeto asociado con el identificador de entrada que se pasa en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada que se pasa en el parámetro _lpEntryID_ está en un formato no reconoce. Normalmente, este valor se devuelve si el proveedor de libreta de direcciones que contiene el objeto no está abierto. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::OpenEntry** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamar a **IMAPISupport::OpenEntry** para recuperar un puntero a una interfaz que se puede usar para tener acceso a un objeto determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **IMAPISupport::OpenEntry** sólo cuando no sabe qué tipo de objeto que va a abrir. Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) en su lugar. Si sabe que va a abrir un contenedor de la libreta de direcciones, un usuario de mensajería, o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md). Estos métodos más específicos son más rápidos que **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** abre todos los objetos como de solo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ y los permisos son suficientes. Establecer uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se le concede dependen de su nivel de acceso, el objeto y el proveedor de servicio que posee el objeto. Para determinar el nivel de acceso del objeto abierto, recuperar su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar que el tipo de objeto devuelto es lo que esperaba. Si el tipo de objeto es como se esperaba, convierta el puntero desde el parámetro _lppUnk_ a un puntero del tipo apropiado. Por ejemplo, si va a abrir una carpeta, convierta _lppUnk_ a un puntero de tipo LPMAPIFOLDER. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

