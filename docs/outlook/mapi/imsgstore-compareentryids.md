---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348793"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes. MAPI pasa esta llamada a un proveedor de servicios sólo si los identificadores únicos (UID) de los dos identificadores de entrada que se van a comparar están controlados por ese proveedor.
  
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
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> a Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> a Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> contempla Un puntero al resultado de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La comparación se realizó correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno de los identificadores de entrada especificados como parámetros no hace referencia a objetos, posiblemente porque los objetos correspondientes no están abiertos y no están disponibles en este momento.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: CompareEntryIDs** compara dos identificadores de entrada que pertenecen al almacén de mensajes para determinar si hacen referencia al mismo objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido (por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes). 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción basándose en el resultado de la comparación. En su lugar, siga el enfoque más conservador posible. Se puede producir un error en **CompareEntryIDs** si, por ejemplo, uno o ambos de los identificadores de entrada contienen un **MAPIUID**no válido. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI usa el método **IMsgStore:: CompareEntryIDs** para comparar los identificadores de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

