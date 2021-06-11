---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- función convertxlref12toxlref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432656"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Intenta convertir un **XLREF12** en **un XLREF**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Parameters

 _pxRef12_ (**LPXLREF12**)
  
Puntero a la estructura de referencia de origen.
  
 _pxRef_ (**LPXLREF**)
  
Puntero a la estructura de referencia de destino en la que se colocará el valor convertido.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **TRUE** si la conversión se ha hecho correctamente, **FALSE** en caso contrario. 
  
## <a name="remarks"></a>Comentarios

La conversión de **XLREF12** a **XLREF** produce un error si la referencia proporcionada hace referencia a una parte de una hoja de cálculo de Excel 2007 que no se admite en versiones anteriores. 
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

