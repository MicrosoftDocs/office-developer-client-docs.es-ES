---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431046"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto. 
  
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
  
> [salida] Puntero al resultado de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La comparación se ha realizado correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno o ambos identificadores de entrada especificados como parámetros no hacen referencia a objetos válidos, posiblemente porque actualmente están sin abrir y no están disponibles.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CompareEntryIDs** se implementa para objetos de compatibilidad con la libreta de direcciones y el proveedor del almacén de mensajes. **CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un único proveedor de servicios para determinar si hacen referencia al mismo objeto. MAPI extrae la [parte MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicios responsable de los objetos. A continuación, MAPI llama al método **CompareEntryIDs** del objeto de inicio de sesión para realizar la comparación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede producirse, por ejemplo, después de instalar una nueva versión de un proveedor de servicios. 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción basada en el resultado de la comparación. En su lugar, toma el enfoque más conservador posible. **CompareEntryIDs** puede producir un error si, por ejemplo, uno o ambos identificadores de entrada contienen una estructura **MAPIUID no** válida. 
  
## <a name="see-also"></a>Consulte también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

