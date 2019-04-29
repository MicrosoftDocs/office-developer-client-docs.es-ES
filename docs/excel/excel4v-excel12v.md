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
- función excel12v [Excel 2007], Excel4v [Excel 2007]
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
  
Llama a una función de hoja de cálculo de Microsoft Excel, a un comando o a una función de hoja de macros o a un comando especial que solo XLL, desde dentro de una DLL, XLL o recurso de código.
  
Todas las versiones recientes de Excel admiten **Excel4v**. A partir de Excel 2007, **Excel12v** es compatible. 
  
Estas funciones solo se pueden llamar cuando Excel ha pasado el control a la DLL o XLL. También se pueden llamar cuando Excel ha pasado el control indirectamente a través de una llamada a Visual Basic para aplicaciones (VBA). No se pueden llamar en ningún otro momento. Por ejemplo, no se pueden llamar durante las llamadas a la función DllMain u otras horas en las que el sistema operativo haya llamado a la DLL, o de un subproceso creado por la DLL. 
  
Las funciones de [Excel4 y Excel12](excel4-excel12.md) aceptan sus argumentos como una lista de longitud variable en la pila, mientras que las funciones **Excel4v** y **Excel12v** aceptan sus argumentos como una matriz. En todos los demás aspectos, **Excel4** se comporta del mismo modo que **Excel4v**y **Excel12** se comporta del mismo modo que **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Número que indica el comando, la función o la función especial a la que se desea llamar. Para obtener una lista de los valores válidos de _iFunction_ , vea la siguiente sección de comentarios. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Un puntero a un **XLOPER** (en el caso de **Excel4v**) o a un **XLOPER12** (en el caso de **Excel12v**) que contendrá el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
Número de argumentos subsiguientes que se van a pasar a la función. En las versiones de Excel hasta 2003 puede ser cualquier número entre 0 y 30. A partir de Excel 2007, puede ser cualquier número comprendido entre 0 y 255.
  
 _RGX_ (**LPXLOPER []** o **LPXLOPER12 []**)
  
Matriz que contiene los argumentos de la función. Todos los argumentos de la matriz deben ser punteros a los valores **XLOPER** o **XLOPER12** . 
  
## <a name="return-value"></a>Valor devuelto

Estas funciones devuelven los mismos valores que **Excel4** y **Excel12**.
  
## <a name="remarks"></a>Comentarios

Estas funciones son útiles cuando el número de argumentos que se pasan al operador es variable. Por ejemplo, **Excel4v** y **Excel12v** son útiles cuando se registran funciones con [xlfRegister](xlfregister-form-1.md) donde el número total de argumentos depende del número de argumentos que toma la función que se está registrando. **Excel4v** y **Excel12v** también son útiles cuando se escribe una función contenedora para **Excel4** o **Excel12**. En estos casos, debe convertir una lista de argumentos de variable, como se proporcionaría normalmente a **Excel4** o **Excel12**, a un argumento de matriz único de tamaño variable para volver a llamar a Excel mediante **Excel4v** o **Excel12v**.
  
### <a name="example"></a>Ejemplo

Para obtener ejemplos de código, vea el código para las funciones de **Excel** y **EXCEL12F** en el SDK de XLL de Excel 2010, en la siguiente ubicación en la que instaló el SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Ver también



[Excel4/Excel12](excel4-excel12.md)

