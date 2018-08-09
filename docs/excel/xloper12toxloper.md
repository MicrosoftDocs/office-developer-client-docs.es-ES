---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper (función) [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815747"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rutina de conversión que se usa para convertir de nuevo **XLOPER12** a la antigua **XLOPER**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parámetros

_pxloper12_ (**LPXLOPER12**)
  
Puntero al origen de **XLOPER12** que se va a convertir. 
  
_pxloper_ (**LPXLOPER**)
  
Puntero al destino **XLOPER** para contener el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Comentarios

Según el tipo de **XLOPER12**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se hace referencia en el destino **XLOPER**. El autor de la llamada es responsable de liberar cualquier memoria asociada con la copia si la conversión es un éxito; Se puede usar **FreeXLOperT** , o se puede realizar directamente mediante el uso de **libre**.
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar cualquier memoria.
  
Puede producirse un error en la conversión de un **XLOPER12** a un **XLOPER** cuando **XLOPER12** contiene una matriz o referencia que es demasiado grande o una cadena que es demasiado larga para el **XLOPER** contener. 
  
**XLOPER12** Cadenas de caracteres anchos de Unicode se convierten en cadenas de bytes **XLOPER** ASCII en un modo que sea configuración regional-dependiente. 
  
El **XLOPER12** **xltypeInt** es un entero con signo de 32 bits, mientras que el **XLOPER** **xltypeInt** es un entero con signo de 16 bits. Cuando un entero **XLOPER12** proporcionado supera el límite de entero **XLOPER** , el número entero se convierte en un doble de 8 bytes y se devuelven en un **XLOPER** de tipo **xltypeNum**. Esto es el único caso en que esta función cambia el tipo de la convertida **XLOPER**.
  
### <a name="example"></a>Ejemplo

Consulte el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para el código para esta función. 
  
## <a name="see-also"></a>Vea también

- [Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

