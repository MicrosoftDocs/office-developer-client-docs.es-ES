---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817105"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Se aplica a**: Outlook 
  
Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a>Sintaxis

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
    
 _lpulRet_
  
> [out] Un puntero al resultado de la comparación. TRUE para indicar que los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los identificadores de entrada comparados correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> Uno o ambos de los identificadores de entrada no pertenecen a la libreta de direcciones.
    
## <a name="remarks"></a>Notas

Los proveedores de la libreta de direcciones implementan el método **CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. 
  
 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; Esta situación puede suceder, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo. 
  
Para obtener más información acerca de cómo crear los identificadores de entrada, vea [Identificadores de entrada de MAPI](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Ver también



[IABLogon: IUnknown](iablogoniunknown.md)

