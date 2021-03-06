---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- función excel [excel 2007], función Excel12f [Excel 2007]
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
  
Funciones de biblioteca de marcos. **Excel** es un contenedor para la [función Excel4.](excel4-excel12.md) **Excel12f** es un contenedor para la [función Excel12.](excel4-excel12.md) Cada uno comprueba que ninguno de los argumentos es cero, lo que indicaría que se ha fallado la creación de **un XLOPER** o **XLOPER12 temporal.** Si se produce un error, cada uno imprime un mensaje de depuración. Una vez finalizada, cada una libera toda la memoria temporal que se haya creado para **XLOPER** y **XLOPER12** temporales.
  
 Solo se puede llamar a **Excel12f** desde un ARCHIVO DLL a partir Excel biblioteca de API de C de 2007. Además, solo funciona cuando se ejecuta a partir de Excel 2007 y se produce un error con **xlretFailed en** caso contrario. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Un número que indica el comando o la función a la que desea llamar. Para obtener más información, vea [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Puntero al resultado de la función evaluada. Excel asignará cualquier memoria que se señala en el resultado y se liberará en una llamada a [xlFree](xlfree.md) una vez que ya no sea necesaria, o si se establece **xlbitXLFree** si se devuelve a Excel. 
  
 _iCount_ (**int**)
  
Número de argumentos que se pasarán a la función. A partir Excel 2007, el límite es 255 argumentos. En versiones anteriores, el límite es 30.
  
 _argument1, ..._
  
Argumentos opcionales para la función. Todos los argumentos deben ser punteros a **XLOPER** s en el caso de **Excel** o **XLOPER12** s en el caso de **Excel12f**.
  
## <a name="return-value"></a>Valor devuelto

Ambas funciones devuelven los mismos códigos de error y de éxito que **Excel4**, **Excel4v**, **Excel12** y **Excel12v**. Vea [Excel4/Excel12 para](excel4-excel12.md) obtener una descripción completa de estos códigos. Además, estas funciones de Framework **devuelven xlretFailed** sin llamar a la API de C si se detecta un puntero NULL a un parámetro. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se pasa un argumento no válido a la **función Excel12f,** que envía un mensaje al depurador. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Excel4/Excel12](excel4-excel12.md)


[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

