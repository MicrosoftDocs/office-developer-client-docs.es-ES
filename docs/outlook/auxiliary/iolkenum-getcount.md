---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtiene el número de cuentas del enumerador.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421826"
---
# <a name="iolkenumgetcount"></a>IOlkEnum::GetCount

Obtiene el número de cuentas del enumerador.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a>Parámetros

_pulCount_
  
> [salida] Puntero al número de objetos que se están enumerando.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Consulte también

- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

