---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe la enumeración a un período de tiempo especificado.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816079"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Restringe la enumeración a un período de tiempo especificado.
  
## <a name="quick-info"></a>Información rápida

Vea [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parámetros

_ftmStart_
  
>  [entrada] La hora de inicio para restringir la enumeración. 
    
_ftmEnd_
  
> [entrada] La hora de finalización para restringir la enumeración.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Este método también restablece la enumeración.
  
## <a name="see-also"></a>Vea también

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

