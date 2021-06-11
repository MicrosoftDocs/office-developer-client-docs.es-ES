---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera la memoria asignada por la interfaz IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408491"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Libera la memoria asignada por la [interfaz IOlkAccountManager.](iolkaccountmanager.md) 
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameters

_pv_
  
> [in] Un puntero a la memoria para liberar.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Use este método para liberar la memoria asignada por [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Vea también

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

