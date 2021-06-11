---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408897"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre el **entryID** mediante la Exchange de direcciones identificada por _pEmsabpUID_. Esta función funciona de forma similar a [IAddrBook::OpenEntry,](iaddrbook-openentry.md) excepto que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abra mediante el proveedor Exchange libreta de direcciones. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
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

 _pEmsmdbUID_
  
> [in] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID_
  
> [in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser : IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la entrada, Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS
  
> Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permiso de lectura y escritura. El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.
    
MAPI_GAL_ONLY
  
> Use solo la GAL para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_MODIFY
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que se haya concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
 _lpulObjType_
  
> [salida] Puntero al tipo de entrada abierta.
    
 _lppUnk_
  
> [salida] Puntero a un puntero de la entrada abierta.
    

