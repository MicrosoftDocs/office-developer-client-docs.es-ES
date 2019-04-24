---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- función xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303909"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rutina de conversión que se usa para convertir del **XLOPER** antiguo al nuevo **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameters

_pxloper_ (**LPXLOPER**)
  
Puntero al **XLOPER** de origen que se va a convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Puntero al **XLOPER12** de destino para que contenga el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

**True** si la conversión se realizó correctamente; de lo contrario, **false** . 
  
## <a name="remarks"></a>Comentarios

Según el tipo de **XLOPER**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se señalan en el **XLOPER12**de destino. El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es un éxito; Se puede usar **FreeXLOper12T** , o bien se puede hacer directamente con **Free**.
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.
  
En general, es posible convertir de cualquier **XLOPER** a **XLOPER12** . Por el contrario, se puede producir un error en la conversión de un **XLOPER12** a un **XLOPER** cuando el **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** la contenga. 
  
**XLOPER** Las cadenas de bytes ASCII se convierten en las cadenas de caracteres anchos Unicode de **XLOPER12** de forma que dependen de la configuración regional. 
  
### <a name="example"></a>Ejemplo

Vea el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función. 
  

