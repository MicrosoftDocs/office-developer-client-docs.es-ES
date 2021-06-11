---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Última modificación: 1 de febrero de 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434168"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una entrada de libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para obtener acceso a la entrada.
  
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
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
_lpEntryID_
  
> [in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.
    
_lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada abierta. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser : IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList : IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
_ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la entrada. Se pueden establecer las siguientes marcas.
    
MAPI_BEST_ACCESS 
  
> Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura. El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Abre una entrada de libreta de direcciones y solo tiene acceso a ella desde la memoria caché. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.
    
MAPI_GAL_ONLY
  
> Use solo la GAL para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
  > [!NOTE]
  > Es posible que MAPI_GAL_ONLY  _ulFlags_ no se defina en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >  `#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que se haya concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para realizar la resolución de nombres. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
_lpulObjType_
  
> [salida] Puntero al tipo de entrada abierta.
    
_lppUnk_
  
> [salida] Puntero a un puntero a la entrada abierta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La entrada se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó abrir una entrada para la que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La entrada representada por  _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> No se reconoce el identificador de entrada especificado _en lpEntryID._ Este valor normalmente se devuelve si el proveedor de libreta de direcciones responsable de la entrada correspondiente no está abierto. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman al **método IAddrBook::OpenEntry** para abrir una entrada de libreta de direcciones. MAPI reenvía la llamada al proveedor de libreta de direcciones adecuado, en función de la estructura [MAPIUID](mapiuid.md) incluida en el identificador de entrada pasado en el _parámetro lpEntryID._ El proveedor de libreta de direcciones abre la entrada como de solo lectura a menos que se establezca MAPI_MODIFY o MAPI_BEST_ACCESS marca del parámetro _ulFlags._ Sin embargo, estas marcas son sugerencias. Si el proveedor de libreta de direcciones no permite la modificación de la entrada solicitada, devuelve MAPI_E_NO_ACCESS. 
  
El  _parámetro lpInterface_ indica qué interfaz debe usarse para tener acceso a la entrada abierta. Si se pasa NULL en  _lpInterface,_ se debe usar la interfaz MAPI estándar para ese tipo de entrada. Dado que el proveedor de libreta de direcciones puede devolver una interfaz diferente a la sugerida por el parámetro  _lpInterface,_ el autor de la llamada debe comprobar el valor devuelto en el parámetro  _lpulObjType_ para determinar si el tipo de objeto devuelto es el esperado. Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro  _lppUnk_ en un tipo que sea más adecuado. 
  
## <a name="see-also"></a>Vea también

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

