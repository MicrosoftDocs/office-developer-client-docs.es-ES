---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crea una copia del enumerador, utilizando la misma restricción de tiempo, pero estableciendo el cursor en el principio del enumerador.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317601"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Crea una copia del enumerador, utilizando la misma restricción de tiempo, pero estableciendo el cursor en el principio del enumerador.
  
## <a name="quick-info"></a>Información rápida

Consulte [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parameters

_ppclone_
  
> contempla Un puntero a puntero a la copia de la interfaz de [IEnumFBBlock](ienumfbblock.md) . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_OUTOFMEMORY  <br/> |Memoria insuficiente para realizar la copia.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de disponibilidad)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

