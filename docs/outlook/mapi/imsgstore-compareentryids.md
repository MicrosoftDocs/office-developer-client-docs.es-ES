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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424255"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes. MAPI pasa esta llamada a un proveedor de servicios solo si ese proveedor controla los identificadores únicos (UID) de ambos identificadores de entrada que se van a comparar.
  
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
  
> [entrada] El recuento de bytes en el identificador de entrada al que apunta el  _parámetro lpEntryID1_  _._
    
 _lpEntryID1_
  
> [entrada] Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El recuento de bytes en el identificador de entrada al que apunta el  _parámetro lpEntryID2_  _._
    
 _lpEntryID2_
  
> [entrada] Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [salida] Puntero al resultado de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La comparación se ha realizado correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno o ambos identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente porque los objetos correspondientes están sin abrir y no están disponibles actualmente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::CompareEntryIDs** compara dos identificadores de entrada que pertenecen al almacén de mensajes para determinar si hacen referencia al mismo objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido (por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes). 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción basada en el resultado de la comparación. En su lugar, tome el enfoque más conservador posible. **CompareEntryIDs** puede producir un error si, por ejemplo, uno o ambos identificadores de entrada contienen un **MAPIUID no válido.** 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa el **método IMsgStore::CompareEntryIDs** para comparar los identificadores de entrada.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

