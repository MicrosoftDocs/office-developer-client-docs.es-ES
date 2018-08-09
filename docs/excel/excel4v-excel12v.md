---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- función Excel12v [excel 2007], Excel4v (función) [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815636"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a un interno función de hoja de cálculo de Microsoft Excel, una función de hoja de macros o un comando, o un solo XLL función especial o un comando, desde dentro de un archivo DLL, XLL o recurso de código.
  
Todas las versiones recientes de Excel admiten la **Excel4v**. Iniciar en Excel 2007, se admite **Excel12v** . 
  
Estas funciones se pueden llamar sólo cuando Excel ha pasado el control a la DLL o XLL. También puede llamar cuando Excel ha pasado control indirectamente a través de una llamada a Visual Basic para aplicaciones (VBA). No se puede llamar en cualquier otro momento. Por ejemplo, no se puede llamar durante las llamadas a la función DllMain u otros momentos cuando el sistema operativo se llama a la DLL, o desde un subproceso creado por el archivo DLL. 
  
Las funciones de [Excel4 y Excel12](excel4-excel12.md) aceptan sus argumentos como una lista de longitud variable en la pila, mientras que las funciones **Excel4v** y **Excel12v** aceptan sus argumentos como una matriz. En todos los demás aspectos, **Excel4** se comporta de la misma que la **Excel4v**y **Excel12** se comporta igual que **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parámetros

 _iFunction_ (**int**)
  
Un número que indica el comando, función o función especial que desea llamar. Para obtener una lista de valores válidos _iFunction_ , vea la siguiente sección de comentarios. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Un puntero a un **XLOPER** (en el caso de **Excel4v**) o un **XLOPER12** (en el caso de **Excel12v**) que contendrá el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
El número de argumentos subsiguientes que se va a pasar a la función. En las versiones de Excel hasta 2003 Esto puede ser cualquier número comprendido entre 0 y 30. Iniciar en Excel 2007, esto puede ser cualquier número comprendido entre 0 y 255.
  
 _rgx_ (**[De LPXLOPER]** o **[] LPXLOPER12**)
  
Una matriz que contiene los argumentos de la función. Todos los argumentos de la matriz deben ser punteros a valores **XLOPER** o **XLOPER12** . 
  
## <a name="return-value"></a>Valor devuelto

Estas funciones devuelven los mismos valores que **Excel4** y **Excel12**.
  
## <a name="remarks"></a>Comentarios

Estas funciones son útiles donde el número de argumentos que se pasan al operador es variable. Por ejemplo, **Excel4v** y **Excel12v** son útiles al registrar funciones mediante el uso de [xlfRegister](xlfregister-form-1.md) donde el número de argumentos totales depende del número de argumentos realizadas por la función que se está registrada. **Excel4v** y **Excel12v** también son útiles cuando se escribe una función de contenedor para **Excel4** o **Excel12**. En estos casos, debe convertir una lista de argumentos de variable, tal y como haría normalmente ser suministrada a **Excel4** o **Excel12**, a un argumento de matriz único de tamaño variable para devolver la llamada en Excel mediante el uso de la **Excel4v** o **Excel12v**.
  
### <a name="example"></a>Ejemplo

Para obtener ejemplos de código, vea el código para las funciones de **Excel** y **Excel12f** en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Vea también



[Excel4/Excel12](excel4-excel12.md)

