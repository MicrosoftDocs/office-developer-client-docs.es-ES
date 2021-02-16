---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtiene una matriz de bytes que contiene el recurso de imagen de la persona.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406713"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtiene una matriz de bytes que contiene el recurso de imagen de la persona. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parámetros

_imagen_
  
> [salida] Puntero a una estructura que especifica una matriz de bytes que representan el recurso de imagen de una persona.
    
## <a name="remarks"></a>Comentarios

Los recursos de imagen admitidos están en formato .bmp, .jpeg o .png.
  
## <a name="see-also"></a>Consulte también

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

