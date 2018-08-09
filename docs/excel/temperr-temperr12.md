---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperr (función) [excel 2007], TempErr12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815697"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** que contiene un error de hoja de cálculo de Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parámetros

 _err_
  
El código de error que desee, o su equivalente numérico literal, tal como se muestra en la siguiente tabla.
  
|**Error**|**Código de error definido en XLCALL. H**|**Equivalente decimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Devuelve un **xltypeBool** que contiene el código de error que se pasó. 
  
## <a name="example"></a>Ejemplo

¡En este ejemplo se usa la función **TempErr12** para devolver #VALUE! Error en Excel. 
  
> [!NOTE]
> La función de biblioteca de Framework **TempErr12** asigna memoria de un búfer interno, que normalmente se libera cuando se llama a la función de Framework **Excel12f** . Si en el ejemplo se llama a esta función repetidamente sin **Excel12f** que se llama, se produce una pérdida de memoria. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

