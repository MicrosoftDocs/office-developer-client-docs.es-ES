---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Función xlopertoxloper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404599"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rutina de conversión usada para convertir del **XLOPER** antiguo al **nuevo XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameters

_pxloper_ (**LPXLOPER**)
  
Puntero al **XLOPER de origen** que se va a convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Puntero al **XLOPER12 de destino** para contener el valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

**TRUE** si la conversión se ha hecho correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Comentarios

Según el tipo de **XLOPER,** esta función asigna un nuevo búfer de memoria para los valores convertidos, que se apuntan en el **XLOPER12** de destino. El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es correcta; **FreeXLOper12T** se puede usar o se puede hacer directamente con **free**.
  
Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.
  
En general, la conversión de **cualquier XLOPER** a **un XLOPER12** es posible. En cambio, la conversión de **un XLOPER12** a **un XLOPER** puede producir un error cuando **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** contenga. 
  
**XLOPER** Las cadenas de bytes ASCII se convierten en cadenas de caracteres anchos Unicode **XLOPER12** de una forma que depende de la configuración regional. 
  
### <a name="example"></a>Ejemplo

Vea el archivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función. 
  

