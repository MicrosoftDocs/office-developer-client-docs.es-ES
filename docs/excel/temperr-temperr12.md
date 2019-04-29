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
- función templator [Excel 2007], función TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410612"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de .NET Framework que crea un**XLOPER12** de **XLOPER**/ temporal que contiene un error de hoja de cálculo de Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parameters

 _err_
  
El código de error deseado, o su equivalente numérico literal, como se muestra en la siguiente tabla.
  
|**Error**|**Código de error definido en XLCALL. H**|**Equivalente decimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |comprendi  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15   <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |veintitrés  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |32  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Devuelve una **xltypeBool** que contiene el código de error que se ha pasado. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función **TempErr12** para devolver un #VALUE! error a Excel. 
  
> [!NOTE]
> La función **TempErr12** de la biblioteca de Marcos asigna memoria de un búfer interno, que normalmente se libera cuando se llama a la función **Excel12f** de Framework. Si se llama a esta función de ejemplo repetidamente sin llamar a **Excel12f** , se produce una pérdida de memoria. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

