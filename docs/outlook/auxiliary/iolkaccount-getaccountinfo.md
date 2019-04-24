---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtiene la información de tipos y categorías de la cuenta especificada.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318189"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtiene la información de tipos y categorías de la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameters

_pclsidType_
  
> contempla El identificador de clase para el tipo de cuenta. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> contempla El número de categorías en _prgclsidCategory_.
    
_prgclsidCategory_
  
> contempla Matriz de categorías a las que está asociada esta cuenta. La matriz tiene el tamaño * _pcCategories_. El valor de cada categoría de la matriz debe ser uno de los siguientes:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Después de que se devuelva este método, debe liberar *prgclsidCategory* mediante [IOlkAccount:: FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount:: GetAccountInfo** no admite la categoría de la libreta de direcciones para una cuenta de Exchange. Si la cuenta es una cuenta de Exchange (*pclsidType* es **CLSID_OlkMAPIAccount** ) y la cuenta implementa la libreta de direcciones, al llamar a **IOlkAccount:: GetAccountInfo** no se devolverá **CLSID_OlkAddressBook** como una categoría en * prgclsidCategory* . 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

