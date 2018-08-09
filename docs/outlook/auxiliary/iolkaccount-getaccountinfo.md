---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtiene la información de tipo y las categorías de la cuenta especificada.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816153"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtiene la información de tipo y las categorías de la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parámetros

_pclsidType_
  
> [out] El identificador de clase para el tipo de cuenta. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] El número de categorías en _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Una matriz de categorías a las que está asociada esta cuenta. La matriz es de tamaño * _pcCategories_. El valor de cada categoría de la matriz debe ser uno de estos procedimientos:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Después de que devuelve este método, debe liberar *prgclsidCategory* mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** no es compatible con la categoría de la libreta de direcciones para una cuenta de Exchange. Si la cuenta es un intercambio cuenta (*pclsidType* es **CLSID_OlkMAPIAccount** ) y la cuenta implementa la libreta de direcciones, llamada **IOlkAccount::GetAccountInfo** no devolverá **CLSID_OlkAddressBook** como una categoría en * prgclsidCategory* . 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

