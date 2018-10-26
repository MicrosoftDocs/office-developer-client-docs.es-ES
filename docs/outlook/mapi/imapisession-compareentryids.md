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
ms.openlocfilehash: 745c1b10cbbb24389cace7911d7c5fd37fe09472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586854"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [entrada] Un puntero para el primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ . 
    
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
  
> Uno o ambos de los identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente debido a que estos objetos están actualmente sin abrir y no está disponible.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un proveedor de servicio único para determinar si hacen referencia al mismo objeto. MAPI extrae la parte [MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicio responsable de los objetos y, a continuación, llama a **CompareEntryIDs** (método) del objeto de su inicio de sesión para llevar a cabo la comparación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El método **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido. Esta situación puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de servicios. 
  
Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación. En su lugar, tomar el enfoque más conservador posible. **CompareEntryIDs** puede producirse un error si, por ejemplo, uno o ambos de los identificadores de entrada contienen un **MAPIUID**de no válido. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa el método **IMAPISession::CompareEntryIDs** para comparar dos identificadores de entrada que un usuario escribe.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

