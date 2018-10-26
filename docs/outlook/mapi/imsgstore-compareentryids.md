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
ms.openlocfilehash: 640923511241b08e5a86e9733aab5cc2e9237c23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576578"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes. MAPI pasa esta llamada a un proveedor de servicio únicamente si los identificadores únicos (UID) en ambos identificadores de entrada que se va a comparar son resueltos por dicho proveedor.
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [entrada] Un puntero para el primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [entrada] Un puntero para el segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [out] Un puntero al resultado de la comparación. TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La comparación realizada correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno o ambos de los identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente debido a que los objetos correspondientes están sin abrir y no está disponible en presentan.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::CompareEntryIDs** compara dos identificadores de entrada que pertenecen al almacén de mensajes para determinar si hacen referencia al mismo objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido (por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes). 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación. En su lugar, tomar el enfoque más conservador posible. **CompareEntryIDs** puede producirse un error si, por ejemplo, uno o ambos de los identificadores de entrada contiene un **MAPIUID**de no válido. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa el método **IMsgStore::CompareEntryIDs** para comparar los identificadores de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

