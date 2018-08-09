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
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817057"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Hace referencia a**: Outlook 
  
Se abre la **propiedad entryID** utilizando la libreta de direcciones de Exchange identificado por _pEmsabpUID_. Esta función funciona de manera similar a [IAddrBook::OpenEntry](iaddrbook-openentry.md) excepto en que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abre mediante el proveedor de la libreta de direcciones de Exchange esperado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Parámetros

 _pEmsmdbUID_
  
> [entrada] Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada a la función se comporta como [IAddrBook::Details](iaddrbook-details.md). Si este parámetro es NULL o un cero MAPIUID, esta función se comporta como [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones que se usó para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID_
  
> [entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  [entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada open. Pasando NULL, devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada, se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS
  
> Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos. Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura. El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.
    
MAPI_GAL_ONLY
  
> Usar sólo la lista global de direcciones para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_MODIFY
  
> Las solicitudes que se abre la entrada con leer y permiso de escritura. Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
 _lpulObjType_
  
> [out] Un puntero al tipo de la entrada que se abrió.
    
 _lppUnk_
  
> [out] Un puntero a un puntero de la entrada que se abrió.
    

