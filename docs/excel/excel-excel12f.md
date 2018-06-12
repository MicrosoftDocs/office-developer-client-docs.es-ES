---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- función de Excel [excel 2007], Excel12f (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815563"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de la biblioteca de Framework. **Excel** es un contenedor para la función de [Excel4](excel4-excel12.md) . **Excel12f** es un contenedor para la función [Excel12](excel4-excel12.md) . Cada uno de ellos se comprueba que ninguno de los argumentos es cero, lo que podría indicar que no se pudieron la creación de un temporal **XLOPER** o **XLOPER12** . Si se produce un error, cada uno de ellos se imprime un mensaje de depuración. Cuando haya terminado, cada uno de ellos libera toda la memoria temporal que se han creado para temporal s **XLOPER**y **XLOPER12**.
  
 **Excel12f** sólo se pueden llamar desde una DLL a partir de la biblioteca de API de C de Excel 2007. Además, sólo funciona cuando se ejecuta comenzando con Excel 2007 y se produce un error con **xlretFailed** en caso contrario. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Sintaxis

 _iFunction_ (**int**)
  
Un número que indica el comando o la función que desea llamar. Para obtener más información, vea [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Un puntero al resultado de la función evaluada. Cualquier memoria señalado en el resultado habrá se hayan asignado mediante Excel y debe liberarse en una llamada a [xlFree](xlfree.md) una vez que ya no sea necesaria, o mediante la configuración **xlbitXLFree** si devolver a Excel. 
  
 _iCount_ (**int**)
  
El número de argumentos que se pasan a la función. Iniciar en Excel 2007, el límite es 255 argumentos. En versiones anteriores, el límite es 30.
  
 _argumento1..._
  
Los argumentos opcionales a la función. Todos los argumentos deben ser punteros a s **XLOPER**en el caso de **Excel**, o s **XLOPER12**en el caso de **Excel12f**.
  
## <a name="return-value"></a>Valor devuelto

Ambas funciones devuelven el mismo error y los códigos de éxito como **Excel4**, **Excel4v**, **Excel12**y **Excel12v**. Para obtener una descripción completa de estos códigos, vea [Excel4/Excel12](excel4-excel12.md) . Además, estas funciones de Framework devuelven **xlretFailed** sin llamar a la API de C si un puntero NULL a un parámetro se detecta. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se pasa un argumento no válido para la función **Excel12f** , que envía un mensaje para el depurador. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>Ver también



[Excel4/Excel12](excel4-excel12.md)


[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

