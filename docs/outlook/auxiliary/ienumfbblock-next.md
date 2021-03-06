---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422141"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.
  
## <a name="quick-info"></a>Información rápida

Vea [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameters

_celta_
  
> [in] Número de bloques de datos de disponibilidad en  *pblk*  que se recuperarán. 
    
_pblk_
  
> [in] Puntero a una matriz de bloques de disponibilidad. A la matriz se le asigna un tamaño de *celta.* Los bloques de disponibilidad solicitados se devuelven en esta matriz. 
    
_pcfetch_
  
> [salida] El número de bloques de disponibilidad devueltos realmente en  *pblk*  . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Se ha devuelto el número de bloques solicitado.  <br/> |
|S_FALSE  <br/> |No se ha devuelto el número de bloques solicitado.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de disponibilidad)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

