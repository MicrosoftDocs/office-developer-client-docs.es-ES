---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- función tempstr [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418046"
---
# <a name="tempstr"></a>TempStr

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de Framework en desuso que crea un **XLOPER** temporal que contiene una cadena de bytes **xltypeStr** . Toma una cadena de origen terminada en NULL como entrada. Intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de la cadena subsiguiente. No siempre es un aspecto seguro que hacer: Microsoft Excel puede bloquearse si se pasa una cadena de solo lectura. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parámetros

 _str_
  
Un puntero a la cadena de origen terminada en nulo. **TempStr** trunca las cadenas que tienen más de 255 bytes. 
  
## <a name="return-value"></a>Valor devuelto

Devuelve una cadena **xltypeStr** que contiene un puntero al búfer de cadena pasado. 
  
## <a name="remarks"></a>Comentarios

Esta manera de crear cadenas temporales ahora está en desuso en favor de la forma en que funcionan tanto [TempStrConst como TempStr12](tempstrconst-tempstr12.md) . Estas funciones asignan un nuevo búfer de memoria y copian la cadena que se ha pasado en ella. No se modifican las cadenas de entrada de **TempStrConst** y **TempStr12** , por lo que se declaran como **const**. Por el contrario, se modifica la cadena de entrada a **TempStr** y, por lo tanto, no se puede declarar como **const**. El primer carácter de la cadena de entrada se trata como espacio para un carácter de longitud y se sobrescribe con esta función.
  
## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

