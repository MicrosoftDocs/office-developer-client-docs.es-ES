---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429911"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , con la diferencia de que obtiene automáticamente el **emsabpUID** de la fila resuelta y abre el **entryID**.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
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

 _prwResolved_
  
> a Un puntero a la fila resuelta que se usa para obtener la **emsabpUID** y abrir la **entryID**.
    
 _pAddrBook_
  
> a La libreta de direcciones que se usa para abrir el identificador de entrada. No puede ser nulo.
    
 _cbEntryID_
  
> a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir. 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta. Al pasar NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre la entrada. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS
  
> Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura. El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la entrada abierta y recuperar la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usa sólo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se realice correctamente, potencialmente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada puedan devolver un error.
    
MAPI_GAL_ONLY
  
> Usa sólo la GAL para la resolución de nombres. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_MODIFY
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.
    
MAPI_NO_CACHE
  
> No usa la libreta de direcciones sin conexión para realizar la resolución de nombres. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
 _lpulObjType_
  
> contempla Puntero al tipo de la entrada abierta.
    
 _lppUnk_
  
> contempla Un puntero a un puntero de la entrada abierta.
    

