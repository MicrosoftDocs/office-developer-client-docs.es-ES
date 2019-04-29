---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera la memoria asignada por la interfaz IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406202"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Libera la memoria asignada por la interfaz [IOlkAccount](iolkaccount.md) . 
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameters

_argumento_
  
> a Puntero a la memoria que se va a liberar.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Use este método para liberar la memoria asignada por [IOlkAccount:: GetProp](iolkaccount-getprop.md) (si el valor de la propiedad Account especificada es un tipo binary o String) y [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Ver también

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

