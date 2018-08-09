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
description: 'Última modificación: 01 de febrero de 2013'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19817148"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Hace referencia a**: Outlook 
  
Se abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para tener acceso a la entrada.
  
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

## <a name="parameters"></a>Parámetros

_cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
_lpEntryID_
  
> [entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.
    
_lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open. Pasando NULL, devuelve la interfaz del objeto estándar. Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
_ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada. Se pueden establecer las siguientes marcas.
    
MAPI_BEST_ACCESS 
  
> Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura. El cliente puede recuperar el nivel de acceso que se ha concedido por llamar al método open de la entrada [IMAPIProp::GetProps](imapiprop-getprops.md) y recuperación de la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Se abre una entrada de la libreta de direcciones y tiene acceso a él sólo desde la memoria caché. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.
    
MAPI_GAL_ONLY
  
> Usar sólo la lista global de direcciones para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
  > [!NOTE]
  > _UlFlags_ MAPI_GAL_ONLY no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Las solicitudes de que la entrada se abre con permiso de lectura y escritura. Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben suponer que se ha concedido permiso de lectura y escritura, independientemente de si se ha establecido MAPI_MODIFY.
    
MAPI_NO_CACHE
  
> No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
_lpulObjType_
  
> [out] Un puntero al tipo de la entrada que se abrió.
    
_lppUnk_
  
> [out] Un puntero a un puntero a la entrada que se abrió.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La entrada se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado abrir una entrada para la que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La entrada representada por _lpEntryID_ no existe. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> No se reconoce el identificador de entrada especificado en _lpEntryID_ . Normalmente, este valor se devuelve si el responsable de la entrada correspondiente del proveedor de libreta de direcciones no está abierto. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **IAddrBook::OpenEntry** para abrir una entrada de la libreta de direcciones. MAPI reenvía la llamada a la libreta de direcciones adecuado, basándose en la estructura [MAPIUID](mapiuid.md) que se incluye en el identificador de entrada que se pasa en el parámetro _lpEntryID_ . El proveedor de la libreta de direcciones abre la entrada como de sólo lectura a menos que se establece la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ . Sin embargo, estos marcadores son sugerencias. Si el proveedor de la libreta de direcciones no permitir la modificación de la entrada de solicitado, devuelve MAPI_E_NO_ACCESS. 
  
El parámetro _lpInterface_ indica qué interfaz se debe utilizar para tener acceso a la entrada que se abrió. Pasando NULL en _lpInterface_ indica que se debe usar la interfaz estándar de MAPI para ese tipo de entrada. Debido a que el proveedor de la libreta de direcciones podría devolver una interfaz diferente de aquél al que sugiere el parámetro _lpInterface_ , el llamador debe comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es ¿Qué se esperaba. Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro _lppUnk_ a un tipo que sea más adecuado. 
  
## <a name="see-also"></a>Vea también

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

