---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtiene la información de tipo y categorías de la cuenta especificada.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437906"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtiene la información de tipo y categorías de la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameters

_pclsidType_
  
> [salida] Identificador de clase para el tipo de cuenta. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [salida] El número de categorías de  _prgclsidCategory_.
    
_prgclsidCategory_
  
> [salida] Una matriz de categorías a las que está asociada esta cuenta. La matriz es de tamaño * _pcCategories_. El valor de cada categoría de la matriz debe ser uno de los siguientes:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Después de que este método devuelve, debe liberar  *prgclsidCategory*  mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** no admite la categoría de libreta de direcciones para una Exchange cuenta. Si la cuenta es una cuenta de Exchange (*pclsidType* es **CLSID_OlkMAPIAccount** ), y la cuenta implementa la libreta de direcciones, llamar a **IOlkAccount::GetAccountInfo** no devolverá **CLSID_OlkAddressBook** como categoría en *prgclsidCategory* . 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

