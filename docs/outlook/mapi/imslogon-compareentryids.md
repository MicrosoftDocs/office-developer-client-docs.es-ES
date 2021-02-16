---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410136"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto. MAPI hace referencia a esta llamada a un proveedor de servicios solo si ese proveedor controla los identificadores únicos (UID) de ambos identificadores de entrada que se van a comparar.
  
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
  
> [entrada] El tamaño, en bytes, del identificador de entrada al que apunta el  _parámetro lpEntryID1_  _._
    
 _lpEntryID1_
  
> [entrada] Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El tamaño, en bytes, del identificador de entrada al que apunta el  _parámetro lpEntryID2_  _._
    
 _lpEntryID2_
  
> [entrada] Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [salida] Puntero al resultado devuelto de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::CompareEntryIDs** para comparar dos identificadores de entrada de una entrada determinada en un almacén de mensajes para determinar si hacen referencia al mismo objeto. Si los dos identificadores de entrada hacen referencia al mismo objeto, **CompareEntryIDs** establece el parámetro  _lpulResult_ en TRUE; si hacen referencia a diferentes objetos, **CompareEntryIDs** establece  _lpulResult_ en FALSE. 
  
 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esto puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de almacenamiento de mensajes. 
  
## <a name="see-also"></a>Consulte también



[IMSLogon : IUnknown](imslogoniunknown.md)

