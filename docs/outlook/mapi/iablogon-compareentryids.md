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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438375"
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
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [in] Número de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulRet_
  
> [salida] Puntero al resultado de la comparación. TRUE para indicar que los dos identificadores de entrada hacen referencia al mismo objeto; en caso contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los identificadores de entrada se compararon correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> Uno o ambos identificadores de entrada no pertenecen al proveedor de libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

Los proveedores de libreta de direcciones implementan el **método CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. 
  
 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; esta situación puede producirse, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo. 
  
Para obtener más información acerca de cómo crear identificadores de entrada, vea [Mapi Entry Identifiers](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Vea también



[IABLogon : IUnknown](iablogoniunknown.md)

