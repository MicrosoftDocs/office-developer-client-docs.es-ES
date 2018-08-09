---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- TempStr (función) [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815709"
---
# <a name="tempstr"></a>TempStr

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca Framework en desuso que crea un temporal **XLOPER** que contiene una cadena de bytes **xltypeStr** . Toma una cadena terminada en null de origen como entrada. Intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de cadena subsiguientes. No siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de sólo lectura. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parámetros

 _str_
  
Un puntero a la cadena de origen terminada en null. **TempStr** trunca cadenas que son mayores de 255 bytes. 
  
## <a name="return-value"></a>Valor devuelto

Devuelve una cadena de **xltypeStr** que contiene un puntero en el búfer de cadena que se pasa. 
  
## <a name="remarks"></a>Comentarios

Este modo de creación de cadenas temporales ahora está en desuso en favor de la manera en que ambos trabajo [TempStrConst y TempStr12](tempstrconst-tempstr12.md) . Estas funciones asignación un nuevo búfer de memoria y copie la cadena que se pasan en él. Las cadenas de entrada para **TempStrConst** y **TempStr12** no se modificarán y por lo que se declaran como **const**. Por el contrario, la cadena de entrada a **TempStr** se ha modificado y no se puede declarar como **const**. El primer carácter de la cadena de entrada se trata como espacio para un carácter de longitud y se sobrescribe por esta función.
  
## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

