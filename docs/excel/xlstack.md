---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- función xlstack [Excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429982"
---
# <a name="xlstack"></a>xlStack

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comprueba la cantidad de espacio restante en la pila.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el número de bytes (**xltypeInt**) restantes en la pila.
  
## <a name="remarks"></a>Comentarios

La cantidad de espacio de pila disponible de versiones recientes desborda el entero de 16 bits con signo del **XLOPER**. Esto significa que **xlStack** puede devolver un valor entre-32767 y 32768 cuando se llama usando **XLOPER**s y **Excel4** o **Excel4v**. Para obtener el valor correcto en este caso, debe convertir el valor devuelto a un unsigned short.
  
A partir de Excel 2007, debe llamar a esta función con **XLOPER12**s y **Excel12** o **Excel12v**, en cuyo caso el valor devuelto es la cantidad de espacio de pila disponible o 64 KB, lo que sea menor.
  
Excel tiene una cantidad limitada de espacio en la pila y debe tener cuidado de no saturar este espacio. No ponga nunca estructuras de datos muy grandes en la pila y convierta tantas variables locales como sea posible. Evite llamar a las funciones de forma recursiva, ya que de este modo se llenará rápidamente la pila.
  
Si sospecha que está sobreutilizando la pila, llame a esta función con frecuencia para ver la cantidad de espacio de pila que queda.
  
## <a name="example"></a>Ejemplo

En el primer ejemplo se muestra un mensaje de alerta que contiene la cantidad de espacio de pila `\SAMPLES\EXAMPLE\EXAMPLE.C`restante y que se incluye en. El segundo ejemplo hace lo mismo, ya que se trabaja con **XLOPER**y no incluido en el código de ejemplo del SDK.
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>Ver también

- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

