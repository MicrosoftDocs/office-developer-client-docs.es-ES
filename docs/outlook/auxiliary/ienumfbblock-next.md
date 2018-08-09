---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816088"
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

## <a name="parameters"></a>Parámetros

_celt_
  
> [entrada] El número de datos de disponibilidad se bloquea en *pblk* para recuperar. 
    
_PBLK_
  
> [entrada] Un puntero a una matriz de bloques de libre/ocupado. La matriz se asigna un tamaño de *celt* . Los bloques de libre/ocupado solicitados se devuelven en esta matriz. 
    
_pcfetch_
  
> [out] El número de bloques de libre/ocupado devueltos realmente en *pblk* . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Ha devuelto el número solicitado de bloques.  <br/> |
|S_FALSE  <br/> |El número de bloques de solicitado no ha devuelto.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de libre/ocupado)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

