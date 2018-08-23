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
ms.openlocfilehash: 9572f44f1f4865fcce5d7aa8bd8478340b0de968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594722"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) excepto en que obtiene el **emsabpUID** de la fila resuelta automáticamente y se abre la **propiedad entryID**.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Parámetros

 _prwResolved_
  
> [entrada] Un puntero a la fila resuelta que se usa para obtener la **emsabpUID** y abra el **entryID**.
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones que se usó para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID_
  
> [entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  [entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada open. Pasando NULL, devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS
  
> Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos. Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura. El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Utiliza sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.
    
MAPI_GAL_ONLY
  
> Utiliza sólo la lista global de direcciones para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_MODIFY
  
> Las solicitudes que se abre la entrada con leer y permiso de escritura. Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.
    
MAPI_NO_CACHE
  
> No utiliza la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
 _lpulObjType_
  
> [out] Un puntero al tipo de la entrada que se abrió.
    
 _lppUnk_
  
> [out] Un puntero a un puntero de la entrada que se abrió.
    

