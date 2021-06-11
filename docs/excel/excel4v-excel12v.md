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
- función excel12v [excel 2007],función Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414994"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función Microsoft Excel hoja de cálculo interna, una función o un comando de hoja de macros o un comando especial de XLL desde un recurso dll, XLL o código.
  
Todas las versiones recientes de Excel **admiten Excel4v**. A partir Excel 2007, **se admite Excel12v.** 
  
Estas funciones solo se pueden llamar cuando Excel ha pasado el control a la DLL o XLL. También se pueden llamar cuando Excel ha pasado el control indirectamente a través de una llamada a Visual Basic para Aplicaciones (VBA). No se puede llamar a ellos en otro momento. Por ejemplo, no se puede llamar a ellos durante las llamadas a la función DllMain u otras veces en las que el sistema operativo haya llamado a la DLL o desde un subproceso creado por el DLL. 
  
Las funciones de Excel4 y [Excel12](excel4-excel12.md) aceptan sus argumentos como una lista de longitud variable en la pila, mientras que las funciones **Excel4v** y **Excel12v** aceptan sus argumentos como una matriz. En todos los demás aspectos, **Excel4** se comporta igual que **Excel4v** y **Excel12** se comporta igual que **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Un número que indica el comando, la función o la función especial a la que desea llamar. Para obtener una lista de valores  _iFunction_ válidos, consulte la sección Comentarios siguientes. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Puntero a **un XLOPER** (en el caso de **Excel4v**) o a **un XLOPER12** (en el caso de **Excel12v**) que contendrán el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
Número de argumentos posteriores que se pasarán a la función. En las versiones de Excel hasta 2003, puede ser cualquier número del 0 al 30. A partir Excel 2007, puede ser cualquier número del 0 al 255.
  
 _rgx_ (**LPXLOPER []** o **LPXLOPER12 []**)
  
Matriz que contiene los argumentos de la función. Todos los argumentos de la matriz deben ser punteros a **valores XLOPER** o **XLOPER12.** 
  
## <a name="return-value"></a>Valor devuelto

Estas funciones devuelven los mismos valores que **Excel4** y **Excel12**.
  
## <a name="remarks"></a>Comentarios

Estas funciones son útiles cuando el número de argumentos que se pasan al operador es variable. Por ejemplo, **Excel4v** y **Excel12v** son útiles al registrar funciones mediante [xlfRegister](xlfregister-form-1.md) donde el número de argumentos totales depende del número de argumentos tomados por la función que se está registrando. **Excel4v** y **Excel12v** también son útiles al escribir una función contenedora para **Excel4** o **Excel12**. En estos casos, debe convertir una lista de argumentos variables, como normalmente se suministraría a **Excel4** o **Excel12,** en un único argumento de matriz de tamaño variable para volver a llamar a Excel mediante **Excel4v** o **Excel12v**.
  
### <a name="example"></a>Ejemplo

Para obtener ejemplos de código, vea el código de las funciones **Excel** y **Excel12f** en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Vea también



[Excel4/Excel12](excel4-excel12.md)

