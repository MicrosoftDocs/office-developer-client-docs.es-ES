---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 (función) [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815762"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rutina de conversión que se usa para convertir de la antigua **XLOPER** a la nueva **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Sintaxis

_pxloper_ (**LPXLOPER**)
  
Puntero al origen de **XLOPER** que se va a convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Puntero al destino **XLOPER12** para contener el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Notas

Según el tipo de la **XLOPER**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se hace referencia en el destino **XLOPER12**. El autor de la llamada es responsable de liberar cualquier memoria asociada con la copia si la conversión es un éxito; Se puede usar **FreeXLOper12T** , o puede realizarse directamente con **gratuita**.
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar cualquier memoria.
  
En general, la conversión de cualquier **XLOPER** a un **XLOPER12** es posible. Por el contrario, la conversión de un **XLOPER12** un **XLOPER** puede producirse un error cuando el **XLOPER12** contiene una matriz o referencia que es demasiado grande o una cadena que es demasiado larga para el **XLOPER** contener. 
  
**XLOPER** Cadenas de bytes ASCII se convierten en cadenas de caracteres anchos de Unicode **XLOPER12** de una manera que depende de la configuración regional. 
  
### <a name="example"></a>Ejemplo

Consulte el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para el código para esta función. 
  

