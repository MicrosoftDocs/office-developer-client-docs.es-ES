---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424262"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones determinado para determinar si hacen referencia al mismo objeto de libreta de direcciones. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID1_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._ 
    
 _lpEntryID1_
  
> [entrada] Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._ 
    
 _lpEntryID2_
  
> [entrada] Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [salida] Puntero al resultado de la comparación. El contenido de  _lpulResult_ se establece en TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, el contenido se establece en FALSE. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno o ambos identificadores de entrada pasados con los parámetros  _lpEntryID1_ o  _lpEntryID2_ no son reconocidos por ningún proveedor de libreta de direcciones. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y los proveedores de servicios llaman al método **CompareEntryIDs** para comparar dos identificadores de entrada que pertenecen a un único proveedor de libreta de direcciones para determinar si hacen referencia al mismo objeto. **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede producirse, por ejemplo, después de instalar una nueva versión de un proveedor de libreta de direcciones. 
  
MAPI pasa esta llamada al proveedor de libreta de direcciones responsable de los identificadores de entrada, determinando el proveedor adecuado al hacer coincidir la estructura [MAPIUID](mapiuid.md) en los identificadores de entrada con la estructura **MAPIUID** registrada por el proveedor. 
  
Si los dos identificadores de entrada hacen referencia al mismo objeto, **CompareEntryIDs** establece el contenido del parámetro  _lpulResult_ en TRUE; si hacen referencia a diferentes objetos, **CompareEntryIDs** establece el contenido en FALSE. En cualquier caso, **CompareEntryIDs** devuelve S_OK. Si **CompareEntryIDs** devuelve un error, que puede producirse si ningún proveedor de libreta de direcciones ha registrado una estructura **MAPIUID** que coincida con la de los identificadores de entrada, los clientes y proveedores no deben realizar ninguna acción en función del resultado de la comparación. En su lugar, deben tomar el enfoque más conservador de la acción que se está realizando. 
  
## <a name="see-also"></a>Consulte también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

