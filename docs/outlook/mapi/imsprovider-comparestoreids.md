---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431711"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada del almacén de mensajes para determinar si hacen referencia al mismo objeto Store.
  
```cpp
HRESULT CompareStoreIDs(
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
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> a Puntero al primer identificador de entrada que se va a comparar.
    
 _cbEntryID2_
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> a Puntero al segundo identificador de entrada que se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> contempla Un puntero al resultado devuelto de la comparación. TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

MAPI llama al método **IMSProvider:: CompareStoreIDs** cuando procesa una llamada al método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . En este momento, se llama a **CompareStoreIDs** para determinar qué sección de perfil, si la hay, está asociada con el almacén de mensajes que se abre. Se puede realizar una llamada de **CompareStoreIDs** cuando no hay ningún almacén de mensajes abierto para un determinado proveedor de almacén. Además, MAPI también llama a **CompareStoreIDs** cuando procesa una llamada del proveedor de almacén al método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Los identificadores de entrada comparados por **CompareStoreIDs** son para la biblioteca de vínculos dinámicos (dll) del proveedor de almacenamiento actual y son identificadores de entrada de almacén no ajustados. Para obtener más información sobre los identificadores de entrada de almacén, vea [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
La comparación de los identificadores de entrada es útil porque un objeto puede tener más de un identificador de entrada válido. Esto puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de almacenamiento de mensajes. 
  
## <a name="see-also"></a>Ver también



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

