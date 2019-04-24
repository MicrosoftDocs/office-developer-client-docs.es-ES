---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- función convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310993"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de Framework que intenta convertir un **XLREF** en un **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameters

 _pxRef_ (**LPXLREF**)
  
Puntero a la estructura de referencia de origen.
  
 _pxRef12_ (**LPXLREF12**)
  
Puntero a la estructura de referencia de destino en la que se va a colocar el valor convertido.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **True** si la conversión se realizó correctamente; de lo contrario, **false** . 
  
## <a name="remarks"></a>Comentarios

Siempre que el **XLREF** pasado sea válido, esta operación siempre debe realizarse correctamente. Por el contrario, la conversión de la otra forma de **XLREF12** a **XLREF**, realizada por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), produce un error si la referencia proporcionada hace referencia a parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.
  
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



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

