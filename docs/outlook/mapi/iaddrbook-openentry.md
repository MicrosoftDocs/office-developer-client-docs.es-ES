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
  
Abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que puede usarse para tener acceso a la entrada.
  
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
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
_lpEntryID_
  
> a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.
    
_lpInterface_
  
> a Puntero al identificador de interfaz (IID) de la interfaz que se va a usar para obtener acceso a la entrada abierta. Al pasar NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
_ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre la entrada. Se pueden establecer los siguientes indicadores.
    
MAPI_BEST_ACCESS 
  
> Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura. El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del elemento abierto y recuperar la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Abre una entrada de la libreta de direcciones y solo obtiene acceso a ella desde la memoria caché. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que la llamada se realice correctamente, posiblemente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.
    
MAPI_GAL_ONLY
  
> Use solamente la GAL para la resolución de nombres. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
  > [!NOTE]
  > Es posible que el MAPI_GAL_ONLY _ulFlags_ no esté definido en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Solicita que la entrada se abra con permiso de lectura y escritura. Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para realizar la resolución de nombres. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
_lpulObjType_
  
> contempla Puntero al tipo de la entrada abierta.
    
_lppUnk_
  
> contempla Un puntero a un puntero a la entrada abierta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La entrada se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó abrir una entrada para la que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La entrada representada por _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> No se reconoce el identificador de entrada especificado en _lpEntryID_ . Normalmente, este valor se devuelve si el proveedor de la libreta de direcciones responsable de la entrada correspondiente no está abierto. 
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de servicios llaman al método **IAddrBook:: OpenEntry** para abrir una entrada de la libreta de direcciones. MAPI reenvía la llamada al proveedor de libreta de direcciones adecuado, en función de la estructura [MAPIUID](mapiuid.md) incluida en el identificador de entrada que se ha pasado en el parámetro _lpEntryID_ . El proveedor de la libreta de direcciones abre la entrada como de solo lectura a menos que se establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ . Sin embargo, estos marcadores son sugerencias. Si el proveedor de la libreta de direcciones no permite la modificación de la entrada solicitada, devuelve MAPI_E_NO_ACCESS. 
  
El parámetro _lpInterface_ indica qué interfaz debe usarse para tener acceso a la entrada abierta. Pasar NULL en _lpInterface_ indica que se debe usar la interfaz MAPI estándar para ese tipo de entrada. Como el proveedor de la libreta de direcciones puede devolver una interfaz diferente a la que sugiere el parámetro _lpInterface_ , el autor de la llamada debe comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es Qué se esperaba. Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro _lppUnk_ en un tipo más adecuado. 
  
## <a name="see-also"></a>Ver también

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

