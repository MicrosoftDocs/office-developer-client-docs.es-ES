---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Función xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422911"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rutina de conversión usada para convertir del **nuevo XLOPER12** al **XLOPER antiguo**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameters

_pxloper12_ (**LPXLOPER12**)
  
Puntero al **origen XLOPER12** que se va a convertir. 
  
_pxloper_ (**LPXLOPER**)
  
Puntero al **XLOPER de destino** para contener el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

**TRUE** si la conversión se ha hecho correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Comentarios

Según el tipo de **XLOPER12**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se apuntan en el **XLOPER de** destino. El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es correcta; **FreeXLOperT** puede usarse o puede hacerse directamente mediante **el uso** gratuito de .
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.
  
La conversión de **un XLOPER12** a **un XLOPER** puede producir un error cuando **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** contenga. 
  
**XLOPER12** Las cadenas de caracteres anchos Unicode se convierten en cadenas de bytes ASCII **XLOPER** de una forma que depende de la configuración regional. 
  
**XLOPER12** **xltypeInt** es un entero con signo de 32 bits, mientras que **XLOPER** **xltypeInt** es un entero con signo de 16 bits. Cuando un entero **XLOPER12** proporcionado supera el límite de un entero **XLOPER,** el entero se convierte en un doble de 8 bytes y se devuelve en un **XLOPER** de tipo **xltypeNum**. Este es el único caso en el que esta función cambia el tipo de **XLOPER convertido.**
  
### <a name="example"></a>Ejemplo

Vea el archivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función. 
  
## <a name="see-also"></a>Vea también

- [Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

