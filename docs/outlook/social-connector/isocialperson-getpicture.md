---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtiene una matriz de bytes que contiene el recurso de imagen para la persona.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821095"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtiene una matriz de bytes que contiene el recurso de imagen para la persona. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Sintaxis

_imagen_
  
> [out] Un puntero a una estructura que especifica una matriz de bytes que representan el recurso de imagen de una persona.
    
## <a name="remarks"></a>Notas

Compatible con los recursos están en .bmp, .jpeg o .png formato de imagen.
  
## <a name="see-also"></a>Ver también

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)

