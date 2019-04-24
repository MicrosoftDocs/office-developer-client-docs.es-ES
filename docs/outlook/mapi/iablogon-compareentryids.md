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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279611"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
 _lpulRet_
  
> contempla Un puntero al resultado de la comparación. TRUE para indicar que los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los identificadores de entrada se comparó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> Uno o ambos de los identificadores de entrada no pertenecen al proveedor de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. 
  
 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; una situación de este tipo puede ocurrir, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo. 
  
Para obtener más información acerca de cómo crear identificadores de entrada, consulte identificadores de [entrada MAPI](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Vea también



[IABLogon : IUnknown](iablogoniunknown.md)

