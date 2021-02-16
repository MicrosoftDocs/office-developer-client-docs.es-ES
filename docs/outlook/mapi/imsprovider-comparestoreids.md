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
  
Compara dos identificadores de entrada de almacén de mensajes para determinar si hacen referencia al mismo objeto de almacén.
  
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

MAPI llama al **método IMSProvider::CompareStoreIDs** cuando procesa una llamada al método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) **Se llama a CompareStoreIDs** en este punto para determinar qué sección de perfil, si la hay, está asociada con el almacén de mensajes que se abre. Se **puede realizar una llamada CompareStoreIDs** cuando no hay ningún almacén de mensajes abierto para un proveedor de almacenamiento determinado. Además, MAPI también llama a **CompareStoreIDs** cuando procesa una llamada de proveedor de almacén al método [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md) 
  
Los identificadores de entrada que comparan los **CompareStoreID son** para la biblioteca de vínculos dinámicos (DLL) del proveedor de almacenamiento actual y son identificadores de entrada de almacén sin envolver. Para obtener más información acerca del ajuste de identificadores de entrada del almacén, vea [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Comparar identificadores de entrada es útil porque un objeto puede tener más de un identificador de entrada válido. Esto puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de almacenamiento de mensajes. 
  
## <a name="see-also"></a>Consulte también



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

