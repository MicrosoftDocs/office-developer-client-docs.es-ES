---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- función xlStack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815744"
---
# <a name="xlstack"></a>xlStack

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comprueba la cantidad de espacio libre en la pila.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el número de bytes (**xltypeInt**) restante en la pila.
  
## <a name="remarks"></a>Comentarios

La cantidad de espacio de pila disponible de versiones recientes desborda el entero con signo de 16 bits de la **XLOPER**. Esto significa que **xlStack** puede devolver un valor entre-32767 y 32768 cuando llama a mediante **XLOPER**s y **Excel4** o **Excel4v**. Para obtener el valor correcto en este caso, debe convertir el valor devuelto para un unsigned short.
  
Inicio de Excel 2007, se debe llamar a esta función con s **XLOPER12**y **Excel12** o **Excel12v**, en cuyo caso el valor devuelto es la cantidad de espacio de pila disponible o 64 KB, lo que es el menor.
  
Excel dispone de una cantidad limitada de espacio en la pila y que debe tener cuidado para no de este espacio de saturación. Nunca coloca las estructuras de datos muy grandes en la pila y realice todas las variables locales como sea posible estática. Evite llamar a funciones de forma recursiva, ya va a rellenar rápidamente arriba de la pila.
  
Si sospecha que son sobrepasar la pila, llamar a esta función con frecuencia para ver cuánto espacio de pila queda.
  
## <a name="example"></a>Ejemplo

El primer ejemplo se muestra un mensaje de alerta que contiene la cantidad de pila espacio izquierda y está incluido en `\SAMPLES\EXAMPLE\EXAMPLE.C`. El segundo ejemplo hace lo mismo, trabajar con s **XLOPER**y no está incluido en el código de ejemplo SDK.
  
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

## <a name="see-also"></a>Vea también

- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

