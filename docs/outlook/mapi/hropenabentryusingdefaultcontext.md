---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434343"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la misma función que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) excepto que usa **el emsmdbUID** heredado como el _parámetro pEmsmdbUID._ No use esta función a menos que no pueda obtener el **emsmdbUID** correcto para la llamada a [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _pmsess_
  
> [in] La sesión iniciada **en IMAPISession**. No puede ser NULL.
    
 _pAddrBook_
  
> [in] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID_
  
> [in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser : IMAPIProp](imailuserimapiprop.md). Para las listas de distribución es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para los contenedores es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la entrada. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS
  
> Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permiso de lectura y escritura. El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usa solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.
    
MAPI_GAL_ONLY
  
> Usa solo la GAL para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_MODIFY
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que se haya concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.
    
MAPI_NO_CACHE
  
> No usa la libreta de direcciones sin conexión para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
 _lpulObjType_
  
> [salida] Puntero al tipo de entrada abierta.
    
 _lppUnk_
  
> [salida] Puntero a un puntero de la entrada abierta.
    

