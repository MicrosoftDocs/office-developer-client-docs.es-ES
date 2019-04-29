---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- función de Excel [Excel 2007], función Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431676"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funciones de la biblioteca de .NET Framework. **Excel** es un contenedor para la función [Excel4](excel4-excel12.md) . **Excel12f** es un contenedor para la función [Excel12](excel4-excel12.md) . Cada uno de ellos comprueba que ninguno de los argumentos es cero, lo que indicaría que no se pudo crear un **XLOPER** o **XLOPER12** temporal. Si se produce un error, cada uno imprime un mensaje de depuración. Cuando termine, cada uno liberará toda la memoria temporal que se podría haber creado para los **XLOPER**y **XLOPER12**temporales, s.
  
 **Excel12f** sólo se puede llamar desde una DLL a partir de la biblioteca API 2007 C de Excel. Además, solo funciona cuando se ejecuta a partir de Excel 2007 y se produce un error con **xlretFailed** en caso contrario. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Un número que indica el comando o la función a la que desea llamar. Para obtener más información, consulte [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Un puntero a resultado de la función evaluada. Cualquier memoria a la que apuntaba el resultado habrá sido asignada por Excel y debe liberarse en una llamada a [xlFree](xlfree.md) una vez que ya no se necesite, o estableciendo **xlbitXLFree** si se devuelve a Excel. 
  
 _iCount_ (**int**)
  
Número de argumentos que se van a pasar a la función. A partir de Excel 2007, el límite es de 255 argumentos. En versiones anteriores, el límite es 30.
  
 _argumento1,..._
  
Argumentos opcionales de la función. Todos los argumentos deben ser punteros a **XLOPER**s en el caso de **Excel**, o **XLOPER12**s en el caso de **Excel12f**.
  
## <a name="return-value"></a>Valor devuelto

Ambas funciones devuelven los mismos códigos de error y de éxito que **Excel4**, **Excel4v**, **Excel12**y **Excel12v**. Consulte [Excel4/Excel12](excel4-excel12.md) para obtener una descripción completa de estos códigos. Además, estas funciones de marco devuelven **xlretFailed** sin llamar a la API de C si se detecta un puntero nulo a un parámetro. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se pasa un argumento incorrecto a la función **Excel12f** , que envía un mensaje al depurador. 
  
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


[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

