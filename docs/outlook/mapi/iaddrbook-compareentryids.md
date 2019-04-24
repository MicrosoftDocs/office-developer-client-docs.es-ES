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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348891"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones determinado para determinar si hacen referencia al mismo objeto de la libreta de direcciones. 
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> a Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> a Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> contempla Un puntero al resultado de la comparación. El contenido de _lpulResult_ se establece en true si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, el contenido se establece en FALSE. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno o ambos de los identificadores de entrada pasados con los parámetros _lpEntryID1_ o _lpEntryID2_ no son reconocidos por ningún proveedor de libreta de direcciones. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y los proveedores de servicios llaman al método **CompareEntryIDs** para comparar dos identificadores de entrada que pertenecen a un único proveedor de libreta de direcciones para determinar si hacen referencia al mismo objeto. **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de libretas de direcciones. 
  
MAPI pasa esta llamada al proveedor de la libreta de direcciones que es responsable de los identificadores de entrada y determina el proveedor adecuado al hacer coincidir la estructura [MAPIUID](mapiuid.md) de los identificadores de entrada con la estructura **MAPIUID** registrada por el proveedor. 
  
Si los dos identificadores de entrada hacen referencia al mismo objeto, **CompareEntryIDs** establece el contenido del parámetro _lpulResult_ en true; Si hacen referencia a objetos diferentes, **CompareEntryIDs** establece el contenido en false. En cualquier caso, **CompareEntryIDs** Devuelve S_OK. Si **CompareEntryIDs** devuelve un error, lo que puede ocurrir si ningún proveedor de la libreta de direcciones ha registrado una estructura **MAPIUID** que coincide con la de los identificadores de entrada, los clientes y los proveedores no deben realizar ninguna acción basada en el resultado de la entre. En su lugar, deberían tomar el enfoque más conservador para la acción que se está llevando a cabo. 
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

