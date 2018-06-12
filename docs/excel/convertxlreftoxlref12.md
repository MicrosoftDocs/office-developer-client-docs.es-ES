---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12 (función) [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815531"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de Framework que intenta convertir un **XLREF** en un **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Sintaxis

 _pxRef_ (**LPXLREF**)
  
Puntero a la estructura del origen de referencia.
  
 _pxRef12_ (**LPXLREF12**)
  
Puntero a la estructura de referencia de destino en el que el valor convertido es que se va a colocar.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

 **TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Notas

Siempre que se pasan en **XLREF** es válida, esta operación debe ser siempre correcta. Por el contrario, conversión de la otra forma de **XLREF12** **XLREF**, realizado por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), se produce un error si la referencia proporcionada hace referencia a la parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

