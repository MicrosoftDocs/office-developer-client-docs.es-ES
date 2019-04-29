---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- función xloper12toxloper [Excel 2007]
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
  
Rutina de conversión que se usa para convertir del nuevo **XLOPER12** al **XLOPER**anterior.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameters

_pxloper12_ (**LPXLOPER12**)
  
Puntero al **XLOPER12** de origen que se va a convertir. 
  
_pxloper_ (**LPXLOPER**)
  
Puntero al **XLOPER** de destino que contendrá el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

**True** si la conversión se realizó correctamente; de lo contrario, **false** . 
  
## <a name="remarks"></a>Comentarios

Según el tipo de **XLOPER12**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se señalan en el **XLOPER**de destino. El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es un éxito; **FreeXLOperT** se puede usar o puede realizarse directamente con **Free**.
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.
  
Se puede producir un error en la conversión de un **XLOPER12** a un **XLOPER** cuando el **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** la contenga. 
  
**XLOPER12** Las cadenas Unicode de caracteres anchos se convierten en cadenas de bytes ASCII de **XLOPER** de manera que dependen de la configuración regional. 
  
El **** **xltypeInt** XLOPER12 es un entero con signo de 32 bits, mientras que el **xltypeInt** de **XLOPER** es un entero de 16 bits con signo. Cuando un entero de **XLOPER12** proporcionado supera el límite de un tipo entero **XLOPER** , el entero se convierte en un Double de 8 bytes y se devuelve en un **XLOPER** de tipo **xltypeNum**. Este es el único caso en el que esta función cambia el tipo del **XLOPER**convertido.
  
### <a name="example"></a>Ejemplo

Vea el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función. 
  
## <a name="see-also"></a>Ver también

- [Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

