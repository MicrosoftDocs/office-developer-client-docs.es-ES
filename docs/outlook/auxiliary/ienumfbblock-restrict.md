---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe la enumeración a un período de tiempo especificado.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431949"
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

## <a name="parameters"></a>Parameters

_ftmStart_
  
>  [in] Hora de inicio para restringir la enumeración. 
    
_ftmEnd_
  
> [in] Hora de finalización para restringir la enumeración.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Este método también restablece la enumeración.
  
## <a name="see-also"></a>Vea también

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

