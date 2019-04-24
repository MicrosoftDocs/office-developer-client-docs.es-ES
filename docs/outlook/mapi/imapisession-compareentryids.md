---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338461"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> contempla Un puntero al resultado de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La comparación se realizó correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Uno de los identificadores de entrada especificados como parámetros no hace referencia a objetos, posiblemente porque estos objetos no están abiertos actualmente y no están disponibles.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un único proveedor de servicios para determinar si hacen referencia al mismo objeto. MAPI extrae la parte [MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicios responsable de los objetos y, a continuación, llama al método **CompareEntryIDs** del objeto de inicio de sesión para realizar la comparación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El método **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de servicios. 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción basándose en el resultado de la comparación. En su lugar, siga el enfoque más conservador posible. Se puede producir un error en **CompareEntryIDs** si, por ejemplo, uno o ambos de los identificadores de entrada contienen un **MAPIUID**no válido. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CbaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI usa el método **IMAPISession:: CompareEntryIDs** para comparar dos identificadores de entrada que especifica un usuario.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

