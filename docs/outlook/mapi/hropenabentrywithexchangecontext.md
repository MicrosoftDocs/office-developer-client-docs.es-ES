---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434056"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre el **entryID** mediante la libreta de direcciones de Exchange identificada **por pEmsmdbUID**. Esta función funciona de forma similar a [IAddrBook::D etails,](iaddrbook-details.md) excepto que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abre mediante el proveedor de libretas de direcciones de Exchange esperado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _pmsess_
  
> [entrada] La sesión iniciada **en IMAPISession**. No puede ser NULL.
    
 _pEmsmdbUID_
  
> [entrada] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID_
  
> [entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
>  [entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se abre la entrada. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS
  
> Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente. Por ejemplo, si el cliente tiene permisos de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura. El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usa solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo caché de Exchange y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.
    
MAPI_GAL_ONLY
  
> Usa solo la GAL para realizar la resolución de nombres. Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.
    
MAPI_MODIFY
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben suponer que se ha concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.
    
MAPI_NO_CACHE
  
> No usa la libreta de direcciones sin conexión para realizar la resolución de nombres. Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.
    

