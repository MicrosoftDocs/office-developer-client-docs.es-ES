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
ms.openlocfilehash: 807e592cf535ac060fd275075035ae8beb7d6e78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817115"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Hace referencia a**: Outlook 
  
Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones concreto para determinar si hacen referencia al mismo objeto de la libreta de direcciones. 
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [entrada] Un puntero para el primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [entrada] Un puntero para el segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [out] Un puntero al resultado de la comparación. El contenido de _lpulResult_ está establecido en TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; de lo contrario, el contenido se establece en FALSE. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Cualquier proveedor de la libreta de direcciones no reconoce uno o ambos de los identificadores de entrada pasados con los parámetros _lpEntryID1_ o _lpEntryID2_ . 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y proveedores llamada de servicio **CompareEntryIDs** (método) para comparar dos identificadores de entrada que pertenece a un proveedor de libreta de direcciones único para determinar si hacen referencia al mismo objeto. **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de la libreta de direcciones. 
  
MAPI pasa esta llamada a la libreta de direcciones que se encarga de los identificadores de entrada, determinar el proveedor adecuado de forma que coincidan con la estructura [MAPIUID](mapiuid.md) en los identificadores de entrada con la estructura **MAPIUID** registrada por el proveedor. 
  
Si los identificadores de dos entrada hacer referencia al mismo objeto, **CompareEntryIDs** establece el contenido del parámetro _lpulResult_ en TRUE; Si hacen referencia a objetos diferentes, **CompareEntryIDs** establece el contenido en FALSE. En cualquier caso, **CompareEntryIDs** devuelve S_OK. Si **CompareEntryIDs** devuelve un error, lo que puede ocurrir si ningún proveedor de libreta de direcciones ha registrado una estructura **MAPIUID** que coincida con el de los identificadores de entrada, los clientes y proveedores no deben realizar ninguna acción en función del resultado de la comparación. En su lugar, que deben seguir el enfoque más conservador para la acción que se lleva a cabo. 
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

